package(default_visibility = ["//visibility:public"])

licenses(["notice"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_library",
    "go_test",
)

go_library(
    name = "go_default_library",
    srcs = [
        "helpers.go",
        "types.go",
    ],
    importpath = "k8s.io/kubernetes/cmd/libs/go2idl/client-gen/types",
    tags = ["automanaged"],
    deps = ["//cmd/vendor/k8s.io/gengo/namer:go_default_library"],
)

go_test(
    name = "go_default_test",
    srcs = ["helpers_test.go"],
    importpath = "k8s.io/kubernetes/cmd/libs/go2idl/client-gen/types",
    library = ":go_default_library",
    tags = ["automanaged"],
)

filegroup(
    name = "package-srcs",
    srcs = glob(["**"]),
    tags = ["automanaged"],
    visibility = ["//visibility:private"],
)

filegroup(
    name = "all-srcs",
    srcs = [":package-srcs"],
    tags = ["automanaged"],
)
