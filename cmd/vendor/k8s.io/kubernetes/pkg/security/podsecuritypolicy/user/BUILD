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
        "doc.go",
        "mustrunas.go",
        "nonroot.go",
        "runasany.go",
        "types.go",
    ],
    importpath = "k8s.io/kubernetes/pkg/security/podsecuritypolicy/user",
    tags = ["automanaged"],
    deps = [
        "//cmd/vendor/k8s.io/apimachinery/pkg/util/validation/field:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/pkg/api:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/pkg/apis/extensions:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/pkg/security/podsecuritypolicy/util:go_default_library",
    ],
)

go_test(
    name = "go_default_test",
    srcs = [
        "mustrunas_test.go",
        "nonroot_test.go",
        "runasany_test.go",
    ],
    importpath = "k8s.io/kubernetes/pkg/security/podsecuritypolicy/user",
    library = ":go_default_library",
    tags = ["automanaged"],
    deps = [
        "//cmd/vendor/k8s.io/kubernetes/pkg/api:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/pkg/apis/extensions:go_default_library",
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
