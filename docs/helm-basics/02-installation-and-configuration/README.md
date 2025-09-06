# Helm Installation & Basic Commands

## Installation Methods

### 1. Ubuntu (Snap)

```bash
# Install Helm using Snap
sudo snap install helm
sudo snap install helm --classic
```

* The `--classic` flag allows Helm to access host system files (e.g., kubeconfig), enabling it to connect with Kubernetes clusters.
* Verify installation:

```bash
helm version
```

### 2. Ubuntu/Debian (APT)

```bash
# Add Helm GPG key
curl https://baltocdn.com/helm/signing.asc | sudo apt-key add -

# Install transport support
sudo apt-get install apt-transport-https --yes

# Add Helm repository
echo "deb https://baltocdn.com/helm/stable/debian/ all main" \
  | sudo tee /etc/apt/sources.list.d/helm-stable-debian.list

# Update package list and install Helm
sudo apt-get update
sudo apt-get install helm
```

* Verify installation:

```bash
helm version
```

### 3. FreeBSD (pkg)

```bash
pkg install helm
helm version
```

📖 **Reference:** [Helm Official Installation Docs](https://helm.sh/docs/intro/install/)

---

## Common Helm Commands

### Release Management

```bash
helm install <release_name> <chart>       # Install a chart
helm upgrade <release_name> <chart>       # Upgrade an existing release
helm uninstall <release_name>             # Remove a release
helm list                                 # List installed releases
helm status <release_name>                # Show release status
helm history <release_name>               # Show release history
helm rollback <release_name> <revision>   # Rollback to a previous revision
```

### Repositories

```bash
helm repo add <repo_name> <repo_url>      # Add new repo
helm repo update                          # Update all repos
helm repo list                            # List configured repos
helm search repo <keyword>                # Search for charts in repos
```

### Chart Inspection & Validation

```bash
helm show values <chart>                  # Show default values of a chart
helm get values <release_name>            # Get values of a release
helm template <chart>                     # Render manifests without installing
helm dependency update <chart_directory>  # Update chart dependencies
helm lint <chart_directory>               # Lint chart for common issues
```

---

## Notes

* Replace placeholders (`<release_name>`, `<chart>`, `<repo_name>`, `<repo_url>`, `<keyword>`, `<chart_directory>`, `<revision>`) with actual values.
* Always verify installation with `helm version`.
