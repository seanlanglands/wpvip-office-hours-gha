# WordPress VIP — GitHub Actions Office Hours

Welcome to the repo that showcases examples and resources that were covered during our October 2025 Office Hours presentation about leveraging GitHub Actions.

## VIP Documentation

* [Build and deploying on VIP guide](https://docs.wpvip.com/code-deployment/default-deployment/build-and-deploy/)
* [Deploying built files from .gitignore and .deployignore](https://docs.wpvip.com/code-deployment/default-deployment/build-and-deploy/ci-cd/#h-deploying-built-files-from-gitignore)
* [VIP-CLI and CI Automation](https://docs.wpvip.com/vip-cli/advanced-usage/#h-automation)
* [Custom Deployment with continuous deployment](https://docs.wpvip.com/code-deployment/custom-deployment/continuous-deployment/)
* [Updating an environment’s deploying branch](https://docs.wpvip.com/code-deployment/default-deployment/deploying-branches/update/)

## Resources

* [Simplified GitHub Actions workflow example](https://github.com/Automattic/vip-go-build/blob/master/.github/workflows/ci-sample.yml)
* [Reusable boilerplate deploy.sh script](https://raw.githubusercontent.com/Automattic/vip-go-build/master/deploy.sh)
* [Migrating from CircleCI to GitHub Actions](https://docs.github.com/en/actions/tutorials/migrate-to-github-actions/manual-migrations/migrate-from-circleci)
* [Migrating from Travis CI to GitHub Actions](https://docs.github.com/en/actions/tutorials/migrate-to-github-actions/manual-migrations/migrate-from-travis-ci)
* [ektos/act: Run your GitHub Actions locally](https://github.com/nektos/act)
* [Parsely/wp-parsely: Matrix strategy example](https://github.com/Parsely/wp-parsely/blob/develop/.github/workflows/integration-tests.yml)


## Directories and Files

The following directories/files are relevant to the GitHub Actions demo. All other files you see in this repo are based on our [vip-go-skeleton](https://github.com/Automattic/vip-go-skeleton) starting point project for your VIP application.

* `.github/workflows/ci-build-and-deploy.yml`: Basic example of a single workflow job that triggers on a commit push to a branch and builds static assets for a theme.
* `.github/workflows/ci-monorepo-build-and-deploy.yml`: Workflow that demonstrates multiple sequential jobs, dependency caching, and artifacts.
* `client-mu-plugins/custom-blocks-plugin` and `themes/child-theme`: Basic example of a custom plugin and theme that both require production-ready assets to be built during a CI/CD pipeline.
* `composer.json`: Configured to pull in a WordPress plugin from Packagist, which is used in our pipeline.
* `.deployignore`: Demonstrates excluding `src` directories from being deployed.
* `.gitignore`: Demonstrates excluding `build` and composer installed plugins directories from being deployed.
