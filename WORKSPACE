workspace(name = "com_github_livegrep_livegrep")

git_repository(
  name = "org_pubref_rules_protobuf",
  remote = "https://github.com/pubref/rules_protobuf",
  commit = "7d12b7e3f1d40086a2d28ce900cd7980ab8f2758",
)

load("//tools/build_defs:externals.bzl",
     "new_patched_http_archive",
)

new_patched_http_archive(
  name = "divsufsort",
  url = "https://codeload.github.com/y-256/libdivsufsort/tar.gz/2.0.1",
  sha256 = "9164cb6044dcb6e430555721e3318d5a8f38871c2da9fd9256665746a69351e0",
  build_file = "//third_party:BUILD.divsufsort",
  patch_file = "//third_party:divsufsort.patch",
  strip_prefix = "libdivsufsort-2.0.1",
  type = "tgz",
)

git_repository(
  name = "com_googlesource_code_re2",
  remote = "git://github.com/google/re2",
  commit = "b94b7cd42e9f02673cd748c1ac1d16db4052514c",
)

git_repository(
  name = "gflags",
  remote = "git://github.com/gflags/gflags",
  commit = "a69b2544d613b4bee404988710503720c487119a"
)

git_repository(
  name = "com_github_nelhage_boost",
  remote = "git://github.com/nelhage/rules_boost",
  commit = "c0740579878e84ca98eddc826003b6eecefbb5ff",
)
# local_repository(
#   name = "com_github_nelhage_boost",
#   path = "../rules_boost",
# )

load("@com_github_nelhage_boost//:boost/boost.bzl",
     "boost_deps")
boost_deps()

new_patched_http_archive(
  name = "com_github_sparsehash",
  url = "https://github.com/sparsehash/sparsehash/archive/sparsehash-2.0.3.tar.gz",
  sha256 = "05e986a5c7327796dad742182b2d10805a8d4f511ad090da0490f146c1ff7a8c",
  build_file = "//third_party:BUILD.sparsehash",
  strip_prefix = "sparsehash-sparsehash-2.0.3/",
  patch_file = "//third_party:sparsehash.patch",
)

new_patched_http_archive(
  name = "com_github_json_c",
  url = "https://s3.amazonaws.com/json-c_releases/releases/json-c-0.12.1-nodoc.tar.gz",
  sha256 = "5a617da9aade997938197ef0f8aabd7f97b670c216dc173977e1d56eef9e1291",
  strip_prefix = "json-c-0.12.1",
  build_file = "//third_party:BUILD.json_c",
  patch_file = "//third_party:json_c.patch",
  add_prefix = "json-c",
)

git_repository(
    name = "io_bazel_rules_go",
    remote = "https://github.com/bazelbuild/rules_go.git",
    commit = "3b13b2dba81e09ec213ccbd4da56ad332cb5d3dc",
)

load("@io_bazel_rules_go//go:def.bzl",
     "go_repositories", "new_go_repository")

go_repositories()
new_go_repository(
  name = "org_golang_x_net",
  importpath = "golang.org/x/net",
  commit = "73058b0420c0c24a7f9ec3eb6f624ac85d2ed035",
)

new_go_repository(
  name = "org_golang_google_appengine",
  importpath = "google.golang.org/appengine/",
  commit = "46239ca616842c00f41b8cbc6bbf2bd6ffbfcdad",
)

new_go_repository(
  name = "org_golang_x_oauth2",
  importpath = "golang.org/x/oauth2",
  commit = "25b4fb1468cb89700c7c060cb99f30581a61f5e3",
)

load("//tools/build_defs:libgit2.bzl",
     "new_libgit2_archive",
)

new_libgit2_archive(
  name = "com_github_libgit2",
  url = "https://github.com/libgit2/libgit2/archive/v0.24.1.tar.gz",
  version = "0.24.1",
  sha256 = "0269ec198c54e44f275f8f51e7391681a03aa45555e2ab6ce60b0757b6bde3de",
  build_file = "//third_party:BUILD.libgit2",
)

load("@org_pubref_rules_protobuf//go:rules.bzl", "go_proto_repositories")
load("@org_pubref_rules_protobuf//cpp:rules.bzl", "cpp_proto_repositories")

go_proto_repositories();
cpp_proto_repositories();

git_repository(
    name = "io_bazel_buildifier",
    commit = "0ca1d7991357ae7a7555589af88930d82cf07c0a",
    remote = "https://github.com/bazelbuild/buildifier.git",
)
