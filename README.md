
# k8s-hcloud-infrastructure-role

Role to create the necessary infrastructure in hetzner cloud for a cluster in kubernetes


## Requirements

- awx.awx

- hetzner.hcloud
## Role Variables



| name | type  |   default	|  required 	|
|---	|---	|---	|---	|
|  hcloud_instance_image 	|   str  	|  ubuntu-20.04 	|   No	|
|  hcloud_num_masters_nodes 	|  number 	|  1 	|   No	|
|  hcloud_num_workers_nodes 	| number  	|  2 	|  No 	|
|  hcloud_master_instance_type 	|  str 	|  cx11 	|  No 	|
| hcloud_workers_instance_type |  str 	|   cx11	|  No 	|
| hcloud_token  |  str 	|   None	|   **Yes**	|
| hcloud_private_network | str| None| **Yes**|
| hcloud_ssh_keys| list| []| No
| awx_inventory_name | str| default | None|
|awx_controller_host| str| None| No|
|awx_controller_protocol| str| None|No|
|awx_controller_token| str| None| No|
|awx_controller_username|str|None|No|
|awx_controller_password| str | None|No|
|awx_group_master| str|k8s-masters| No|
|awx_group_nodes| str|k8s-workers|No|
|awx_organization| str|k8s|No|
## Example Playbook

    -  name:  Run role
	   hosts:  127.0.0.1
       roles:
         -  "k8s-hcloud-infrastructure"

  
  

## License


  

BSD

  

Eugeni Bejan

------------------

  


