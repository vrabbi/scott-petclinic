load('.tanzu/tanzu_tilt_extensions.py', 'tanzu_k8s_yaml')


SOURCE_IMAGE = os.getenv("SOURCE_IMAGE", default='ghcr.io/vrabbi/scott-petclinic-source')
LOCAL_PATH = os.getenv("LOCAL_PATH", default='.')

custom_build('ghcr.io/vrabbi/scott-petclinic',
    "tanzu apps workload apply -f config/workload.yaml --live-update \
      --local-path " + LOCAL_PATH + " --source-image " + SOURCE_IMAGE + " --yes && \
    .tanzu/wait.sh scott-petclinic",
  ['pom.xml', './target/classes'],
  live_update = [
    sync('./target/classes', '/workspace/BOOT-INF/classes')
  ],
  skips_local_docker=True
)
allow_k8s_contexts('tkg-tap-beta-3-cls-admin@tkg-tap-beta-3-cls')
tanzu_k8s_yaml('scott-petclinic', 'ghcr.io/vrabbi/scott-petclinic', './config/workload.yaml')
