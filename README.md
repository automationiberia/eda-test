# EDA-Tests
# High Level steps


. Packages required
   ```
$ ansible --version # >= core 2.15.2
$  python3 -m pip install ansible-navigator>=3.4.2 --user
$  python3 -m pip install ansible-builder>=3.0.0 --user
   ```

. Run the playbook to apply the configuration in the automation eda:
   ```
    ansible-navigator run playbooks/config-eda.yaml -i localhost -m stdout --eei quay.io/automationiberia/eda/ee-acm-eda:latest --eev /tmp/:/tmp/ -e @vars/vault.yaml --vault-password-file .vault-password  -e'{ansible_async_dir: /home/runner/.ansible_async/}
   ```
