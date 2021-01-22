Downloading and Verifying Electron Cash
========================================

**IMPORTANT: it is vital that you only use information and downloads from https://electroncash.org**

Android
-------
Install the app from the `PlayStore <https://play.google.com/store/apps/details?id=org.electroncash.electroncash3>`_.

The PlayStore has verification of downloads built into the system, no verification is needed.

Linux
-----

- retrieve Jonald's public key from his repo. You only need to do this once but it is recommended to insure that you
  are installing an original version of electron cash.

  - ``wget "https://github.com/fyookball/keys-n-hashes/raw/master/pubkeys/jonaldkey2.txt"``
  - ``gpg --import jonaldkey2.txt``

- Download the latest version from https://electroncash.org. You need the ``tar.gz`` file, such as ``ElectronCash-3.1.2.tar.gz``
- Download the correct signature and checksum files from https://github.com/fyookball/keys-n-hashes/tree/master/sigs-and-sums
- Verify the download

  - ``sha256sum -c SHA256.ElectronCash-3.1.2.tar.gz.txt``
  - ``gpg --verify ElectronCash-3.1.2.tar.gz.sig``
