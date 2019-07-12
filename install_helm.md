#### Setting up the Helm CLI


	docker run -t --entrypoint=/bin/cp -v /usr/local/bin:/data ibmcom/helm:v2.4.1  /helm /data/

	mkdir -p /var/lib/helm; export HELM_HOME=/var/lib/helm

	helm init --client-only


#### Helm verification


	helm version
	
	helm list
	
	
	
### Reference

https://www.ibm.com/support/knowledgecenter/en/SSBS6K_1.2.0/app_center/create_helm_cli.html