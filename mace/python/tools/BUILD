py_library(
    name = "converter_lib",
    srcs = [
        "convert_util.py",
        "graph_util.py",
        "tf_dsp_converter_lib.py",
        "converter_tool/base_converter.py",
        "converter_tool/shape_inference.py",
        "converter_tool/tensorflow_converter.py",
        "converter_tool/caffe_converter.py",
        "converter_tool/transformer.py",
    ],
    srcs_version = "PY2AND3",
    deps = [
        ":memory_optimizer",
        "//mace/proto:mace_py",
        "//third_party/caffe:caffe_py",
    ],
)

py_library(
    name = "model_saver_lib",
    srcs = [
        "model_saver.py",
    ],
    srcs_version = "PY2AND3",
    deps = [
        "//mace/proto:mace_py",
    ],
)

py_binary(
    name = "memory_optimizer",
    srcs = ["memory_optimizer.py"],
    srcs_version = "PY2AND3",
    deps = [
        "//mace/proto:mace_py",
    ],
)

py_binary(
    name = "converter",
    srcs = ["converter.py"],
    srcs_version = "PY2AND3",
    deps = [
        ":converter_lib",
        ":model_saver_lib",
        "@six_archive//:six",
    ],
)
