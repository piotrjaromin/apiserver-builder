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
        "checkpoint_store.go",
        "convert.go",
        "doc.go",
        "docker_checkpoint.go",
        "docker_container.go",
        "docker_image.go",
        "docker_legacy.go",
        "docker_sandbox.go",
        "docker_service.go",
        "docker_stats.go",
        "docker_streaming.go",
        "exec.go",
        "helpers.go",
        "helpers_unsupported.go",
        "naming.go",
        "security_context.go",
        "selinux_util.go",
    ] + select({
        "@io_bazel_rules_go//go/platform:linux_amd64": [
            "helpers_linux.go",
        ],
        "@io_bazel_rules_go//go/platform:windows_amd64": [
            "helpers_windows.go",
        ],
        "//conditions:default": [],
    }),
    importpath = "k8s.io/kubernetes/pkg/kubelet/dockershim",
    tags = ["automanaged"],
    deps = [
        "//vendor/github.com/blang/semver:go_default_library",
        "//vendor/github.com/docker/docker/api/types:go_default_library",
        "//vendor/github.com/docker/docker/api/types/container:go_default_library",
        "//vendor/github.com/docker/docker/api/types/filters:go_default_library",
        "//vendor/github.com/docker/docker/api/types/strslice:go_default_library",
        "//vendor/github.com/docker/docker/pkg/jsonmessage:go_default_library",
        "//vendor/github.com/docker/go-connections/nat:go_default_library",
        "//cmd/vendor/github.com/golang/glog:go_default_library",
        "//cmd/vendor/k8s.io/api/core/v1:go_default_library",
        "//cmd/vendor/k8s.io/apimachinery/pkg/apis/meta/v1:go_default_library",
        "//cmd/vendor/k8s.io/apimachinery/pkg/util/errors:go_default_library",
        "//cmd/vendor/k8s.io/apimachinery/pkg/util/sets:go_default_library",
        "//cmd/vendor/k8s.io/apimachinery/pkg/util/wait:go_default_library",
        "//cmd/vendor/k8s.io/client-go/tools/remotecommand:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/pkg/apis/componentconfig:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/pkg/credentialprovider:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/pkg/kubelet/apis/cri:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/pkg/kubelet/apis/cri/v1alpha1/runtime:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/pkg/kubelet/cm:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/pkg/kubelet/container:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/pkg/kubelet/dockershim/cm:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/pkg/kubelet/dockershim/errors:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/pkg/kubelet/dockershim/libdocker:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/pkg/kubelet/leaky:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/pkg/kubelet/network:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/pkg/kubelet/network/cni:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/pkg/kubelet/network/hostport:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/pkg/kubelet/network/kubenet:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/pkg/kubelet/qos:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/pkg/kubelet/server/streaming:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/pkg/kubelet/types:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/pkg/kubelet/util/cache:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/pkg/kubelet/util/ioutils:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/pkg/security/apparmor:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/pkg/util/exec:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/pkg/util/hash:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/pkg/util/term:go_default_library",
    ],
)

go_test(
    name = "go_default_test",
    srcs = [
        "checkpoint_store_test.go",
        "convert_test.go",
        "docker_checkpoint_test.go",
        "docker_container_test.go",
        "docker_image_test.go",
        "docker_legacy_test.go",
        "docker_sandbox_test.go",
        "docker_service_test.go",
        "helpers_test.go",
        "naming_test.go",
        "security_context_test.go",
        "selinux_util_test.go",
    ] + select({
        "@io_bazel_rules_go//go/platform:linux_amd64": [
            "helpers_linux_test.go",
        ],
        "//conditions:default": [],
    }),
    data = [
        "fixtures/seccomp/sub/subtest",
        "fixtures/seccomp/test",
    ],
    importpath = "k8s.io/kubernetes/pkg/kubelet/dockershim",
    library = ":go_default_library",
    tags = ["automanaged"],
    deps = [
        "//vendor/github.com/blang/semver:go_default_library",
        "//vendor/github.com/docker/docker/api/types:go_default_library",
        "//vendor/github.com/docker/docker/api/types/container:go_default_library",
        "//vendor/github.com/docker/docker/pkg/jsonmessage:go_default_library",
        "//vendor/github.com/docker/go-connections/nat:go_default_library",
        "//cmd/vendor/github.com/golang/mock/gomock:go_default_library",
        "//vendor/github.com/stretchr/testify/assert:go_default_library",
        "//vendor/github.com/stretchr/testify/require:go_default_library",
        "//cmd/vendor/k8s.io/apimachinery/pkg/util/clock:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/pkg/kubelet/apis/cri/v1alpha1/runtime:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/pkg/kubelet/container:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/pkg/kubelet/container/testing:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/pkg/kubelet/dockershim/errors:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/pkg/kubelet/dockershim/libdocker:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/pkg/kubelet/dockershim/testing:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/pkg/kubelet/network:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/pkg/kubelet/network/testing:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/pkg/kubelet/types:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/pkg/kubelet/util/cache:go_default_library",
        "//cmd/vendor/k8s.io/kubernetes/pkg/security/apparmor:go_default_library",
    ] + select({
        "@io_bazel_rules_go//go/platform:linux_amd64": [
            "//cmd/vendor/k8s.io/api/core/v1:go_default_library",
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
    srcs = [
        ":package-srcs",
        "//pkg/kubelet/dockershim/cm:all-srcs",
        "//pkg/kubelet/dockershim/errors:all-srcs",
        "//pkg/kubelet/dockershim/libdocker:all-srcs",
        "//pkg/kubelet/dockershim/remote:all-srcs",
        "//pkg/kubelet/dockershim/testing:all-srcs",
    ],
    tags = ["automanaged"],
)
