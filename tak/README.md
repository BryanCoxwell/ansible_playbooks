# Docker TAK Server Installation

This role will:
- Install docker and docker-compose
- Create docker images from the included zip archive (sourced from Tak.gov)
- Create and start docker containers for the TAK server and TAK database. 

If the `generate_certs` variable is set to `true`, the role will also:
- Create a root CA from the given configuration variables
- Create a server certificate from this root CA
- Create a single user certificate with admin privileges

The admin user certificate will need to be SCP'd off of the remote machine from `/opt/tak/certs/files/admin.p12` to the local machine and then installed in the admin user's browser in order to access 
the TAK Server web GUI (reachable at https://<SERVER_IP>:8443/)