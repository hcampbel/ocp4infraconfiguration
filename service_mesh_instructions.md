# Red Hat Service Mesh Installation Instructions

### Pre-requisites

1. Install the `ElasticSearch Operator` - already installed as a part of Cluster Logging Service
2. Install the `Jaeger Operator`
3. Install the `Kiali Operator`
4. Ensure the account used to install has `cluster-admin` role

#### Installing Jaegar
1. Log in to the OpenShift Container Platform web console.
1. Navigate to **Operators → OperatorHub.**
1. Type **Jaeger** into the filter box to locate the Jaeger Operator.
1. Click the **Jaeger Operator** provided by Red Hat to display information about the Operator.
1. Click **Install**
1. On the **Create Operator Subscription** page, select **All namespaces on the cluster (default)**. This installs the Operator in the default `openshift-operators` project and makes the Operator available to all projects in the cluster.
1. Select the **stable** Update Channel.
1. Select the **Automatic** Approval Strategy.
1. Click **Subscribe**
1. The **Installed Operators** page displays the Jaeger Operator’s installation progress.


#### Installing the Kiali Operator

1. Log in to the OpenShift Container Platform web console.
1. Navigate to **Operators → OperatorHub**.
1. Type **Kiali** into the filter box to find the Kiali Operator.
1. Click the **Kiali Operator** provided by Red Hat to display information about the Operator.
1. Click **Install**.
1. On the **Create Operator Subscription** page, select **All namespaces on the cluster (default)**. This installs the Operator in the default `openshift-operators` project and makes the Operator available to all projects in the cluster.
1. Select the **stable** Update Channel.
1. Select the **Automatic** Approval Strategy.
1. Click **Subscribe**.
1. The **Installed Operators** page displays the Kiali Operator’s installation progress.

#### Installing the Red Hat Service Mesh Operator
1. Log in to the OpenShift Container Platform web console.
1. Navigate to **Operators → OperatorHub**.
1. Type **Red Hat OpenShift Service Mesh** into the filter box to find the Red Hat OpenShift Service Mesh Operator.
1. Click the Red Hat OpenShift Service Mesh Operator to display information about the Operator.
1. On the **Create Operator Subscription** page, select **All namespaces on the cluster (default)**. This installs the Operator in the default `openshift-operators` project and makes the Operator available to all projects in the cluster.
1. Click **Install**.
1. Select the **stable** Update Channel.
1. Select the **Automatic** Approval Strategy.
1. Click **Subscribe**.
1. The **Installed Operators** page displays the Red Hat OpenShift Service Mesh Operator’s installation progress.

#### Deploying the Red Hat OpenShift Service Mesh control plane

1. Log in to the OpenShift Container Platform web console as a user with the cluster-admin role.
1. Create a project named `istio-system`.
1. Navigate to **Operators → Installed Operators**.
1. If necessary, select `istio-system` from the Project menu. You may have to wait a few moments for the Operators to be copied to the new project.
1. Click the Red Hat OpenShift Service Mesh Operator. Under Provided APIs, the Operator provides links to create two resource types: A `ServiceMeshControlPlane` resource and a `ServiceMeshMemberRoll` resource
1. Under Istio Service Mesh Control Plane click **Create ServiceMeshControlPlane**.
1. On the Create Service Mesh Control Plane page, modify the YAML for the default `ServiceMeshControlPlane` template as needed.
1. Click **Create** to create the control plane. The Operator creates Pods, services, and Service Mesh control plane components based on your configuration parameters.
1. Click the **Istio Service Mesh Control Plane** tab.
1. Click the name of the new control plane.
1. Click the **Resources** tab to see the Red Hat OpenShift Service Mesh control plane resources the Operator created and configured.

#### Creating the Red Hat OpenShift Service Mesh member roll

1. If you don’t already have projects for your mesh, or you are starting from scratch, create a project. It must be different from istio-system.
1. Log in to the OpenShift Container Platform web console.
Navigate to Operators → Installed Operators.
1. Click the Project menu and choose the project where your ServiceMeshControlPlane is deployed from the list, for example istio-system.
1. Click the Red Hat OpenShift Service Mesh Operator.
1. Click the All Instances tab.
1. Click Create New, and then select Create Istio Service Mesh Member Roll.
1. On the Create Service Mesh Member Roll page, modify the YAML to add your projects as members. You can add any number of projects, but a project can only belong to one ServiceMeshMemberRoll resource.
1. Click Create to save the Service Mesh Member Roll.