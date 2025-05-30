# Ansible DevX 
## End to End Developer Experience, from Developing into Production AAP, a seamless process. 

### Tasklist #1:
    1. Explore the demo environment setup for you. 

    2. The magic of all of this demo is the devfile.yaml.
    - The devfile contains the container configurations for the IDE we're currently running. 
    - The image 'ghcr.io/ansible/ansible-devspaces' contains all of the Ansible dev tools necessary for lint, molecule, navigator, builder and more.
    - You can set requests/limits for the container workspace, env variables and more. 

    3. 2 sample collections are available under the collections directory.   
    - sample_collection: This can be used to test Molecule/Linting locally from the terminal in VSCode. 
    - github_action_sample: This collection is configured with github actions to run molecule tests. It spins up a fedora 42 container, installs necessary dependencies and tests this collection/role. From there it will actually install and configure apache in the container and complete the testing scenario with Molecule. This will be demonstrated later by viewing the results of the Github Actions when pushing changes to Dev branch. 

    4. Ansible lint configuration: '.ansible-lint'
    - Inspect the file to see the configuration for linting locally within the Git repo. 

    5. Precommit Configuration: .pre-commit-config.yaml
    - Inspect the file to see the configuration for pre-commit checks that are run after file changes are made, prior to commiting changes and pushing to the repo. 

    6. Example playbook.yml
    - This playbook will be used to show the End to End developer workflow.
    - Once authored to desired state, pre-commit checks will run against the file to check for linting errors. From there when pushed to the 'dev' branch, github actions will run the Ansible-lint checks as well as the defined Molecule scenario. Once completed and passed you can create a pull request to merge the changes to prod. 