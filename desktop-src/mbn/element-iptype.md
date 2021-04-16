---
description: Мбнпрофиликст \/ ... \/ Иптипе (v4)
MS-HAID: WWAN\_profile\_v4.element\_IPType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPType
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 918355cdfc90863539da5f29aff542654a95f5e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542194"
---
# <a name="span-idwwan_profile_v4element_iptypespanmbnprofileextiptype-v4"></a><span id="WWAN_profile_v4.element_IPType"></span>Мбнпрофиликст \/ ... \/ Иптипе (v4)

Указывает тип IP-адреса, используемый для этого подключения к данным.

Этот элемент впервые находится в версии v4 схемы. Элемент может иметь одно из следующих значений.

| Значение   | Значение                                       |
|---------|-----------------------------------------------|
| Значение по умолчанию | Тип IP-адреса должен быть выбран более низкими слоями     |
| IPv4    | Использовать IPv4                                      |
| IPv6;    | использовать IPv6                                      |
| IPv4v6  | Используйте IPv4 и (или) IPv6, как доступно.           |
| кслат    | Использование 464XLAT для туннелирования IPv4 через IPv6-сети |

 

## <a name="element-hierarchy"></a>Иерархия элементов

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;[\<Context\>](element-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;**\<IPType\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;[\<Context\>](element-1-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;**\<IPType\>**

## <a name="syntax"></a>Синтаксис

``` syntax
<IPType>

  "Default" | "IPv4" | "IPv6" | "IPv4v6" | "XLAT"

</IPType>
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
<td><a href="element-context.md">Контекст</a></td>
<td><p>Задает параметры, необходимые для установления подключения к данным.</p></td>
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

 

 



