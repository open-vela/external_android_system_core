#
# Copyright (C) 2023 Xiaomi Corporation
#
# Licensed under the Apache License, Version 2.0 (the "License"); you may not
# use this file except in compliance with the License. You may obtain a copy of
# the License at
#
# http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS, WITHOUT
# WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the
# License for the specific language governing permissions and limitations under
# the License.
#

if(CONFIG_ANDROID_LIBCUTILS)

  # global include path
  set_property(
    TARGET nuttx
    APPEND
    PROPERTY NUTTX_INCLUDE_DIRECTORIES ${CMAKE_CURRENT_LIST_DIR}/include)

  if(NOT DEFINED GCCVER)
    execute_process(COMMAND ${CMAKE_CXX_COMPILER} --version
                    OUTPUT_VARIABLE GCC_VERSION_OUTPUT)
    string(REGEX MATCH "\\+\\+.* ([0-9]+)\\.[0-9]+" GCC_VERSION_REGEX
                 "${GCC_VERSION_OUTPUT}")
    set(GCCVER ${CMAKE_MATCH_1})
  endif()

  if(GCCVER EQUAL 12)
    target_compile_options(android PRIVATE -Wno-maybe-uninitialized)
  endif()

  target_sources(
    android
    PRIVATE android_get_control_file.cpp
            ashmem-host.cpp
            canned_fs_config.cpp
            config_utils.cpp
            fs_config.cpp
            fs.cpp
            hashmap.cpp
            iosched_policy.cpp
            load_file.cpp
            multiuser.cpp
            native_handle.cpp
            partition_utils.cpp
            record_stream.cpp
            socket_inaddr_any_server_unix.cpp
            socket_local_client_unix.cpp
            socket_local_server_unix.cpp
            socket_network_client_unix.cpp
            sockets_unix.cpp
            sockets.cpp
            str_parms.cpp)
endif()
