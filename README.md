# docker build -t centos-systemd-sshd .
docker build -t centos-systemd-sshd .
# docker run instance
docker run --privileged --name centos-systemd-sshd -v /sys/fs/cgroup:/sys/fs/cgroup:ro -p 2222:22 -d centos-systemd-sshd
