Ansible Role: Ruby
=========

Installs the Ruby programming language

WIP Notice
----------

This role is a Work-In-Progress. It is limited in the following ways:

* Only tested within very few OSes/versions

Requirements
------------

None

Role Variables
--------------

    ruby_from_source:         false
    ruby_version:             2.3
    ruby_version_full:        2.3.3
    ruby_download_dir:        "{{ ansible_env.HOME}}"
    ruby_dir:                 "ruby-{{ ruby_version_full }}"
    ruby_download_file:       "{{ ruby_dir }}.tar.gz"
    ruby_url:                 "https://cache.ruby-lang.org/pub/ruby/{{ ruby_version }}/{{ ruby_download_file }}"
    ruby_checksum:            "241408c8c555b258846368830a06146e4849a1d58dcaf6b14a3b6a73058115b7"
    ruby_checksum_algorithm:  sha256
    ruby_install_dir:         "/usr/local"
    ruby_configure_options:   "--enable-shared
                               --disable-install-doc
                               --prefix={{ ruby_install_dir }}"

Dependencies
------------

None

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: app_servers
      roles:
         - { role: ruby }

License
-------

CC0

Author Information
------------------

Drew Heles
