# Ansible DevX 
## End to End Developer Experience, from Dev into Production AAP.

### Tasklist #3:
        1. Now that we have updates to our code base, we've run lint against our playbook, passed the production profile locally, and a successful local molecule run we can then check in our code to Github. 

                - Navigate to the source control tab on the left hand side of the VScode workspace. (Shortcut CTRL+SHIFT+G).

                - Enter a commit message to describe your changes and click on `Commit`. 

                - If an error pops  up to configure your Git username and email please run the following.

                 `git config --global user.email "you@example.com"`
                 `git config --global user.name "Firstname Lastname"`

                - Now with git configured try to commit your changes again. 

                - Once commited then sync to the remote repository. 

        2. From here we can shift to the actual Github repo to view the Github actions that have begun as a result of us pushing changes to the repo. 

                - Navigate to: https://github.com/aoyawale/ansible-devspaces-demo/actions 

                - You will see two actions that match with your commit, one for "ansible-lint" and another for "Molecule CI".

                - If you drill into ansible-lint - step 3 titled "Run ansible-lint" around line 203 of the stdout you should see that our production profile passed and this job was successful. 

        3. Return to the Github actions page and drill into "Molecul CI" job that completed as well.

        - In the Molecule CI action we can see it sets up a container, pulls the git repo into it and configures python, dependencies and then runs the Molecule scenario specified. 

        - Inspect the 5th job titled "Run Molecule tests"

        - You'll notice on line ~100 if you expand "Molecule default > converge" that our molecule scenario is installing an Apache server, copies a web page to the container and ensures Apache's services are configured persistently then it restarts the Apache service. 

        - Further down around line 169 "Molecule default > verify" checks that Apache is serving web requests. 

        - Our scenario with Molecule continues to run cleanup, and destroys the container instance before completing. 

        - Please proceed to Tasklist 4. 