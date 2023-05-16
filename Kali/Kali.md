# Kali

Copied from: [CISAgov](https://github.com/cisagov/docker-kali-ansible)

## Build

`docker build --tag cisagov/docker-kali-ansible .`

## Use

1. Install Docker.
2. Pull this image from Docker Hub: `docker pull cisagov/docker-kali-ansible:latest` (or use the image you built earlier).
3. Run a container from the image: `docker run --detach --privileged --cgroupns=host --volume=/sys/fs/cgroup:/sys/fs/cgroup:rw cisagov/docker-kali-ansible:latest`
4. Use Ansible inside the container:
    - `docker exec --tty [container_id] env TERM=xterm ansible --version`
    - `docker exec --tty [container_id] env TERM=xterm ansible-playbook /path/to/ansible/playbook.yml --syntax-check`
