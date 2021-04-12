---
description: исаддитионалпдпконтекстпрофиле
MS-HAID: WWAN\_profile\_v3.element\_IsAdditionalPdpContextProfile
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: исаддитионалпдпконтекстпрофиле
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 169aa9a34a561f65eed5dfc315e7711ef6bb9bf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343355"
---
# <a name="span-idwwan_profile_v3element_isadditionalpdpcontextprofilespanisadditionalpdpcontextprofile"></a><span id="WWAN_profile_v3.element_IsAdditionalPdpContextProfile"></span>исаддитионалпдпконтекстпрофиле

Элемент **исаддитионалпдпконтекстпрофиле** содержит **логическое** значение, равное **true** , если это дополнительный профиль "PDP" (протокол пакетных данных) и **значение false** в противном случае. Значение по умолчанию — **false**.

Профиль "дополнительный контекст PDP" — это профиль, который не активируется через порт по умолчанию физического адаптера, и установка этого элемента равным true гарантирует, что этот профиль не будет отображаться в пользовательском интерфейсе ненадлежащим образом.

Обратите внимание, что если для этого элемента задано значение true, необходимо также выполнить следующие условия.

-   Элемент [**по умолчанию**](./schema-isdefault-mbnprofile-element.md) должен быть не указан или установлен в значение **false** , чтобы профиль был допустимым.
-   Чтобы профиль был допустимым, элемент [**ConnectionMode**](./schema-connectionmode-mbnprofile-element.md) должен быть неопределенным или иметь значение " **вручную** ".

## <a name="element-hierarchy"></a>Иерархия элементов

**<IsAdditionalPdpContextProfile>**

## <a name="syntax"></a>Синтаксис

``` syntax
<IsAdditionalPdpContextProfile>

  boolean

</IsAdditionalPdpContextProfile>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Атрибуты и элементы

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>Атрибуты

Нет.

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Дочерние элементы

Нет.

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
<td><p>https://www.microsoft.com/networking/WWAN/profile/v3</p></td>
</tr>
</tbody>
</table>

 

 
