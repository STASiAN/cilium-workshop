# cilium-workshop
![Image of EBPF](https://cilium.io/static/5bbf931b72bfbe12c32b629d414ab777/a4d88/k8s_ship.png)
https://cilium.io/blog/2020/11/10/ebpf-future-of-networking/

### Cilium - eBPF-based Networking, Observability, and Security

![Image](https://cilium.io/static/6c69375bdc369895441cdc52ae9801dc/8b936/cilium_arch.png)

https://cilium.io/blog/2020/06/22/cilium-18

![Image ](https://cilium.io/static/ceb5512de15120b9c2043f87a1e468ff/742d3/intro.png)

## kube-proxy remove
https://docs.cilium.io/en/v1.10/gettingstarted/kubeproxy-free/

Cilium’s kube-proxy replacement depends on the Host-Reachable Services feature, therefore a v4.19.57, v5.1.16, v5.2.0 or more recent Linux kernel is required. Linux kernels v5.3 and v5.8 add additional features that Cilium can use to further optimize the kube-proxy replacement implementation.
```bash
kubectl delete ds kube-proxy -n kube-system
```
