..
   SPDX-License-Identifier: AGPL-3.0-or-later

   ----------------------------------------------------------------------
   Copyright © 2024, 2025  Pellegrino Prevete

   All rights reserved
   ----------------------------------------------------------------------

   This program is free software: you can redistribute it and/or modify
   it under the terms of the GNU Affero General Public License as published by
   the Free Software Foundation, either version 3 of the License, or
   (at your option) any later version.

   This program is distributed in the hope that it will be useful,
   but WITHOUT ANY WARRANTY; without even the implied warranty of
   MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
   GNU Affero General Public License for more details.

   You should have received a copy of the GNU Affero General Public License
   along with this program.  If not, see <https://www.gnu.org/licenses/>.


========================
evm-openpgp-key-publish
========================

------------------------------------------------------------------------------
Ethereum Virtual Machine-compatible network OpenPGP Key Server keys publisher
------------------------------------------------------------------------------
:Version: evm-contract-call |version|
:Manual section: 1

Synopsis
========

evm-openpgp-key-publish *[options]* *address* *key* ( -H *gnupg_home* -f *fingerprint* )

Description
===========

Publishes Ethereum Virtual Machine (EVM) compatible
networks' external owner accounts (EOAs) associated
OpenPGP keys produced with EVM GNUPG on
the EVM OpenPGP Key Server.

It uses EVM Contracts Tools to perform contract
operations and main EVMFS implementation to upload
the keys on the chain.

Arguments
===========

* *address* *key* 



Networks
=========
All those supported by
'evm-chains-info' as
well as direct RPC addresses.

Options
=======

-H gnupg_home           GnuPG configuration directory.
-t input_type           It can be 'file', 'fingerprint' or
                        'evmfs'.
-S                      If enabled it won't upload the
                        key file to the EVMfs.


Contract options
===================

-A ks_address           Address of the EVM OpenPGP Key Server
                        on the network.
-V ks_version           Version of the target EVM OpenPGP Key
                        Server.


LibEVM options
================

-u                      Whether to retrieve key server
                        address from user directory or from
                        a custom deployment.
-d deployments_dir      Contracts deployments directory.
-n network              EVM network name.


Credentials options
======================

-N wallet_name          Wallet name.
-w wallet_path          Wallet path.
-p wallet_password      Wallet password.
-s wallet_seed          Wallet seed path.
-k api_key              Etherscan-like service key.


Applications options
=======================

-C cache_dir            Work directory

-h                      Display help.
-c                      Enable color output
-v                      Enable verbose output

Bugs
====

https://github.com/themartiancompany/evm-openpgp-keyserver/-/issues

Copyright
=========

Copyright Pellegrino Prevete. AGPL-3.0.

See also
========

* evm-openpgp-key-publish
* evm-gpg
* evm-gpg-decrypt
* evm-gpg-key-address-check
* evm-gpg-signature-verify
* evm-wallet
* evm-contract-call
* libevm
* gpg-key-info
* gpg-signature-info
* gpg-signature-verify


.. include:: variables.rst
