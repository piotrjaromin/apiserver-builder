package(default_visibility = ["//visibility:public"])

licenses(["notice"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_library",
    "go_test",
)

go_test(
    name = "go_default_test",
    srcs = ["metrics_test.go"],
    importpath = "k8s.io/kubernetes/staging/src/k8s.io/apiserver/pkg/endpoints/metrics",
    library = ":go_default_library",
    tags = ["automanaged"],
)

go_library(
    name = "go_default_library",
    srcs = ["metrics.go"],
    importpath = "k8s.io/kubernetes/staging/src/k8s.io/apiserver/pkg/endpoints/metrics",
    tags = ["automanaged"],
    deps = [
        "//vendor/github.com/emicklei/go-restful:go_default_library",
        "//vendor/github.com/prometheus/client_golang/prometheus:go_default_library",
        "//cmd/vendor/k8s.io/apimachinery/pkg/util/net:go_default_library",
    ],
)
