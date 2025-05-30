# Ansible DevX 
## End to End Developer Experience, from Dev into Production AAP.

### Tasklist #2:
        1. Begin testing the playbook.yml in the main directory. 

        - Login to registry.redhat.io with podman. 

                `podman login registry.redhat.io`

                enter username and password when prompted

        - After logging into the registry successfully you can run the following command with Ansible-navigator to test the playbook.

                `ansible-navigator run playbook.yml -i aap-cac-job-template/inventory`

                The ansible-navigator.yml configuration already sets mode to stdout and specified the execution environment for you. 
                
        2. Now that we've run our playbook inside of an execution environment locally, lets ensure our code has been linted and is ready for commit/push to our dev branch. 

                Run the following to lint our playbook - `ansible-lint playbook.yml`

                You should see the following output: "Passed: 0 failure(s), 0 warning(s) on 1 files. Last profile that met the validation criteria was 'production'."

        3. If this playbook was a part of our collection/role we could then run molecule locally to test our scenario. 

                Thankfully we have an example setup to demonstrate
                
                Run - `cd collections/ansible_collections/sample_namespace/sample_collection/extensions/`

                Then run `molecule test` to kickoff the test scenario locally. 

        4. After the molecule test completes then we can proceed to check in our code changes.

                Please proceed to tasklist 3.