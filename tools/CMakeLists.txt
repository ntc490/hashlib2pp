#
# hashlib++ - a simple hash library for C++
#
# Copyright (c) 2007-2010 Benjamin Grüdelbach
#
# Redistribution and use in source and binary forms, with or without modification,
# are permitted provided that the following conditions are met:
#
# 	1)     Redistributions of source code must retain the above copyright
# 	       notice, this list of conditions and the following disclaimer.
#
# 	2)     Redistributions in binary form must reproduce the above copyright
# 	       notice, this list of conditions and the following disclaimer in
# 	       the documentation and/or other materials provided with the
# 	       distribution.
#
# THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS" AND
# ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED
# WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE
# DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT OWNER OR CONTRIBUTORS BE LIABLE FOR
# ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES
# (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES;
# LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON
# ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT
# (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS
# SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.
#
#-----------------------------------------------------------------------
#
# This is the hashlib++ makefile. It builds and installs hashlib++ as a
# static library. See the documentation for more information.
#
# Benjamin Grüdelbach
# Mi 10 Okt 2007
#
# CMake by Nathan Crapo Jul 2022
#
#-----------------------------------------------------------------------
# Edit the following lines to meet your needs
cmake_minimum_required(VERSION 3.16)

add_executable(hello hello.cpp)
add_executable(h h.cpp)
add_executable(libtest libtest.cpp)

target_link_libraries(hello hl++)
target_link_libraries(h hl++)
target_link_libraries(libtest hl++)

# Don't normally include these in installation
# install(TARGETS hello h libtest EXPORT helloTargets
#   RUNTIME DESTINATION bin
#   )
