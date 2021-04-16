---
description: Перечисление, описывающее тип сетевого подключения, к которому применим профиль.
MS-HAID: WWAN\_profile\_v4.simpleType\_iwlanApplicabilityType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Простой тип Ивланаппликабилититипе
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80013fa21574221de24a7fc8309e4459a80ad670
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542178"
---
# <a name="span-idwwan_profile_v4simpletype_iwlanapplicabilitytypespaniwlanapplicabilitytype-simple-type"></a><span id="WWAN_profile_v4.simpleType_iwlanApplicabilityType"></span>Простой тип Ивланаппликабилититипе

Перечисление, описывающее тип сетевого подключения, к которому применим профиль.

``` syntax
<xs:simpleType name="iwlanApplicabilityType">
    <xs:restriction
        base="token"
    >
        <xs:enumeration
            value="CellularOnly"
         />
        <xs:enumeration
            value="CellularAndIwlan"
         />
        <xs:enumeration
            value="IwlanOnly"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a>Значения перечисления

Простой тип **ивланаппликабилититипе** определяет следующие значения.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Значение</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>целлуларонли</td>
<td><p>Профиль действителен только для подключений по сотовой сети.</p></td>
</tr>
<tr class="even">
<td>целлуларандивлан</td>
<td><p>Профиль действителен для сотовой сети или Wi-Fi разгрузки подключений.</p></td>
</tr>
<tr class="odd">
<td>ивланонли</td>
<td><p>Профиль действителен только для Wi-Fi разгрузок подключений.</p></td>
</tr>
</tbody>
</table>

 

 



