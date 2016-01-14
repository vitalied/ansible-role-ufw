Ansible Role for UFW
====================

[![Build Status](https://travis-ci.org/pantarei/ansible-role-ufw.svg?branch=master)](https://travis-ci.org/pantarei/ansible-role-ufw)
 [![GitHub tag](https://img.shields.io/github/tag/pantarei/ansible-role-ufw.svg)](https://github.com/pantarei/ansible-role-ufw)
 [![GitHub license](https://img.shields.io/github/license/pantarei/ansible-role-ufw.svg)](https://github.com/pantarei/ansible-role-ufw/blob/master/LICENSE)
 [![Ansible Role](https://img.shields.io/ansible/role/6153.svg)](https://galaxy.ansible.com/detail#/role/6153)

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
<th align="left">parameter</th>
<th align="left">required</th>
<th align="left">default</th>
<th align="left">choices</th>
<th align="left">comments</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left">ufw_state</td>
<td align="left">yes</td>
<td align="left">enabled</td>
<td align="left"><ul>
<li>enabled</li>
<li>disabled</li>
<li>reloaded</li>
<li>reset</li>
</ul></td>
<td align="left">Pass value as <code>state</code> to <a href="http://docs.ansible.com/ansible/ufw_module.html">ufw module</a>.</td>
</tr>
<tr class="even">
<td align="left">ufw_logging</td>
<td align="left">yes</td>
<td align="left">on</td>
<td align="left"><ul>
<li>on</li>
<li>off</li>
<li>low</li>
<li>medium</li>
<li>high</li>
<li>full</li>
</ul></td>
<td align="left">Pass value as <code>logging</code> to <a href="http://docs.ansible.com/ansible/ufw_module.html">ufw module</a>.</td>
</tr>
<tr class="odd">
<td align="left">ufw_direction</td>
<td align="left">no</td>
<td align="left"><a href="https://github.com/pantarei/ansible-role-ufw/blob/master/defaults/main.yml">defaults/main.yml</a></td>
<td align="left"><ul>
<li><code>[]</code></li>
<li><code>list</code></li>
</ul></td>
<td align="left">Skip setup policy per direction if <code>[]</code>, or pass list as <code>direction</code> to <a href="http://docs.ansible.com/ansible/ufw_module.html">ufw module</a>.</td>
</tr>
<tr class="even">
<td align="left">ufw_interface</td>
<td align="left">no</td>
<td align="left"><a href="https://github.com/pantarei/ansible-role-ufw/blob/master/defaults/main.yml">defaults/main.yml</a></td>
<td align="left"><ul>
<li><code>[]</code></li>
<li><code>list</code></li>
</ul></td>
<td align="left">Skip setup rule per interface if <code>[]</code>, or pass list as <code>interface</code> to <a href="http://docs.ansible.com/ansible/ufw_module.html">ufw module</a>.</td>
</tr>
<tr class="odd">
<td align="left">ufw_from_ip</td>
<td align="left">no</td>
<td align="left"><a href="https://github.com/pantarei/ansible-role-ufw/blob/master/defaults/main.yml">defaults/main.yml</a></td>
<td align="left"><ul>
<li><code>[]</code></li>
<li><code>list</code></li>
</ul></td>
<td align="left">Skip setup rule per from_ip if <code>[]</code>, or pass list as <code>from_ip</code> to <a href="http://docs.ansible.com/ansible/ufw_module.html">ufw module</a>.</td>
</tr>
<tr class="even">
<td align="left">ufw_to_port</td>
<td align="left">no</td>
<td align="left"><a href="https://github.com/pantarei/ansible-role-ufw/blob/master/defaults/main.yml">defaults/main.yml</a></td>
<td align="left"><ul>
<li><code>[]</code></li>
<li><code>list</code></li>
</ul></td>
<td align="left">Skip setup rule per to_port if <code>[]</code>, or pass list as <code>to_port</code> to <a href="http://docs.ansible.com/ansible/ufw_module.html">ufw module</a>.</td>
</tr>
<tr class="odd">
<td align="left">ufw_route</td>
<td align="left">no</td>
<td align="left"><a href="https://github.com/pantarei/ansible-role-ufw/blob/master/defaults/main.yml">defaults/main.yml</a></td>
<td align="left"><ul>
<li><code>[]</code></li>
<li><code>list</code></li>
</ul></td>
<td align="left">Skip setup rule per route if <code>[]</code>, or pass list as <code>route</code> to <a href="http://docs.ansible.com/ansible/ufw_module.html">ufw module</a>.</td>
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
    -   <https://twitter.com/hswong3i>
    -   <https://github.com/hswong3i>

