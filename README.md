# oqsprovider Binaries

GitHub Action to compile https://github.com/open-quantum-safe/oqs-provider

## Install

	cp oqsprovider.so /usr/lib/*/ossl-modules/

In `/etc/ssl/openssl.cnf` add in `[provider_sect]` section:

	oqsprovider = oqs_sect

Uncomment `activate = 1` in `[default_sect]` section and add below:

	[oqs_sect]
	activate = 1

Also see: https://github.com/openssl/openssl/blob/master/README-PROVIDERS.md#loading-providers
