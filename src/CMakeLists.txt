cmake_minimum_required(VERSION 3.16)
project(hl++ LANGUAGES CXX)

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

