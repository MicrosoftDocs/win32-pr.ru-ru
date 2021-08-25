---
description: Профилекреатионтипе (в Модемдмконфигпрофиле)
MS-HAID: WWAN\_profile\_v4.element\_1\_ProfileCreationType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Профилекреатионтипе (в Модемдмконфигпрофиле)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29867412bbadc8041bcf864a9575b0fc6001a499
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479960"
---
# <a name="span-idwwan_profile_v4element_1_profilecreationtypespanprofilecreationtype-in-modemdmconfigprofile"></a><span id="WWAN_profile_v4.element_1_ProfileCreationType"></span>Профилекреатионтипе (в Модемдмконфигпрофиле)

Указывает, каким способом был создан профиль DM для модема.

Это значение используется для принятия решения о том, может ли пользователь удалить профиль. Пользователи могут удалять только профили **усерпровисионед** .

## <a name="element-hierarchy"></a>Иерархия элементов

[<ModemDMConfigProfile>](element-modemdmconfigprofile.md)  
**<ProfileCreationType>**

## <a name="syntax"></a>Синтаксис

``` syntax
<ProfileCreationType>

  "UserProvisioned" | "AdminProvisioned" | "OperatorProvisioned" | "DeviceProvisioned"

</ProfileCreationType>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Атрибуты и элементы

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>Атрибуты

Нет.

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Дочерние элементы

Нет.

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Родительские элементы


| Родительский элемент | Описание | 
|----------------|-------------|
| <a href="element-modemdmconfigprofile.md">ModemDMConfigProfile</a> | <p>Профиль конфигурации DM для модема.</p> | 


 

## <a name="related-elements"></a>Связанные элементы

Следующие элементы имеют то же имя, что и это одно, но различное содержимое или атрибуты:

-   **[Профилекреатионтипе (в Мбнпрофиликст)](element-profilecreationtype.md)**

## <a name="requirements"></a>Требования


| | | <p>Пространство имен</p> | <p>https://www.microsoft.com/networking/WWAN/profile/v4</p> | 


 

 



