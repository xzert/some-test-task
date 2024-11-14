
## Task: Prepare the OS using Ansible
### Using Ansible, implement the ability to perform the following actions (and repeat them on other servers in the future):
- [ ] Implement the procedure of encrypting the second disk in the system (where there is no root partition) (partition name should be specified in the inventory).
- [ ] Implement a procedure to encrypt the partition that is present on the disk next to the root partition.
- [ ] Disabling C-state for all available CPUs.
- [ ] Switching CPU operation from power-saving mode to more productive mode.
- [ ] Rename the active network interface to "net0". Display information about the renamed interface during the playbook. 
- [ ] At the end of the playbook execution, a list of CPUs should be displayed, as well as information about Intel Hyper-Threading (AMD multithreading).

## General Requirements:
  - When designing playbooks and roles, attention should be paid to error handling and correct task execution messages.
  - Each playbook or role should be described in a separate README file along with startup and validation instructions/
  - All required files (playbooks, roles, scripts) must be submitted along with the result of the assignment.
## Evaluation:
### The candidate will be evaluated on the following criteria:
  - Quality of writing Ansible playbooks and roles.
  - Overall code organization.
  - Understanding of basic Ansible concepts and system administration.

After completing the assignment, please provide git-repository or archive of the roles, playbooks and README files so that they can be evaluated and tested.
