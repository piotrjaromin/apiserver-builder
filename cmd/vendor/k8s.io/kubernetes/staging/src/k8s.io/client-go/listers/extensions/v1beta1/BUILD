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
        "daemonset.go",
        "daemonset_expansion.go",
        "deployment.go",
        "deployment_expansion.go",
        "expansion_generated.go",
        "ingress.go",
        "podsecuritypolicy.go",
        "replicaset.go",
        "replicaset_expansion.go",
        "scale.go",
        "thirdpartyresource.go",
    ],
    importpath = "k8s.io/kubernetes/staging/src/k8s.io/client-go/listers/extensions/v1beta1",
    tags = ["automanaged"],
    deps = [
        "//cmd/vendor/k8s.io/api/apps/v1beta1:go_default_library",
        "//cmd/vendor/k8s.io/api/core/v1:go_default_library",
        "//cmd/vendor/k8s.io/api/extensions/v1beta1:go_default_library",
        "//cmd/vendor/k8s.io/apimachinery/pkg/api/errors:go_default_library",
        "//cmd/vendor/k8s.io/apimachinery/pkg/apis/meta/v1:go_default_library",
        "//cmd/vendor/k8s.io/apimachinery/pkg/labels:go_default_library",
        "//cmd/vendor/k8s.io/client-go/tools/cache:go_default_library",
    ],
)

go_test(
    name = "go_default_test",
    srcs = ["daemonset_expansion_test.go"],
    importpath = "k8s.io/kubernetes/staging/src/k8s.io/client-go/listers/extensions/v1beta1",
    library = ":go_default_library",
    tags = ["automanaged"],
    deps = [
        "//cmd/vendor/k8s.io/api/core/v1:go_default_library",
        "//cmd/vendor/k8s.io/api/extensions/v1beta1:go_default_library",
        "//cmd/vendor/k8s.io/apimachinery/pkg/apis/meta/v1:go_default_library",
        "//cmd/vendor/k8s.io/apimachinery/pkg/labels:go_default_library",
        "//cmd/vendor/k8s.io/apimachinery/pkg/util/sets:go_default_library",
        "//cmd/vendor/k8s.io/client-go/tools/cache:go_default_library",
    ],
)
