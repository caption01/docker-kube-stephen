Definition of K8S config

Key -> apiVersion

- define set of object configuration

Key -> kind

- Pod: setting runing container

  - run one or more related contianer

- Service: setting networking kube cluster

  - ClusterIP: Expose a set of pods to other object in cluster

  - NodePort: expose container to outsid word
    (only on dev purpose)

  - LoadBalancer: handle traffic into a cluster

  - Ingress: expose a set of container to the outside word

- Deployment: Maintains a set of "Pod"

- PersistentVolumeClaim: kubernites storage

  - type static: ready serve resoure storage

  - type dynamic: reserve resoure storage when have require

- Secrets: Secret env inject into cluster by imparelative command

  - kubectl create secret generic <secret_name> --from-literal [key]=[value]

Key -> metadata: matching traffic

- lables: matching traffic

  - components: specific lable/selector matching system.

Key -> spec

- ports: setting traffic of pod.

  - port: Set port for other point to their self
    (open contact channel)

  - targetPort: Set target port to direct to
    (point target pod)

  - nodePort: to open external(broweser) connection.

- selector: matching traffic

  - work with Pod-labels to select matched pod and send traffic to.
