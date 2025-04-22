load("@aspect_rules_py//py:defs.bzl", "py_binary")

py_binary(
    name = "build_wheel",
    srcs = [
        "setup.py",
    ],
    args = [
        "build_ext",
        "-j64",
        "bdist_wheel",
    ],
    data = glob(
        [
            "*",
            "core/**/target/*",
            "bin/*",
            "*.py",
            "**/*.py",
        ],
        allow_empty = True,
        exclude_directories = 0,
    ),
    deps = [
        "@pip//grpcio_tools:pkg",
        "@pip//netifaces:pkg",
        "@pip//numpy:pkg",
        "@pip//packaging:pkg",
        "@pip//pandas:pkg",
        "@pip//pip:pkg",
        "@pip//protobuf:pkg",
        "@pip//pyspark:pkg",
        "@pip//ray:pkg",
        "@pip//setuptools:pkg",
        "@pip//wheel:pkg",
    ],
)
