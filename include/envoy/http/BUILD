licenses(["notice"])  # Apache 2

load(
    "//bazel:envoy_build_system.bzl",
    "envoy_cc_library",
    "envoy_package",
)

envoy_package()

envoy_cc_library(
    name = "access_log_interface",
    hdrs = ["access_log.h"],
    deps = [
        ":header_map_interface",
        ":protocol_interface",
        "//include/envoy/common:optional",
        "//include/envoy/common:time_interface",
        "//include/envoy/upstream:upstream_interface",
    ],
)

envoy_cc_library(
    name = "async_client_interface",
    hdrs = ["async_client.h"],
    deps = [
        ":message_interface",
        "//include/envoy/common:optional",
    ],
)

envoy_cc_library(
    name = "codec_interface",
    hdrs = ["codec.h"],
    deps = [
        ":header_map_interface",
        ":protocol_interface",
        "//include/envoy/buffer:buffer_interface",
    ],
)

envoy_cc_library(
    name = "codes_interface",
    hdrs = ["codes.h"],
)

envoy_cc_library(
    name = "conn_pool_interface",
    hdrs = ["conn_pool.h"],
    deps = [
        ":codec_interface",
        "//include/envoy/event:deferred_deletable",
        "//include/envoy/upstream:upstream_interface",
    ],
)

envoy_cc_library(
    name = "filter_interface",
    hdrs = ["filter.h"],
    deps = [
        ":access_log_interface",
        ":codec_interface",
        ":header_map_interface",
        "//include/envoy/event:dispatcher_interface",
        "//include/envoy/router:router_interface",
        "//include/envoy/ssl:connection_interface",
    ],
)

envoy_cc_library(
    name = "header_map_interface",
    hdrs = ["header_map.h"],
)

envoy_cc_library(
    name = "message_interface",
    hdrs = ["message.h"],
    deps = [
        ":header_map_interface",
        "//include/envoy/buffer:buffer_interface",
    ],
)

envoy_cc_library(
    name = "protocol_interface",
    hdrs = ["protocol.h"],
)
