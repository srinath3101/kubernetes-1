load("@io_bazel_rules_go//go:def.bzl", "go_library", "go_test")

go_library(
    name = "go_default_library",
    srcs = [
        "cache.go",
        "extended_resources.go",
        "interface.go",
        "node_info.go",
        "util.go",
    ],
    importpath = "k8s.io/kubernetes/plugin/pkg/scheduler/schedulercache",
    visibility = ["//visibility:public"],
    deps = [
        "//pkg/apis/core/v1/helper:go_default_library",
        "//plugin/pkg/scheduler/algorithm/priorities/util:go_default_library",
        "//plugin/pkg/scheduler/util:go_default_library",
        "//vendor/github.com/golang/glog:go_default_library",
        "//vendor/k8s.io/api/core/v1:go_default_library",
        "//vendor/k8s.io/api/policy/v1beta1:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/api/resource:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/labels:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/util/wait:go_default_library",
        "//vendor/k8s.io/client-go/tools/cache:go_default_library",
    ],
)

go_test(
    name = "go_default_test",
    srcs = [
        "cache_test.go",
        "node_info_test.go",
    ],
    importpath = "k8s.io/kubernetes/plugin/pkg/scheduler/schedulercache",
    library = ":go_default_library",
    deps = [
        "//plugin/pkg/scheduler/algorithm/priorities/util:go_default_library",
        "//plugin/pkg/scheduler/util:go_default_library",
        "//vendor/github.com/stretchr/testify/require:go_default_library",
        "//vendor/k8s.io/api/core/v1:go_default_library",
        "//vendor/k8s.io/api/policy/v1beta1:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/api/resource:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/apis/meta/v1:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/labels:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/util/intstr:go_default_library",
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
    visibility = ["//visibility:public"],
)
