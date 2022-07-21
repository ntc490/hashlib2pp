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

add_library(hl++
  hashlibpp.h
  hl_md5.cpp
  hl_md5.h
  hl_md5wrapper.cpp
  hl_md5wrapper.h
  hl_sha1.cpp
  hl_sha1.h
  hl_sha1wrapper.cpp
  hl_sha1wrapper.h
  hl_sha256.cpp
  hl_sha256.h
  hl_sha256wrapper.cpp
  hl_sha256wrapper.h
  hl_sha2ext.cpp
  hl_sha2ext.h
  hl_sha384wrapper.cpp
  hl_sha512wrapper.cpp
  hl_wrapperfactory.cpp
  hl_wrapperfactory.h
  hl_exception.h
  hl_hashwrapper.h
  hl_sha2mac.h
  hl_sha384wrapper.h
  hl_sha512wrapper.h
  hl_types.h
  )

add_library(hl++::hl++ ALIAS hl++)
target_include_directories(hl++
  PUBLIC
  ${PROJECT_SOURCE_DIR}/src
  )

# Install library
install(TARGETS hl++ EXPORT hl++Targets
  LIBRARY DESTINATION lib
  INCLUDES DESTINATION include
  )

# Install header files
install(FILES
  ${PROJECT_SOURCE_DIR}/src/hl_hashwrapper.h
  ${PROJECT_SOURCE_DIR}/src/hl_wrapperfactory.h
  ${PROJECT_SOURCE_DIR}/src/hl_exception.h
  ${PROJECT_SOURCE_DIR}/src/hl_md5.h
  ${PROJECT_SOURCE_DIR}/src/hl_md5wrapper.h
  ${PROJECT_SOURCE_DIR}/src/hl_sha1.h
  ${PROJECT_SOURCE_DIR}/src/hl_sha1wrapper.h
  ${PROJECT_SOURCE_DIR}/src/hl_sha2mac.h
  ${PROJECT_SOURCE_DIR}/src/hl_sha256.h
  ${PROJECT_SOURCE_DIR}/src/hl_sha256wrapper.h
  ${PROJECT_SOURCE_DIR}/src/hl_sha2ext.h
  ${PROJECT_SOURCE_DIR}/src/hl_sha384wrapper.h
  ${PROJECT_SOURCE_DIR}/src/hl_sha512wrapper.h
  ${PROJECT_SOURCE_DIR}/src/hl_types.h
  ${PROJECT_SOURCE_DIR}/src/hashlibpp.h
  DESTINATION include
  )
