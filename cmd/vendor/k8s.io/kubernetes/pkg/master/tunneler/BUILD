package(default_visibility = ["//visibility:public"])

licenses(["notice"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_library",
    "go_test",
)

go_test(
    name = "go_default_test",
    srcs = ["ssh_test.go"],
    importpath = "k8s.io/kubernetes/pkg/master/tunneler",
    library = ":go_default_library",
    tags = ["automanaged"],
    deps = [
        "//vendor/github.com/stretchr/testify/assert:go_default_library",
        "//cmd/vendor/k8s.io/apimachinery/pkg/util/clock:go_default_library",
    ],
)

go_library(
    name = "go_default_library",
    srcs = ["ssh.go"],
    importpath = "k8s.io/kubernetes/pkg/master/tunneler",
    tags = ["automanaged"],
    deps = [
        "//cmd/vendor/github.com/golang/glog:go_default_library",
        "//vendor/github.com/prometheus/client_golang/prometheus:go_default_library",
        "//cmd/vendor/k8s.io/apimachinery/pkg/util/clock:go_default_library",
        "//cmd/vendor/k8s.io/apimachinery/pkg/util/wait:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/pkg/ssh:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/pkg/util/file:go_default_library",
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
