package(default_visibility = ["//visibility:public"])

licenses(["notice"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_library",
    "go_test",
)

go_test(
    name = "go_default_test",
    srcs = ["tokenfile_test.go"],
    importpath = "k8s.io/apiserver/pkg/authentication/token/tokenfile",
    library = ":go_default_library",
    tags = ["automanaged"],
    deps = ["//vendor/k8s.io/apiserver/pkg/authentication/user:go_default_library"],
)

go_library(
    name = "go_default_library",
    srcs = ["tokenfile.go"],
    importpath = "k8s.io/apiserver/pkg/authentication/token/tokenfile",
    tags = ["automanaged"],
    deps = [
        "//vendor/github.com/golang/glog:go_default_library",
        "//vendor/k8s.io/apiserver/pkg/authentication/user:go_default_library",
    ],
)
