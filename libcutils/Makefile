#
# Copyright (C) 2023 Xiaomi Corporation
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#      http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.
#

include $(APPDIR)/Make.defs

CXXEXT = .cpp

ifeq ($(GCCVER),12)
CXXFLAGS += -Wno-maybe-uninitialized
endif

CXXSRCS += android_get_control_file.cpp
CXXSRCS += ashmem-host.cpp
CXXSRCS += canned_fs_config.cpp
CXXSRCS += config_utils.cpp
CXXSRCS += fs_config.cpp
CXXSRCS += fs.cpp
CXXSRCS += hashmap.cpp
CXXSRCS += iosched_policy.cpp
CXXSRCS += load_file.cpp
CXXSRCS += multiuser.cpp
CXXSRCS += native_handle.cpp
CXXSRCS += partition_utils.cpp
CXXSRCS += record_stream.cpp
CXXSRCS += socket_inaddr_any_server_unix.cpp
CXXSRCS += socket_local_client_unix.cpp
CXXSRCS += socket_local_server_unix.cpp
CXXSRCS += socket_network_client_unix.cpp
CXXSRCS += sockets_unix.cpp
CXXSRCS += sockets.cpp
CXXSRCS += str_parms.cpp

include $(APPDIR)/Application.mk
