## Run the environment
```shell
#If build fails because ansible, just run it again
docker-compose build
docker-compose up -d
```

Login on the control node and add the passwordless login to the managed node
```shell
sshpass -p "dockerpassword" ssh-copy-id ansibleadmin@10.0.5.3 -o StrictHostKeyChecking=no
```

## References:
- https://www.redhat.com/en/blog/system-administrators-guide-getting-started-ansible-fast
- https://docs.docker.com/engine/examples/running_ssh_service/
- https://docs.docker.com/compose/compose-file/
- https://hub.docker.com/r/jdeathe/centos-ssh