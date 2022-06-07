# Prerequisites

## Microsoft Azure

This tutorial leverages [Microsoft Azure](https://azure.microsoft.com/en-us/) to streamline provisioning of the compute infrastructure required to bootstrap a Kubernetes cluster from the ground up. [Sign up](https://azure.microsoft.com/en-us/free/) for $200 in free credits.

> The compute resources required for this tutorial exceed the Azure free tier.

## nix* Environment

If you're running this tutorial from a Linux or macOS machine, you're all set. If you're running on Windows, you'll need to use WSL. Instructions for setting that up can be found in the official docs [HERE](https://docs.microsoft.com/en-us/windows/wsl/install).

## Azure CLI

### Install the Azure CLI

Follow the Azure CLI [documentation](https://docs.microsoft.com/en-us/cli/azure/install-azure-cli?view=azure-cli-latest) to install and configure the `az` command line utility.

### Set a Default Compute Region

This tutorial assumes a default compute region has been configured.

If you are using the `az` command-line tool for the first time, you'll need to `login`:

```
az login
```

Set a default compute region:

```
az configure --default region=eastus
```

## Running Commands in Parallel with tmux

[tmux](https://github.com/tmux/tmux/wiki) can be used to run commands on multiple compute instances at the same time. Labs in this tutorial may require running the same commands across multiple compute instances, in those cases consider using tmux and splitting a window into multiple panes with `synchronize-panes` enabled to speed up the provisioning process.

> The use of tmux is optional and not required to complete this tutorial.

![tmux screenshot](images/tmux-screenshot.png)

> Enable `synchronize-panes`: `ctrl+b` then `shift :`. Then type `set synchronize-panes on` at the prompt. To disable synchronization: `set synchronize-panes off`.

Next: [Installing the Client Tools](02-client-tools.md)
