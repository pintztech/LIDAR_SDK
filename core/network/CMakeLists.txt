aux_include_directory(. HDRS)
aux_source_directory(. SRCS)
add_to_lidar_headers(${HDRS})
add_to_lidar_sources(${SRCS})

IF (WIN32)
add_to_lidar_libraries(setupapi ws2_32)
ELSE()
add_to_lidar_libraries(rt)
ENDIF()                                            
