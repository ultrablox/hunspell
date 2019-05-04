
ADD_LIBRARY(hunspell STATIC 
  affentry.cxx 
  affixmgr.cxx
  csutil.cxx
  filemgr.cxx
  hashmgr.cxx
  hunspell.cxx
  hunzip.cxx
  phonet.cxx
  replist.cxx
  suggestmgr.cxx
)



INCLUDE_DIRECTORIES("${CMAKE_INSTALL_PREFIX}/include")

set(HEADER_FILES 
  affentry.hxx
  affixmgr.hxx
  atypes.hxx
  baseaffix.hxx
  csutil.hxx
  filemgr.hxx
  hashmgr.hxx
  htypes.hxx
  hunspell.h
  hunspell.hxx
  hunzip.hxx
  langnum.hxx
  phonet.hxx
  replist.hxx
  suggestmgr.hxx
  utf_info.hxx
  w_char.hxx
  hunvisapi.h
)


set_target_properties(hunspell PROPERTIES PUBLIC_HEADER "${HEADER_FILES}")

install(TARGETS hunspell
  ARCHIVE DESTINATION ${CMAKE_INSTALL_PREFIX}/lib
  LIBRARY DESTINATION ${CMAKE_INSTALL_PREFIX}/lib
  PUBLIC_HEADER DESTINATION ${CMAKE_INSTALL_PREFIX}/include/hunspell
)
