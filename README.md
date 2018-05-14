#Supported tags and respective Dockerfile links

- [`0.1.0`, `0.1.0` (*0.1.0/Dockerfile*)](https://github.com/Accenture/adop-ldap-ltb/blob/master/Dockerfile)

# What is ldap-ltb?

ldap-ltb is a wrapper for the LDAP Tool Box (LTB) Self Service Password utility, 
which is a PHP application that allows users to change their password in an LDAP directory. 

# How to use this image

The easiest for to run ldap-ltb image is as follow:
```
      $ docker run --name=<your-container-name> -dt \
        -e LDAP_LTB_URL="<your-ldap-url>" \
        -e LDAP_LTB_PWD="<your-ldap-admin-password>" \
        --net=<your-network-name> \
        accenture/adop-ldap-ltb:VERSION
```
after the above ldap-ltb will be available at: http://ldap-ltb
        
# Configuration

The service configuration is externalised and stored the 'assets' directory.

Runtime configuration can be provided using environment variables:

* LDAP_LTB_URL, the LDAP URI, i.e. ldap-host:389
* LDAP_LTB_BS, the LDAP user BASE_DN
* LDAP_LTB_DN, the LDAP admin DN
* LDAP_LTB_PWD, the password to use connecting to LDAP service

Note : Default password policies is setup with following rules -

* Minimum length: 9
* Maximum length: no limit
* Minimum number of lowercase characters: 1
* Minimum number of uppercase characters: 1
* Minimum number of digits: 1
* Minimum number of special characters: 1
* Your new password can not be the same as your old password

# License
 Please view [licence information](LICENCE.md) for the software contained on this image.

#Supported Docker versions

This image is officially supported on Docker version 1.9.1.

# User feedback

## Documentation
Documentation for this image is available in the [LDAP Tool Box page](http://ltb-project.org/wiki/documentation/self-service-password). 
Additional documentaion can be found under the [`docker-library/docs` GitHub repo](https://github.com/docker-library/docs). Be sure to familiarize yourself with the [repository's `README.md` file](https://github.com/docker-library/docs/blob/master/README.md) before attempting a pull request.

## Issues
If you have any problems with or questions about this image, please contact us through a [GitHub issue](https://github.com/Accenture/ldap-ltb/issues).

## Contribute
You are invited to contribute new features, fixes, or updates, large or small; we are always thrilled to receive pull requests, and do our best to process them as fast as we can.

Before you start to code, we recommend discussing your plans through a [GitHub issue](https://github.com/Accenture/ldap-ltb/issues), especially for more ambitious contributions. This gives other contributors a chance to point you in the right direction, give you feedback on your design, and help you find out if someone else is working on the same thing.
