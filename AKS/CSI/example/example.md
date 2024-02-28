```

HRS+sda06@T2P-LAP037 MINGW64 ~
$ curl -skSL https://raw.githubusercontent.com/kubernetes-sigs/azuredisk-csi-driver/v1.9.0/deploy/uninstall-driver.sh | bash -s v1.9.0 --
Uninstalling Azure Disk CSI driver, version: v1.9.0 ...
customresourcedefinition.apiextensions.k8s.io "volumesnapshots.snapshot.storage.k8s.io" deleted
customresourcedefinition.apiextensions.k8s.io "volumesnapshotclasses.snapshot.storage.k8s.io" deleted
customresourcedefinition.apiextensions.k8s.io "volumesnapshotcontents.snapshot.storage.k8s.io" deleted
daemonset.apps "csi-azuredisk-node" deleted
daemonset.apps "csi-azuredisk-node-win" deleted
csidriver.storage.k8s.io "disk.csi.azure.com" deleted
serviceaccount "csi-azuredisk-node-sa" deleted
clusterrole.rbac.authorization.k8s.io "csi-azuredisk-node-secret-role" deleted
Uninstalled Azure Disk CSI driver successfully.

HRS+sda06@T2P-LAP037 MINGW64 ~
$ curl -skSL https://raw.githubusercontent.com/kubernetes-sigs/azuredisk-csi-driver/v1.9.0/deploy/install-driver.sh | bash -s v1.9.0 --
Installing Azure Disk CSI driver, version: v1.9.0 ...
csidriver.storage.k8s.io/disk.csi.azure.com created
serviceaccount/csi-azuredisk-controller-sa created
clusterrole.rbac.authorization.k8s.io/azuredisk-external-provisioner-role created
clusterrolebinding.rbac.authorization.k8s.io/azuredisk-csi-provisioner-binding created
clusterrole.rbac.authorization.k8s.io/azuredisk-external-attacher-role created
clusterrolebinding.rbac.authorization.k8s.io/azuredisk-csi-attacher-binding created
clusterrole.rbac.authorization.k8s.io/azuredisk-external-snapshotter-role created
clusterrolebinding.rbac.authorization.k8s.io/azuredisk-csi-snapshotter-binding created
clusterrole.rbac.authorization.k8s.io/azuredisk-external-resizer-role created
clusterrolebinding.rbac.authorization.k8s.io/azuredisk-csi-resizer-role created
clusterrole.rbac.authorization.k8s.io/csi-azuredisk-controller-secret-role created
clusterrolebinding.rbac.authorization.k8s.io/csi-azuredisk-controller-secret-binding created
serviceaccount/csi-azuredisk-node-sa created
clusterrole.rbac.authorization.k8s.io/csi-azuredisk-node-secret-role created
clusterrolebinding.rbac.authorization.k8s.io/csi-azuredisk-node-secret-binding created
deployment.apps/csi-azuredisk-controller created
daemonset.apps/csi-azuredisk-node configured
daemonset.apps/csi-azuredisk-node-win configured
deployment.apps/csi-azuredisk-controller configured
Azure Disk CSI driver installed successfully.

--------------------




# Upgrade CSI
# Uninstall first, then install new version
# Install CSI driver development version on a Kubernetes cluster 1.30
https://github.com/kubernetes-sigs/azuredisk-csi-driver/blob/master/docs/install-csi-driver-v1.30.0.md

curl -skSL https://raw.githubusercontent.com/kubernetes-sigs/azuredisk-csi-driver/v1.30.0/deploy/install-driver.sh | bash -s v1.30.0 snapshot --


HRS+sda06@T2P-LAP037 MINGW64 ~
$ curl -skSL https://raw.githubusercontent.com/kubernetes-sigs/azuredisk-csi-driver/v1.30.0/deploy/install-driver.sh | bash -s v1.30.0 snapshot --
Installing Azure Disk CSI driver, version: v1.30.0 ...
csidriver.storage.k8s.io/disk.csi.azure.com created
serviceaccount/csi-azuredisk-controller-sa created
clusterrole.rbac.authorization.k8s.io/azuredisk-external-provisioner-role created
clusterrolebinding.rbac.authorization.k8s.io/azuredisk-csi-provisioner-binding created
clusterrole.rbac.authorization.k8s.io/azuredisk-external-attacher-role created
clusterrolebinding.rbac.authorization.k8s.io/azuredisk-csi-attacher-binding created
clusterrole.rbac.authorization.k8s.io/azuredisk-external-snapshotter-role created
clusterrolebinding.rbac.authorization.k8s.io/azuredisk-csi-snapshotter-binding created
clusterrole.rbac.authorization.k8s.io/azuredisk-external-resizer-role created
clusterrolebinding.rbac.authorization.k8s.io/azuredisk-csi-resizer-role created
clusterrole.rbac.authorization.k8s.io/csi-azuredisk-controller-secret-role created
clusterrolebinding.rbac.authorization.k8s.io/csi-azuredisk-controller-secret-binding created
serviceaccount/csi-azuredisk-node-sa created
clusterrole.rbac.authorization.k8s.io/csi-azuredisk-node-role created
clusterrolebinding.rbac.authorization.k8s.io/csi-azuredisk-node-secret-binding created
daemonset.apps/csi-azuredisk-node created
daemonset.apps/csi-azuredisk-node-win created
deployment.apps/csi-azuredisk-controller created
install snapshot driver ...
customresourcedefinition.apiextensions.k8s.io/volumesnapshotclasses.snapshot.storage.k8s.io configured
customresourcedefinition.apiextensions.k8s.io/volumesnapshotcontents.snapshot.storage.k8s.io configured
Error from server (AlreadyExists): error when creating "https://raw.githubusercontent.com/kubernetes-sigs/azuredisk-csi-driver/v1.30.0/deploy/v1.30.0/crd-csi-snapshot.yaml": customresourcedefinitions.apiextensions.k8s.io "volumesnapshots.snapshot.storage.k8s.io" already exists

HRS+sda06@T2P-LAP037 MINGW64 ~
$ curl -skSL https://raw.githubusercontent.com/kubernetes-sigs/azuredisk-csi-driver/v1.30.0/deploy/uninstall-driver.sh | bash -s v1.30.0 --
Uninstalling Azure Disk CSI driver, version: v1.30.0 ...
deployment.apps "csi-azuredisk-controller" deleted
daemonset.apps "csi-azuredisk-node" deleted
daemonset.apps "csi-azuredisk-node-win" deleted
csidriver.storage.k8s.io "disk.csi.azure.com" deleted
customresourcedefinition.apiextensions.k8s.io "volumesnapshots.snapshot.storage.k8s.io" deleted
customresourcedefinition.apiextensions.k8s.io "volumesnapshotclasses.snapshot.storage.k8s.io" deleted
customresourcedefinition.apiextensions.k8s.io "volumesnapshotcontents.snapshot.storage.k8s.io" deleted
serviceaccount "csi-azuredisk-controller-sa" deleted
clusterrole.rbac.authorization.k8s.io "azuredisk-external-provisioner-role" deleted
clusterrolebinding.rbac.authorization.k8s.io "azuredisk-csi-provisioner-binding" deleted
clusterrole.rbac.authorization.k8s.io "azuredisk-external-attacher-role" deleted
clusterrolebinding.rbac.authorization.k8s.io "azuredisk-csi-attacher-binding" deleted
clusterrole.rbac.authorization.k8s.io "azuredisk-external-snapshotter-role" deleted
clusterrolebinding.rbac.authorization.k8s.io "azuredisk-csi-snapshotter-binding" deleted
clusterrole.rbac.authorization.k8s.io "azuredisk-external-resizer-role" deleted
clusterrolebinding.rbac.authorization.k8s.io "azuredisk-csi-resizer-role" deleted
clusterrole.rbac.authorization.k8s.io "csi-azuredisk-controller-secret-role" deleted
clusterrolebinding.rbac.authorization.k8s.io "csi-azuredisk-controller-secret-binding" deleted
serviceaccount "csi-azuredisk-node-sa" deleted
clusterrole.rbac.authorization.k8s.io "csi-azuredisk-node-role" deleted
clusterrolebinding.rbac.authorization.k8s.io "csi-azuredisk-node-secret-binding" deleted
Uninstalled Azure Disk CSI driver successfully.



```
