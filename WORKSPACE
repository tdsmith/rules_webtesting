# Copyright 2016 Google Inc.
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
#
################################################################################
#
workspace(name = "io_bazel_rules_webtesting")

http_archive(
    name = "io_bazel_rules_go",
    sha256 = "f7e42a4c1f9f31abff9b2bdee6fe4db18bc373287b7e07a5b844446e561e67e2",
    strip_prefix = "rules_go-4c9a52aba0b59511c5646af88d2f93a9c0193647",
    urls = [
        "http://mirror.bazel.build/github.com/bazelbuild/rules_go/archive/4c9a52aba0b59511c5646af88d2f93a9c0193647.tar.gz",
        "https://github.com/bazelbuild/rules_go/archive/4c9a52aba0b59511c5646af88d2f93a9c0193647.tar.gz",
    ],
)

load("@io_bazel_rules_go//go:def.bzl", "go_repositories")

go_repositories()

load("//web:repositories.bzl", "browser_repositories", "web_test_repositories")

web_test_repositories()

browser_repositories(
    chromium = True,
    firefox = True,
)

http_archive(
    name = "io_bazel_rules_sass",
    sha256 = "4bd44d81747d06e8334570d413b714218b7759db0883df807e28127e9d59fe80",
    strip_prefix = "rules_sass-931508528093364b86abd44a5b9401e5150f1ba7",
    urls = [
        "http://mirror.bazel.build/github.com/bazelbuild/rules_sass/archive/931508528093364b86abd44a5b9401e5150f1ba7.tar.gz",
        "https://github.com/bazelbuild/rules_sass/archive/931508528093364b86abd44a5b9401e5150f1ba7.tar.gz",
    ],
)

load("@io_bazel_rules_sass//sass:sass.bzl", "sass_repositories")

sass_repositories()

http_archive(
    name = "io_bazel_skydoc",
    sha256 = "06d855d8412cae1461d4131481a26d71ba9457914473803df65b110ea4dd6a88",
    strip_prefix = "skydoc-0.1.1",
    urls = [
        "http://mirror.bazel.build/github.com/bazelbuild/skydoc/archive/0.1.1.tar.gz",
        "https://github.com/bazelbuild/skydoc/archive/0.1.1.tar.gz",
    ],
)

load("@io_bazel_skydoc//skylark:skylark.bzl", "skydoc_repositories")

skydoc_repositories()
