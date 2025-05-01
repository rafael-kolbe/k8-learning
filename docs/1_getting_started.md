The main difference of containers and virtual machines is that with containers, they share the same operating system between all of them, but a virtual machine has to run independent operating systems for each application.

Images are template packages used to create containers with its own set of configurations.
When creating a container, just specify the image. This can be done in a `yaml` file.
Also, images are made and configured in a `Dockerfile` file.

Kubernetes is an orchestration technology that manages multiple containers.
