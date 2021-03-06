---
title: OID\_WDI\_SET\_END\_DWELL\_TIME
author: windows-driver-content
description: OID\_WDI\_SET\_END\_DWELL\_TIME is typically sent during an Action Frame exchange, either when WDI has to wait some time before sending a followup Action Frame, or when the protocol sequence is complete.
ms.assetid: 8ED1FDB1-BFDB-4522-8FF8-00D3B59EE43C
ms.author: windowsdriverdev 
ms.date: 0718/2017 
ms.topic: article 
ms.prod: windows-hardware 
ms.technology: windows-devices 
keywords:
 - OID_WDI_SET_END_DWELL_TIME Network Drivers Starting with Windows Vista
---

# OID\_WDI\_SET\_END\_DWELL\_TIME


OID\_WDI\_SET\_END\_DWELL\_TIME is typically sent during an Action Frame exchange, either when WDI has to wait some time before sending a followup Action Frame, or when the protocol sequence is complete. This command can be sent on the device port or station port.

| Scope | Set serialized with task | Normal execution time (seconds) |
|-------|--------------------------|---------------------------------|
| Port  | No                       | 1                               |

 

On receipt of this command, the firmware can choose to stop dwelling on the channel that had been specified when WDI sent the command to send the Action Frame. If the Dwell Time had already expired, the firmware should ignore this command.

## Set property parameters


No additional parameters. The data in the header is sufficient.
## Set property results


No additional data. The data in the header is sufficient.
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

 

 


--------------------
[Send comments about this topic to Microsoft](mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback%20%5Bnetvista\netvista%5D:%20OID_WDI_SET_END_DWELL_TIME%20%20RELEASE:%20%286/30/2017%29&body=%0A%0APRIVACY%20STATEMENT%0A%0AWe%20use%20your%20feedback%20to%20improve%20the%20documentation.%20We%20don't%20use%20your%20email%20address%20for%20any%20other%20purpose,%20and%20we'll%20remove%20your%20email%20address%20from%20our%20system%20after%20the%20issue%20that%20you're%20reporting%20is%20fixed.%20While%20we're%20working%20to%20fix%20this%20issue,%20we%20might%20send%20you%20an%20email%20message%20to%20ask%20for%20more%20info.%20Later,%20we%20might%20also%20send%20you%20an%20email%20message%20to%20let%20you%20know%20that%20we've%20addressed%20your%20feedback.%0A%0AFor%20more%20info%20about%20Microsoft's%20privacy%20policy,%20see%20http://privacy.microsoft.com/default.aspx. "Send comments about this topic to Microsoft")


