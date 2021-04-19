---
description: Модемдмконфигпрофиле \/ ... \/ Ауспротокол (v4)
MS-HAID: WWAN\_profile\_v4.element\_1\_AuthProtocol
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Ауспротокол (v4)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5e6c5a25-fe9e-4d0a-8b5b-4ff585f562af
api_name:
- AuthProtocol
api_type:
- Schema
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 99a4b02ec173e070f4a6d615f3632f11f4949b64
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/05/2021
ms.locfileid: "106388858"
---
# <a name="span-idwwan_profile_v4element_1_authprotocolspanmodemdmconfigprofileauthprotocol-v4"></a><span id="WWAN_profile_v4.element_1_AuthProtocol"></span>Модемдмконфигпрофиле \/ ... \/ Ауспротокол (v4)

>Указывает протокол проверки подлинности, используемый для активации контекста протокола данных пакетов (PDP).

Обратите внимание, что в версии v4 для этого элемента доступно новое значение перечисления. **Автовыбор** означает, что протокол проверки подлинности должен быть выбран более низкими слоями.

Дополнительные сведения см. в документации по элементу [**ауспротокол**](./schema-authprotocol-contexttype-element.md) v1.

## <a name="element-hierarchy"></a>Иерархия элементов

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;[\<Context\>](element-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;**\<AuthProtocol\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;[\<Context\>](element-1-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;**\<AuthProtocol\>**

## <a name="syntax"></a>Синтаксис

``` syntax
<AuthProtocol>

  "NONE" | "PAP" | "CHAP" | "MsCHAPv2" | "AutoSelection"

</AuthProtocol>
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
<td><a href="element-1-context.md">Контекст</a></td>
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

 

 
