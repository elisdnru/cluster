# Provisioning

Ansible playbooks for Docker Swarm cluster setup.

# Set Up

Install Ansible. Create inventory file with SSH credentials of your virtual machines by example:

```
cp hosts.yml.dist hosts.yml
```

Set up cluster:

```
make cluster
```

Generate deployment SSH-key and register it for `deploy` user:

```
make generate-deploy-key
make authorize-deploy
```

If you use private Docker registry log in to the registry from manager virtual machine:

```
make docker-login
```
