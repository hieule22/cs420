cc_test(
  name = "buffer_test",
  srcs = ["buffer_test.cc"],
  size = "small",
  deps = [
       "//src:buffer",
       "//third_party/gtest:gtest_main",
  ],
)

cc_test(
  name = "scanner_test",
  srcs = ["scanner_test.cc"],
  size = "small",
  deps = [
       "//src:scanner",
       "//src:buffer",
       "//third_party/gtest:gtest_main",
       "//util:ptr_util",
  ],
)

filegroup(
  name = "exported_testdata",
  srcs = glob([
       "data/*.in",
       "data/*.out",
  ]),
)

cc_test(
  name = "scanner_all_test",
  srcs = ["scanner_all_test.cc"],
  size = "small",
  deps = [
       "//src:scanner",
       "//third_party/gtest:gtest_main",
  ],
  data = [
       ":exported_testdata",
  ],
)