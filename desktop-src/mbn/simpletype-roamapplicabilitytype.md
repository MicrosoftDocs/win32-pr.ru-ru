---
description: Роамаппликабилититипе описывает условия роуминга, для которых применяется перемещаемый профиль.
MS-HAID: WWAN\_profile\_v4.simpleType\_roamApplicabilityType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Простой тип Роамаппликабилититипе
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95d81214ab5a44dcac60bb5e1a6accc81b0d0418
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897273"
---
# <a name="span-idwwan_profile_v4simpletype_roamapplicabilitytypespanroamapplicabilitytype-simple-type"></a><span id="WWAN_profile_v4.simpleType_roamApplicabilityType"></span>Простой тип Роамаппликабилититипе

Роамаппликабилититипе описывает условия роуминга, для которых применяется перемещаемый профиль.

Это более выразительный атрибут, чем [**роамконтролтипе**](simpletype-roamcontroltype.md), и профиль должен использовать либо **Роамконтролтипе** , либо **роамаппликабилититипе**, но не оба. (Если профиль использует оба значения, применяются оба. Результатом является пересечение двух.)

Этот атрибут используется для различения нескольких профилей с несвязанными условиями роуминга для указания различных атрибутов профиля для, например домашних и перемещаемых.

Существует три возможных состояния регистрации домашних и перемещаемых компьютеров:

-   Главная: зарегистрировано в домашней сети
-   Партнер: Зарегистрирован в сети, тесно связанной с домашней сетью
-   Не партнер: Зарегистрирован в сети, которая не тесно связана с домашней сетью

Точное значение "Partner" зависит от сети, но оно представляет более близкую связь с более выгодными тарифами, чем у другого партнера. Это может быть, если у оператора, основанного на регионе, есть бизнес-трансляция для использования радио доступа другого оператора за пределами своей домашней области. Он также может представлять разницу между перемещением в пределах региона (например, ЕС) и за его пределами.

``` syntax
<xs:simpleType name="roamApplicabilityType">
    <xs:restriction
        base="token"
    >
        <xs:enumeration
            value="NonPartnerOnly"
         />
        <xs:enumeration
            value="PartnerOnly"
         />
        <xs:enumeration
            value="HomeOnly"
         />
        <xs:enumeration
            value="HomeAndPartner"
         />
        <xs:enumeration
            value="PartnerAndNonpartner"
         />
        <xs:enumeration
            value="AllRoaming"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a>Значения перечисления

Простой тип **роамаппликабилититипе** определяет следующие значения.

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
<td>нонпартнеронли</td>
<td><p>Этот профиль используется только при роуминге в сети, отличной от партнера</p></td>
</tr>
<tr class="even">
<td>партнеронли</td>
<td><p>Этот профиль используется только при роуминге в сети партнера</p></td>
</tr>
<tr class="odd">
<td>хомеонли</td>
<td><p>Этот профиль используется только в домашней сети.</p></td>
</tr>
<tr class="even">
<td>хомеандпартнер</td>
<td><p>Этот профиль используется только дома или в партнерской сети</p></td>
</tr>
<tr class="odd">
<td>партнеранднонпартнер</td>
<td><p>Этот профиль используется, если вы не дома (роуминг в любой сети)</p></td>
</tr>
<tr class="even">
<td>аллроаминг</td>
<td><p>Этот профиль используется во всех сетях</p></td>
</tr>
</tbody>
</table>

 

 



