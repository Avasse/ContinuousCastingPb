INCLUDE_DIRECTORIES(
  ${ARTIS_BINARY_DIR}/src
  ${ARTIS_SOURCE_DIR}/src
  ${Boost_INCLUDE_DIRS}
  ${GLIBMM_INCLUDE_DIRS}
  ${LIBXML_INCLUDE_DIRS})

LINK_DIRECTORIES(
  ${GLIBMM_LIBRARY_DIRS}
  ${LIBXML_LIBRARY_DIR}
  ${Boost_LIBRARY_DIRS})

SET(COMMON_SCHEDULER_HPP HeapScheduler.hpp SchedulerHandle.hpp
  VectorScheduler.hpp)

INSTALL(FILES ${COMMON_SCHEDULER_HPP} DESTINATION
  ${ARTIS_INCLUDE_DIRS}/common/scheduler)