# FreeRDP: A Remote Desktop Protocol Client
# libfreerdp cmake build script
#
# Copyright 2012 Marc-Andre Moreau <marcandre.moreau@gmail.com>
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

add_subdirectory(utils)
add_subdirectory(gdi)
add_subdirectory(rail)
add_subdirectory(cache)
add_subdirectory(codec)
add_subdirectory(crypto)
add_subdirectory(channels)
add_subdirectory(locale)
add_subdirectory(core)

