# Charts Repo Actions Demo

![](https://i.imgur.com/waxVImv.png)
### [View all Roadmaps](https://github.com/nholuongut/all-roadmaps) &nbsp;&middot;&nbsp; [Best Practices](https://github.com/nholuongut/all-roadmaps/blob/main/public/best-practices/) &nbsp;&middot;&nbsp; [Questions](https://www.linkedin.com/in/nholuong/)
<br/>

Example project to demo testing and hosting a chart repository with GitHub Pages and Actions.

## Actions

* [@helm/kind-action](https://github.com/nholuongut/kind-action)
* [@helm/chart-testing-action](https://github.com/nholuongut/chart-testing-action)
* [@helm/chart-releaser-action](https://github.com/nholuongut/chart-releaser-action)

## Project Status

`main` supports Helm 3 only, i. e. both `v1` and `v2` [API version](https://helm.sh/docs/topics/charts/#the-apiversion-field) charts are installable.

## Chart Sources

* `charts/example-v1`: Sample chart with API version v1
* `charts/example-v2`: Sample chart with API version v2
* `charts/dependencies-v1`: Simple chart with API version v1 to test dependencies from an external Charts repo
* `charts/dependencies-v2`: Simple chart with API version v2 to test dependencies from an external Charts repo

## How-To

You can automatically test and host your own chart repository with GitHub Pages and Actions by following these steps.

### Steps

The prerequisites listed in the READMEs for [actions](#actions) above _must_ be complete before the steps below, or your charts' initial versions won't be released.

1. Use the `main` branch for all of the below, if you wish to use the Actions workflow files as-is
1. Copy the `.github/workflows` files from this project to yours
1. Add your charts to a parent directory in the project (`/charts` is most straightforward, as it's the default. To change this see [helm/chart-testing > configuration > chart-dirs](https://github.com/nholuongut/chart-testing#configuration))
1. Optional: To list your charts repo publicly on the [Helm Hub](https://hub.helm.sh), see [Helm Hub > How To Add Your Helm Charts](https://github.com/helm/hub#how-to-add-your-helm-charts). Consider also pushing to [CNCF Artifact Hub](https://artifacthub.io/)

### Results

* The [Lint and Test Charts](/.github/workflows/lint-test.yaml) workflow uses [@helm/kind-action](https://www.github.com/helm/kind-action) GitHub Action to spin up a [kind](https://kind.sigs.k8s.io/) Kubernetes cluster, and [@helm/chart-testing-action](https://www.github.com/helm/chart-testing-action) to lint and test your charts on every Pull Request and push
* The [Release Charts](/.github/workflows/release.yaml) workflow uses [@helm/chart-releaser-action](https://www.github.com/helm/chart-releaser-action) to turn your GitHub project into a self-hosted Helm chart repo. It does this – during every push to `main` – by checking each chart in your project, and whenever there's a new chart version, creates a corresponding [GitHub release](https://help.github.com/en/github/administering-a-repository/about-releases) named for the chart version, adds Helm chart artifacts to the release, and creates or updates an `index.yaml` file with metadata about those releases, which is then hosted on GitHub Pages
* You should now be able to add your charts repo with `helm repo add <owner> https://<owner>.github.io/<project>`

# 🚀 I'm are always open to your feedback.  Please contact as bellow information:
### [Contact ]
* [Name: Nho Luong]
* [Skype](luongutnho_skype)
* [Github](https://github.com/nholuongut/)
* [Linkedin](https://www.linkedin.com/in/nholuong/)
* [Email Address](luongutnho@hotmail.com)
* [PayPal.me](https://www.paypal.com/paypalme/nholuongut)

![](https://i.imgur.com/waxVImv.png)
![](Donate.png)
[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/nholuong)

# License
* Nho Luong (c). All Rights Reserved.🌟
