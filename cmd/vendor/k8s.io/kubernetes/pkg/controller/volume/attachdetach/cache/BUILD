package(default_visibility = ["//visibility:public"])

licenses(["notice"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_library",
    "go_test",
)

go_library(
    name = "go_default_library",
    srcs = [
        "actual_state_of_world.go",
        "desired_state_of_world.go",
    ],
    importpath = "k8s.io/kubernetes/pkg/controller/volume/attachdetach/cache",
    tags = ["automanaged"],
    deps = [
        "//cmd/vendor/github.com/golang/glog:go_default_library",
        "//cmd/vendor/k8s.io/api/core/v1:go_default_library",
        "//cmd/vendor/k8s.io/apimachinery/pkg/types:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/pkg/volume:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/pkg/volume/util/operationexecutor:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/pkg/volume/util/types:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/pkg/volume/util/volumehelper:go_default_library",
    ],
)

go_test(
    name = "go_default_test",
    srcs = [
        "actual_state_of_world_test.go",
        "desired_state_of_world_test.go",
    ],
    importpath = "k8s.io/kubernetes/pkg/controller/volume/attachdetach/cache",
    library = ":go_default_library",
    tags = ["automanaged"],
    deps = [
        "//cmd/vendor/k8s.io/api/core/v1:go_default_library",
        "//cmd/vendor/k8s.io/apimachinery/pkg/types:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/pkg/controller/volume/attachdetach/testing:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/pkg/volume/testing:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/pkg/volume/util/types:go_default_library",
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
