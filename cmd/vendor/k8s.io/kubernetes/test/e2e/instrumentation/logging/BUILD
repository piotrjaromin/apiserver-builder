package(default_visibility = ["//visibility:public"])

licenses(["notice"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_library",
)

go_library(
    name = "go_default_library",
    srcs = [
        "es.go",
        "es_kibana.go",
        "es_utils.go",
        "generic_soak.go",
        "sd.go",
        "sd_events.go",
        "sd_soak.go",
        "sd_utils.go",
        "utils.go",
    ],
    importpath = "k8s.io/kubernetes/test/e2e/instrumentation/logging",
    tags = ["automanaged"],
    deps = [
        "//cmd/vendor/github.com/onsi/ginkgo:go_default_library",
        "//cmd/vendor/github.com/onsi/gomega:go_default_library",
        "//vendor/golang.org/x/net/context:go_default_library",
        "//vendor/golang.org/x/oauth2/google:go_default_library",
        "//vendor/google.golang.org/api/logging/v2beta1:go_default_library",
        "//vendor/google.golang.org/api/pubsub/v1:go_default_library",
        "//cmd/vendor/k8s.io/api/core/v1:go_default_library",
        "//cmd/vendor/k8s.io/apimachinery/pkg/api/resource:go_default_library",
        "//cmd/vendor/k8s.io/apimachinery/pkg/apis/meta/v1:go_default_library",
        "//cmd/vendor/k8s.io/apimachinery/pkg/fields:go_default_library",
        "//cmd/vendor/k8s.io/apimachinery/pkg/labels:go_default_library",
        "//cmd/vendor/k8s.io/apimachinery/pkg/util/wait:go_default_library",
        "//cmd/vendor/k8s.io/client-go/util/integer:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/pkg/api:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/test/e2e/framework:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/test/e2e/instrumentation:go_default_library",
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
