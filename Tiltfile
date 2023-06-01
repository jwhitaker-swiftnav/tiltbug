docker_build(
  'myapp',
  '.',
  dockerfile='apps/myapp/build/Dockerfile'
)

k8s_resource(
  'myapp',
  labels='myapp',
  objects=[
    'myapp:namespace',
  ]
)

k8s_yaml(
  kustomize('./apps/myapp/k8s')
)
