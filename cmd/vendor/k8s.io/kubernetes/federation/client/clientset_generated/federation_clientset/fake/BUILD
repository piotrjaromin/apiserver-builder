package(default_visibility = ["//visibility:public"])

licenses(["notice"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_library",
)

go_library(
    name = "go_default_library",
    srcs = [
        "clientset_generated.go",
        "doc.go",
        "register.go",
    ],
    importpath = "k8s.io/kubernetes/federation/client/clientset_generated/federation_clientset/fake",
    tags = ["automanaged"],
    deps = [
        "//cmd/vendor/k8s.io/api/autoscaling/v1:go_default_library",
        "//cmd/vendor/k8s.io/api/batch/v1:go_default_library",
        "//cmd/vendor/k8s.io/api/core/v1:go_default_library",
        "//cmd/vendor/k8s.io/api/extensions/v1beta1:go_default_library",
        "//cmd/vendor/k8s.io/apimachinery/pkg/apis/meta/v1:go_default_library",
        "//cmd/vendor/k8s.io/apimachinery/pkg/runtime:go_default_library",
        "//cmd/vendor/k8s.io/apimachinery/pkg/runtime/schema:go_default_library",
        "//cmd/vendor/k8s.io/apimachinery/pkg/runtime/serializer:go_default_library",
        "//cmd/vendor/k8s.io/apimachinery/pkg/watch:go_default_library",
        "//cmd/vendor/k8s.io/client-go/discovery:go_default_library",
        "//cmd/vendor/k8s.io/client-go/discovery/fake:go_default_library",
        "//cmd/vendor/k8s.io/client-go/testing:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/federation/apis/federation/v1beta1:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/federation/client/clientset_generated/federation_clientset:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/federation/client/clientset_generated/federation_clientset/typed/autoscaling/v1:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/federation/client/clientset_generated/federation_clientset/typed/autoscaling/v1/fake:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/federation/client/clientset_generated/federation_clientset/typed/batch/v1:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/federation/client/clientset_generated/federation_clientset/typed/batch/v1/fake:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/federation/client/clientset_generated/federation_clientset/typed/core/v1:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/federation/client/clientset_generated/federation_clientset/typed/core/v1/fake:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/federation/client/clientset_generated/federation_clientset/typed/extensions/v1beta1:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/federation/client/clientset_generated/federation_clientset/typed/extensions/v1beta1/fake:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/federation/client/clientset_generated/federation_clientset/typed/federation/v1beta1:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/federation/client/clientset_generated/federation_clientset/typed/federation/v1beta1/fake:go_default_library",
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
