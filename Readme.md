I opened a terminal or command prompt and executed the following command to create a static public IP address:

```
az network public-ip create --resource-group 1-afc99f53-playground-sandbox --name httbin-ip --sku Standard --allocation-method static
```

After the IP address is created,   I executed the following command to retrieve the IP address:

az network public-ip show --resource-group 1-afc99f53-playground-sandbox --name httbin-ip --query ipAddress --output tsv

Once I had the IP address, I deployed the httbin Helm chart to the AKS cluster. I executed the following command to deploy the chart

```
helm install httbin stable/httbin --set service.type=LoadBalancer --set service.loadBalancerIP=20.84.87.227
```

