package(default_visibility = ["//visibility:public"])

licenses(["notice"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_library",
    "go_test",
)

go_test(
    name = "go_default_test",
    srcs = ["union_test.go"],
    importpath = "k8s.io/apiserver/pkg/authorization/union",
    library = ":go_default_library",
    tags = ["automanaged"],
    deps = ["//cmd/vendor/k8s.io/apiserver/pkg/authorization/authorizer:go_default_library"],
)

go_library(
    name = "go_default_library",
    srcs = ["union.go"],
    importpath = "k8s.io/apiserver/pkg/authorization/union",
    tags = ["automanaged"],
    deps = [
        "//cmd/vendor/k8s.io/apimachinery/pkg/util/errors:go_default_library",
        "//cmd/vendor/k8s.io/apiserver/pkg/authorization/authorizer:go_default_library",
    ],
)
