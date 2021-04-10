---
description: профилекондитионедон
MS-HAID: WWAN\_profile\_v4.element\_ProfileConditionedOn
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: профилекондитионедон
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 729b95872be68ea814b35a593082b2366284f0dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144818"
---
# <a name="span-idwwan_profile_v4element_profileconditionedonspanprofileconditionedon"></a><span id="WWAN_profile_v4.element_ProfileConditionedOn"></span>профилекондитионедон

Указывает условия, которые должны быть удовлетворены для применения профиля.

Этот элемент является новым для v4. Он позволяет указать несколько профилей, которые применяются в различных условиях, а также для автоматического использования соответствующего профиля. Этот элемент является необязательным. Если его не указать, профиль всегда будет применяться в соответствии с указанными условиями.

## <a name="element-hierarchy"></a>Иерархия элементов

[<MBNProfileExt>](element-mbnprofileext.md)  
**<ProfileConditionedOn>**

## <a name="syntax"></a>Синтаксис

``` syntax
<ProfileConditionedOn>

  <!-- Child elements -->
  CellularClass?,
  RATApplicability?,
  RoamApplicability?,
  IMSI?,
  IwlanApplicability?

</ProfileConditionedOn>
```

### <a name="key"></a>Ключ

`?`   необязательно (ноль или один)

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Атрибуты и элементы

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>Атрибуты

Нет.

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Дочерние элементы

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Дочерний элемент</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="element-cellularclass.md">целлуларкласс</a></td>
<td><p>Указывает, что этот профиль активен, только если указан текущий класс сотовой связи. В противном случае профиль неприменим и не может использоваться для активации контекста протокола данных пакетов (PDP).</p></td>
</tr>
<tr class="even">
<td><a href="element-imsi.md">IMSI</a></td>
<td><p>Указывает, что этот профиль активен, только если указана текущая IMSI в ICCID. В противном случае профиль неприменим и не может использоваться для активации контекста протокола данных пакетов (PDP).</p></td>
</tr>
<tr class="odd">
<td><a href="element-iwlanapplicability.md">ивланаппликабилити</a></td>
<td><p>Указывает, что этот профиль активен только при подключении к сети ИВЛАН. В противном случае профиль неприменим и не может использоваться для активации контекста протокола данных пакетов (PDP). Значение этого элемента должно быть допустимым значением <a href="simpletype-iwlanapplicabilitytype.md"><strong>ивланаппликабилититипе</strong></a> .</p></td>
</tr>
<tr class="even">
<td><a href="element-ratapplicability.md">ратаппликабилити</a></td>
<td><p>Указывает, что этот профиль активен, только если указан тип RAT. В противном случае профиль неприменим и не может использоваться для активации контекста протокола данных пакетов (PDP).</p></td>
</tr>
<tr class="odd">
<td><a href="element-roamapplicability.md">роамаппликабилити</a></td>
<td><p>Указывает, что этот профиль активен, только если указано текущее перемещаемое условие. В противном случае профиль неприменим и не может использоваться для активации контекста протокола данных пакетов (PDP). Значение этого элемента должно быть допустимым значением <a href="simpletype-roamapplicabilitytype.md"><strong>роамаппликабилититипе</strong></a> .</p></td>
</tr>
</tbody>
</table>

 

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

 

 



