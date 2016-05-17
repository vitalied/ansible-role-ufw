Ansible Role for UFW
====================

[![Build Status](https://travis-ci.org/pantarei/ansible-role-ufw.svg?branch=master)](https://travis-ci.org/pantarei/ansible-role-ufw)
[![GitHub tag](https://img.shields.io/github/tag/pantarei/ansible-role-ufw.svg)](https://github.com/pantarei/ansible-role-ufw)
[![GitHub license](https://img.shields.io/github/license/pantarei/ansible-role-ufw.svg)](https://github.com/pantarei/ansible-role-ufw/blob/master/LICENSE)

Ansible Role for Ubuntu UFW Management.

Requirements
------------

This role require Ansible 2.0 or higher.

This role was designed for Ubuntu Server 14.04 LTS.

Role Variables
--------------

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th>parameter</th>
<th>required</th>
<th>default</th>
<th>choices</th>
<th>comments</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ufw_state</td>
<td>yes</td>
<td>enabled</td>
<td><ul>
<li>enabled</li>
<li>disabled</li>
<li>reloaded</li>
<li>reset</li>
</ul></td>
<td>Pass value as <code>state</code> to <a href="http://docs.ansible.com/ansible/ufw_module.html">ufw module</a>.</td>
</tr>
<tr class="even">
<td>ufw_logging</td>
<td>yes</td>
<td>on</td>
<td><ul>
<li>on</li>
<li>off</li>
<li>low</li>
<li>medium</li>
<li>high</li>
<li>full</li>
</ul></td>
<td>Pass value as <code>logging</code> to <a href="http://docs.ansible.com/ansible/ufw_module.html">ufw module</a>.</td>
</tr>
<tr class="odd">
<td>ufw_direction</td>
<td>no</td>
<td><a href="https://github.com/pantarei/ansible-role-ufw/blob/master/defaults/main.yml">defaults/main.yml</a></td>
<td><ul>
<li><code>[]</code></li>
<li><code>list</code></li>
</ul></td>
<td>Skip setup policy per direction if <code>[]</code>, or pass list as <code>direction</code> to <a href="http://docs.ansible.com/ansible/ufw_module.html">ufw module</a>.</td>
</tr>
<tr class="even">
<td>ufw_interface</td>
<td>no</td>
<td><a href="https://github.com/pantarei/ansible-role-ufw/blob/master/defaults/main.yml">defaults/main.yml</a></td>
<td><ul>
<li><code>[]</code></li>
<li><code>list</code></li>
</ul></td>
<td>Skip setup rule per interface if <code>[]</code>, or pass list as <code>interface</code> to <a href="http://docs.ansible.com/ansible/ufw_module.html">ufw module</a>.</td>
</tr>
<tr class="odd">
<td>ufw_from_ip</td>
<td>no</td>
<td><a href="https://github.com/pantarei/ansible-role-ufw/blob/master/defaults/main.yml">defaults/main.yml</a></td>
<td><ul>
<li><code>[]</code></li>
<li><code>list</code></li>
</ul></td>
<td>Skip setup rule per from_ip if <code>[]</code>, or pass list as <code>from_ip</code> to <a href="http://docs.ansible.com/ansible/ufw_module.html">ufw module</a>.</td>
</tr>
<tr class="even">
<td>ufw_to_port</td>
<td>no</td>
<td><a href="https://github.com/pantarei/ansible-role-ufw/blob/master/defaults/main.yml">defaults/main.yml</a></td>
<td><ul>
<li><code>[]</code></li>
<li><code>list</code></li>
</ul></td>
<td>Skip setup rule per to_port if <code>[]</code>, or pass list as <code>to_port</code> to <a href="http://docs.ansible.com/ansible/ufw_module.html">ufw module</a>.</td>
</tr>
<tr class="odd">
<td>ufw_route</td>
<td>no</td>
<td><a href="https://github.com/pantarei/ansible-role-ufw/blob/master/defaults/main.yml">defaults/main.yml</a></td>
<td><ul>
<li><code>[]</code></li>
<li><code>list</code></li>
</ul></td>
<td>Skip setup rule per route if <code>[]</code>, or pass list as <code>route</code> to <a href="http://docs.ansible.com/ansible/ufw_module.html">ufw module</a>.</td>
</tr>
</tbody>
</table>

Dependencies
------------

No additional role dependencies.

Example Playbook
----------------

    - hosts: servers
      roles:
        - { role: hswong3i.ufw, ufw_state: 'enabled', ufw_logging: 'on' }

License
-------

-   Code released under [MIT](https://github.com/pantarei/ansible-role-ufw/blob/master/LICENSE)
-   Docs released under [CC BY 4.0](http://creativecommons.org/licenses/by/4.0/)

Author Information
------------------

-   Wong Hoi Sing Edison
    -   <a href="https://twitter.com/hswong3i" class="uri" class="uri">https://twitter.com/hswong3i</a>
    -   <a href="https://github.com/hswong3i" class="uri" class="uri">https://github.com/hswong3i</a>

