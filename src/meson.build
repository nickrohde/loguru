cxx = meson.get_compiler('cpp')

libdl_dep = cxx.find_library(
    'dl', 
    required : true
)
thread_dep = dependency('threads')

loguru_sources = [
    'loguru.cpp'
]

libloguru = library(
    'loguru',
    loguru_sources,
    version      : '2.1.0',
    soversion    : '0',
    install      : true,
    include_directories : inc
    dependencies : [thread_dep, libdl_dep]
)

loguru_dep = declare_dependency(
    link_with : libloguru, 
    include_directories : inc
)
