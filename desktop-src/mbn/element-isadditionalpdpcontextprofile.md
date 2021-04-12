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
# <a name="span-idwwan_profile_v3element_isadditionalpdpcontextprofilespanisadditionalpdpcontextprofile"></a><span data-ttu-id="06c55-103"><span id="WWAN_profile_v3.element_IsAdditionalPdpContextProfile"></span>исаддитионалпдпконтекстпрофиле</span><span class="sxs-lookup"><span data-stu-id="06c55-103"><span id="WWAN_profile_v3.element_IsAdditionalPdpContextProfile"></span>IsAdditionalPdpContextProfile</span></span>

<span data-ttu-id="06c55-104">Элемент **исаддитионалпдпконтекстпрофиле** содержит **логическое** значение, равное **true** , если это дополнительный профиль "PDP" (протокол пакетных данных) и **значение false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="06c55-104">The **IsAdditionalPdpContextProfile** element contains a **boolean** that is **true** if this is an "additional PDP (Packet Data Protocol) context" profile and **false**, otherwise.</span></span> <span data-ttu-id="06c55-105">Значение по умолчанию — **false**.</span><span class="sxs-lookup"><span data-stu-id="06c55-105">Default is **false**.</span></span>

<span data-ttu-id="06c55-106">Профиль "дополнительный контекст PDP" — это профиль, который не активируется через порт по умолчанию физического адаптера, и установка этого элемента равным true гарантирует, что этот профиль не будет отображаться в пользовательском интерфейсе ненадлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="06c55-106">An "additional PDP context" profile is a profile that does not get activated over the physical adapter default port, and setting this element to true ensures that this profile is not displayed inappropriately in the user interface.</span></span>

<span data-ttu-id="06c55-107">Обратите внимание, что если для этого элемента задано значение true, необходимо также выполнить следующие условия.</span><span class="sxs-lookup"><span data-stu-id="06c55-107">Note that if this element is set to true, then the following must also be true.</span></span>

-   <span data-ttu-id="06c55-108">Элемент [**по умолчанию**](./schema-isdefault-mbnprofile-element.md) должен быть не указан или установлен в значение **false** , чтобы профиль был допустимым.</span><span class="sxs-lookup"><span data-stu-id="06c55-108">The [**IsDefault**](./schema-isdefault-mbnprofile-element.md) element must be unspecified or set to **false** for the profile to be valid.</span></span>
-   <span data-ttu-id="06c55-109">Чтобы профиль был допустимым, элемент [**ConnectionMode**](./schema-connectionmode-mbnprofile-element.md) должен быть неопределенным или иметь значение " **вручную** ".</span><span class="sxs-lookup"><span data-stu-id="06c55-109">The [**ConnectionMode**](./schema-connectionmode-mbnprofile-element.md) element must be unspecified or set to **manual** for the profile to be valid.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="06c55-110">Иерархия элементов</span><span class="sxs-lookup"><span data-stu-id="06c55-110">Element hierarchy</span></span>

**<IsAdditionalPdpContextProfile>**

## <a name="syntax"></a><span data-ttu-id="06c55-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="06c55-111">Syntax</span></span>

``` syntax
<IsAdditionalPdpContextProfile>

  boolean

</IsAdditionalPdpContextProfile>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="06c55-112"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Атрибуты и элементы</span><span class="sxs-lookup"><span data-stu-id="06c55-112"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="06c55-113"><span id="attributes"></span><span id="ATTRIBUTES"></span>Атрибуты</span><span class="sxs-lookup"><span data-stu-id="06c55-113"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="06c55-114">Нет.</span><span class="sxs-lookup"><span data-stu-id="06c55-114">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="06c55-115"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="06c55-115"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="06c55-116">Нет.</span><span class="sxs-lookup"><span data-stu-id="06c55-116">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="06c55-117"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="06c55-117"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<span data-ttu-id="06c55-118">Этот внешний элемент (Document) не может содержаться в каких-либо других элементах.</span><span class="sxs-lookup"><span data-stu-id="06c55-118">This outermost (document) element may not be contained by any other elements.</span></span>

## <a name="requirements"></a><span data-ttu-id="06c55-119">Требования</span><span class="sxs-lookup"><span data-stu-id="06c55-119">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="06c55-120">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="06c55-120">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v3</p></td>
</tr>
</tbody>
</table>

 

 
