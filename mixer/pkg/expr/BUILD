load("@io_bazel_rules_go//go:def.bzl", "go_library", "go_test")

go_library(
    name = "go_default_library",
    srcs = [
        "evaluator.go",
        "expr.go",
        "func.go",
    ],
    visibility = ["//visibility:public"],
    deps = [
        "//mixer/pkg/attribute:go_default_library",
        "//mixer/pkg/config/proto:go_default_library",
        "//mixer/pkg/pool:go_default_library",
        "@com_github_golang_glog//:go_default_library",
        "@io_istio_api//mixer/v1/config/descriptor:descriptor",
    ],
)

go_test(
    name = "go_default_test",
    size = "small",
    srcs = [
        "expr_test.go",
    ],
    library = ":go_default_library",
    deps = [
        "//mixer/pkg/config/proto:go_default_library",
        "@io_istio_api//mixer/v1/config/descriptor:descriptor",
    ],
)
