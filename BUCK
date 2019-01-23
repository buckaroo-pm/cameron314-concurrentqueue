load('//:buckaroo_macros.bzl', 'buckaroo_deps_from_package')

pthread = buckaroo_deps_from_package('github.com/buckaroo-pm/host-pthread')

prebuilt_cxx_library(
  name = 'concurrentqueue',
  header_only = True,
  header_namespace = '',
  exported_headers = glob([
    '*.h',
  ]),
  platform_deps = [
    ('linux.*', pthread),
  ],
  visibility = [
    'PUBLIC',
  ],
)
