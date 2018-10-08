# Copyright 2017 The TensorFlow Lattice Authors.
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#      http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.
# ==============================================================================
licenses(["notice"])  # Apache 2.0 License

package(
    default_visibility = [
        "//tensorflow_lattice:__subpackages__",
    ],
)

exports_files(["LICENSE"])

# All python tests can run under python 2 and 3.

# estimators.
py_library(
    name = "hparams",
    srcs = ["hparams.py"],
    srcs_version = "PY2AND3",
    deps = [
        "//tensorflow_lattice/python:regularizers",
    ],
)

py_test(
    name = "hparams_test",
    size = "small",
    srcs = ["hparams_test.py"],
    srcs_version = "PY2AND3",
    deps = [
        ":hparams",
    ],
)

py_library(
    name = "base",
    srcs = ["base.py"],
    srcs_version = "PY2AND3",
    deps = [
        "//tensorflow_lattice/python:tools",
    ],
)

py_test(
    name = "base_test",
    size = "medium",
    srcs = ["base_test.py"],
    srcs_version = "PY2AND3",
    deps = [
        ":base",
        "//tensorflow_lattice/python:test_data",
    ],
)

py_library(
    name = "calibrated",
    srcs = ["calibrated.py"],
    srcs_version = "PY2AND3",
    deps = [
        ":base",
        ":hparams",
        "//tensorflow_lattice/python:keypoints_initialization",
        "//tensorflow_lattice/python:pwl_calibration_layers",
        "//tensorflow_lattice/python:regularizers",
        "//tensorflow_lattice/python:tools",
    ],
)

py_test(
    name = "calibrated_test",
    size = "small",
    srcs = ["calibrated_test.py"],
    srcs_version = "PY2AND3",
    deps = [
        ":calibrated",
    ],
)

py_library(
    name = "calibrated_linear",
    srcs = ["calibrated_linear.py"],
    srcs_version = "PY2AND3",
    deps = [
        ":calibrated",
        ":hparams",
    ],
)

py_test(
    name = "calibrated_linear_test",
    size = "large",
    srcs = ["calibrated_linear_test.py"],
    srcs_version = "PY2AND3",
    deps = [
        ":calibrated_linear",
        "//tensorflow_lattice/python:test_data",
    ],
)

py_library(
    name = "calibrated_lattice",
    srcs = ["calibrated_lattice.py"],
    srcs_version = "PY2AND3",
    deps = [
        ":calibrated",
        ":hparams",
        "//tensorflow_lattice/python:lattice_layers",
        "//tensorflow_lattice/python:regularizers",
    ],
)

py_test(
    name = "calibrated_lattice_test",
    size = "large",
    srcs = ["calibrated_lattice_test.py"],
    srcs_version = "PY2AND3",
    deps = [
        ":calibrated_lattice",
        "//tensorflow_lattice/python:test_data",
    ],
)

py_library(
    name = "calibrated_rtl",
    srcs = ["calibrated_rtl.py"],
    srcs_version = "PY2AND3",
    deps = [
        ":calibrated",
        ":hparams",
        "//tensorflow_lattice/python:lattice_layers",
        "//tensorflow_lattice/python:regularizers",
    ],
)

py_test(
    name = "calibrated_rtl_test",
    size = "large",
    srcs = ["calibrated_rtl_test.py"],
    srcs_version = "PY2AND3",
    deps = [
        ":calibrated_rtl",
        "//tensorflow_lattice/python:test_data",
    ],
)

py_library(
    name = "calibrated_etl",
    srcs = ["calibrated_etl.py"],
    srcs_version = "PY2AND3",
    deps = [
        ":calibrated",
        ":hparams",
        "//tensorflow_lattice/python:lattice_layers",
        "//tensorflow_lattice/python:monotone_linear_layers",
        "//tensorflow_lattice/python:pwl_calibration_layers",
        "//tensorflow_lattice/python:regularizers",
    ],
)

py_test(
    name = "calibrated_etl_test",
    size = "large",
    srcs = ["calibrated_etl_test.py"],
    srcs_version = "PY2AND3",
    deps = [
        ":calibrated_etl",
        "//tensorflow_lattice/python:test_data",
    ],
)

py_library(
    name = "separately_calibrated_rtl",
    srcs = ["separately_calibrated_rtl.py"],
    srcs_version = "PY2AND3",
    deps = [
        ":calibrated",
        ":hparams",
        "//tensorflow_lattice/python:lattice_layers",
        "//tensorflow_lattice/python:regularizers",
    ],
)

py_test(
    name = "separately_calibrated_rtl_test",
    size = "large",
    srcs = ["separately_calibrated_rtl_test.py"],
    srcs_version = "PY2AND3",
    deps = [
        ":separately_calibrated_rtl",
        "//tensorflow_lattice/python:test_data",
    ],
)
