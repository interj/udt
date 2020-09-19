
add_library(udt
    api.cpp
    buffer.cpp
    cache.cpp
    ccc.cpp
    channel.cpp
    common.cpp
    core.cpp
    epoll.cpp
    list.cpp
    md5.cpp
    packet.cpp
    queue.cpp
    window.cpp
    api.h
    buffer.h
    cache.h
    ccc.h
    channel.h
    common.h
    core.h
    epoll.h
    list.h
    md5.h
    packet.h
    queue.h
    udt.h
    window.h
)

install(FILES
    api.h
    buffer.h
    cache.h
    ccc.h
    channel.h
    common.h
    core.h
    epoll.h
    list.h
    md5.h
    packet.h
    queue.h
    udt.h
    window.h
    DESTINATION include/udt)


