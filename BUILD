load("@rules_python//python:proto.bzl", "py_proto_library")

proto_library(
    name = "dummy_pb2",
    srcs = ["dummy.proto"],
    visibility = ["//:__subpackages__"],
)

py_proto_library(
    name = "dummy_py_pb2",
    deps = [
        ":dummy_pb2",
    ],
)

py_binary(
    name = "app",
    srcs = ["app.py"],
    main = "app.py",
    srcs_version = "PY3",
    deps = [
        # Comment out this line to make the issue go away.
        # ":dummy_py_pb2",
        "@pypi_kubernetes//:pkg",
        "@pypi_protobuf//:pkg",
    ],
)
