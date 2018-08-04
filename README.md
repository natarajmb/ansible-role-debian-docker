Ansible Role: debian-docker
===========================

Installs docker-ce and allows to re-configures docker home. As most development machines tends to have more space on /home with assumption it was partitioned rather than using one big root.

This would also come in handy when you want to back up docker home or mount a seperate drive for docker.

Requirements
------------

Debian 9.x install with Ansible 2.x.

Role Variables
--------------

Listed below are the variables you can set to customise the role, with their default values.

  change_docker_home: true

Indicates if we have to overirde the default docker home from /var/lib/docker

  new_docker_home: /home/docker

If you have chosen to override the docker home above varible allows you tot set the path for new home

Dependencies
------------

None.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: docker-server
      vars_file:
        - vars/main.yml
      roles:
        - { role: natarajmb.debian-docker }

License
-------

MIT / BSD

Author Information
------------------

Nataraj Basappa created this role in 2018 while replatforming Cognitivenode services from hardware install to containerization.
