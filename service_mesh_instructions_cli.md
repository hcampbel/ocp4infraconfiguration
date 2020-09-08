# Install Maistra Istio Operator (Red Hat OpenShift Service Mesh) via CLI

## Installing the Jaegar Operator

```bash
oc new-project observability # create the project for the jaeger operator
oc create -n observability -f https://raw.githubusercontent.com/hcampbel/ocp4infraconfiguration/master/maistra-deployment/jaegar-operator/jaegartracing_v1_jaegar_crd.yaml
oc create -n observability -f https://raw.githubusercontent.com/hcampbel/ocp4infraconfiguration/master/maistra-deployment/jaegar-operator/service_account.yaml
oc create -n observability -f https://raw.githubusercontent.com/hcampbel/ocp4infraconfiguration/master/maistra-deployment/jaegar-operator/role.yaml
oc create -n observability -f https://raw.githubusercontent.com/hcampbel/ocp4infraconfiguration/master/maistra-deployment/jaegar-operator/role_binding.yaml
oc create -n observability -f https://raw.githubusercontent.com/hcampbel/ocp4infraconfiguration/master/maistra-deployment/jaegar-operator/operator.yaml
```

## Installing the Kiali Operator

```bash
bash <(curl -L https://git.io/getLatestKialiOperator) --operator-image-version v1.0.0 --operator-watch-namespace '**' --accessible-namespaces '**' --operator-install-kiali false
```

Additional details related to the Kiali Operator can be found [here](https://www.kiali.io/documentation/getting-started).

## Installing the Istio Operator

```bash
$ oc apply -n istio-operator -f https://raw.githubusercontent.com/maistra/istio-operator/maistra-1.1.7/deploy/servicemesh-operator.yaml
```

By default, the operator watches for `ServiceMeshControlPlane` in all namespaces. Typically, a cluster-wide control plane is installed in `istio-system`. For example:

```bash
oc apply -n istio-system -f https://raw.githubusercontent.com/maistra/istio-operator/maistra-1.1.7/deploy/examples/maistra_v1_servicemeshcontrolplane_cr_full.yaml
```



