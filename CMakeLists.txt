# MQ2Profiler
# Forked from RedGuides/MQ2Profiler (github.com/RedGuides org sweep, forum-plugins-2026-08-02
# follow-up batch). Vendored as a git submodule tracking https://github.com/blbruegg/MQ2Profiler
# (fork of RedGuides/MQ2Profiler). See F:\\EQProject\\docs\\re_progress.md for the write-up.

include("../../Plugin.cmake")

set(MQ2Profiler_SOURCES
    "MQ2Profiler.cpp"
    "date.h"
)

source_groups("Source Files" ${MQ2Profiler_SOURCES})

add_library(MQ2Profiler SHARED
    ${MQ2Profiler_SOURCES}
)

set_target_properties(MQ2Profiler PROPERTIES FOLDER "core/plugins")

target_Plugin_props(MQ2Profiler)

target_link_libraries(MQ2Profiler PRIVATE MQ2Main)
