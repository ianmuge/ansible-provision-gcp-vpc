# Prerequites
Set the GCP project variables on the workspace environment
```
export GCP_PROJECT="" && \
export GCP_AUTH_KIND="serviceaccount" && \
export GCP_SERVICE_ACCOUNT_FILE="" && \
export GCP_SCOPES="https://www.googleapis.com/auth/compute" && \
export GCP_ZONE='us-central1-a'
```

# Deployment Instructions
This will spawn a full VPC with:
- Firewall Rules
- Regional Auto-routing
On CLI you can run the command shown below. 

```
ansible-playbook -T 60 -f 100 main.yml -e "vpc_name={vpc name}"
```
You can modify a number of variables from the individual service variables

## Tower Setup
On Ansible Tower, you will need to let the scm sync and run the project on the UI
P.S.
You might need to define some define some variables to enable for proper deployment of assets and setup


