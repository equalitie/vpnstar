vpnstar
=======

ansible recipe for star-toplogy connected VPN servers offering a shared internal network along with external connectivity.

The internal server runs Redmine and Samba as demonstration services.

requirements
--------
* python
* python-httplib2

configuration
--------
* A gpg keypair must be created (via ```gpg --gen-key```) and then exported as a binary (to a .gpg file). This is to be placed in roles/common/files/backup.gpg.
* The gpg key ID and passphrase should be stored in site.yml for install
* An ssh keypair must be created (via ```ssh-keygen```) and then installed into roles/common/files/id_rsa.backup and id_rsa.backup.pub.
* A shared secret key for the internal VPN (use ```easy-rsa``` if you're feeling lazy) must be created and copied into roles/openvpn-internal-*/files/
