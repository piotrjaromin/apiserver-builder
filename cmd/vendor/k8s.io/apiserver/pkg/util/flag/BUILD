package(default_visibility = ["//visibility:public"])

licenses(["notice"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_library",
    "go_test",
)

go_test(
    name = "go_default_test",
    srcs = ["namedcertkey_flag_test.go"],
    importpath = "k8s.io/apiserver/pkg/util/flag",
    library = ":go_default_library",
    tags = ["automanaged"],
    deps = ["//cmd/vendor/github.com/spf13/pflag:go_default_library"],
)

go_library(
    name = "go_default_library",
    srcs = [
        "configuration_map.go",
        "flags.go",
        "namedcertkey_flag.go",
        "string_flag.go",
        "tristate.go",
    ],
    importpath = "k8s.io/apiserver/pkg/util/flag",
    tags = ["automanaged"],
    deps = [
        "//cmd/vendor/github.com/golang/glog:go_default_library",
        "//cmd/vendor/github.com/spf13/pflag:go_default_library",
    ],
)
