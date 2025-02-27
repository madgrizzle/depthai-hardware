.. _bw1098ffc:

OAK-FFC-3P-OG
=============

.. image:: /_static/images/BW1098FFC/BW1098FFC_front.jpg

Overview
********

The OAK-FFC-3P-OG (BW1098FFC) baseboard has three FFC interfaces which allow for two :ref:`OAK-FFC-OV9282 <bg0250tg>` camera modules (stereo pair) 
and one :ref:`OAK-FFC-IMX378 <bg0249>` RGB camera module. This board can also be used with adapters for the Raspberry Pi HQ Camera, using 
the :ref:`Raspberry Pi Adapter Board <bw0253>`.

Baseboards and cameras (BW1098FFC + :ref:`OAK-FFC-OV9282 <bg0250tg>` + :ref:`OAK-FFC-IMX378 <bg0249>`) together:

.. image:: /_static/images/BW1098FFC/with_camera.jpeg

Board Layout
************

.. image:: /_static/images/BW1098FFC/BW1098FFC_diag.jpg

Dimensions and Weight
*********************

* Width: 60 mm
* Height: 40 mm
* Length: 20.5 mm
* Weight: 40g

.. image:: /_static/images/BW1098FFC/BW1098FFC_dims.jpg

Key features
************

* 2 OAK-FFC-OV9282 mono camera module interfaces
* 1 OAK-FFC-IMX378 RGB camera module interface
* 5V power input via barrel jack
* USB 3.1 Gen 1 Type-C
* Pads for DepthAI SoM 1.8V SPI
* Pads for DepthAI SoM 3.3V SDIO
* Pads for DepthAI SoM 1.8V Aux Signals (I2C, UART, GPIO)
* 5V Fan/Aux header
* Pads for DepthAI SoM aux signals
* Design files produced with Altium Designer 20

Minimal and maximal perceiving distances of the camera
******************************************************

Minimal depth perceiving distance of the camera depends on mono camera FOV, resolution, baseline and stereo depth mode, more info is available on the `Stereo Depth documentation <https://docs.luxonis.com/projects/api/en/latest/components/nodes/stereo_depth/#min-stereo-depth-distance>`__.

Since OAK-FFC-3P-OG has modular mono cameras, it also has a custom baseline (depending on how it is set up). The formulas for minimal depth perceiving distances are:

- Min distance (800P) = :code:`882.5 * baseline / 95`
- Min distance (400P) = :code:`441.25 * baseline / 95`
- Min distance with extended disparity (800P) = :code:`882.5 * baseline / 190`
- Min distance with extended disparity (400P) = :code:`max(441.25 * baseline / 190, 19.6)`

Maximal perceiving distance for OAK-FFC-3P-OG = :code:`baseline/2 * tan((90 - 71.9/1280) * PI/180)`

For more information about the maximum distance see the `Stereo Depth documentation <https://docs.luxonis.com/projects/api/en/latest/components/nodes/stereo_depth/#max-stereo-depth-distance>`__.

Getting started
***************

The OAK-FFC-3P-OG accepts 5V (+/-10%) from a 5.5m x 2.5mm barrel jack, and interfaces to a host via USB 3.1 Gen1 Type-C. With cameras and 
the :ref:`OAK-SoM <bw1099>`, total power consumption usually stays below the 900ma specification of USB 3, but Type-C power of 1.5A or greater is recommended.

Interfacing with the OAK-SoM is also possible with OAK-FFC-3P-OG connector pads J3, J4, and J5. These pads are designed for the Amphenol/FCI 
20021121-00010T1LF or equivalent. Please refer to the schematics for pinout information.

The reset button resets the OAK-SoM only.

The 5V LED indicates 5V power is present on the OAK-FFC-3P-OG. The PG LED indicates "power good" from the OAK-SoM. The "RUN" LED indicates 
that the OAK-SoM is not in reset.

Datasheets
**********

* `Assembly Drawing <https://github.com/luxonis/depthai-hardware/blob/master/BW1098FFC_DepthAI_USB3/Docs/Assembly%20Drawing%20PDF/Production.PDF>`__
* `Assembly Outputs <https://github.com/luxonis/depthai-hardware/tree/master/BW1098FFC_DepthAI_USB3/Docs/Assembly%20Outputs>`__
* `Fabrication Drawing <https://github.com/luxonis/depthai-hardware/blob/master/BW1098FFC_DepthAI_USB3/Docs/Fabrication%20Drawing%20PDF/Production.PDF>`__
* `Fabrication Outputs <https://github.com/luxonis/depthai-hardware/tree/master/BW1098FFC_DepthAI_USB3/Docs/Fabrication%20Outputs>`__
* `Schematic <https://github.com/luxonis/depthai-hardware/blob/master/BW1098FFC_DepthAI_USB3/Docs/Schematic%20PDF/Production.PDF>`__

Altium Design Files
*******************

See files `here <https://github.com/luxonis/depthai-hardware/tree/master/BW1098FFC_DepthAI_USB3/PCB>`__

3D Models
*********

Download `here <https://github.com/luxonis/depthai-hardware/tree/master/BW1098FFC_DepthAI_USB3/3D_Models>`__

Brochures
*********

* `Brochure <https://github.com/luxonis/depthai-hardware/blob/master/BW1098FFC_DepthAI_USB3/BW1098FFC_Datasheet.pdf>`__

.. include::  /pages/includes/footer-short.rst
