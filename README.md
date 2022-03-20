# yq

Source : https://dev.to/vikcodes/yq-a-command-line-tool-that-will-help-you-handle-your-yaml-resources-better-8j9
Packages: https://github.com/mikefarah/yq/releases/tag/v4.23.1


What is yq?
yq is a command-line tool designed to transform YAML. It is similar to jq which focuses on transforming JSON instead of YAML.

What can it do?
yq can take a YAML file as an input and:

Read values from the file.
Add new values.
Update Existing values.
Generate new YAML files.
Convert YAML into JSON.
Merge two or more YAML files.

Use Cases: 
```
apiVersion: v1
kind: Pod
metadata:
  name: test-pod
spec:
  containers:
  - name: test-container
    image: k8s.gcr.io/busybox
    env:
    - name: DB_URL
      value: postgres://db_url:5432
```
```
$ yq r pod.yaml "spec.containers[0].env[0].value"
postgres://db_url:5432
```
