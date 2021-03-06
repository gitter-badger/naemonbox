======================
Fusioninventory Client Installation
======================

Windows Client
=========

+ Select the version to install for your architecture :
.. image:: /images/fusioninventory-agent_windows.png
+ The installer detects the system language installed . Leave blank and click OK.
.. image:: /images/fusioninventory-agent_windows-lang.png
+ Click Next 
.. image:: /images/fusioninventory-agent_windows-1.png
+ Agree with the license terms and click Next
.. image:: /images/fusioninventory-agent_windows-2.png
+ Click Next
.. image:: /images/fusioninventory-agent_windows-3.png
+ Click Next
.. image:: /images/fusioninventory-agent_windows-4.png
+ In the field Servers Mode, enter the IP @ of GLPI server : http://your_ip_address/glpi/plugins/fusioninventory/
.. image:: /images/fusioninventory-agent_windows-6.png
+ Click Install , Next, and Close.
fusioninventory-agent_windows-7.png


ESX Client
=========
FusionInventory can contact a ESX/ESXi/vCenter serveur using the VMware SOAP API. It will identify the ESX server and the associated virtual machine. At the end, it will push XML inventory of the machines to the server. Do the following commands, as root :

.. code-block:: console

    # fusioninventory-esx --user root --password 'password' --host @IP --directory /tmp
    # fusioninventory-injector -v --file /tmp/HOSTNAME-2013-11-04-07-13-32.ocs -u http://your_ip_address/glpi/plugins/fusioninventory/

GLPI Console
=========

It does take a little bit more time, we could take a cup of coffee and then we can see the machine appear in GLPI inventory .
Some alerts depending on the criticality threshold in Naemon to automatically trigger the creation of incident tickets in GLPI .
