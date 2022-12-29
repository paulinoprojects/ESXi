## ESXi Basic Network Traffic Explained
![VM Network Traffic](https://user-images.githubusercontent.com/111991325/209737771-87e5f408-5e49-46be-a849-8c46d539be29.png)

#### Key Terms
- vNICs
- Port Groups
- vSwitch (vShpere Standard Switch)
- DSwitch (Distrubuted Switch)
- VMkernal Ports
- VMNICs


#### Key Term Relation
 1. Hosts (indivdual VMs) use <b>vNICs</b> -> 
 2. VM vNICs are assigned to <b>Port Groups</b> that are defined with VLANs on the <b>vSwitch</b>(vShpere Standard Switch or Distributed Switch) -> 
 3. Port Groups are linked to a <b>VMNIC</b> which servers as an uplinks to the physical switch in the network (best practice to aggregate links on) 


![VMkernal Ports](https://user-images.githubusercontent.com/111991325/209893545-50a8a976-ae96-4e78-8ca2-9231f1d49ece.png)

- <b>VMkernel Ports</b> are port on the vSwitch used for special traffic (not host traffic) such as Management, Stroage, vMotion, this is how vCenter and the hosts communicate.
- <b>VMNICs</b> are the physical adapters of the ESXi Host itself, can only be assigned to 


#### DSwitch - Distributed Switch
- Create and Manage DSwitch in vCenter.
- We create distributed port groups to span many hosts and ensure identical configuration.
- VMkernal ports and uplinks still need to be configured on an individual host.
- Features & Benefits for DSwitch
  - Private VLANs: Hosts can be governored within the same subnets such as creating isolated community VLANs.
  - NIC Teaming / Load Based Teaming: Allows dynamic traffic load balancing to ensure efficent usage of bandwidth.  
  - DEMO: Migrating VMs to A Distributed Switch
