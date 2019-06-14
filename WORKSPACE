load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")
load("@bazel_tools//tools/build_defs/repo:git.bzl", "git_repository")


########################
# BOOST:

git_repository(
    name = "com_github_nelhage_rules_boost",
    commit = "6d6fd834281cb8f8e758dd9ad76df86304bf1869",
    shallow_since = "1543903644 -0800",
    remote = "https://github.com/nelhage/rules_boost",
)

load("@com_github_nelhage_rules_boost//:boost/boost.bzl", "boost_deps")
boost_deps()

########################
# External CC

http_archive(
   name = "rules_foreign_cc",
   strip_prefix = "rules_foreign_cc-master",
   url = "https://github.com/bazelbuild/rules_foreign_cc/archive/master.zip",
   sha256 = "353e41e99f93c0219994a7c4402a80cd04bd044703818d199c66ff82ec4ee85b"
)

load("@rules_foreign_cc//:workspace_definitions.bzl", "rules_foreign_cc_dependencies")
rules_foreign_cc_dependencies()

########################
# Catch

http_archive(
    name = "catch",
    url = "https://github.com/cgrinker/Catch2/archive/5e6488fd9949cb41d717a72c8c4603b7e37d68cd.zip",
    sha256 = "91e3e0610572adefa301a6e55ac48ab0a3c8ff61787ce6930e346ff36e86905c",
    strip_prefix = "Catch2-5e6488fd9949cb41d717a72c8c4603b7e37d68cd",
)

########################
# spdlog:

http_archive(
    name = "spdlog",
    urls = ["https://github.com/cgrinker/spdlog/archive/3bf4a07dc286e10fa32d6503fded647c9ee02d26.zip"],
    strip_prefix = "spdlog-3bf4a07dc286e10fa32d6503fded647c9ee02d26",
    sha256 = "d00ccd202e2abae832441b9121330a4b8b82fdc60564edb315c89506fa3772c3",
)

########################
# stdext
http_archive(
    name = "stdext",
    urls = ["https://github.com/cultlang/stdext/archive/v1.0.0.zip"],
    strip_prefix = "stdext-1.0.0",
    sha256 = "2c008ad1de4e520c2b7ef24ea6d20e677afd1cf411274cb89da7aa08e853b3f1",
)

########################
# Fmt
http_archive(
    name = "fmt",
    urls = ["https://github.com/cgrinker/fmt/archive/f16f77297e6bb4df38d4c858edb3295f55716cb4.zip"],
    strip_prefix = "fmt-f16f77297e6bb4df38d4c858edb3295f55716cb4",
    sha256 = "edcacda20bf46be208fbc49cedee2a8a321005dd833752ccc6aa7a1a9d75dc23",
)
