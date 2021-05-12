# tilt-mysql

A general MySQL instance to use locally with Kubernetes services that expect an external MySQL instance

# Requirements

- A Mac (Linux might work, not sure)
- make (I think comes with xcode, git, etc)
- docker-desktop - Enabled Kubernetes (and disable Fuse)
- kubectl - https://kubernetes.io/docs/tasks/tools/install-kubectl/
- kustomize - https://kubectl.docs.kubernetes.io/installation/kustomize/
- tilt - https://docs.tilt.dev/install.html

# Run

- `make up` - Starts MySQL by firing up tilt, hit space to see the GUI, maps mysql data dir to data/ here, ctrl-c to exit
- `make down` - Cleans everything up
- `make client` - Connects to mysql on server (password: local)

# Access

Make sure you `make up` before trying to access MySQL or starting any k8s service needs it.

From within kubernetes, host (DNS) is `db.mysql` at port `3306`.

From your Mac, host is `localhost` at port `3306`.
