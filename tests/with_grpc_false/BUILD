package(default_visibility = ["//visibility:public"])

# See https://github.com/pubref/rules_protobuf/issues/48

load("@org_pubref_rules_protobuf//cpp:rules.bzl", "cc_proto_library")
load("@org_pubref_rules_protobuf//java:rules.bzl", "java_proto_library")

filegroup(
    name = "protos",
    srcs = ["message.proto"],
)

cc_proto_library(
    name = "cpp",
    imports = [
        "external/com_google_protobuf/src/",
    ],
    inputs = [
        "@com_google_protobuf//:well_known_protos",
    ],
    protos = [":protos"],
    verbose = 0,
    with_grpc = False,
)

java_proto_library(
    name = "java",
    imports = [
        "external/com_google_protobuf/src/",
    ],
    inputs = [
        "@com_google_protobuf//:well_known_protos",
    ],
    protos = [":protos"],
    verbose = 0,
    with_grpc = False,
)
