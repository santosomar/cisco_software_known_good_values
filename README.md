# Cisco Software Known Good Values 
In order to provide a level of security integrity, Cisco devices must be verified as running authentic and valid software. Currently, Cisco devices in the field have no point of reference to determine whether the software they are running is authentic Cisco software. The Cisco IV application uses a system to compare collected image integrity data to Known Good Values (KGV) for Cisco software.

Cisco produces and publishes a Known Good Value Data file that contains KGV's for many of its products. This KGV file is in standard JSON format, is signed by Cisco, and is bundled with other files into a KGV Combo Bundle that can be retrieved from Cisco.

These files can also be downloaded from: https://www.cisco.com/c/en/us/about/trust-center/downloads.html

The contents of the KGV Combo Bundle can also be used with "home grown" or customer developed scripts or applications. The KGV values are standard JSON objects and elements and can be used by any software that can parse JSON data.

The current Cisco produced KGV Data File includes measurements for the following component categories:

* Boot Integrity Visibility
* Boot0 image measurements
* Bootloader image measurements
* Boot OS image measurements
* Running image file measurements

** Important: **
Always verify the signature of the KGV data before using the contents to assign integrity to your network elements. If the signature on the KGV data can not be verified, then the contents of the KGV data can not be trusted.

Cisco's Integrity Verification application verifies the signature on the KGV data automatically, but any "home grown" or customized scripts would need to implement this step prior to using the KGV Combo Bundle data.
