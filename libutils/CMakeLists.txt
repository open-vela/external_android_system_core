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

if(CONFIG_ANDROID_LIBUTILS)

  # global include path
  set_property(
    TARGET nuttx
    APPEND
    PROPERTY NUTTX_CXX_INCLUDE_DIRECTORIES ${CMAKE_CURRENT_LIST_DIR}/include)

  target_sources(
    android
    PRIVATE Errors.cpp
            FileMap.cpp
            JenkinsHash.cpp
            LightRefBase.cpp
            Looper.cpp
            misc.cpp
            NativeHandle.cpp
            Printer.cpp
            RefBase.cpp
            SharedBuffer.cpp
            StopWatch.cpp
            String8.cpp
            String16.cpp
            StrongPointer.cpp
            SystemClock.cpp
            Threads.cpp
            Timers.cpp
            Tokenizer.cpp
            Unicode.cpp
            VectorImpl.cpp)
endif()
