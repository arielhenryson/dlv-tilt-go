# -*- mode: Python -*-

docker_build('example-go-image', '.', dockerfile='deployments/Dockerfile')
k8s_yaml('deployments/kubernetes.yaml')
k8s_resource('example-go', port_forwards=8000)
k8s_resource('example-go', port_forwards=2345)
