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