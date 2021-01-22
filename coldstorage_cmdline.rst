Using cold storage with the command line
========================================

This page will show you how to sign a transaction with
an offline Electron Cash wallet, using the command line.

Create an unsigned transaction
------------------------------

With your online (watching-only) wallet, create an
unsigned transaction:

.. code-block:: bash

   electron-cash payto 1Cpf9zb5Rm5Z5qmmGezn6ERxFWvwuZ6UCx 0.1 --unsigned > unsigned.txn

The unsigned transaction is stored in a file named 'unsigned.txn'.
Note that the --unsigned option is not needed if you use a
watching-only wallet.

You may view it using:

.. code-block:: bash

   cat unsigned.txn | electron-cash deserialize -

Sign the transaction
--------------------

The serialization format of Electron Cash contains the master
public key needed and key derivation, used by the offline
wallet to sign the transaction.

Thus we only need to pass the serialized transaction to
the offline wallet:

.. code-block:: bash

   cat unsigned.txn | electron-cash signtransaction - > signed.txn

The command will ask for your password, and save the
signed transaction in 'signed.txn'

Broadcast the transaction
-------------------------

Send your transaction to the Bitcoin Cash network, using broadcast:

.. code-block:: bash

   cat signed.txn | electron-cash broadcast -

If successful, the command will return the ID of the
transaction.
