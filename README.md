# [kubeman] kubectl-version_manager
A kubectl plugin for automate synchronize version between kubectl and kubernetes server version

## Installation
#### Prerequisites
* You **MUST** install `kubectl krew` from [here](https://krew.sigs.k8s.io/docs/user-guide/setup/install/).
* Then installing `kubectl-version_manager` plugin.

    ```shell
    # Get from source
    $ git clone https://github.com/ardikabs/kubectl-version_manager.git
    $ cd kubectl-version_manager
    $ chmod +x kubectl-version_manager
    $ sudo cp -p kubectl-version_manager $HOME/.krew/bin
    ```

## Usage
>
#### Run `kubectl version-manager activate`
This command would activate kubectl version-manager as named with `kubeman`.<b>
```bash
$ kubectl version-manager activate
:: Kubeman is activated ::

WARNING: To be able to run kubeman CLI, you need to add
the following to your /home/alpha/.zshrc:

Add the kubeman CLI to your path with:

    export PATH="$PATH:$HOME/.local/bin"

and restart your shell.

$ export PATH="$PATH:$HOME/.local/bin"
$ kubeman version --short
Client Version: v1.14.10
Server Version: v1.14.10-gke.17
$ kubeman --help
kubectl controls the Kubernetes cluster manager.

 Find more information at: https://kubernetes.io/docs/reference/kubectl/overview/

Basic Commands (Beginner):
  create         Create a resource from a file or from stdin.
  expose         Take a replication controller, service, deployment or pod and expose it as a new Kubernetes Service
  run            Run a particular image on the cluster
  set            Set specific features on objects

...
```
Basically `kubeman` is a thin wrapper of kubectl to match version between kubectl and kubernetes server version based on context given.

#### Run `kubectl version-manager list`
This command would show you the list of available kubectl binary version
```bash
$ kubectl version-manager list
VERSION
v1.10.13
v1.14.10
v1.16.6
v1.17.0
...
```

## TODO
* Unit test (?)