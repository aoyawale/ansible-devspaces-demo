# Ansible DevX 
## End to End Developer Experience, from Dev into Production AAP.

### Tasklist #4:
        1. Now that we have pushed content to Dev successfully from our Dev Spaces workpace lets switch hats and create a pull request to merge our changes to our production branch. 

        - Webhooks in our demo environment have been configured to run when changes are pushed to our repo. 

        - Navigate to the Github repo: https://github.com/aoyawale/ansible-devspaces-demo 

        2. You should see a banner, "dev had recent pushes" - "Compare & pull request"

        - Click Compare and pull request. 

        - Select the correct repo and branch to merge the changes into. 

        - Enter a nice title and description for your pull request and the select "Create pull request."

        3. Scroll down to the checks section and you'll see 2 actions were created on push based actions (when we pushed to dev).

        - Additionally, based on our lint and molecule CI files in the .github/workflows directory in this repo we have an additional action created off of pull requests. 

        - Once those jobs finish you can now merge the pull request and the changes from dev will be promoted to prod. 

        - Confirm merge if prompted.

        4. Now that our changes are pushed to the prod branch lets process to tasklist 5, now shifting over to AAP. 

        - Proceed to Tasklist 5. 