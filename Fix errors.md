# Fix Errors

- Error cannot start VirtualBox Linux kernel module
```
Solution: Disable secure boot in BIOS
```

- Error starting host:  Error creating host: Error executing step: Creating VM.
: Unable to start the VM: /usr/bin/VBoxManage startvm minikube --type headless failed:
VBoxManage: error: VT-x is disabled in the BIOS for all CPU modes (VERR_VMX_MSR_ALL_VMX_DISABLED)
```
Solution: Enable Virtualization Techonology is enabled in BIOS.
```

- Error restarting cluster:  restarting kube-proxy: waiting for kube-proxy to be up for configmap update: timed out waiting for the condition
```
Solution: "minikube delete" and "minikube start" . [link](https://github.com/kubernetes/minikube/issues/2755#issuecomment-385624552 "Github")

```

- Error Auto Scaling - timed out waiting for the condition: kubectl run -i --tty load-generator --image=busybox /bin/sh

while true; do wget -q -O- http://wordpress.default.svc.cluster.local; done

1. `minikube` no longer has `metrics-server` enabled by default. To enable it:
```
minikube addons enable metrics-server
```
2. Wordpress redirects to canonical name by default. Unfortunately, it believes that you should be using port 31938 so it redirects to that. In the actual container, nothing is listening to that port You could disable redirection by adding `remove_action('template_redirect', 'redirect_canonical');` to `wp-config.php`. However, I think it's much easier to just generate the load on your machine (only tested on Linux, YMMV):
```
while true; do wget -q -O -S $(minikube service wordpress --url); done
```
