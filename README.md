# cilium-workshop
## eBPF - The Future of Networking & Security
![k8s](https://cilium.io/static/5bbf931b72bfbe12c32b629d414ab777/a4d88/k8s_ship.png)

https://cilium.io/blog/2020/11/10/ebpf-future-of-networking/

### Cilium - eBPF-based Networking, Observability, and Security

![arch](https://cilium.io/static/6c69375bdc369895441cdc52ae9801dc/8b936/cilium_arch.png)

## Cilium 1.8: XDP Load Balancing, Cluster-wide Flow Visibility, Host Network Policy, Native GKE & Azure modes, Session Affinity, CRD-mode Scalability, Policy Audit mode, ...
https://cilium.io/blog/2020/06/22/cilium-18

![xdp](https://cilium.io/static/ceb5512de15120b9c2043f87a1e468ff/742d3/intro.png)

## Hubble Network, Service & Security Observability for Kubernetes
![hubble](https://github.com/cilium/hubble/raw/master/Documentation/images/hubble_arch.png)


## Kubernetes Without kube-proxy
https://docs.cilium.io/en/v1.10/gettingstarted/kubeproxy-free/

Cilium’s kube-proxy replacement depends on the Host-Reachable Services feature, therefore a v4.19.57, v5.1.16, v5.2.0 or more recent Linux kernel is required. Linux kernels v5.3 and v5.8 add additional features that Cilium can use to further optimize the kube-proxy replacement implementation.
```bash
kubectl delete ds kube-proxy -n kube-system
```

## Local Redirect Policy (beta)
https://docs.cilium.io/en/v1.10/gettingstarted/local-redirect-policy/

### Use Cases

Local Redirect Policy allows Cilium to support the following use cases:
### Node-local DNS cache
DNS node-cache listens on a static IP to intercept traffic from application pods to the cluster’s DNS service VIP by default, which will be bypassed when Cilium is handling service resolution at or before the veth interface of the application pod. To enable the DNS node-cache in a Cilium cluster, the following example steers traffic to a local DNS node-cache which runs as a normal pod.
## values.yaml
full: https://github.com/cilium/cilium/blob/v1.10.0/install/kubernetes/cilium/values.yaml

minimal: https://github.com/stasian/cilium-workshop/values.yml


## NetworkPolicy Editor: Create, Visualize, and Share Kubernetes NetworkPolicies
https://cilium.io/blog/2021/02/10/network-policy-editor

http://editor.cilium.io/

## Cilium Network Policies

### Policy Enforcement Modes
https://docs.cilium.io/en/v1.10/policy/intro/
## Cilium Star Wars Demo
https://github.com/cilium/star-wars-demo

## Useful CLI commands

```bash
kubectl exec -it cilium-pod -n kube-system -- bash
```

```bash
cilium status --verbose
cilium monitor --type policy-verdict
cilium identity list
cilium endpoint list
hubble observe -f
cilium-health status
```
# Bugs
https://github.com/cilium/cilium/pull/15148
