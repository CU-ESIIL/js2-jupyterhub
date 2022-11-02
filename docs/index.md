[<img src="./assets/cacao-logo.png" width="250"/>](https://cacao.jetstream-cloud.org/){target=_blank}
## Getting Started with CACAO

[Create an ACCESS account](https://access-ci.org/){target=_blank}

[Requesting an allocation on Jetstream-2](https://docs.jetstream-cloud.org/alloc/overview/){target=_blank}

## Logging into CACAO

Click here: [https://cacao.jetstream-cloud.org/](https://cacao.jetstream-cloud.org/){target=_blank} URL

[<img src="./assets/signin.png" width="250"/>](https://cacao.jetstream-cloud.org/){target=_blank}

CACAO uses ACCESS-CI [CILogon](https://www.cilogon.org/) with DuoAuth

[<img src="./assets/login.png" width="750"/>](./assets/login.png){target=_blank}

[Setting up DuoAuth Multi-Factor Identity](https://identity.access-ci.org/manage-mfa.html){target=_blank}

[<img src="./assets/duo.png" width="250"/>](./assets/duo.png){target=_blank}

You should now see the CACAO homepage

[<img src="./assets/home.png" width="750"/>](./assets/home.png){target=_blank}


## Creating Credentials

Before you can use Jetstream2 you need to create credentials for your user profile.

[<img src="./assets/credentials.png" width="750"/>](./assets/credentials.png){target=_blank}


Select the **+ Add Credential** button in the upper right of the panel

[<img src="./assets/new_credential.png" width="250"/>](./assets/new_credential.png){target=_blank}

Select the **Cloud Credential** option and select **Jetstream 2**

[<img src="./assets/select_cloud.png" width="750"/>](./assets/select_cloud.png){target=_blank}

Select any of the Jetstream2 Cloud Projects that you have access to (it may be only one project if this is your first time)

[<img src="./assets/project.png" width="750"/>](./assets/project.png){target=_blank}

You should now see a completed summary with success:

[<img src="./assets/summary.png" width="750"/>](./assets/summary.png){target=_blank}

Optionally, you can also create a Public SSH Key for yourself.

[<img src="./assets/new_credential.png" width="250"/>](./assets/new_credential.png){target=_blank}

SSH keys are a good way to secure your deployments

[<img src="./assets/sshkey.png" width="500"/>](./assets/sshkey.png){target=_blank}

## Create a New Deployment

CACAO uses the concept of Deployments for new projects

Select the Deployments tab on the left side:

[<img src="./assets/deployments.png" width="750"/>](./assets/deployments.png){target=_blank}

Click the **+ Add Deployment** button

Select the **launch a multi-vm zero-to-jupyterhub** template

[<img src="./assets/deployment.png" width="750"/>](./assets/deployment.png){target=_blank}

## Create a new Jupyter Hub

### Set the Region to launch your Jupyter Hub 

??? Info "Currently CACAO only supports Jetstream2"

    The only region available to you in Jetstream2 is the Indiana University (IU)

    You may create Credentials in the future with different cloud providers (Commercial or OpenStack) 

[<img src="./assets/region.png" width="750"/>](./assets/region.png){target=_blank}

### Set the Parameters

[<img src="./assets/parameters.png" width="750"/>](./assets/parameters.png){target=_blank}

### Set up Authentication

There are two types of user authentication

Dummy Authentication allows you to create new user names and dummy passwords

[<img src="./assets/auth_dummy.png" width="750"/>](./assets/auth_dummy.png){target=_blank}

GitHub Authentication is a multi-step process

[<img src="./assets/auth_github.png" width="750"/>](./assets/auth_github.png){target=_blank}

??? Info "Setting up GitHub Authentication"

    TBA

### Set up Users

The JupyterHub users can be created at this time.

??? Tip "Important: you must have an administrative user account"

    Make sure to create at least one user with "admin" privileges at this time

    You can create more accounts later on, so if you're in a hurry you only need one admin before launching the Hub.

    More admins and users can be created in the Jupyter Hub Admin panel

[<img src="./assets/users.png" width="750"/>](./assets/users.png){target=_blank}

### Set up Shared Storage

You can add a Shared Storage volume to your cluster.

You can also choose whether to make this volume "read-only" 

[<img src="./assets/storage.png" width="750"/>](./assets/storage.png){target=_blank}

### Select the appropriate Docker Image

In this step you're actually selecting a Docker Image from a public registry

We recommend you use a featured Project Jupyter Docker Stack image, or one of ours:

`harbor.cyverse.org/rstudio/binder:latest`

`harbor.cyverse.org/jupyter/minimal:latest`

`harbor.cyverse.org/jupyter/datascience:latest`

[<img src="./assets/image.png" width="750"/>](./assets/image.png){target=_blank}

### Review and deploy :material-rocket:

[<img src="./assets/review.png" width="750"/>](./assets/review.png){target=_blank}
