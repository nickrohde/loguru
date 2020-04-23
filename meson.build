project(
    'Loguru', 
    'cpp', 
    version : '2.1.0', 
    license : 'MIT', 
    default_options : [
        'cpp_std=c++17'
    ]
)

cxx = meson.get_compiler('cpp')

libdl_dep = cxx.find_library(
    'dl', 
    required : true
)
thread_dep = dependency('threads')

install_headers('loguru.hpp')

loguru_sources = [
    'loguru.cpp'
]

libloguru = library(
    'loguru',
    loguru_sources,
    version      : '2.1.0',
    soversion    : '0',
    install      : true,
    dependencies : [thread_dep, libdl_dep]
)

# library dependency for external use
loguru_dep = libloguru
libloguru_dep = libloguru
