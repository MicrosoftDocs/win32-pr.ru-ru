---
description: Модемдмконфигпрофиле \/ роамаппликабилити (v4)
MS-HAID: WWAN\_profile\_v4.element\_1\_RoamApplicability
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: роамаппликабилити
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2286a0a0c675698ce4d55186eaf8b9a5cf41f211
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897281"
---
# <a name="span-idwwan_profile_v4element_1_roamapplicabilityspanmodemdmconfigprofileroamapplicability-v4"></a><span data-ttu-id="22860-103"><span id="WWAN_profile_v4.element_1_RoamApplicability"></span>Модемдмконфигпрофиле \/ роамаппликабилити (v4)</span><span class="sxs-lookup"><span data-stu-id="22860-103"><span id="WWAN_profile_v4.element_1_RoamApplicability"></span>ModemDMConfigProfile\/RoamApplicability (v4)</span></span>

<span data-ttu-id="22860-104">Указывает, что этот профиль активен, только если указано текущее перемещаемое условие.</span><span class="sxs-lookup"><span data-stu-id="22860-104">Specifies that this profile is active only when the current roaming condition is the one specified.</span></span> <span data-ttu-id="22860-105">В противном случае профиль неприменим и не может использоваться для активации контекста протокола данных пакетов (PDP).</span><span class="sxs-lookup"><span data-stu-id="22860-105">Otherwise, the profile is not applicable, and cannot be used to activate a Packet Data Protocol (PDP) context.</span></span> <span data-ttu-id="22860-106">Значение этого элемента должно быть допустимым значением [**роамаппликабилититипе**](simpletype-roamapplicabilitytype.md) .</span><span class="sxs-lookup"><span data-stu-id="22860-106">The value of this element must be a valid [**roamApplicabilityType**](simpletype-roamapplicabilitytype.md) value.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="22860-107">Иерархия элементов</span><span class="sxs-lookup"><span data-stu-id="22860-107">Element hierarchy</span></span>

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;**\<RoamApplicability\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;**\<RoamApplicability\>**

## <a name="syntax"></a><span data-ttu-id="22860-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="22860-108">Syntax</span></span>

``` syntax
<RoamApplicability>

  "NonPartnerOnly" | "PartnerOnly" | "HomeOnly" | "HomeAndPartner" | "PartnerAndNonpartner" | "AllRoaming"

</RoamApplicability>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="22860-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Атрибуты и элементы</span><span class="sxs-lookup"><span data-stu-id="22860-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="22860-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Атрибуты</span><span class="sxs-lookup"><span data-stu-id="22860-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="22860-111">Нет.</span><span class="sxs-lookup"><span data-stu-id="22860-111">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="22860-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="22860-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="22860-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="22860-113">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="22860-114"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="22860-114"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="22860-115">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="22860-115">Parent Element</span></span></th>
<th><span data-ttu-id="22860-116">Описание</span><span class="sxs-lookup"><span data-stu-id="22860-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="22860-117"><a href="element-modemdmconfigprofile.md">ModemDMConfigProfile</a></span><span class="sxs-lookup"><span data-stu-id="22860-117"><a href="element-modemdmconfigprofile.md">ModemDMConfigProfile</a></span></span></td>
<td><p><span data-ttu-id="22860-118">Профиль конфигурации DM для модема.</span><span class="sxs-lookup"><span data-stu-id="22860-118">Modem DM configuration profile.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="22860-119"><a href="element-profileconditionedon.md">профилекондитионедон</a></span><span class="sxs-lookup"><span data-stu-id="22860-119"><a href="element-profileconditionedon.md">ProfileConditionedOn</a></span></span></td>
<td><p><span data-ttu-id="22860-120">Указывает условия, которые должны быть удовлетворены для применения профиля.</span><span class="sxs-lookup"><span data-stu-id="22860-120">Specifies the conditions which must be satisfied for a profile to be applicable.</span></span></p>
<p><span data-ttu-id="22860-121">Этот элемент является новым для v4.</span><span class="sxs-lookup"><span data-stu-id="22860-121">This element is new for v4.</span></span> <span data-ttu-id="22860-122">Он позволяет указать несколько профилей, которые применяются в различных условиях, а также для автоматического использования соответствующего профиля.</span><span class="sxs-lookup"><span data-stu-id="22860-122">It enables you to specify multiple profiles that apply in different conditions, and for the proper profile to be used automatically when it is applicable.</span></span> <span data-ttu-id="22860-123">Этот элемент является необязательным.</span><span class="sxs-lookup"><span data-stu-id="22860-123">This element is optional.</span></span> <span data-ttu-id="22860-124">Если его не указать, профиль всегда будет применяться в соответствии с указанными условиями.</span><span class="sxs-lookup"><span data-stu-id="22860-124">If you do not specify it, then the profile is always applicable with respect to the conditions listed.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="22860-125">Требования</span><span class="sxs-lookup"><span data-stu-id="22860-125">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="22860-126">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="22860-126">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



