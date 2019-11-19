## Deploy Hyper-converged GlusterFS/Heketi storage solution on K8s cluster
1. Clone this repo
```
	$ git clone https://github.com/cmotta2016/gluster-kubernetes.git
```
2. Edit topology.json file to match your cluster topology  
```
	$ cd gluster-kubernetes/deploy
	$ vim topology.json
```
3. Deploy stack  
```
	$ ./gk-deploy -g --admin-key <your_password> --user-key <your_password> -v
```
4. Adjust glusterfs-secret.yaml and glusterfs-storageclass.yaml and apply them  
```
	$ kubectl create -f glusterfs-secret.yaml
	$ kubectl create -f glusterfs-storageclass.yaml
```
