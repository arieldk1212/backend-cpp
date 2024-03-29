cmake_minimum_required(VERSION 3.2)

PROJECT(CPP_HTTP_SERVER_ON_DOCKER)

add_library(boost_beast INTERFACE)

target_include_directories(boost_beast
                           SYSTEM
                           INTERFACE
                           "${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/beast/include")

ADD_EXECUTABLE(cpp_http_server main.cpp)

include_directories("${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/asio/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/assert/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/assign/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/atomic/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/beast/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/bimap/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/bind/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/callable_traits/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/chrono/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/circular_buffer/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/compatibility/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/compute/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/concept_check/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/config/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/container/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/container_hash/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/context/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/contract/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/conversion/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/convert/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/core/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/coroutine/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/coroutine2/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/crc/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/date_time/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/describe/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/detail/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/dll/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/dynamic_bitset/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/endian/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/exception/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/fiber/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/filesystem/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/flyweight/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/foreach/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/format/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/function/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/function_types/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/functional/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/fusion/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/geometry/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/gil/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/graph/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/graph_parallel/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/hana/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/headers/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/heap/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/histogram/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/hof/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/icl/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/integer/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/interprocess/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/intrusive/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/io/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/iostreams/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/iterator/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/json/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/lambda/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/lambda2/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/leaf/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/lexical_cast/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/local_function/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/locale/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/lockfree/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/log/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/logic/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/math/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/metaparse/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/move/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/mp11/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/mpi/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/mpl/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/msm/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/multi_array/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/multi_index/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/multiprecision/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/mysql/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/nowide/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/numeric/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/optional/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/outcome/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/parameter/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/parameter_python/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/pfr/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/phoenix/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/poly_collection/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/polygon/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/pool/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/predef/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/preprocessor/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/process/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/program_options/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/property_map/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/property_map_parallel/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/property_tree/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/proto/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/ptr_container/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/python/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/qvm/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/random/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/range/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/ratio/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/rational/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/regex/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/safe_numerics/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/scope_exit/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/serialization/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/signals2/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/smart_ptr/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/sort/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/spirit/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/stacktrace/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/statechart/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/static_assert/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/static_string/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/stl_interfaces/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/system/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/test/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/thread/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/throw_exception/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/timer/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/tokenizer/include"
"${CMAKE_CURRENT_LIST_DIR}/3rdparty/boost/libs/tti/include")