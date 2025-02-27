.. _sj2088poe:

OAK-D-PoE
=========

.. image:: /_static/images/SJ2088POE/oak-d-poe_2.png

Overview
********

The OAK-D-PoE baseboard offers full 802.3af, Class 3 PoE compliance with 1000BASE-T speeds. The OAK-D-POE baseboard has three on-board 
cameras which implement stereo and RGB vision, piped directly into the DepthAI SoM for depth and AI processing. The data is then output 
to a host via USB 3.1 Gen1 (Type-C) or via 1000BASE-T ethernet connection. Ther OAK-D-POE board exposes boot selection switches, allowing 
the end user to boot the :ref:`OAK-SoM-Pro <bw2099>` module from USB or the on-board eMMC or NOR flash.

Board Layout
************

.. image:: /_static/images/SJ2088POE/SJ2088POE_b.jpg
.. image:: /_static/images/SJ2088POE/SJ2088POE_dim.jpg

Dimensions and Weight
*********************
* Width: 130 mm
* Height: 101 mm
* Length: 31 mm
* Weight: 361g

.. image:: /_static/images/SJ2088POE/OAK-D-PoE-dimensions.svg

Key features
************

* Fully compatible with all :ref:`OAK-D <bw1098oak>` features
* :ref:`IP67 rated <IP67 rated PoE enclosures>` enclosure compatible with standard tripod mount (1/4"-20)
* Interface for OAK-SoM-Pro
* USB 3.1 Gen1 Type-C
* Power-over-Ethernet (PoE) power source
* 1000BASE-T ethernet for data
* Header access for OAK-SoM-Pro 1.8V Aux Signals (I2C, , Module Reset)
* Micro SD connector for DepthAI SoM 3.3V SDIO
* On-board PCIe ref clk for OAK-SoM-Pro and PCIe/Ethernet bridge
* User-selectable OAK-SoM-Pro boot configuration switches
* Design files produced with Altium Designer 20
* :ref:`PoE injector <Powering PoE devices>` is required to power the device.


.. image:: /_static/images/SJ2088POE/OAK-POE_cameras.jpg

Minimal and maximal perceiving distances of the camera
******************************************************

Minimal depth perceiving distance of the camera depends on mono camera FOV, resolution, baseline and stereo depth mode, more info is available on the `Stereo Depth documentation <https://docs.luxonis.com/projects/api/en/latest/components/nodes/stereo_depth/#min-stereo-depth-distance>`__.

OAK-D-PoE has a baseline of 7.5cm and by varying the resolution and stereo depth mode, we get the following minimal depth perceiving distances:

- Min distance (800P): ~ 70cm
- Min distance (400P): ~ 35cm
- Min distance with extended disparity (800P): ~ 35cm
- Min distance with extended disparity (400P): ~ 19.6cm

Maximal perceiving distance for OAK-D-PoE: 38.4 meters

For more information about the maximum distance see the `Stereo Depth documentation <https://docs.luxonis.com/projects/api/en/latest/components/nodes/stereo_depth/#max-stereo-depth-distance>`__.

Power usage
***********

Power usage for OAK-D-PoE ranges between 2.00 W (standby) and 5.5 W (max consumption). More information on the power usage is below:

* Standby: 2.00 W
* Normal operation (running :code:`python depthai_demo.py`): 5.25 W
* Max consumption power (running :code:`python depthai_demo.py -s left right color disparity rectified_left depth`): 5.50 W

.. image:: /_static/images/SJ2088POE/OAK-D-PoE-power-usage.jpeg

Getting started
***************

.. note:: 
    For more information on how to start with POE devices, check our guide `Getting started with PoE <https://docs.luxonis.com/en/latest/pages/tutorials/getting-started-with-poe/>`__.


The OAK-D-POE accepts power input from any 802.3af, Class 3 PoE circuitry. So this for example includes any/every PoE UniFi Switch 
(e.g. US-8-150W) and any other standard POE switch and/or 802.3af PoE injector. Power consumption is typically 5W, 
leaving ~7.5W available if active lighting is desired additionally over PoE/etc.

If an outdoor rated PoE switch is needed, one option is the EP-S16.

Interfacing with the OAK-SoM-Pro is also possible with :ref:`PoE board <bw2096poe>` connector pads J5 which expose :ref:`OAK-SoM-Pro <bw2099>` auxiliary I/O. This header 
is Amphenol/FCI 20021121-00010T1LF or equivalent. Please refer to the schematics for pinout information.

The reset button resets the OAK-SoM-Pro only.
The 5V LED indicates 5V power is present on the PoE Board.
The PG LED indicates "power good" from the OAK-SoM-Pro.
The "RUN" LED indicates that the OAK-SoM-Pro is not in reset.

**Caution should be taken when handling any PoE circuit board. Do not directly touch the circuitry as potentials upto and exceeding 
57V may exist. Always use electronics handling best practices.**

.. image:: /_static/images/SJ2088POE/oak-d-poe.png

Datasheets
**********

* `Assembly Drawing <https://github.com/luxonis/depthai-hardware/blob/master/SJ2088POE_PoE_Board/Docs/Assembly%20Drawing%20PDF/Production.PDF>`__
* `Assembly Outputs <https://github.com/luxonis/depthai-hardware/tree/master/SJ2088POE_PoE_Board/Docs/Assembly%20Outputs>`__
* `Fabrication Drawing <https://github.com/luxonis/depthai-hardware/blob/master/SJ2088POE_PoE_Board/Docs/Fabrication%20Drawing%20PDF/Production.PDF>`__
* `Fabrication Outputs <https://github.com/luxonis/depthai-hardware/tree/master/SJ2088POE_PoE_Board/Docs/Fabrication%20Outputs>`__
* `Schematic <https://github.com/luxonis/depthai-hardware/tree/master/SJ2088POE_PoE_Board/Docs/Schematic%20PDF>`__

Altium Design Files
*******************

See files `here <https://github.com/luxonis/depthai-hardware/tree/master/SJ2088POE_PoE_Board/PCB>`__

3D Models
*********

Download `here <https://github.com/luxonis/depthai-hardware/tree/master/SJ2088POE_PoE_Board/3D_Models>`__


.. include::  /pages/includes/footer-short.rst
