Running Gerrit on OpenShift
---------------------------

Create an account at https://www.openshift.com

On your client machine, install rhc and setup with the newly created account on openshift for the first time.

    gem install rhc
    rhc setup --server openshift.redhat.com --rhlogin LOGIN --password PASSWORD
    
The below command creates a DIY 0.1 application, and import the quickstart code:

    rhc app create <app name> diy --from-code=https://github.com/over9000/gerrit-openshift-quickstart.git

You can now checkout Gerrit application at:

    http://<app name>-<your namespace>.rhcloud.com

Login is configured to be OpenID. The first registered user will be in the Administrators group.
