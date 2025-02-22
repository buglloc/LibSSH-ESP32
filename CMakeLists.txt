idf_component_register(
SRC_DIRS
  "src"
  "src/threads"
  "src/external"
INCLUDE_DIRS
  "src"
PRIV_REQUIRES
  mbedtls lwip
)

target_compile_options(${COMPONENT_LIB} PRIVATE -DESP32 -Wno-error=format -Wno-error=char-subscripts)
