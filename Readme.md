# Deploy a Virtual Machine with Cloud Init

<a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fkenmuse%2Farm-init%2Fmaster%2Fazuredeploy.json" target="_blank">
    <img src="http://azuredeploy.net/deploybutton.png"/>
</a>
<a href="http://armviz.io/#/?load=hhttps%3A%2F%2Fraw.githubusercontent.com%2Fkenmuse%2Farm-init%2Fmaster%2Fazuredeploy.json" target="_blank">
    <img src="http://armviz.io/visualizebutton.png"/>
</a>

This template allows you to create a Linux Virtual Machine which will be initialized using a remotely hosted cloud config. This template also deploys a Storage Account, Virtual Network, Public IP address, NSG, and a Network Interface. It creates two sample users, both with the password **secret**.

## Verifying the results
- Custom Data in the file `/var/lib/cloud/instance/user-data.txt`.
- Creation of a file called `/home/demo/example`
- User accounts using `cut -d: -f1 /etc/passwd`
- Web server running on port 80 (nginx) with hello world.
- Logs at `/var/log/cloud-init.log` and `/var/log/cloud-init-output.log`
