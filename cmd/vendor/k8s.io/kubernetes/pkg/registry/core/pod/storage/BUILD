package(default_visibility = ["//visibility:public"])

licenses(["notice"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_library",
    "go_test",
)

go_test(
    name = "go_default_test",
    srcs = ["storage_test.go"],
    importpath = "k8s.io/kubernetes/pkg/registry/core/pod/storage",
    library = ":go_default_library",
    tags = ["automanaged"],
    deps = [
        "//vendor/golang.org/x/net/context:go_default_library",
        "//cmd/vendor/k8s.io/api/core/v1:go_default_library",
        "//cmd/vendor/k8s.io/apimachinery/pkg/api/equality:go_default_library",
        "//cmd/vendor/k8s.io/apimachinery/pkg/api/errors:go_default_library",
        "//cmd/vendor/k8s.io/apimachinery/pkg/apis/meta/v1:go_default_library",
        "//cmd/vendor/k8s.io/apimachinery/pkg/apis/meta/v1alpha1:go_default_library",
        "//cmd/vendor/k8s.io/apimachinery/pkg/fields:go_default_library",
        "//cmd/vendor/k8s.io/apimachinery/pkg/labels:go_default_library",
        "//cmd/vendor/k8s.io/apimachinery/pkg/runtime:go_default_library",
        "//cmd/vendor/k8s.io/apimachinery/pkg/util/diff:go_default_library",
        "//cmd/vendor/k8s.io/apiserver/pkg/endpoints/request:go_default_library",
        "//cmd/vendor/k8s.io/apiserver/pkg/registry/generic:go_default_library",
        "//cmd/vendor/k8s.io/apiserver/pkg/registry/rest:go_default_library",
        "//cmd/vendor/k8s.io/apiserver/pkg/storage:go_default_library",
        "//cmd/vendor/k8s.io/apiserver/pkg/storage/errors:go_default_library",
        "//cmd/vendor/k8s.io/apiserver/pkg/storage/etcd/testing:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/pkg/api:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/pkg/registry/registrytest:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/pkg/securitycontext:go_default_library",
    ],
)

go_library(
    name = "go_default_library",
    srcs = [
        "eviction.go",
        "storage.go",
    ],
    importpath = "k8s.io/kubernetes/pkg/registry/core/pod/storage",
    tags = ["automanaged"],
    deps = [
        "//cmd/vendor/k8s.io/apimachinery/pkg/api/errors:go_default_library",
        "//cmd/vendor/k8s.io/apimachinery/pkg/apis/meta/v1:go_default_library",
        "//cmd/vendor/k8s.io/apimachinery/pkg/labels:go_default_library",
        "//cmd/vendor/k8s.io/apimachinery/pkg/runtime:go_default_library",
        "//cmd/vendor/k8s.io/apimachinery/pkg/util/wait:go_default_library",
        "//cmd/vendor/k8s.io/apiserver/pkg/endpoints/request:go_default_library",
        "//cmd/vendor/k8s.io/apiserver/pkg/registry/generic:go_default_library",
        "//cmd/vendor/k8s.io/apiserver/pkg/registry/generic/registry:go_default_library",
        "//cmd/vendor/k8s.io/apiserver/pkg/registry/rest:go_default_library",
        "//cmd/vendor/k8s.io/apiserver/pkg/storage:go_default_library",
        "//cmd/vendor/k8s.io/apiserver/pkg/storage/errors:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/pkg/api:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/pkg/api/pod:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/pkg/api/validation:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/pkg/apis/policy:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/pkg/client/clientset_generated/internalclientset/typed/policy/internalversion:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/pkg/client/retry:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/pkg/kubelet/client:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/pkg/printers:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/pkg/printers/internalversion:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/pkg/printers/storage:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/pkg/registry/cachesize:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/pkg/registry/core/pod:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/pkg/registry/core/pod/rest:go_default_library",
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
