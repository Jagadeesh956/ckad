# CKAD Practice Tasks

## Task 1
Create a new Pod named `pod-alpha` in Namespace `team-alpha` using image `busybox:1.31.0`. The container should be named `busybox-alpha` and run the command `echo "Hello Alpha" && sleep 1d`.

## Task 2
Scale the Deployment `deploy-beta` in Namespace `team-beta` to 4 replicas.

## Task 3
Expose the Deployment `deploy-gamma` in Namespace `team-gamma` using a ClusterIP Service named `svc-gamma` on port 80, targeting container port 80.

## Task 4
Add a readiness probe to the Pod `pod-delta` in Namespace `team-delta`. The probe should execute `cat /tmp/ready` every 5 seconds, with an initial delay of 10 seconds.

## Task 5
Create a Job named `job-epsilon` in Namespace `team-epsilon` that runs image `busybox:1.31.0`, executes `echo "Job Done"` and completes 2 times in parallel.

## Task 6
Create a PersistentVolumeClaim named `pvc-zeta` in Namespace `team-zeta` requesting 1Gi storage with ReadWriteOnce access mode, no storage class.

## Task 7
Mount the PersistentVolumeClaim `pvc-zeta` at `/data` in the Pod `pod-zeta` in Namespace `team-zeta`.

## Task 8
Create a Secret named `secret-eta` in Namespace `team-eta` with data `key1=value1` and `key2=value2`. Mount it as environment variables in a new Pod named `pod-eta` using image `busybox:1.31.0`.

## Task 9
Create a ConfigMap named `config-theta` in Namespace `team-theta` with data `config.txt=Hello World`. Mount it at `/config` in a new Deployment named `deploy-theta` with 2 replicas of image `nginx:1.17.3-alpine`.

## Task 10
Add a sidecar container named `sidecar-iota` to the Deployment `deploy-iota` (create it if needed) in Namespace `team-iota`, using image `busybox:1.31.0`, which tails a log file to stdout.

## Task 11
Add an InitContainer named `init-kappa` to the Deployment `deploy-kappa` (create it) in Namespace `team-kappa`, using image `busybox:1.31.0`, which creates a file `/init/done`.

## Task 12
Change the Service `svc-lambda` in Namespace `team-lambda` to NodePort type on port 30001.

## Task 13
Create a NetworkPolicy named `np-mu` in Namespace `team-mu` that allows ingress from pods with label `app=frontend` to pods with label `app=backend` on port 8080.

## Task 14
Set resource requests and limits on the Deployment `deploy-nu` in Namespace `team-nu`: requests 100m CPU, 128Mi memory; limits 200m CPU, 256Mi memory.

## Task 15
Configure the Deployment `deploy-xi` in Namespace `team-xi` to use ServiceAccount `sa-xi`.

## Task 16
Add labels `env=prod` and `team=xi` to all Pods in Namespace `team-xi` with label `app=deploy-xi`.

## Task 17
Check the rollout history of Deployment `deploy-omicron` in Namespace `team-omicron` and rollback to revision 1 if needed.

## Task 18
Create a StorageClass named `sc-fast` in Namespace `team-pi` with provisioner `fast-provisioner` and reclaim policy Delete.

## Task 19
Create a Pod named `pod-rho` in Namespace `team-rho` with liveness probe checking HTTP on port 80, path `/health`, initial delay 30s, period 10s.

## Task 20
Troubleshoot why the Service `svc-sigma` in Namespace `team-sigma` is not reachable. Fix the selector mismatch and confirm with curl from a test pod.