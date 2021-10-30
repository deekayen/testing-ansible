# Ansible managed

With ansible_managed, you can outputs several types of `ansible_managed` comments to a text file.

The ansible_managed playbook helps you practice the output options the `ansible_managed` magic variable with `comment()` filter.

If you use `ansible_managed`, you can remind your system administrators about which files are under configuration management by Ansible.

You'll like `ansible_managed` because you'll help remind your co-workers, peers, subversive trolls, and chaos engineers that the files they're editing may be clobbered and overwritten by files managed by Ansible.

Using `ansible_managed` is better than static files in your ansible roles because you can update the contents of the comment block dymamically with the last timestamp Ansible updated the file and where to find the template that sourced the changes.

The default output file is copied to the home folder of the ansible user you run on your control machine as `hello_world.txt`.

Note that this example folder has an ansible.cfg file to override the default value output by `ansible_managed`, which is normally just "Ansible managed".


## Prerequisites

Ansible: 1.9

This example does not have any specific operating system dependencies.

## Dependencies

None.

## Example

```
deekayen-macbook testing-ansible/ansible_managed ‹main*› » ansible-playbook -i localhost, ansible_managed.yml
 ____________
< PLAY [all] >
 ------------
          \
           \         _.-````'-,_
          _,.,_ ,-'`           `'-.,_
        /)     (                   '``-.
       ((      ) )                      `\
         \)    (_/                        )\
         |       /)           '    ,'    / \
         `\    ^'            '     (    /  ))
           |      _/\ ,     /    ,,`\   (  "`
           \Y,   |   \  \  | ````| / \_ \
             `)_/     \  \  )    ( >  ( >
                       \( \(     |/   |/
                      /_(/_(    /_(  /_(

 ________________________
< TASK [Gathering Facts] >
 ------------------------
          \
           \         _.-````'-,_
          _,.,_ ,-'`           `'-.,_
        /)     (                   '``-.
       ((      ) )                      `\
         \)    (_/                        )\
         |       /)           '    ,'    / \
         `\    ^'            '     (    /  ))
           |      _/\ ,     /    ,,`\   (  "`
           \Y,   |   \  \  | ````| / \_ \
             `)_/     \  \  )    ( >  ( >
                       \( \(     |/   |/
                      /_(/_(    /_(  /_(

ok: [localhost]
 ____________________________________________________
< TASK [Copy the template to parse ansible_managed.] >
 ----------------------------------------------------
          \
           \         _.-````'-,_
          _,.,_ ,-'`           `'-.,_
        /)     (                   '``-.
       ((      ) )                      `\
         \)    (_/                        )\
         |       /)           '    ,'    / \
         `\    ^'            '     (    /  ))
           |      _/\ ,     /    ,,`\   (  "`
           \Y,   |   \  \  | ````| / \_ \
             `)_/     \  \  )    ( >  ( >
                       \( \(     |/   |/
                      /_(/_(    /_(  /_(

changed: [localhost]
 ____________
< PLAY RECAP >
 ------------
          \
           \         _.-````'-,_
          _,.,_ ,-'`           `'-.,_
        /)     (                   '``-.
       ((      ) )                      `\
         \)    (_/                        )\
         |       /)           '    ,'    / \
         `\    ^'            '     (    /  ))
           |      _/\ ,     /    ,,`\   (  "`
           \Y,   |   \  \  | ````| / \_ \
             `)_/     \  \  )    ( >  ( >
                       \( \(     |/   |/
                      /_(/_(    /_(  /_(

localhost                  : ok=2    changed=1    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0
```
The contents of the hello_world.txt output are similar to the following:

```
Plain hash:
#
# This file is managed by Ansible.
#
# Update this in the ansible.cfg found by the playbook.
# template: templates/hello_world.txt.j2
# date: 2021-10-29 22:35:35
# user: deekayen
# host: deekayen-macbook.local
#

C/PHP:
//
// This file is managed by Ansible.
//
// Update this in the ansible.cfg found by the playbook.
// template: templates/hello_world.txt.j2
// date: 2021-10-29 22:35:35
// user: deekayen
// host: deekayen-macbook.local
//

C block/PHP:
/*
 *
 * This file is managed by Ansible.
 *
 * Update this in the ansible.cfg found by the playbook.
 * template: templates/hello_world.txt.j2
 * date: 2021-10-29 22:35:35
 * user: deekayen
 * host: deekayen-macbook.local
 *
 */

Erlang:
%
% This file is managed by Ansible.
%
% Update this in the ansible.cfg found by the playbook.
% template: templates/hello_world.txt.j2
% date: 2021-10-29 22:35:35
% user: deekayen
% host: deekayen-macbook.local
%

XML/HTML:
<!--
 -
 - This file is managed by Ansible.
 -
 - Update this in the ansible.cfg found by the playbook.
 - template: templates/hello_world.txt.j2
 - date: 2021-10-29 22:35:35
 - user: deekayen
 - host: deekayen-macbook.local
 -
-->

Customized:
###
#
# This file is managed by Ansible.
#
# Update this in the ansible.cfg found by the playbook.
# template: templates/hello_world.txt.j2
# date: 2021-10-29 22:35:35
# user: deekayen
# host: deekayen-macbook.local
#
###
```

## Issues

Submit your improvements and errata to the [GitHub issue queue](https://github.com/deekayen/testing-ansible/issues)

## License

You are free to copy, modify, and distribute this `ansible_managed` example with attribution under the terms of the BSD-3-Clause license. See the LICENSE file for details.

## About the author

This project was created by [David Norman](https://dkn.me) as an example for [Testing Ansible](https://testingansible.rocks).
