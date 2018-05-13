git_repository(
    name = "io_bazel_rules_go",
    remote = "https://github.com/bazelbuild/rules_go.git",
    commit = "167cb55932c4a415edf839f750bdd7366f2f1613",
)

load("@io_bazel_rules_go//go:def.bzl", "go_rules_dependencies", "go_register_toolchains", "go_repository")

# Repos for grpc.
go_repository(
  name = "org_golang_google_grpc",
  importpath = "google.golang.org/grpc",
  commit = "41344da2231b913fa3d983840a57a6b1b7b631a1",
)

go_repository(
  name = "org_golang_x_net",
  importpath = "golang.org/x/net",
  commit = "2491c5de3490fced2f6cff376127c667efeed857",
)



go_rules_dependencies()
go_register_toolchains()

load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

http_archive(
    name = "io_bazel_rules_docker",
    sha256 = "6dede2c65ce86289969b907f343a1382d33c14fbce5e30dd17bb59bb55bb6593",
    strip_prefix = "rules_docker-0.4.0",
    urls = ["https://github.com/bazelbuild/rules_docker/archive/v0.4.0.tar.gz"],
)

load(
    "@io_bazel_rules_docker//go:image.bzl",
    _go_image_repos = "repositories",
)

_go_image_repos()
