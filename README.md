`ansible-playbook -i inventory main.yml`

invokes role `foo` and role `bar`. You may expect role `foobar` to be invoked but it is not. This is because Ansible resolves the roles "early" in the process. The implication is that we can NOT use host variables to decide which role to invoke.

`ansible-playbook -i inventory main_fails.yml`

Shows that run-time host variables can NOT be used to determine which role to invoke.
