package(default_visibility = ["//visibility:public"])

licenses(["notice"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_library",
    "go_test",
)

go_test(
    name = "go_default_test",
    srcs = ["converter_test.go"],
    importpath = "k8s.io/kubernetes/staging/src/k8s.io/apimachinery/pkg/conversion/unstructured",
    library = ":go_default_library",
    tags = ["automanaged"],
    deps = [
        "//cmd/vendor/k8s.io/apimachinery/pkg/util/diff:go_default_library",
        "//cmd/vendor/k8s.io/apimachinery/pkg/util/json:go_default_library",
    ],
)

go_library(
    name = "go_default_library",
    srcs = [
        "converter.go",
        "doc.go",
    ],
    importpath = "k8s.io/kubernetes/staging/src/k8s.io/apimachinery/pkg/conversion/unstructured",
    tags = ["automanaged"],
    deps = [
        "//cmd/vendor/github.com/golang/glog:go_default_library",
        "//cmd/vendor/k8s.io/apimachinery/pkg/api/equality:go_default_library",
        "//cmd/vendor/k8s.io/apimachinery/pkg/util/diff:go_default_library",
        "//cmd/vendor/k8s.io/apimachinery/pkg/util/json:go_default_library",
        "//cmd/vendor/k8s.io/apimachinery/pkg/util/runtime:go_default_library",
    ],
)
