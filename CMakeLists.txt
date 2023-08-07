if(CONFIG_LIBUNITYTEST)
zephyr_interface_library_named(LIBUNITYTEST)

zephyr_include_directories(.)

zephyr_library()
zephyr_library_sources(
    unity/unity.c
)

zephyr_library_link_libraries(LIBUNITYTEST)
target_link_libraries(LIBUNITYTEST INTERFACE zephyr_interface)
endif()