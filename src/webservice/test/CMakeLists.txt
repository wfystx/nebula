nebula_add_test(
    NAME
        flags_access_test
    SOURCES
        FlagsAccessTest.cpp
    OBJECTS
        $<TARGET_OBJECTS:http_client_obj>
        $<TARGET_OBJECTS:ws_obj>
        $<TARGET_OBJECTS:base_obj>
        $<TARGET_OBJECTS:process_obj>
        $<TARGET_OBJECTS:fs_obj>
        $<TARGET_OBJECTS:stats_obj>
        $<TARGET_OBJECTS:time_obj>
    LIBRARIES
        proxygenhttpserver
        proxygenlib
        wangle
        gtest
)


nebula_add_test(
    NAME
        stats_read_test
    SOURCES
        StatsReaderTest.cpp
    OBJECTS
        $<TARGET_OBJECTS:http_client_obj>
        $<TARGET_OBJECTS:ws_obj>
        $<TARGET_OBJECTS:base_obj>
        $<TARGET_OBJECTS:process_obj>
        $<TARGET_OBJECTS:fs_obj>
        $<TARGET_OBJECTS:stats_obj>
        $<TARGET_OBJECTS:time_obj>
    LIBRARIES
        proxygenhttpserver
        proxygenlib
        wangle
        gtest
)

nebula_add_test(
    NAME
        http_status_test
    SOURCES
        StatusHandlerTest.cpp
    OBJECTS
        $<TARGET_OBJECTS:http_client_obj>
        $<TARGET_OBJECTS:ws_obj>
        $<TARGET_OBJECTS:stats_obj>
        $<TARGET_OBJECTS:process_obj>
        $<TARGET_OBJECTS:fs_obj>
        $<TARGET_OBJECTS:time_obj>
        $<TARGET_OBJECTS:base_obj>
    LIBRARIES
        proxygenhttpserver
        proxygenlib
        wangle
        gtest
)
