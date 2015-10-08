# Sentry with Postgresql, using Ansible

Run it in Vagrant

    $ ansible-galaxy install -r requirements.yml
    $ vagrant up

# Deploy on your server

- Change [vars.yml](https://github.com/javaguirre/sentry-ansible-postgres-example/blob/master/vars.yml) to use your configuration.
- Change [your host](https://github.com/javaguirre/sentry-ansible-postgres-example/blob/master/host)

```
$ ansible-playbook -i host site.yml --ask-sudo-pass
```

You are done!
