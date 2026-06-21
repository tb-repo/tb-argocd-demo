# tb-argocd-demo
This repo is designed to understand a simple deployment using ArgoCD on K8S cluster

## Add The Manifest File

Create this path in the GitHub repository:

```text
manifests/app.yml
```

Commit the file to the repository's `main` branch.

The final GitHub repository should look like this:

```text
tb-argocd-demo
`-- manifests
    `-- app.yml
```

## Optional Local Git Flow

If students prefer using Git locally:

```bash
mkdir tb-argocd-demo
cd tb-argocd-demo
mkdir manifests
copy <path>\app.yml manifests\app.yml
git init
git add manifests/app.yml
git commit -m "Add Argo CD demo app"
git branch -M main
git remote add origin https://github.com/<GITHUB_USERNAME>/argocd-demo-app.git
git push -u origin main
```

Replace `<GITHUB_USERNAME>` with the student's GitHub username.

## What The YAML Creates

The sample `app.yml` file contains three Kubernetes objects:

| Object | Purpose |
| --- | --- |
| ConfigMap | Stores a simple `index.html` page |
| Deployment | Runs two nginx Pods |
| Service | Exposes the Pods inside the cluster |

## Important Detail

Argo CD needs a repository URL and a path.

For this lab:

```text
Repository URL:
  https://github.com/<GITHUB_USERNAME>/tb-argocd-demo.git

Path:
  manifests
```

The next sub-session uses these values in the Argo CD UI.

## Review Questions

1. Why are we committing YAML to GitHub instead of applying it with `kubectl`?
2. Why should the lab repository be public unless credentials are configured?
3. What path should Argo CD read from the repository?
4. Which Kubernetes objects are defined in the sample file?
