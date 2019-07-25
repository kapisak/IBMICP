#### Setting up the Helm CLI


	docker run -t --entrypoint=/bin/cp -v /usr/local/bin:/data ibmcom/helm:v2.4.1  /helm /data/

	mkdir -p /var/lib/helm; export HELM_HOME=/var/lib/helm

	helm init --client-only


#### Helm verification


	helm version
	
	helm list
	



## Trobleshoting 

##### How to download helm from ICP cluster

	curl -kLo helm-linux-amd64-v2.12.3.tar.gz https://10.40.41.134:8443/api/cli/helm-linux-amd64.tar.gz
	

##### Helm version shows Error: cannot connect to Tiller



	cp cluster/cfc-certs/helm/admin.crt /cert.pem

	cp cluster/cfc-certs/helm/admin.key /key.pem

	helm init --client-only

	helm version --tls

Reference : https://www-01.ibm.com/support/docview.wss?uid=ibm10728481
	
### Reference

https://www.ibm.com/support/knowledgecenter/en/SSBS6K_1.2.0/app_center/create_helm_cli.html

