package(default_visibility = ["//visibility:public"])

licenses(["notice"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_library",
)

go_library(
    name = "go_default_library",
    srcs = ["interfaces.go"],
    importpath = "k8s.io/kubernetes/federation/pkg/dnsprovider/providers/google/clouddns/internal/interfaces",
    tags = ["automanaged"],
    deps = [
        "//vendor/google.golang.org/api/googleapi:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/federation/pkg/dnsprovider/rrstype:go_default_library",
    ],
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
