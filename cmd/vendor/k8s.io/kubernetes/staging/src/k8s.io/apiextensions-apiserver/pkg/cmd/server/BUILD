package(default_visibility = ["//visibility:public"])

licenses(["notice"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_library",
)

go_library(
    name = "go_default_library",
    srcs = ["start.go"],
    importpath = "k8s.io/kubernetes/staging/src/k8s.io/apiextensions-apiserver/pkg/cmd/server",
    tags = ["automanaged"],
    deps = [
        "//cmd/vendor/github.com/spf13/cobra:go_default_library",
        "//cmd/vendor/k8s.io/apiextensions-apiserver/pkg/apis/apiextensions/v1beta1:go_default_library",
        "//cmd/vendor/k8s.io/apiextensions-apiserver/pkg/apiserver:go_default_library",
        "//cmd/vendor/k8s.io/apimachinery/pkg/apis/meta/v1/unstructured:go_default_library",
        "//cmd/vendor/k8s.io/apiserver/pkg/registry/generic:go_default_library",
        "//cmd/vendor/k8s.io/apiserver/pkg/server:go_default_library",
        "//cmd/vendor/k8s.io/apiserver/pkg/server/options:go_default_library",
    ],
)
