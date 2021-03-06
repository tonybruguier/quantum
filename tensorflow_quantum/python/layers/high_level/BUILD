package(default_visibility = ["//visibility:public"])

licenses(["notice"])

# Export for the PIP package.
exports_files(["__init__.py"])

py_library(
    name = "high_level",
    srcs = ["__init__.py"],
    srcs_version = "PY3",
    deps = [
        ":controlled_pqc",
        ":noisy_controlled_pqc",
        ":pqc",
        ":noisy_pqc",
    ],
)

py_library(
    name = "controlled_pqc",
    srcs = ["controlled_pqc.py"],
    srcs_version = "PY3",
    deps = [
        "//tensorflow_quantum/python:util",
        "//tensorflow_quantum/python/layers/circuit_construction:elementary",
        "//tensorflow_quantum/python/layers/circuit_executors:expectation",
        "//tensorflow_quantum/python/layers/circuit_executors:sampled_expectation",
    ],
)

py_library(
    name = "noisy_controlled_pqc",
    srcs = ["noisy_controlled_pqc.py"],
    srcs_version = "PY3",
    deps = [
        "//tensorflow_quantum/python:util",
        "//tensorflow_quantum/python/layers/circuit_construction:elementary",
        "//tensorflow_quantum/core/ops/noise:noisy_expectation_op_py",
        "//tensorflow_quantum/core/ops/noise:noisy_sampled_expectation_op_py",
        "//tensorflow_quantum/python/differentiators:parameter_shift",
    ],
)

py_library(
    name = "pqc",
    srcs = ["pqc.py"],
    srcs_version = "PY3",
    deps = [
        "//tensorflow_quantum/python:util",
        "//tensorflow_quantum/python/layers/circuit_construction:elementary",
        "//tensorflow_quantum/python/layers/circuit_executors:expectation",
        "//tensorflow_quantum/python/layers/circuit_executors:sampled_expectation",
    ],
)

py_library(
    name = "noisy_pqc",
    srcs = ["noisy_pqc.py"],
    srcs_version = "PY3",
    deps = [
        "//tensorflow_quantum/python:util",
        "//tensorflow_quantum/python/layers/circuit_construction:elementary",
        "//tensorflow_quantum/core/ops/noise:noisy_expectation_op_py",
        "//tensorflow_quantum/core/ops/noise:noisy_sampled_expectation_op_py",
        "//tensorflow_quantum/python/differentiators:parameter_shift",
    ],
)

py_test(
    name = "controlled_pqc_test",
    srcs = ["controlled_pqc_test.py"],
    python_version = "PY3",
    deps = [
        ":controlled_pqc",
        "//tensorflow_quantum/python:util",
    ],
)

py_test(
    name = "pqc_test",
    srcs = ["pqc_test.py"],
    python_version = "PY3",
    deps = [
        ":pqc",
        "//tensorflow_quantum/python:util",
    ],
)

py_test(
    name = "noisy_controlled_pqc_test",
    srcs = ["noisy_controlled_pqc_test.py"],
    python_version = "PY3",
    deps = [
        ":noisy_controlled_pqc",
        "//tensorflow_quantum/python:util",
    ],
)
      
py_test(
    name = "noisy_pqc_test",
    srcs = ["noisy_pqc_test.py"],
    python_version = "PY3",
    deps = [
        ":noisy_pqc",
        "//tensorflow_quantum/python:util",
    ],
)
