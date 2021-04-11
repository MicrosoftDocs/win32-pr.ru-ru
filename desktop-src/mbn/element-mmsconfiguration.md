---
description: ммсконфигуратион
MS-HAID: WWAN\_profile\_v4.element\_MmsConfiguration
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: ммсконфигуратион
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cb98506476558ed0e39df11bab4b9446de4fd3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263040"
---
# <a name="span-idwwan_profile_v4element_mmsconfigurationspanmmsconfiguration"></a><span id="WWAN_profile_v4.element_MmsConfiguration"></span>ммсконфигуратион

Сведения о конфигурации для службы обмена сообщениями мультимедиа (MMS).

Помимо настройки элементов конфигурации в этом элементе, профиль MMS должен иметь следующие параметры.

-   Его элемент [**Name**](element-name.md) должен содержать уникальное для всей системы имя.
-   Его [**профилекреатионтипе**](./schema-profilecreationtype-mbnprofile-element.md) должен быть установлен в значение **усерпровисионед**.
-   Его [**симикЦид**](/windows/win32/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid) должен содержать ICCID SIM-карты, для которой предназначен этот профиль.
-   Его [**ConnectionMode**](./schema-connectionmode-mbnprofile-element.md) должен быть установлен в значение " **вручную**".
-   Его [**пурпосеграупгуид**](element-purposegroupguid.md) должен содержать GUID для группы целей MMS.
-   Его [**исаддитионалпдпконтекстпрофиле**](/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)) должен быть установлен в **значение true**.

## <a name="element-hierarchy"></a>Иерархия элементов

[<MBNProfileExt>](element-mbnprofileext.md)  
**<MmsConfiguration>**

## <a name="syntax"></a>Синтаксис

``` syntax
<MmsConfiguration>

  <!-- Child elements -->
  MmscUrl?,
  MmscPort?,
  MmsMaximumMessageSize?

</MmsConfiguration>
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
<td><a href="element-mmsmaximummessagesize.md">MmsMaximumMessageSize</a></td>
<td><p>Указывает максимальный размер MMS сообщений в килобайтах. Необязательный элемент.</p></td>
</tr>
<tr class="even">
<td><a href="element-mmscport.md">MmscPort</a></td>
<td><p>Указывает номер порта сервера ММСК для устройства. Укажите значение 0, чтобы указать, что конкретный порт не указан. Необязательный элемент.</p></td>
</tr>
<tr class="odd">
<td><a href="element-mmscurl.md">MmscUrl</a></td>
<td><p>Указывает URL-адрес сервера ММСК для устройства. Необязательный элемент.</p></td>
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

 

 
