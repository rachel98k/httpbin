az network public-ip create --resource-group 1-afc99f53-playground-sandbox --name httbin-ip --sku Standard --allocation-method static



az network public-ip show --resource-group 1-afc99f53-playground-sandbox --name httbin-ip --query ipAddress --output tsv


