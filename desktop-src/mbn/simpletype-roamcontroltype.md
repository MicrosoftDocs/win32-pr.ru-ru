---
description: Описывает, как профиль управляет перемещением.
MS-HAID: WWAN\_profile\_v4.simpleType\_roamControlType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Простой тип Роамконтролтипе
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19243625c07afae49011638a37734a5515e626d6
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480240"
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


| Значение | Описание | 
|-------|-------------|
| аллроамалловед | <p>Роуминг разрешен в сетях партнера и других партнеров.</p> | 
| партнерроамалловед | <p>Роуминг разрешен только в партнерских сетях.</p> | 
| нороамалловед | <p>Роуминг не разрешен.</p> | 


 

 



