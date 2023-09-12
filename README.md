NTPSec Client
=============

This role sets up time synchronization using NTPSec.
It uses NTS to ensure secure time synchronization.

Requirements
------------

NTS was implemented in NTPSec 1.1.4. Since this role uses the package management to install NTPSec, the target system's distribution needs to provide at least NTPSec 1.1.4.
Furthermore, it need to provide at least OpenSSL 1.1, since NTS requires TLSv1.3, which is not supported by older version of OpenSSL.

Role Variables
--------------

* `ntpsec_client_servers`  
  A list of servers to synchronize with.
  The servers need to support NTS.
  Defaults to `time.cloudflare.com`.

License
-------

MIT
