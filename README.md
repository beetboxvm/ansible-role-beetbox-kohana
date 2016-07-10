# Ansible Role: Beetbox Kohana

[![CircleCI](https://circleci.com/gh/beetboxvm/ansible-role-beetbox-kohana.svg?style=svg)](https://circleci.com/gh/beetboxvm/ansible-role-beetbox-kohana)

An Ansible role that creates and configures a Kohana project on beetbox.

## Requirements

This role is specifically developed as an extension to beetbox -- https://github.com/drupalmel/beetbox

## Role Variables

Available variables are listed below, along with default values:

Checkout Kohana project.

    kohana_checkout: no

Kohana project git respository. 

    kohana_repo: "https://github.com/kohana/kohana.git"

Kohana project version. This can be the full 40-character SHA-1 hash, the literal string HEAD, a branch name, or a tag name.

    kohana_version: "HEAD"
    
Kohana checkout depth. git is history truncated to the specified number or revisions.
    
    kohana_checkout_depth: 1
    
Configure Kohana.
    
    kohana_configure: no
    
Kohana timezone.
    
    kohana_timezone: "America/Chicago"
    
Kohana base URL.
    
    kohnana_base_url: /
    
Kohana salt.
    
    kohana_salt: "{{ 'beetbox' | password_hash('sha512') }}"
    
Remove install script.
    
    kohana_remove_install: no


# beetbox

https://github.com/beetboxvm/beetbox

## Requirements

* [Vagrant](https://www.vagrantup.com/) >= 1.8
* [Virtualbox](https://www.virtualbox.org/)
* [Vagrant Hostsupdater](https://github.com/cogitatio/vagrant-hostsupdater)
* [Vagrant Auto-network](https://github.com/oscar-stack/vagrant-auto_network)

## Quickstart

  1. Open terminal (or [git bash](https://msysgit.github.io/) for windows users) and run the following commands --

  ```
  git clone https://github.com/beetboxvm/ansible-role-beetbox-kohana.git kohana && cd $_
  vagrant up
  ```

  2. Go to http://kohana.local/

  ```
  username: admin
  password: admin
  ```

## License

MIT
