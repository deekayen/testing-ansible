# Input validation

The two playbooks in this demonstration outline two different ways of requiring a `terminate` variable at runtime. If the terminate variable is not defined, we intentionally want the playbook to fail and abort execution.

## Assert

In the assert playbook, we check to be sure the `terminate` is defined and that it follows our imaginary virtual machine hostname formatting style guide, which requires an integer on the end of the hostname. If either condition fails, the playbook aborts.

### Example commands

```
$ ansible-playbook -i localhost, -e "terminate=oldhost1" assert.yml
```

## Argument specs

This more modern addition was added in Ansible 2.11 and defines expected arguments in the role's `meta/argument_specs.yml` file. At its introduction, it was only helpful for input validation when requiring a variable or matching it against a list of acceptable options.

https://docs.ansible.com/ansible/latest/user_guide/playbooks_reuse_roles.html#role-argument-validation

### Example commands

```
$ ansible-playbook -i localhost, -e "terminate=oldhost1" argument_specs.yml
```

![argument specs example playbook output](files/argument_specs_console.png)
