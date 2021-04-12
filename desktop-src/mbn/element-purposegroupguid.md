---
description: пурпосеграупгуид
MS-HAID: WWAN\_profile\_v4.element\_PurposeGroupGuid
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: пурпосеграупгуид
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d20d6c9d1687ea0e3fca344fd3b534ccc0b3ee57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423794"
---
# <a name="span-idwwan_profile_v4element_purposegroupguidspanpurposegroupguid"></a><span id="WWAN_profile_v4.element_PurposeGroupGuid"></span>пурпосеграупгуид

Представляет один профиль в Пурпосеграуп профилей.

Профили указываются по значению [**гуидтипе**](simpletype-guidtype.md) .

Определены четыре значения GUID, перечисленные в следующей таблице.

| Целевая группа | Код GUID                                 |
|---------------|--------------------------------------|
| Интернет      | 3E5545D2-1137-4DC8-A198-33F1C657515F |
| MMS           | 53E2C5D3-D13C-4068-AA38-9C48FF2E55A8 |
| IMS           | 474D66ED-0E4B-476B-A455-19BB1239ED13 |
| супл          | 6D42669F-52A9-408E-9493-1071DCC437BD |

 

## <a name="element-hierarchy"></a>Иерархия элементов

[<MBNProfileExt>](element-mbnprofileext.md)  
[<PurposeGroups>](element-purposegroups.md)  
**<PurposeGroupGuid>**

## <a name="syntax"></a>Синтаксис

``` syntax
<PurposeGroupGuid>

  guidType

</PurposeGroupGuid>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Атрибуты и элементы

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>Атрибуты

Нет.

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Дочерние элементы

Нет.

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
<td><a href="element-purposegroups.md">пурпосеграупс</a></td>
<td><p>Необязательный список групп профилей, где каждая группа включает профили, используемые для общего назначения.</p>
<p>Этот элемент является новым для V4 схемы.</p>
<p>Один профиль может быть указан в нескольких группах.</p></td>
</tr>
</tbody>
</table>

 

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

 

 



