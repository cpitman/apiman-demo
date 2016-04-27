This demo is a work in progress. Here is what is done so far:

Run `vagrant up` (warning, currently need a self built RHEL image):

  * Creates VM
  * Installs Ansible
  * Installs Docker
  * Builds helloworld-rs Docker Image on Wildfly
  * Deploys helloworld-rs and apiman
  
After `vagrant up`, you can access apiman at (http://localhost:8080/apimanui) with the username "admin" and the password "admin123!".

Currently you must configure apiman after standing it up. In order to do this, you will need to create an Organization, then define the API (accessable at http://db:8080/jboss-helloworld-rs/rest), create a plan, and then a client. Instructions and automation for this are a work in progress.
  
Remaining ToDos:

  * Either move vagrant box to Centos or include instructions for getting the RHEL CDK
  * Configure apiman on `vagrant up`
  * Add instructions for how to use apiman and the helloworld service
  * Configure Mutual SSL authentication between apiman and Wildfly