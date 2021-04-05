---
description: ратаппликабилити
MS-HAID: WWAN\_profile\_v4.element\_RATApplicability
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: ратаппликабилити
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 155f8e216b6ec00f123d0fe0f378fd9db2e4d75f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897534"
---
# <a name="span-idwwan_profile_v4element_ratapplicabilityspanratapplicability"></a><span data-ttu-id="d322d-103"><span id="WWAN_profile_v4.element_RATApplicability"></span>ратаппликабилити</span><span class="sxs-lookup"><span data-stu-id="d322d-103"><span id="WWAN_profile_v4.element_RATApplicability"></span>RATApplicability</span></span>

<span data-ttu-id="d322d-104">Указывает, что этот профиль активен, только если указан тип RAT.</span><span class="sxs-lookup"><span data-stu-id="d322d-104">Specifies that this profile is active only when the RAT type is the one specified.</span></span> <span data-ttu-id="d322d-105">В противном случае профиль неприменим и не может использоваться для активации контекста протокола данных пакетов (PDP).</span><span class="sxs-lookup"><span data-stu-id="d322d-105">Otherwise, the profile is not applicable, and cannot be used to activate a Packet Data Protocol (PDP) context.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="d322d-106">Иерархия элементов</span><span class="sxs-lookup"><span data-stu-id="d322d-106">Element hierarchy</span></span>

[<MBNProfileExt>](element-mbnprofileext.md)  
[<ProfileConditionedOn>](element-profileconditionedon.md)  
**<RATApplicability>**

## <a name="syntax"></a><span data-ttu-id="d322d-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d322d-107">Syntax</span></span>

``` syntax
<RATApplicability>

  "LTE_eHRPD" | "3GPP_LEGACY"

</RATApplicability>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="d322d-108"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Атрибуты и элементы</span><span class="sxs-lookup"><span data-stu-id="d322d-108"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="d322d-109"><span id="attributes"></span><span id="ATTRIBUTES"></span>Атрибуты</span><span class="sxs-lookup"><span data-stu-id="d322d-109"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="d322d-110">Нет.</span><span class="sxs-lookup"><span data-stu-id="d322d-110">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="d322d-111"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="d322d-111"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="d322d-112">Нет.</span><span class="sxs-lookup"><span data-stu-id="d322d-112">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="d322d-113"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="d322d-113"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d322d-114">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="d322d-114">Parent Element</span></span></th>
<th><span data-ttu-id="d322d-115">Описание</span><span class="sxs-lookup"><span data-stu-id="d322d-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d322d-116"><a href="element-profileconditionedon.md">профилекондитионедон</a></span><span class="sxs-lookup"><span data-stu-id="d322d-116"><a href="element-profileconditionedon.md">ProfileConditionedOn</a></span></span></td>
<td><p><span data-ttu-id="d322d-117">Указывает условия, которые должны быть удовлетворены для применения профиля.</span><span class="sxs-lookup"><span data-stu-id="d322d-117">Specifies the conditions which must be satisfied for a profile to be applicable.</span></span></p>
<p><span data-ttu-id="d322d-118">Этот элемент является новым для v4.</span><span class="sxs-lookup"><span data-stu-id="d322d-118">This element is new for v4.</span></span> <span data-ttu-id="d322d-119">Он позволяет указать несколько профилей, которые применяются в различных условиях, а также для автоматического использования соответствующего профиля.</span><span class="sxs-lookup"><span data-stu-id="d322d-119">It enables you to specify multiple profiles that apply in different conditions, and for the proper profile to be used automatically when it is applicable.</span></span> <span data-ttu-id="d322d-120">Этот элемент является необязательным.</span><span class="sxs-lookup"><span data-stu-id="d322d-120">This element is optional.</span></span> <span data-ttu-id="d322d-121">Если его не указать, профиль всегда будет применяться в соответствии с указанными условиями.</span><span class="sxs-lookup"><span data-stu-id="d322d-121">If you do not specify it, then the profile is always applicable with respect to the conditions listed.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="d322d-122">Требования</span><span class="sxs-lookup"><span data-stu-id="d322d-122">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d322d-123">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d322d-123">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



