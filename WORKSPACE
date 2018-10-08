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
workspace(name = "tensorflow_lattice")

local_repository(
    name = "org_tensorflow",
    path = "tensorflow",
)

# This rule is from TensorFlow's WORKSPACE.
http_archive(
    name = "io_bazel_rules_closure",
    sha256 = "a38539c5b5c358548e75b44141b4ab637bba7c4dc02b46b1f62a96d6433f56ae",
    strip_prefix = "rules_closure-dbb96841cc0a5fb2664c37822803b06dab20c7d1",
    urls = [
        "https://mirror.bazel.build/github.com/bazelbuild/rules_closure/archive/dbb96841cc0a5fb2664c37822803b06dab20c7d1.tar.gz",
        "https://github.com/bazelbuild/rules_closure/archive/dbb96841cc0a5fb2664c37822803b06dab20c7d1.tar.gz",  # 2018-04-13
    ],
)

PROTOBUF_URLS = [
    "https://mirror.bazel.build/github.com/google/protobuf/archive/v3.6.0.tar.gz",
    "https://github.com/google/protobuf/archive/v3.6.0.tar.gz",
]
PROTOBUF_SHA256 = "50a5753995b3142627ac55cfd496cebc418a2e575ca0236e29033c67bd5665f4"
PROTOBUF_STRIP_PREFIX = "protobuf-3.6.0"

http_archive(
    name = "protobuf_archive",
    sha256 = PROTOBUF_SHA256,
    strip_prefix = PROTOBUF_STRIP_PREFIX,
    urls = PROTOBUF_URLS,
)

load("//tf:tf_configure.bzl", "tf_configure")

tf_configure(
    name = "local_config_tf",
)