kotti-ansible
=============

Simply ansible playbook to install kotti inside a virtualenv.

There are some variables at the top of install.yml. You should probably set base_dir at least.

  vars:
    # local
    base_dir: /Users/michaelc/python_dev
    site_virtualenv_name: kotti-27
    virtualenv: "{{ base_dir }}/{{ site_virtualenv_name }}"
    virtualenv_bin: /usr/local/bin/virtualenv
    # kotti
    requirements: https://raw.githubusercontent.com/disko/Kotti/feature/pcreate_scaffolds/requirements.txt
    kotti_repo: git+https://github.com/disko/Kotti.git@feature/pcreate_scaffolds#egg=kotti
    sample_config: https://raw.githubusercontent.com/disko/Kotti/feature/pcreate_scaffolds/app.ini
    # sample_config: https://raw.githubusercontent.com/disko/Kotti/feature/pcreate_scaffolds/development.ini


Currently, we assume you have a system python and already have installed virtualenv with something like pip.

We create a virtualenv inside base_dir, and install kotti inside that virtualenv.

Right now, this points to a development branch!
