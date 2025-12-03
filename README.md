**CleanStart Container for Kube-Proxy**

Kube-proxy is a network proxy that runs on each node in a Kubernetes cluster, maintaining network rules on nodes and enabling network communication to Pods. It implements the Kubernetes Service concept by maintaining network rules and performing connection forwarding.

**Key Features**
* Kubernetes v1.34.0 network proxy
* Supports iptables, ipvs, and nftables proxy modes
* Health and metrics endpoints included
* Optimized for cloud-native environments

**Common Use Cases**
* Kubernetes cluster network proxy
* Service load balancing and routing
* Network rule management on cluster nodes

**Pull Commands**
Download the container image

```bash
docker pull cleanstart/kube-proxy:latest-dev
```

**Quick Test**
Verify the image works

```bash
docker run --rm cleanstart/kube-proxy:latest-dev --version
```

**Best Practices**
* Use specific image tags for production (avoid latest-dev)
* Configure required capabilities: NET_ADMIN and SYS_MODULE
* Run as DaemonSet in Kubernetes (one pod per node)
* Monitor health endpoint on port 10256

**
### 
### Resources

- Official Documentation: https://kubernetes.io/docs/reference/command-line-tools-reference/kube-proxy/
- View Provenance, Specifications, SBOM, Signature at: https://images.cleanstart.com/images/kube-proxy
- Docker Hub: https://hub.docker.com/r/cleanstart/kube-proxy
- CleanStart All Images: https://images.cleanstart.com
- CleanStart All Community Images: https://hub.docker.com/u/cleanstart

---

### Vulnerability Disclaimer

CleanStart offers Docker images that include third-party open-source libraries and packages maintained by independent contributors. While CleanStart maintains these images and applies industry-standard security practices, it cannot guarantee the security or integrity of upstream components beyond its control.

Users acknowledge and agree that open-source software may contain undiscovered vulnerabilities or introduce new risks through updates. CleanStart shall not be liable for security issues originating from third-party libraries, including but not limited to zero-day exploits, supply chain attacks, or contributor-introduced risks.

Security remains a shared responsibility: CleanStart provides updated images and guidance where possible, while users are responsible for evaluating deployments and implementing appropriate controls.
