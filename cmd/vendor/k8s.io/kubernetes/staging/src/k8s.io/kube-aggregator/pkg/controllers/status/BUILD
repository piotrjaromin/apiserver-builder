package(default_visibility = ["//visibility:public"])

licenses(["notice"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_library",
    "go_test",
)

go_library(
    name = "go_default_library",
    srcs = ["available_controller.go"],
    importpath = "k8s.io/kubernetes/staging/src/k8s.io/kube-aggregator/pkg/controllers/status",
    tags = ["automanaged"],
    deps = [
        "//cmd/vendor/github.com/golang/glog:go_default_library",
        "//cmd/vendor/k8s.io/api/core/v1:go_default_library",
        "//cmd/vendor/k8s.io/apimachinery/pkg/api/errors:go_default_library",
        "//cmd/vendor/k8s.io/apimachinery/pkg/api/meta:go_default_library",
        "//cmd/vendor/k8s.io/apimachinery/pkg/apis/meta/v1:go_default_library",
        "//cmd/vendor/k8s.io/apimachinery/pkg/conversion:go_default_library",
        "//cmd/vendor/k8s.io/apimachinery/pkg/labels:go_default_library",
        "//cmd/vendor/k8s.io/apimachinery/pkg/runtime:go_default_library",
        "//cmd/vendor/k8s.io/apimachinery/pkg/util/runtime:go_default_library",
        "//cmd/vendor/k8s.io/apimachinery/pkg/util/wait:go_default_library",
        "//cmd/vendor/k8s.io/client-go/informers/core/v1:go_default_library",
        "//cmd/vendor/k8s.io/client-go/listers/core/v1:go_default_library",
        "//cmd/vendor/k8s.io/client-go/tools/cache:go_default_library",
        "//cmd/vendor/k8s.io/client-go/util/workqueue:go_default_library",
        "//cmd/vendor/k8s.io/kube-aggregator/pkg/apis/apiregistration:go_default_library",
        "//cmd/vendor/k8s.io/kube-aggregator/pkg/client/clientset_generated/internalclientset/typed/apiregistration/internalversion:go_default_library",
        "//cmd/vendor/k8s.io/kube-aggregator/pkg/client/informers/internalversion/apiregistration/internalversion:go_default_library",
        "//cmd/vendor/k8s.io/kube-aggregator/pkg/client/listers/apiregistration/internalversion:go_default_library",
        "//cmd/vendor/k8s.io/kube-aggregator/pkg/controllers:go_default_library",
    ],
)

go_test(
    name = "go_default_test",
    srcs = ["available_controller_test.go"],
    importpath = "k8s.io/kubernetes/staging/src/k8s.io/kube-aggregator/pkg/controllers/status",
    library = ":go_default_library",
    tags = ["automanaged"],
    deps = [
        "//cmd/vendor/k8s.io/api/core/v1:go_default_library",
        "//cmd/vendor/k8s.io/apimachinery/pkg/apis/meta/v1:go_default_library",
        "//cmd/vendor/k8s.io/client-go/listers/core/v1:go_default_library",
        "//cmd/vendor/k8s.io/client-go/testing:go_default_library",
        "//cmd/vendor/k8s.io/client-go/tools/cache:go_default_library",
        "//cmd/vendor/k8s.io/kube-aggregator/pkg/apis/apiregistration:go_default_library",
        "//cmd/vendor/k8s.io/kube-aggregator/pkg/client/clientset_generated/internalclientset/fake:go_default_library",
        "//cmd/vendor/k8s.io/kube-aggregator/pkg/client/listers/apiregistration/internalversion:go_default_library",
    ],
)
