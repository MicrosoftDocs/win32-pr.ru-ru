---
description: пурпосеграупс
MS-HAID: WWAN\_profile\_v4.element\_PurposeGroups
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: пурпосеграупс
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3b158938e1a41f6ab8d3f1df0cae6a2166bc21c
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2021
ms.locfileid: "122630940"
---
# <a name="span-idwwan_profile_v4element_purposegroupsspanpurposegroups"></a><span id="WWAN_profile_v4.element_PurposeGroups"></span>пурпосеграупс

Необязательный список групп профилей, где каждая группа включает профили, используемые для общего назначения.

Этот элемент является новым для V4 схемы.

Один профиль может быть указан в нескольких группах.

## <a name="element-hierarchy"></a>Иерархия элементов

[<MBNProfileExt>](element-mbnprofileext.md)  
**<PurposeGroups>**

## <a name="syntax"></a>Синтаксис

``` syntax
<PurposeGroups>

  <!-- Child elements -->
  PurposeGroupGuid{1,10}

</PurposeGroups>
```

### <a name="key"></a>Ключ

`{}`   конкретный диапазон вхождений

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Атрибуты и элементы

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>Атрибуты

Отсутствует.

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Дочерние элементы

<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Дочерний элемент</th>
<th>Описание:</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="element-purposegroupguid.md">пурпосеграупгуид</a></td>
<td><p>Представляет один профиль в Пурпосеграуп профилей.</p>
<p>Профили указываются по значению <a href="simpletype-guidtype.md"><strong>гуидтипе</strong></a> .</p>
<p>Определены четыре значения GUID, перечисленные в следующей таблице.</p>
<table>
<thead>
<tr class="header">
<th>Целевая группа</th>
<th>Код GUID</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Internet</td>
<td>3E5545D2-1137-4DC8-A198-33F1C657515F</td>
</tr>
<tr class="even">
<td>MMS</td>
<td>53E2C5D3-D13C-4068-AA38-9C48FF2E55A8</td>
</tr>
<tr class="odd">
<td>IMS</td>
<td>474D66ED-0E4B-476B-A455-19BB1239ED13</td>
</tr>
<tr class="even">
<td>супл</td>
<td>6D42669F-52A9-408E-9493-1071DCC437BD</td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>

 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Родительские элементы

<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Родительский элемент</th>
<th>Описание:</th>
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

 

## <a name="requirements"></a>Требования

<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Пространство имен</p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



