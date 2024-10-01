load("@rules_python//python:defs.bzl", "py_binary", "py_test")
load("@rules_python//python:pip.bzl", "compile_pip_requirements")
load("@rules_python//python:packaging.bzl", "py_wheel", 'py_package')



compile_pip_requirements(
    name = "requirements",
    src = "requirements.in",
    requirements_txt = "requirements_lock.txt",
)

py_wheel(
    name = "array_record_wheel",
    distribution = "array_record",
    version = "0.6.0",
    deps = [
        "//array_record/python:array_record_data_source",
        "//array_record/python:array_record_module",
        "//array_record/python:init",
        "//array_record/beam:beam",
        "//array_record:package_info",
    ],
)
