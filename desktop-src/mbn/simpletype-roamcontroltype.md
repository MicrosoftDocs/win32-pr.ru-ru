---
description: Описывает, как профиль управляет перемещением.
MS-HAID: WWAN\_profile\_v4.simpleType\_roamControlType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Простой тип Роамконтролтипе
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 911e379773e7d8eabfb7a1524b1a21ba16718a53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701619"
---
# <a name="span-idwwan_profile_v4simpletype_roamcontroltypespanroamcontroltype-simple-type"></a><span id="WWAN_profile_v4.simpleType_roamControlType"></span>Простой тип Роамконтролтипе

Описывает, как профиль управляет перемещением.

Существует два возможных состояния регистрации роуминга:

-   Партнер: Зарегистрирован в сети, тесно связанной с домашней сетью
-   Не партнер: Зарегистрирован в сети, которая не тесно связана с домашней сетью

Точное значение "Partner" зависит от сети, но оно представляет более близкую связь с более выгодными тарифами, чем у другого партнера. Это может быть, если у оператора, основанного на регионе, есть бизнес-трансляция для использования радио доступа другого оператора за пределами своей домашней области. Он также может представлять разницу между перемещением в пределах региона (например, ЕС) и за его пределами.

Обратите внимание, что [**роамаппликабилититипе**](simpletype-roamapplicabilitytype.md) является более выразительным атрибутом, чем **роамконтролтипе**, и профиль должен использовать либо **роамконтролтипе** , либо **роамаппликабилититипе**, но не оба. (Если профиль использует оба значения, применяются оба. Результатом является пересечение двух.)

``` syntax
<xs:simpleType name="roamControlType">
    <xs:restriction>
        <xs:enumeration
            value="AllRoamAllowed"
         />
        <xs:enumeration
            value="PartnerRoamAllowed"
         />
        <xs:enumeration
            value="NoRoamAllowed"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a>Значения перечисления

Простой тип **роамконтролтипе** определяет следующие значения.

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
<td>аллроамалловед</td>
<td><p>Роуминг разрешен в сетях партнера и других партнеров.</p></td>
</tr>
<tr class="even">
<td>партнерроамалловед</td>
<td><p>Роуминг разрешен только в партнерских сетях.</p></td>
</tr>
<tr class="odd">
<td>нороамалловед</td>
<td><p>Роуминг не разрешен.</p></td>
</tr>
</tbody>
</table>

 

 



