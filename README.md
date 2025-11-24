# ollama
Images used: 
- ollama/ollama:0.12.6
- prom/node-exporter:v1.7.0
- ghcr.io/open-webui/open-webui:0.6.36

# Environment details
- Windows 10 as base OS with 24gb ram, intel i5-8350U CPU, NVme SSD
- Oracle virtualbox 7.1.6.x
- Ubuntu Linux 24.04.3 LTS x 3 vm's with 50gb storage, 6gb ram, 2 vcpu's for each vm 
- Kubernetes native/vanilla release 1.33, 1 master node, 1 worker node, 1 Ubuntu 24.03.4.x LTS vm acting as NFS server for storage 

# Kubernetes details
- k8s 1.33.5
- Calico networking
- rancher.io/local-path for storage class , nfs-csi & nfs-csi-openwebui for ollama storage

# Procedure to add models 
- Download and run k9s tool
- Get in to the shell of 1 of the ollama container
- Command to download and load model from terminal with example =  ollama pull ollama:3.2 / ollama pull <model-name>:<version>
- DeepSeek model can get downloaded but the openweb UI will throw expection while using the model due to non compatible resources i.e. nVDIA gpu requirement and other. Same for alpaca model.   It requires minimum 6gb ram to run. 

