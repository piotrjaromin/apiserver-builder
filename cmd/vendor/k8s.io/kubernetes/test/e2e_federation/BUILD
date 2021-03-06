package(default_visibility = ["//visibility:public"])

licenses(["notice"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_library",
)

go_library(
    name = "go_default_library",
    srcs = [
        "apiserver.go",
        "authn.go",
        "crud.go",
        "event.go",
        "ingress.go",
        "namespace.go",
        "replicaset.go",
        "service.go",
        "upgrade.go",
        "util.go",
    ],
    importpath = "k8s.io/kubernetes/test/e2e_federation",
    tags = ["automanaged"],
    deps = [
        "//cmd/vendor/github.com/onsi/ginkgo:go_default_library",
        "//cmd/vendor/github.com/onsi/gomega:go_default_library",
        "//cmd/vendor/k8s.io/api/core/v1:go_default_library",
        "//cmd/vendor/k8s.io/api/extensions/v1beta1:go_default_library",
        "//cmd/vendor/k8s.io/apimachinery/pkg/api/errors:go_default_library",
        "//cmd/vendor/k8s.io/apimachinery/pkg/apis/meta/v1:go_default_library",
        "//cmd/vendor/k8s.io/apimachinery/pkg/util/intstr:go_default_library",
        "//cmd/vendor/k8s.io/apimachinery/pkg/util/net:go_default_library",
        "//cmd/vendor/k8s.io/apimachinery/pkg/util/rand:go_default_library",
        "//cmd/vendor/k8s.io/apimachinery/pkg/util/uuid:go_default_library",
        "//cmd/vendor/k8s.io/apimachinery/pkg/util/wait:go_default_library",
        "//cmd/vendor/k8s.io/client-go/kubernetes:go_default_library",
        "//cmd/vendor/k8s.io/client-go/kubernetes/scheme:go_default_library",
        "//cmd/vendor/k8s.io/client-go/tools/clientcmd:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/federation/apis/federation:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/federation/apis/federation/v1beta1:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/federation/client/clientset_generated/federation_clientset:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/federation/client/clientset_generated/federation_clientset/typed/core/v1:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/federation/pkg/federatedtypes:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/federation/pkg/federation-controller/util:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/pkg/api/v1:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/pkg/cloudprovider:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/test/e2e/chaosmonkey:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/test/e2e/common:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/test/e2e/framework:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/test/e2e_federation/framework:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/test/e2e_federation/upgrades:go_default_library",
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
    srcs = [
        ":package-srcs",
        "//test/e2e_federation/framework:all-srcs",
        "//test/e2e_federation/upgrades:all-srcs",
    ],
    tags = ["automanaged"],
)
