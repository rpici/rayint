file(GLOB HEADERS "*.h")
file(GLOB SOURCES "*.cpp")

set(BIN raycast)

add_executable(${BIN} ${SOURCES})
#add_dependencies(${BIN} ext_mve)
target_link_libraries(${BIN}
    # -lmve
    # -lmve_util
    /home/vm/experimental/mve/rpici/mve/libs/util/libmve_util.a
    /home/vm/experimental/mve/rpici/mve/libs/mve/libmve.a
    ${JPEG_LIBRARIES}
    ${PNG_LIBRARIES}
    ${TIFF_LIBRARIES}
)
