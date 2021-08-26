---
description: '\/Контекст модемдмконфигпрофиле (v4)'
MS-HAID: WWAN\_profile\_v4.element\_1\_Context
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Контекст (v4)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8f463f14-95b3-4364-b1b1-549a32291959
api_name:
- Context
api_type:
- Schema
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 36007bc1a7aecb25c2b6d61f74dd826e888a314b
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2021
ms.locfileid: "122624760"
---
# <a name="span-idwwan_profile_v4element_1_contextspanmodemdmconfigprofilecontext-v4"></a><span id="WWAN_profile_v4.element_1_Context"></span>\/Контекст модемдмконфигпрофиле (v4)

Задает параметры, необходимые для установления подключения к данным.

## <a name="element-hierarchy"></a>Иерархия элементов

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;**\<Context\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;**\<Context\>**

## <a name="syntax"></a>Синтаксис

``` syntax
<Context>

  <!-- Child elements -->
  AccessString?,
  UserLogonCred?,
  Compression?,
  AuthProtocol?,
  IPType?

</Context>
```

### <a name="key"></a>Ключ

`?`   необязательно (ноль или один)

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
<td><a href="element-1-accessstring.md">AccessString</a></td>
<td><p>Определяет имя APN или строку вызова, используемые для установки подключения к данным.</p>
<p>Дополнительные сведения см. в документации по элементу <a href="../mbn/schema-accessstring-contexttype-element.md"><strong>акцессстринг</strong></a> v1.</p></td>
</tr>
<tr class="even">
<td><a href="element-1-authprotocol.md">AuthProtocol</a></td>
<td><p>>Указывает протокол проверки подлинности, используемый для активации контекста протокола данных пакетов (PDP).</p>
<p>Обратите внимание, что в версии v4 для этого элемента доступно новое значение перечисления. <strong>Автовыбор</strong> означает, что протокол проверки подлинности должен быть выбран более низкими слоями.</p>
<p>Дополнительные сведения см. в документации по элементу <a href="../mbn/schema-authprotocol-contexttype-element.md"><strong>ауспротокол</strong></a> v1.</p></td>
</tr>
<tr class="odd">
<td><a href="element-1-compression.md">Сжатие</a></td>
<td><p>Указывает, будет ли использоваться сжатие по каналу данных для заголовка и передачи данных.</p>
<p>Дополнительные сведения см. в документации по элементу <a href="../mbn/schema-compression-contexttype-element.md"><strong>сжатия</strong></a> v1.</p></td>
</tr>
<tr class="even">
<td><a href="element-1-iptype.md">IPType</a></td>
<td><p>Указывает тип IP-адреса, используемый для этого подключения к данным.</p>
<p>Этот элемент впервые находится в версии v4 схемы. Элемент может иметь одно из следующих значений.</p>
<table>
<thead>
<tr class="header">
<th>Значение</th>
<th>Значение</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>По умолчанию</td>
<td>Тип IP-адреса должен быть выбран более низкими слоями</td>
</tr>
<tr class="even">
<td>IPv4</td>
<td>Использовать IPv4</td>
</tr>
<tr class="odd">
<td>IPv6</td>
<td>использовать IPv6</td>
</tr>
<tr class="even">
<td>IPv4v6</td>
<td>Используйте IPv4 и (или) IPv6, как доступно.</td>
</tr>
<tr class="odd">
<td>кслат</td>
<td>Использование 464XLAT для туннелирования IPv4 через IPv6-сети</td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
<tr class="odd">
<td><a href="element-1-userlogoncred.md">UserLogonCred</a></td>
<td><p>Учетные данные входа для подключения.</p></td>
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
<tr class="even">
<td><a href="element-modemdmconfigprofile.md">ModemDMConfigProfile</a></td>
<td><p>Профиль конфигурации DM для модема.</p></td>
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

 

 



