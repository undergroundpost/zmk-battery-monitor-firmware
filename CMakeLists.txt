zephyr_library()

zephyr_library_sources_ifdef(CONFIG_ZMK_BATTERY_MONITOR_HID
    src/central/battery_hid.c
    src/central/metadata_client.c
)

zephyr_library_sources_ifdef(CONFIG_ZMK_BATTERY_MONITOR_PERIPHERAL
    src/peripheral/metadata_service.c
)

zephyr_library_include_directories(${APPLICATION_SOURCE_DIR}/include)
zephyr_library_include_directories(src/common)
