klems.motd
=========
[![Build Status](https://travis-ci.org/klems/ansible-role-motd.svg?branch=master)](https://travis-ci.org/klems/ansible-role-motd)

A role that allows you to customize and add colors to your MOTD, depending of your environement (dev/staging/prod)

![dev](https://image.ibb.co/hNrTob/demo_new_dev.png)
![staging](https://image.ibb.co/bLSF1w/demo_new_staging.png)
![prod](https://image.ibb.co/h3a2gw/demo_new_prod.png)

Requirements
------------
Ansible == `2.4`

Role Variables
--------------
### {{ bash_color_prompt }}
Allows you to color parts of your MOTD with bash color codes.

```
bash_color_prompt: "32"
```

### {{ figlet_extra_fonts }}
A list of extra fonts to be downloaded from figlet.org

```
figlet_extra_fonts:
  - smscript.flf
  - stop.flf
```

### {{ figlet_font }}
The font that will be used to display the hostname of the server.

```
figlet_font: "standard.flf"
```

Dependencies
------------
N/A

Example Playbook
----------------
```
- hosts: servers
  roles:
     - { role: klems.motd, bash_color_prompt: 32 }
```

License
-------
BSD

Author Information
------------------
mail: klems@klems.net
