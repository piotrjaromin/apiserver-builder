package(default_visibility = ["//visibility:public"])

licenses(["notice"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_library",
    "go_test",
)

go_test(
    name = "go_default_test",
    srcs = [
        "default_rate_limiters_test.go",
        "delaying_queue_test.go",
        "rate_limitting_queue_test.go",
    ],
    importpath = "k8s.io/kubernetes/staging/src/k8s.io/client-go/util/workqueue",
    library = ":go_default_library",
    tags = ["automanaged"],
    deps = [
        "//cmd/vendor/k8s.io/apimachinery/pkg/util/clock:go_default_library",
        "//cmd/vendor/k8s.io/apimachinery/pkg/util/wait:go_default_library",
    ],
)

go_library(
    name = "go_default_library",
    srcs = [
        "default_rate_limiters.go",
        "delaying_queue.go",
        "doc.go",
        "metrics.go",
        "parallelizer.go",
        "queue.go",
        "rate_limitting_queue.go",
    ],
    importpath = "k8s.io/kubernetes/staging/src/k8s.io/client-go/util/workqueue",
    tags = ["automanaged"],
    deps = [
        "//vendor/github.com/juju/ratelimit:go_default_library",
        "//cmd/vendor/k8s.io/apimachinery/pkg/util/clock:go_default_library",
        "//cmd/vendor/k8s.io/apimachinery/pkg/util/runtime:go_default_library",
    ],
)

go_test(
    name = "go_default_xtest",
    srcs = ["queue_test.go"],
    importpath = "k8s.io/kubernetes/staging/src/k8s.io/client-go/util/workqueue_test",
    tags = ["automanaged"],
    deps = ["//cmd/vendor/k8s.io/client-go/util/workqueue:go_default_library"],
)
