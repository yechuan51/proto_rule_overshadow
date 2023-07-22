# proto_rule_overshadow

Instructions:
1. Run the app with "bazel run //:app", everything should be fine, and you will see google.auth module is imported.
2. Uncomment the BUILD file line that imports the dummy_pb2, run the app again, and you will encounter an error:

   /home/ubuntu/.cache/bazel/_bazel_ubuntu/7e6ecf527bf713b1567f15e2f26950b5/execroot/__main__/bazel-out/k8-fastbuild/bin/app.runfiles/com_github_protocolbuffers_protobuf/python/google/__init__.py
  /home/ubuntu/.cache/bazel/_bazel_ubuntu/7e6ecf527bf713b1567f15e2f26950b5/execroot/__main__/bazel-out/k8-fastbuild/bin/app.runfiles/com_github_protocolbuffers_protobuf/python/google/protobuf/__init__.py
  Traceback (most recent call last):
    File "/home/ubuntu/.cache/bazel/_bazel_ubuntu/7e6ecf527bf713b1567f15e2f26950b5/execroot/__main__/bazel-out/k8-fastbuild/bin/app.runfiles/__main__/app.py", line 5, in <module>
      import google.auth
  ModuleNotFoundError: No module named 'google.auth'
