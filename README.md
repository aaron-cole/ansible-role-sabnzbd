# ansible-role-sabnzbd
 
=========

Ansible Role to install sabnzbd, a free and easy binary newsreader.

Requirements
------------

Minimum Ansible version required is Ansible 2.9

Role Variables
--------------
Role variables have good defined defaults, which are located in `defaults/main.yml`.
Current version includes the following variables with default values:

### Defaults
| Name               | Default Value | Description                  |
|--------------------|---------------|------------------------------|
| `sabnzbd_user`       | sabnzbd | The primary user to run sabnzbd     |
| `sabnzbd_uid`        | *optional* | Commented out by default |
| `sabnzbd_group`      | media | The primary group for `sabnzbd_user` |
| `sabnzbd_group_gid`  | *optional* | Commented out by default |
| `sabnzbd_install_dir` | /opt/sabnzbd | Install directory for sabnzbd |
| `sabnzbd_config_dir` |  /opt/data/sabnzbd | Data directory to store configuration |
| `sabnzbd_git_url` | https://sabnzbd.servarr.com/v1/update/master/updatefile?os=linux&runtime=netcore&arch=x64| Link to the sabnzbd git hub latest release |
| `sabnzbd_port` | 8080 | Port in which sabnzbd operates on, to add to Firewalld |
| `sabnzbd_python_version` | python38 | Python Version to install and configure for Sabnzbd |
| `sabnzbd_packages` |   `see defaults/main.yml for complete list` | List of Packages Required to install and run sabnzbd |

Dependencies
------------

None

Example Playbook
----------------

   - hosts: sabnzbd_servers
      roles:
        - aaron_cole.ansible_role_sabnzbd


License
-------

GPLv3

Author Information
------------------

Created by Aaron Cole

