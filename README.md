## Automated Deployment and Configuration with Ansible for Boilerplates

This project configures an instance of this boilerplate https://github.com/hngprojects/hng_boilerplate_nestjs on a host.

This ansible `main.yaml` file does the following:
- Creates a new user with sudo priviledges
- Creates the neccessary directories and installs the required packages this project needs to run
- Clones the repository containing the boilerplate
- Sets up the PostgreSQL database and save these credentials into a secure file
- Starts the application on port 3000
- Configures Nginx to reverse proxy the application from 3000 to port 80


To start this playbook, run this command, replacing the `inventory.cfg` file with your inventory file containing your hosts: 

```
ansible-playbook main.yaml -b inventory.cfg
```

