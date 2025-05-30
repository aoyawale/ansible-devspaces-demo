# Ansible DevX 
## End to End Developer Experience, from Dev into Production AAP.

### Tasklist #2:
        1. Begin testing the playbook.yml in the main directory. 
        - Login to registry.redhat.io with podman. 
                `podman login registry.redhat.io`
                enter username and password when prompted
        - After logging into the registry successfully you can run the following command with Ansible-navigator to test the playbook. 
                `ansible-navigator run playbook.yml`
                The ansible-navigator.yml configuration already sets mode to stdout and specified the execution environment for you. 
                
