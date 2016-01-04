# Ansible Role: Beetbox Kohana

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

## Dependencies

- Beetbox -- https://github.com/drupalmel/beetbox

## License

MIT