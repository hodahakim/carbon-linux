# Vanilla Debian Packer templates

The templates here are used to create the Debian Vagrant base boxes available at 
https://app.vagrantup.com/debian

## Direct Download

	vagrant init debian/jessie64
	vagrant init debian/wheezy64

## Rebuilding the base boxes
See https://wiki.debian.org/Teams/Cloud/RebuildVagrantBaseBoxes

## Releasing a new minor version:
* export VAGRANT_CLOUD_TOKEN=$(gpg --decrypt ../helpers/token.gpg)
* Call `make ${CODENAME}.uploaded` to build the box, sign the box, upload and release the box on 
  app.vagrantup.com
* Commit the new checksums and changelog, push to salsa


## Credits

  Many thanks to [Mitchell Hashimoto](https://github.com/mitchellh/) for his awesome work on [Packer](https://github.com/mitchellh/packer) and [Vagrant](https://github.com/mitchellh/vagrant), [![Tech-Angels](http://media.tumblr.com/tumblr_m5ay3bQiER1qa44ov.png)](http://www.tech-angels.com)

  
