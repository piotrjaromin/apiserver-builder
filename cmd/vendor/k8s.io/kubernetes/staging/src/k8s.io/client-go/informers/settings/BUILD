package(default_visibility = ["//visibility:public"])

licenses(["notice"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_library",
)

go_library(
    name = "go_default_library",
    srcs = ["interface.go"],
    importpath = "k8s.io/kubernetes/staging/src/k8s.io/client-go/informers/settings",
    tags = ["automanaged"],
    deps = [
        "//cmd/vendor/k8s.io/client-go/informers/internalinterfaces:go_default_library",
        "//cmd/vendor/k8s.io/client-go/informers/settings/v1alpha1:go_default_library",
    ],
)
