# Ansible DevX 
## End to End Developer Experience, from Developing into Production AAP, a seamless process. 

### Tasklist #1:
    1. Explore the demo environment setup for you. 

    2. The magic of all of this demo is the devfile.yaml.

    3. 2 sample collections are available under the collections directory.   
    - sample_collection: This can be used to test Molecule/Linting locally from the terminal in VSCode. 
    - github_action_sample: This collection is configured with github actions to run molecule tests. It spins up a fedora 42 container, installs necessary dependencies and tests this collection/role. From there it will actually install and configure apache in the container and complete the testing scenario with Molecule. This will be demonstrated later by viewing the results of the Github Actions when pushing changes to Dev branch. 

    4. 