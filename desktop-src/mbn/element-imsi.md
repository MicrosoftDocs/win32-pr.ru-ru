---
description: IMSI
MS-HAID: WWAN\_profile\_v4.element\_IMSI
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IMSI
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d873cbc5634f78b8bcb802daea9c6dd0a667b32e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541418"
---
# <a name="span-idwwan_profile_v4element_imsispanimsi"></a><span data-ttu-id="5505f-103"><span id="WWAN_profile_v4.element_IMSI"></span>IMSI</span><span class="sxs-lookup"><span data-stu-id="5505f-103"><span id="WWAN_profile_v4.element_IMSI"></span>IMSI</span></span>

<span data-ttu-id="5505f-104">Указывает, что этот профиль активен, только если указана текущая IMSI в ICCID.</span><span class="sxs-lookup"><span data-stu-id="5505f-104">Specifies that this profile is active only when the current IMSI being used in the ICCID is the one specified.</span></span> <span data-ttu-id="5505f-105">В противном случае профиль неприменим и не может использоваться для активации контекста протокола данных пакетов (PDP).</span><span class="sxs-lookup"><span data-stu-id="5505f-105">Otherwise, the profile is not applicable, and cannot be used to activate a Packet Data Protocol (PDP) context.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="5505f-106">Иерархия элементов</span><span class="sxs-lookup"><span data-stu-id="5505f-106">Element hierarchy</span></span>

[<MBNProfileExt>](element-mbnprofileext.md)  
[<ProfileConditionedOn>](element-profileconditionedon.md)  
**<IMSI>**

## <a name="syntax"></a><span data-ttu-id="5505f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5505f-107">Syntax</span></span>

``` syntax
<IMSI>

  subscriberIdType

</IMSI>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="5505f-108"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Атрибуты и элементы</span><span class="sxs-lookup"><span data-stu-id="5505f-108"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="5505f-109"><span id="attributes"></span><span id="ATTRIBUTES"></span>Атрибуты</span><span class="sxs-lookup"><span data-stu-id="5505f-109"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="5505f-110">Нет.</span><span class="sxs-lookup"><span data-stu-id="5505f-110">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="5505f-111"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="5505f-111"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="5505f-112">Нет.</span><span class="sxs-lookup"><span data-stu-id="5505f-112">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="5505f-113"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="5505f-113"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5505f-114">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="5505f-114">Parent Element</span></span></th>
<th><span data-ttu-id="5505f-115">Описание</span><span class="sxs-lookup"><span data-stu-id="5505f-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5505f-116"><a href="element-profileconditionedon.md">профилекондитионедон</a></span><span class="sxs-lookup"><span data-stu-id="5505f-116"><a href="element-profileconditionedon.md">ProfileConditionedOn</a></span></span></td>
<td><p><span data-ttu-id="5505f-117">Указывает условия, которые должны быть удовлетворены для применения профиля.</span><span class="sxs-lookup"><span data-stu-id="5505f-117">Specifies the conditions which must be satisfied for a profile to be applicable.</span></span></p>
<p><span data-ttu-id="5505f-118">Этот элемент является новым для v4.</span><span class="sxs-lookup"><span data-stu-id="5505f-118">This element is new for v4.</span></span> <span data-ttu-id="5505f-119">Он позволяет указать несколько профилей, которые применяются в различных условиях, а также для автоматического использования соответствующего профиля.</span><span class="sxs-lookup"><span data-stu-id="5505f-119">It enables you to specify multiple profiles that apply in different conditions, and for the proper profile to be used automatically when it is applicable.</span></span> <span data-ttu-id="5505f-120">Этот элемент является необязательным.</span><span class="sxs-lookup"><span data-stu-id="5505f-120">This element is optional.</span></span> <span data-ttu-id="5505f-121">Если его не указать, профиль всегда будет применяться в соответствии с указанными условиями.</span><span class="sxs-lookup"><span data-stu-id="5505f-121">If you do not specify it, then the profile is always applicable with respect to the conditions listed.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="5505f-122">Требования</span><span class="sxs-lookup"><span data-stu-id="5505f-122">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5505f-123">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="5505f-123">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



