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

exports_files(["LICENSE"])

package(
    default_visibility = [
        "//tensorflow_lattice:__subpackages__",
    ],
)


cc_binary(
    name = "ops/_lattice_ops.so",
    srcs = [
        ":ops/lattice_interpolation_ops.cc",
        ":ops/monotone_lattice_ops.cc",
    ],
    deps = [
        "//tensorflow_lattice/cc/kernels:lattice_kernels",
        "//tensorflow_lattice/cc/lib:lattice_structure",
        "@local_config_tf//:libtensorflow_framework",
        "@local_config_tf//:tf_header_lib",        
    ],
    copts = ["-pthread", "-std=c++11", "-D_GLIBCXX_USE_CXX11_ABI=0"],
    linkshared = True,
)

cc_binary(
    name = "ops/_pwl_calibration_ops.so",
    srcs = [
        ":ops/monotonic_projection_op.cc",
        ":ops/pwl_indexing_calibrator_ops.cc",
    ],
    deps = [
        "//tensorflow_lattice/cc/kernels:pwl_calibration_kernels",
        "@local_config_tf//:libtensorflow_framework",
        "@local_config_tf//:tf_header_lib",        
    ],
    copts = ["-pthread", "-std=c++11", "-D_GLIBCXX_USE_CXX11_ABI=0"],
    linkshared = True,
)