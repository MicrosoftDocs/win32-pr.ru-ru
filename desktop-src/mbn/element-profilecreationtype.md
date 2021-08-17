---
description: Профилекреатионтипе (в Мбнпрофиликст)
MS-HAID: WWAN\_profile\_v4.element\_ProfileCreationType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Профилекреатионтипе (в Мбнпрофиликст)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 798f5f300a712f4b614e73007e0d0237c19e41010335d469bd58521a29847805
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119358714"
---
# <a name="span-idwwan_profile_v4element_profilecreationtypespanprofilecreationtype-in-mbnprofileext"></a><span id="WWAN_profile_v4.element_ProfileCreationType"></span>Профилекреатионтипе (в Мбнпрофиликст)

Указывает создателя профиля.

Дополнительные сведения об этом элементе см. в документации по элементу [**профилекреатионтипе**](./schema-profilecreationtype-mbnprofile-element.md) v1.

## <a name="element-hierarchy"></a>Иерархия элементов

[<MBNProfileExt>](element-mbnprofileext.md)  
**<ProfileCreationType>**

## <a name="syntax"></a>Синтаксис

``` syntax
<ProfileCreationType>

  "UserProvisioned" | "AdminProvisioned" | "OperatorProvisioned" | "DeviceProvisioned"

</ProfileCreationType>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Атрибуты и элементы

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>Атрибуты

Отсутствует.

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Дочерние элементы

Отсутствует.

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Родительские элементы

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Родительский элемент</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="element-mbnprofileext.md">MBNProfileExt</a></td>
<td><p>Элемент <strong>мбнпрофиликст</strong> является расширением более раннего элемента мбнпрофиле. Он определяет профиль мобильного широкополосного подключения с более широким набором параметров, чем элемент Мбнпрофиле.</p>
<p>В профиле может быть несколько элементов Мбнпрофиликст, описывающих параметры профиля для определенного набора условий. Используйте дочерний элемент <a href="element-profileconditionedon.md"><strong>профилекондитионедон</strong></a> из <strong>мбнпрофиликст</strong> , чтобы указать, какие операционные условия делают определенный профиль активным.</p></td>
</tr>
</tbody>
</table>

 

## <a name="related-elements"></a>Связанные элементы

Следующие элементы имеют то же имя, что и это одно, но различное содержимое или атрибуты:

-   **[Профилекреатионтипе (в Модемдмконфигпрофиле)](element-1-profilecreationtype.md)**

## <a name="requirements"></a>Требования

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Пространство имен</p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 
