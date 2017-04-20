package(default_visibility = ["//visibility:public"])

load("//bazel:envoy_build_system.bzl", "envoy_cc_library")

envoy_cc_library(
    name = "address_interface",
    hdrs = ["address.h"],
)

envoy_cc_library(
    name = "connection_interface",
    hdrs = ["connection.h"],
    deps = [
        ":address_interface",
        ":filter_interface",
        "//include/envoy/buffer:buffer_interface",
        "//include/envoy/event:deferred_deletable",
        "//include/envoy/ssl:connection_interface",
    ],
)

envoy_cc_library(
    name = "connection_handler_interface",
    hdrs = ["connection_handler.h"],
    deps = [
        ":listen_socket_interface",
        ":listener_interface",
        "//include/envoy/ssl:context_interface",
    ],
)

envoy_cc_library(
    name = "dns_interface",
    hdrs = ["dns.h"],
    deps = ["//include/envoy/network:address_interface"],
)

envoy_cc_library(
    name = "drain_decision_interface",
    hdrs = ["drain_decision.h"],
)

envoy_cc_library(
    name = "filter_interface",
    hdrs = ["filter.h"],
    deps = [
        "//include/envoy/buffer:buffer_interface",
        "//include/envoy/upstream:host_description_interface",
    ],
)

envoy_cc_library(
    name = "listen_socket_interface",
    hdrs = ["listen_socket.h"],
    deps = ["//include/envoy/network:address_interface"],
)

envoy_cc_library(
    name = "listener_interface",
    hdrs = ["listener.h"],
)