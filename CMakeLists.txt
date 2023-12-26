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

# Temporary hack
idf_build_set_property(COMPILE_DEFINITIONS "-DESP32" APPEND)

# Silence char subscripts warning, until it is fixed upstream
idf_build_set_property(COMPILE_OPTIONS "-Wno-char-subscripts" APPEND)
