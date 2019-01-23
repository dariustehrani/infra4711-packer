# infra4711-packer
base image for azure based on ubuntu 18.04 LTS.

# status
[![Build status](https://dev.azure.com/datehran/packer4711/_apis/build/status/packer4711-CI)](https://dev.azure.com/datehran/packer4711/_build/latest?definitionId=3)

# prerequisites
* Azure Account set up
* for non-exploratory use make sure to used managed service identities. TODO LINK
* set up env vars see .packer_profile.sample TODO LINK

# usage
* customize the ubuntu1804.json according to your needs.
* packer validate ubuntu1804.json
* packer run ubuntu1804.json

## changing region and/or location
lookup the corresponding azure source images in your region e.g.
```
az vm image list --all -p Canonical -f UbuntuServer -s 18.04-LTS --location westeurope --all --output table
```

# helpful resources

# bootstrapping packer on azure
https://github.com/hashicorp/packer/blob/master/contrib/azure-setup.sh


