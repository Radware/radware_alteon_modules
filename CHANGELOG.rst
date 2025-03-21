====================================
Radware.Radware_Alteon Release Notes
====================================

.. contents:: Topics

v1.1.4
======

Bugfixes
--------

- fix AL-149430 | fixed apply - to accept successWithWarning

Release Summary
---------------
 
Alteon SDK 0.15b1. Tested with Alteon versions 32.4.22.0, 32.6.20.0, 33.0.16.0, 33.5.12.0, 34.0.8.0 and 34.5.3.0.


v1.1.3
======

Bugfixes
--------

- fix AL-154603 | update Ansible-core minimum version
- fix AL-145193 | update README according to RH template
- fix AL-144639 | fix new ansible-core 2.16.0 sanity failures

Release Summary
---------------

Alteon SDK 0.14b1. Tested with Alteon versions 32.4.17.0, 32.6.15.0, 33.0.12.0, 33.5.7.0, and 34.0.3.0.


v1.1.2
======

Release Summary
---------------

Alteon SDK 0.14b1. Tested with Alteon versions 32.4.17.0, 32.6.15.0, 33.0.12.0, 33.5.7.0, and 34.0.3.0.

v1.1.1
======

Release Summary
---------------

Alteon SDK 0.14b1. Tested with Alteon versions 32.4.17.0, 32.6.15.0, 33.0.12.0, 33.5.7.0, and 34.0.3.0.

v1.1.0
======

Minor Changes
-------------

- AL-13206 - add option to configure hname for virtual service.
- AL-140865 - add examples to the collection.

Bugfixes
--------

- fix AL-141408 - Module alteon_config_ha_config_sync - incorrect parameters in sync_peer state.
- fix AL-141799 - Module alteon_software_vadc_default is not working on certified collection.
- fix lint errors.

New Modules
-----------

- radware.radware_alteon.alteon_config_secure_path_policy - create and manage secure path policy in Radware Alteon
- radware.radware_alteon.alteon_config_security_global - Manage security global parameters in Radware Alteon
- radware.radware_alteon.alteon_config_sideband_policy - create and manage sideband policy in Radware Alteon

v1.0.2
======

Minor Changes
-------------

- Add ansible lint to CI pipeline

v1.0.1
======

Minor Changes
-------------

- Fix as needed for ansible lint

v1.0.0
======

Major Changes
-------------

- Add initial modules
