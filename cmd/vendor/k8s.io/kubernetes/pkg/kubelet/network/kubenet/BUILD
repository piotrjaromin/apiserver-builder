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
        "kubenet.go",
        "kubenet_unsupported.go",
    ] + select({
        "@io_bazel_rules_go//go/platform:linux_amd64": [
            "kubenet_linux.go",
        ],
        "//conditions:default": [],
    }),
    importpath = "k8s.io/kubernetes/pkg/kubelet/network/kubenet",
    tags = ["automanaged"],
    deps = [
        "//cmd/vendor/k8s.io/kubernetes/pkg/apis/componentconfig:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/pkg/kubelet/container:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/pkg/kubelet/network:go_default_library",
    ] + select({
        "@io_bazel_rules_go//go/platform:linux_amd64": [
            "//vendor/github.com/containernetworking/cni/libcni:go_default_library",
            "//vendor/github.com/containernetworking/cni/pkg/types:go_default_library",
            "//vendor/github.com/containernetworking/cni/pkg/types/020:go_default_library",
            "//cmd/vendor/github.com/golang/glog:go_default_library",
            "//vendor/github.com/vishvananda/netlink:go_default_library",
            "//cmd/vendor/k8s.io/api/core/v1:go_default_library",
            "//cmd/vendor/k8s.io/apimachinery/pkg/util/errors:go_default_library",
            "//cmd/vendor/k8s.io/apimachinery/pkg/util/net:go_default_library",
            "//cmd/vendor/k8s.io/apimachinery/pkg/util/sets:go_default_library",
            "//cmd/vendor/k8s.io/kubernetes/pkg/kubelet/network/hostport:go_default_library",
            "//cmd/vendor/k8s.io/kubernetes/pkg/util/bandwidth:go_default_library",
            "//cmd/vendor/k8s.io/kubernetes/pkg/util/dbus:go_default_library",
            "//cmd/vendor/k8s.io/kubernetes/pkg/util/ebtables:go_default_library",
            "//cmd/vendor/k8s.io/kubernetes/pkg/util/exec:go_default_library",
            "//cmd/vendor/k8s.io/kubernetes/pkg/util/iptables:go_default_library",
            "//cmd/vendor/k8s.io/kubernetes/pkg/util/sysctl:go_default_library",
        ],
        "//conditions:default": [],
    }),
)

go_test(
    name = "go_default_test",
    srcs = select({
        "@io_bazel_rules_go//go/platform:linux_amd64": [
            "kubenet_linux_test.go",
        ],
        "//conditions:default": [],
    }),
    importpath = "k8s.io/kubernetes/pkg/kubelet/network/kubenet",
    library = ":go_default_library",
    tags = ["automanaged"],
    deps = select({
        "@io_bazel_rules_go//go/platform:linux_amd64": [
            "//vendor/github.com/stretchr/testify/assert:go_default_library",
            "//vendor/github.com/stretchr/testify/mock:go_default_library",
            "//cmd/vendor/k8s.io/kubernetes/pkg/apis/componentconfig:go_default_library",
            "//cmd/vendor/k8s.io/kubernetes/pkg/kubelet/container:go_default_library",
            "//cmd/vendor/k8s.io/kubernetes/pkg/kubelet/network:go_default_library",
            "//cmd/vendor/k8s.io/kubernetes/pkg/kubelet/network/cni/testing:go_default_library",
            "//cmd/vendor/k8s.io/kubernetes/pkg/kubelet/network/hostport/testing:go_default_library",
            "//cmd/vendor/k8s.io/kubernetes/pkg/kubelet/network/testing:go_default_library",
            "//cmd/vendor/k8s.io/kubernetes/pkg/util/bandwidth:go_default_library",
            "//cmd/vendor/k8s.io/kubernetes/pkg/util/exec:go_default_library",
            "//cmd/vendor/k8s.io/kubernetes/pkg/util/iptables/testing:go_default_library",
            "//cmd/vendor/k8s.io/kubernetes/pkg/util/sysctl/testing:go_default_library",
        ],
        "//conditions:default": [],
    }),
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
