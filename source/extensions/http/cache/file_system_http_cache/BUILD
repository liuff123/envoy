load(
    "//bazel:envoy_build_system.bzl",
    "envoy_cc_library",
    "envoy_extension_package",
    "envoy_proto_library",
)

licenses(["notice"])  # Apache 2

envoy_extension_package()

envoy_proto_library(
    name = "cache_file_header_proto",
    srcs = ["cache_file_header.proto"],
    deps = ["//source/extensions/filters/http/cache:key"],
)

envoy_cc_library(
    name = "cache_file_header_proto_util",
    srcs = ["cache_file_header_proto_util.cc"],
    hdrs = ["cache_file_header_proto_util.h"],
    deps = [
        ":cache_file_header_proto_cc_proto",
        "//envoy/http:header_map_interface",
        "//source/common/buffer:buffer_lib",
        "//source/common/common:macros",
        "//source/extensions/filters/http/cache:http_cache_lib",
        "@com_google_absl//absl/container:flat_hash_set",
        "@com_google_absl//absl/strings",
    ],
)

envoy_cc_library(
    name = "cache_file_fixed_block",
    srcs = ["cache_file_fixed_block.cc"],
    hdrs = ["cache_file_fixed_block.h"],
    deps = [
        "//envoy/buffer:buffer_interface",
        "@com_google_absl//absl/strings",
    ],
)
