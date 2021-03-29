---
description: ModemDMConfigProfile
MS-HAID: WWAN\_profile\_v4.element\_ModemDMConfigProfile
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: ModemDMConfigProfile
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43f4593d1b55b4c95a2ec185fe5545ad7eb04141
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105647161"
---
# <a name="span-idwwan_profile_v4element_modemdmconfigprofilespanmodemdmconfigprofile"></a><span id="WWAN_profile_v4.element_ModemDMConfigProfile"></span>модемдмконфигпрофиле

Профиль конфигурации DM для модема.

## <a name="element-hierarchy"></a>Иерархия элементов

**<ModemDMConfigProfile>**

## <a name="syntax"></a>Синтаксис

``` syntax
<ModemDMConfigProfile>

  <!-- Child elements -->
  Name,
  SimIccID,
  ApnID,
  OemConnectionId,
  RoamApplicability?,
  Context,
  AdminEnable,
  AdminRoamControl,
  ProfileCreationType?,
  any element in a non-schema namespace*

</ModemDMConfigProfile>
```

### <a name="key"></a>Ключ

`?`   необязательно (ноль или один)

`*`   необязательно (ноль или более)

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
<td><a href="element-1-adminenable.md">админенабле</a></td>
<td><p>Указывает, включен ли профиль в административном состоянии. Это новый элемент для v4.</p></td>
</tr>
<tr class="even">
<td><a href="element-1-adminroamcontrol.md">админроамконтрол</a></td>
<td><p>Указывает, управляется ли профиль административным роумингом. Этот элемент является новым для v4. Значением этого элемента является значение <a href="simpletype-roamcontroltype.md"><strong>роамконтролтипе</strong></a> . Это необязательный элемент. Если значение не указано, по умолчанию используется <strong>аллроамалловед</strong> .</p></td>
</tr>
<tr class="odd">
<td><a href="element-1-apnid.md">апнид</a></td>
<td><p>Идентификатор APN, связанный с этим профилем. Этот элемент является новым в v4 и является необязательным.</p></td>
</tr>
<tr class="even">
<td><a href="element-1-context.md">Контекст</a></td>
<td><p>Задает параметры, необходимые для установления подключения к данным.</p></td>
</tr>
<tr class="odd">
<td><a href="element-1-name.md">имя</a>;</td>
<td><p>Имя профиля. Дополнительные сведения см. в документации по элементу <a href="../mbn/schema-name-mbnprofile-element.md"><strong>имени</strong></a> v1.</p></td>
</tr>
<tr class="even">
<td><a href="element-oemconnectionid.md">оемконнектионид</a></td>
<td><p>Идентификатор OEM-подключения для конфигурации DM модема.</p></td>
</tr>
<tr class="odd">
<td><a href="element-1-profilecreationtype.md">Профилекреатионтипе (в Модемдмконфигпрофиле)</a></td>
<td><p>Указывает, каким способом был создан профиль DM для модема.</p>
<p>Это значение используется для принятия решения о том, может ли пользователь удалить профиль. Пользователи могут удалять только профили <strong>усерпровисионед</strong> .</p></td>
</tr>
<tr class="even">
<td><a href="element-1-roamapplicability.md">роамаппликабилити</a></td>
<td><p>Указывает, что этот профиль активен, только если указано текущее перемещаемое условие. В противном случае профиль неприменим и не может использоваться для активации контекста протокола данных пакетов (PDP). Значение этого элемента должно быть допустимым значением <a href="simpletype-roamapplicabilitytype.md"><strong>роамаппликабилититипе</strong></a> .</p></td>
</tr>
<tr class="odd">
<td><a href="element-1-simiccid.md">симикЦид</a></td>
<td><p>Номер Идентифкатион SIM для устройств GSM. Дополнительные сведения см. в документации по элементу <a href="../mbn/schema-simiccid-mbnprofile-element.md"><strong>симикЦид</strong></a> v1.</p></td>
</tr>
</tbody>
</table>

 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Родительские элементы

Этот внешний элемент (Document) не может содержаться в каких-либо других элементах.

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

 

 



