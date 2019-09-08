# docker build -t centos-systemd-sshd .
docker build -t centos-systemd-sshd .
# docker run instance
docker run --privileged --name centos-systemd-sshd -v /sys/fs/cgroup:/sys/fs/cgroup:ro -p 2222:22 -d centos-systemd-sshd

docker run --privileged --name centos-systemd-sshd-dnsmasq -v /root/.pip:/root/.pip -v /root/python-utils:/root/python-utils -v /root/mydnsmasq_20190907:/root/mydnsmasq_20190907 -v /sys/fs/cgroup:/sys/fs/cgroup:ro -d centos-systemd-sshd
