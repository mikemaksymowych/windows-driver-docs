---
title: NDIS\_STATUS\_WDI\_INDICATION\_ASSOCIATION\_PARAMETERS\_REQUEST
author: windows-driver-content
description: Miniport drivers use NDIS\_STATUS\_WDI\_INDICATION\_ASSOCIATION\_PARAMETERS\_REQUEST to request association parameters for a set of BSSIDs from the host.
ms.assetid: 2c8aef86-bb4a-47c6-a839-eb14eb430a31
ms.author: windowsdriverdev 
ms.date: 0718/2017 
ms.topic: article 
ms.prod: windows-hardware 
ms.technology: windows-devices 
keywords:
 - NDIS_STATUS_WDI_INDICATION_ASSOCIATION_PARAMETERS_REQUEST Network Drivers Starting with Windows Vista
---

# NDIS\_STATUS\_WDI\_INDICATION\_ASSOCIATION\_PARAMETERS\_REQUEST


Miniport drivers use NDIS\_STATUS\_WDI\_INDICATION\_ASSOCIATION\_PARAMETERS\_REQUEST to request association parameters for a set of BSSIDs from the host.

| Object |
|--------|
| Port   |

 

This indication can be sent by the adapter when it finds a BSS entry that is a candidate for association based on the current settings. Upon receiving this indication, the host checks if the association parameters are available, and if so, sends them with [OID\_WDI\_SET\_ASSOCIATION\_PARAMETERS](oid-wdi-set-association-parameters.md).

## Payload data


| Type                                                                                                             | Multiple TLV instances allowed | Optional | Description                                   |
|------------------------------------------------------------------------------------------------------------------|--------------------------------|----------|-----------------------------------------------|
| [**WDI\_TLV\_ASSOCIATION\_PARAMETERS\_REQUESTED\_TYPE**](https://msdn.microsoft.com/library/windows/hardware/dn926131) |                                |          | The list of requested association parameters. |
| [**WDI\_TLV\_BSS\_ENTRY**](https://msdn.microsoft.com/library/windows/hardware/dn926162)                                                           | X                              | X        | The list of BSSIDs.                           |

 

Requirements
------------

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Minimum supported client</p></td>
<td><p>Windows 10</p></td>
</tr>
<tr class="even">
<td><p>Minimum supported server</p></td>
<td><p>Windows Server 2016</p></td>
</tr>
<tr class="odd">
<td><p>Header</p></td>
<td>Dot11wdi.h</td>
</tr>
</tbody>
</table>

## See also


[OID\_WDI\_TASK\_CONNECT](oid-wdi-task-connect.md)

 

 


--------------------
[Send comments about this topic to Microsoft](mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback%20%5Bnetvista\netvista%5D:%20NDIS_STATUS_WDI_INDICATION_ASSOCIATION_PARAMETERS_REQUEST%20%20RELEASE:%20%286/30/2017%29&body=%0A%0APRIVACY%20STATEMENT%0A%0AWe%20use%20your%20feedback%20to%20improve%20the%20documentation.%20We%20don't%20use%20your%20email%20address%20for%20any%20other%20purpose,%20and%20we'll%20remove%20your%20email%20address%20from%20our%20system%20after%20the%20issue%20that%20you're%20reporting%20is%20fixed.%20While%20we're%20working%20to%20fix%20this%20issue,%20we%20might%20send%20you%20an%20email%20message%20to%20ask%20for%20more%20info.%20Later,%20we%20might%20also%20send%20you%20an%20email%20message%20to%20let%20you%20know%20that%20we've%20addressed%20your%20feedback.%0A%0AFor%20more%20info%20about%20Microsoft's%20privacy%20policy,%20see%20http://privacy.microsoft.com/default.aspx. "Send comments about this topic to Microsoft")


