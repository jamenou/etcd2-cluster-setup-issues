# etcd2 cluster setup issues

This is a repository about how to setup cluster based on core-os.

1.static setup cluster

etcd2 --name Node1 --initial-advertise-peer-urls http://192.168.0.51:2380 --listen-peer-urls http://192.168.0.51:2380 --listen-client-urls http://192.168.0.51:2379,http://127.0.0.1:2379 --advertise-client-urls http://192.168.0.51:2379 --discovery https://discovery.etcd.io/643b1e1a5f983f95db46fdac4f34a9a2 

etcd2 --name Node2 --initial-advertise-peer-urls http://192.168.0.52:2380 --listen-peer-urls http://192.168.0.52:2380 --listen-client-urls http://192.168.0.52:2379,http://127.0.0.1:2379 --advertise-client-urls http://192.168.0.52:2379 --discovery https://discovery.etcd.io/643b1e1a5f983f95db46fdac4f34a9a2

etcd2 --name Node3 --initial-advertise-peer-urls http://192.168.0.53:2380 --listen-peer-urls http://192.168.0.53:2380 --listen-client-urls http://192.168.0.53:2379,http://127.0.0.1:2379 --advertise-client-urls http://192.168.0.53:2379 --discovery https://discovery.etcd.io/643b1e1a5f983f95db46fdac4f34a9a2

etcd2 --name Node4 --initial-advertise-peer-urls http://192.168.0.54:2380 --listen-peer-urls http://192.168.0.54:2380 --listen-client-urls http://192.168.0.54:2379,http://127.0.0.1:2379 --advertise-client-urls http://192.168.0.54:2379 --discovery https://discovery.etcd.io/643b1e1a5f983f95db46fdac4f34a9a2

etcd2 --name Node5 --initial-advertise-peer-urls http://192.168.0.55:2380 --listen-peer-urls http://192.168.0.55:2380 --listen-client-urls http://192.168.0.55:2379,http://127.0.0.1:2379 --advertise-client-urls http://192.168.0.55:2379 --discovery https://discovery.etcd.io/643b1e1a5f983f95db46fdac4f34a9a2

2.bootstrap cluster
still have some problems and try to figure out.

3.cluster checking command

  etcdctl cluster-health
  etcdctl member list
  systemctl status etcd2
  journalctl -f -u etcd2
  fleetctl status
