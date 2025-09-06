# Helm Commands Cheat Sheet

| Command                                    | Purpose                                                 |
| ------------------------------------------ | ------------------------------------------------------- |
| `helm install <release_name> <chart>`      | Install a Helm chart with a given release name          |
| `helm list`                                | List all installed releases                             |
| `helm upgrade <release_name> <chart>`      | Upgrade an existing release to a new chart version      |
| `helm uninstall <release_name>`            | Uninstall a release                                     |
| `helm status <release_name>`               | Show the current status of a release                    |
| `helm history <release_name>`              | Display revision history of a release                   |
| `helm rollback <release_name> <revision>`  | Rollback a release to a previous revision               |
| `helm repo add <repo_name> <repo_url>`     | Add a new Helm chart repository                         |
| `helm repo update`                         | Update chart list from all configured repositories      |
| `helm repo list`                           | List all configured repositories                        |
| `helm search repo <keyword>`               | Search for charts in configured repositories            |
| `helm show values <chart>`                 | Show default values of a chart                          |
| `helm get values <release_name>`           | Get values of a deployed release                        |
| `helm template <chart>`                    | Render chart as Kubernetes manifests without installing |
| `helm dependency update <chart_directory>` | Update chart dependencies                               |
| `helm lint <chart_directory>`              | Check a chart for syntax and common issues              |

---
