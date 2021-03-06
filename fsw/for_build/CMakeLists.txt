
add_airliner_app_def(lgc
    FILE LGC
    SOURCES
        ${CMAKE_CURRENT_SOURCE_DIR}/../src/lgc_app.cpp
        ${CMAKE_CURRENT_SOURCE_DIR}/../src/lgc_app.h
        ${CMAKE_CURRENT_SOURCE_DIR}/../src/lgc_config_utils.cpp
        ${CMAKE_CURRENT_SOURCE_DIR}/../src/lgc_events.h
        ${CMAKE_CURRENT_SOURCE_DIR}/../src/lgc_msg.h
        ${CMAKE_CURRENT_SOURCE_DIR}/../src/lgc_tbldefs.h
        ${CMAKE_CURRENT_SOURCE_DIR}/../src/lgc_version.h
   
    INCLUDES
        ${CMAKE_CURRENT_SOURCE_DIR}/../src/

    USER_DOCS   ${CMAKE_CURRENT_SOURCE_DIR}/user_doxy.in
    DESIGN_DOCS ${CMAKE_CURRENT_SOURCE_DIR}/detail_doxy.in
)

add_airliner_app_unit_test(lgc-ut
    UTASSERT
    SOURCES
        ${CMAKE_CURRENT_SOURCE_DIR}/../unit_test/lgc_app_test.cpp
        ${CMAKE_CURRENT_SOURCE_DIR}/../unit_test/lgc_app_test.h
        ${CMAKE_CURRENT_SOURCE_DIR}/../unit_test/lgc_cmds_test.cpp
        ${CMAKE_CURRENT_SOURCE_DIR}/../unit_test/lgc_cmds_test.h
        ${CMAKE_CURRENT_SOURCE_DIR}/../unit_test/lgc_config_tbl_test.cpp
        ${CMAKE_CURRENT_SOURCE_DIR}/../unit_test/lgc_config_tbl_test.h
        ${CMAKE_CURRENT_SOURCE_DIR}/../unit_test/lgc_testrunner.cpp
        ${CMAKE_CURRENT_SOURCE_DIR}/../unit_test/lgc_test_utils.cpp
        ${CMAKE_CURRENT_SOURCE_DIR}/../unit_test/lgc_test_utils.h
        ${CMAKE_CURRENT_SOURCE_DIR}/../src/lgc_app.cpp
        ${CMAKE_CURRENT_SOURCE_DIR}/../src/lgc_app.h
        ${CMAKE_CURRENT_SOURCE_DIR}/../src/lgc_config_utils.cpp
        ${CMAKE_CURRENT_SOURCE_DIR}/../src/lgc_events.h
        ${CMAKE_CURRENT_SOURCE_DIR}/../src/lgc_msg.h
        ${CMAKE_CURRENT_SOURCE_DIR}/../src/lgc_tbldefs.h
        ${CMAKE_CURRENT_SOURCE_DIR}/../src/lgc_version.h
        
    INCLUDES
        ${CMAKE_CURRENT_SOURCE_DIR}/../src/
        ${CMAKE_CURRENT_SOURCE_DIR}/../unit_test/
        
    VALGRIND_SUPPRESSION_FILE
        ${CMAKE_CURRENT_SOURCE_DIR}/../unit_test/valgrind.supp
)
