package(default_visibility = ["//visibility:public"])

licenses(["notice"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_library",
)

go_library(
    name = "go_default_library",
    srcs = [
        "doc.go",
        "strategy.go",
    ],
    importpath = "k8s.io/kubernetes/pkg/registry/extensions/podsecuritypolicy",
    tags = ["automanaged"],
    deps = [
        "//cmd/vendor/k8s.io/apimachinery/pkg/fields:go_default_library",
        "//cmd/vendor/k8s.io/apimachinery/pkg/labels:go_default_library",
        "//cmd/vendor/k8s.io/apimachinery/pkg/runtime:go_default_library",
        "//cmd/vendor/k8s.io/apimachinery/pkg/util/validation/field:go_default_library",
        "//cmd/vendor/k8s.io/apiserver/pkg/endpoints/request:go_default_library",
        "//cmd/vendor/k8s.io/apiserver/pkg/registry/generic:go_default_library",
        "//cmd/vendor/k8s.io/apiserver/pkg/registry/rest:go_default_library",
        "//cmd/vendor/k8s.io/apiserver/pkg/storage:go_default_library",
        "//cmd/vendor/k8s.io/apiserver/pkg/storage/names:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/pkg/api:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/pkg/apis/extensions:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/pkg/apis/extensions/validation:go_default_library",
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
    srcs = [
        ":package-srcs",
        "//pkg/registry/extensions/podsecuritypolicy/storage:all-srcs",
    ],
    tags = ["automanaged"],
)
