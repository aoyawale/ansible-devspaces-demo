# Ansible DevX 
## End to End Developer Experience, from Dev into Production AAP.

### Tasklist #5:
        1. Config as Code triggered by Webhooks from Github Prod branch. 

        - Since we've pushed changes to our Github repo prod branch, we can see that our automation was triggered and our config as code playbook was run against AAP itself. 

        - It has taken the playbook.yml from our parent directory in the repo and created a job template for an AAP Job Operator to now execute. 

        - Please review the job_template created from the dev branch initially and execute this job.

        - Job Template: https://aap-devspaces-25-aap.apps.devspaces-sno.arsalan.io/execution/templates/job-template/15/details

        2. To provide your developers a way to verify their code has been successfully promoted and has completed the workflow you can provide them the job_template ID and URL or opt for a Grafana dashboard for Github.

        - Navigate to Grafana Dashboard for Github repo: https://grafana-openshift-user-workload-monitoring.apps.devspaces-sno.arsalan.io/d/iVcSTeyGz/github-default?from=now-90d&to=now&var-datasource=bengnq61q8vlsf&var-organization=hammer-redhat&var-repository=ansible-devspaces-demo&var-labels=$__all&var-branch=prod&var-milestone=$__all 

        - Note this is not pointed at the exact repo used in this demo because the dashboard doesn't support forked repos at this time. 

        - Proceed to the final task, tasklist 6, for static code scanning with Ansible code bot. 