package(default_visibility = ["//visibility:public"])

licenses(["notice"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_library",
)

go_library(
    name = "go_default_library",
    srcs = [
        "controllerrevision.go",
        "deployment.go",
        "interface.go",
        "statefulset.go",
    ],
    importpath = "k8s.io/kubernetes/staging/src/k8s.io/client-go/informers/apps/v1beta1",
    tags = ["automanaged"],
    deps = [
        "//cmd/vendor/k8s.io/api/apps/v1beta1:go_default_library",
        "//cmd/vendor/k8s.io/apimachinery/pkg/apis/meta/v1:go_default_library",
        "//cmd/vendor/k8s.io/apimachinery/pkg/runtime:go_default_library",
        "//cmd/vendor/k8s.io/apimachinery/pkg/watch:go_default_library",
        "//cmd/vendor/k8s.io/client-go/informers/internalinterfaces:go_default_library",
        "//cmd/vendor/k8s.io/client-go/kubernetes:go_default_library",
        "//cmd/vendor/k8s.io/client-go/listers/apps/v1beta1:go_default_library",
        "//cmd/vendor/k8s.io/client-go/tools/cache:go_default_library",
    ],
)
