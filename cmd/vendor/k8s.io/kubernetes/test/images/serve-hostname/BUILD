package(default_visibility = ["//visibility:public"])

licenses(["notice"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_binary",
    "go_library",
)

go_library(
    name = "go_default_library",
    srcs = ["serve_hostname.go"],
    importpath = "k8s.io/kubernetes/test/images/serve-hostname",
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

go_binary(
    name = "serve-hostname",
    importpath = "k8s.io/kubernetes/test/images/serve-hostname",
    library = ":go_default_library",
    tags = ["automanaged"],
)
