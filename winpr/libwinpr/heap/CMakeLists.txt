# WinPR: Windows Portable Runtime
# libwinpr-heap cmake build script
#
# Copyright 2011 O.S. Systems Software Ltda.
# Copyright 2011 Otavio Salvador <otavio@ossystems.com.br>
# Copyright 2011 Marc-Andre Moreau <marcandre.moreau@gmail.com>
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#     http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.

set(WINPR_HEAP_SRCS
	heap.c)

if(WITH_MONOLITHIC_BUILD)
	add_library(winpr-heap OBJECT ${WINPR_HEAP_SRCS})
else()
	add_library(winpr-heap ${WINPR_HEAP_SRCS})
endif()

set_target_properties(winpr-heap PROPERTIES VERSION ${FREERDP_VERSION_FULL} SOVERSION ${FREERDP_VERSION} PREFIX "lib")

if(WITH_MONOLITHIC_BUILD)

else()
	install(TARGETS winpr-heap DESTINATION ${CMAKE_INSTALL_LIBDIR})
endif()
