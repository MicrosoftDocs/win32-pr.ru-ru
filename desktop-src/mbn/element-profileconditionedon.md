---
description: профилекондитионедон
MS-HAID: WWAN\_profile\_v4.element\_ProfileConditionedOn
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: профилекондитионедон
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 729b95872be68ea814b35a593082b2366284f0dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144818"
---
# <a name="span-idwwan_profile_v4element_profileconditionedonspanprofileconditionedon"></a><span data-ttu-id="c4913-103"><span id="WWAN_profile_v4.element_ProfileConditionedOn"></span>профилекондитионедон</span><span class="sxs-lookup"><span data-stu-id="c4913-103"><span id="WWAN_profile_v4.element_ProfileConditionedOn"></span>ProfileConditionedOn</span></span>

<span data-ttu-id="c4913-104">Указывает условия, которые должны быть удовлетворены для применения профиля.</span><span class="sxs-lookup"><span data-stu-id="c4913-104">Specifies the conditions which must be satisfied for a profile to be applicable.</span></span>

<span data-ttu-id="c4913-105">Этот элемент является новым для v4.</span><span class="sxs-lookup"><span data-stu-id="c4913-105">This element is new for v4.</span></span> <span data-ttu-id="c4913-106">Он позволяет указать несколько профилей, которые применяются в различных условиях, а также для автоматического использования соответствующего профиля.</span><span class="sxs-lookup"><span data-stu-id="c4913-106">It enables you to specify multiple profiles that apply in different conditions, and for the proper profile to be used automatically when it is applicable.</span></span> <span data-ttu-id="c4913-107">Этот элемент является необязательным.</span><span class="sxs-lookup"><span data-stu-id="c4913-107">This element is optional.</span></span> <span data-ttu-id="c4913-108">Если его не указать, профиль всегда будет применяться в соответствии с указанными условиями.</span><span class="sxs-lookup"><span data-stu-id="c4913-108">If you do not specify it, then the profile is always applicable with respect to the conditions listed.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="c4913-109">Иерархия элементов</span><span class="sxs-lookup"><span data-stu-id="c4913-109">Element hierarchy</span></span>

[<MBNProfileExt>](element-mbnprofileext.md)  
**<ProfileConditionedOn>**

## <a name="syntax"></a><span data-ttu-id="c4913-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c4913-110">Syntax</span></span>

``` syntax
<ProfileConditionedOn>

  <!-- Child elements -->
  CellularClass?,
  RATApplicability?,
  RoamApplicability?,
  IMSI?,
  IwlanApplicability?

</ProfileConditionedOn>
```

### <a name="key"></a><span data-ttu-id="c4913-111">Ключ</span><span class="sxs-lookup"><span data-stu-id="c4913-111">Key</span></span>

<span data-ttu-id="c4913-112">`?`   необязательно (ноль или один)</span><span class="sxs-lookup"><span data-stu-id="c4913-112">`?`   optional (zero or one)</span></span>

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="c4913-113"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Атрибуты и элементы</span><span class="sxs-lookup"><span data-stu-id="c4913-113"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="c4913-114"><span id="attributes"></span><span id="ATTRIBUTES"></span>Атрибуты</span><span class="sxs-lookup"><span data-stu-id="c4913-114"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="c4913-115">Нет.</span><span class="sxs-lookup"><span data-stu-id="c4913-115">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="c4913-116"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="c4913-116"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c4913-117">Дочерний элемент</span><span class="sxs-lookup"><span data-stu-id="c4913-117">Child Element</span></span></th>
<th><span data-ttu-id="c4913-118">Описание</span><span class="sxs-lookup"><span data-stu-id="c4913-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c4913-119"><a href="element-cellularclass.md">целлуларкласс</a></span><span class="sxs-lookup"><span data-stu-id="c4913-119"><a href="element-cellularclass.md">CellularClass</a></span></span></td>
<td><p><span data-ttu-id="c4913-120">Указывает, что этот профиль активен, только если указан текущий класс сотовой связи.</span><span class="sxs-lookup"><span data-stu-id="c4913-120">Specifies that this profile is active only when the current cellular class is the one specified.</span></span> <span data-ttu-id="c4913-121">В противном случае профиль неприменим и не может использоваться для активации контекста протокола данных пакетов (PDP).</span><span class="sxs-lookup"><span data-stu-id="c4913-121">Otherwise, the profile is not applicable, and cannot be used to activate a Packet Data Protocol (PDP) context.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4913-122"><a href="element-imsi.md">IMSI</a></span><span class="sxs-lookup"><span data-stu-id="c4913-122"><a href="element-imsi.md">IMSI</a></span></span></td>
<td><p><span data-ttu-id="c4913-123">Указывает, что этот профиль активен, только если указана текущая IMSI в ICCID.</span><span class="sxs-lookup"><span data-stu-id="c4913-123">Specifies that this profile is active only when the current IMSI being used in the ICCID is the one specified.</span></span> <span data-ttu-id="c4913-124">В противном случае профиль неприменим и не может использоваться для активации контекста протокола данных пакетов (PDP).</span><span class="sxs-lookup"><span data-stu-id="c4913-124">Otherwise, the profile is not applicable, and cannot be used to activate a Packet Data Protocol (PDP) context.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4913-125"><a href="element-iwlanapplicability.md">ивланаппликабилити</a></span><span class="sxs-lookup"><span data-stu-id="c4913-125"><a href="element-iwlanapplicability.md">IwlanApplicability</a></span></span></td>
<td><p><span data-ttu-id="c4913-126">Указывает, что этот профиль активен только при подключении к сети ИВЛАН.</span><span class="sxs-lookup"><span data-stu-id="c4913-126">Specifies that this profile is active only when connected to an IWLAN network.</span></span> <span data-ttu-id="c4913-127">В противном случае профиль неприменим и не может использоваться для активации контекста протокола данных пакетов (PDP).</span><span class="sxs-lookup"><span data-stu-id="c4913-127">Otherwise, the profile is not applicable, and cannot be used to activate a Packet Data Protocol (PDP) context.</span></span> <span data-ttu-id="c4913-128">Значение этого элемента должно быть допустимым значением <a href="simpletype-iwlanapplicabilitytype.md"><strong>ивланаппликабилититипе</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="c4913-128">The value of this element must be a valid <a href="simpletype-iwlanapplicabilitytype.md"><strong>iwlanApplicabilityType</strong></a> value.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4913-129"><a href="element-ratapplicability.md">ратаппликабилити</a></span><span class="sxs-lookup"><span data-stu-id="c4913-129"><a href="element-ratapplicability.md">RATApplicability</a></span></span></td>
<td><p><span data-ttu-id="c4913-130">Указывает, что этот профиль активен, только если указан тип RAT.</span><span class="sxs-lookup"><span data-stu-id="c4913-130">Specifies that this profile is active only when the RAT type is the one specified.</span></span> <span data-ttu-id="c4913-131">В противном случае профиль неприменим и не может использоваться для активации контекста протокола данных пакетов (PDP).</span><span class="sxs-lookup"><span data-stu-id="c4913-131">Otherwise, the profile is not applicable, and cannot be used to activate a Packet Data Protocol (PDP) context.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4913-132"><a href="element-roamapplicability.md">роамаппликабилити</a></span><span class="sxs-lookup"><span data-stu-id="c4913-132"><a href="element-roamapplicability.md">RoamApplicability</a></span></span></td>
<td><p><span data-ttu-id="c4913-133">Указывает, что этот профиль активен, только если указано текущее перемещаемое условие.</span><span class="sxs-lookup"><span data-stu-id="c4913-133">Specifies that this profile is active only when the current roaming condition is the one specified.</span></span> <span data-ttu-id="c4913-134">В противном случае профиль неприменим и не может использоваться для активации контекста протокола данных пакетов (PDP).</span><span class="sxs-lookup"><span data-stu-id="c4913-134">Otherwise, the profile is not applicable, and cannot be used to activate a Packet Data Protocol (PDP) context.</span></span> <span data-ttu-id="c4913-135">Значение этого элемента должно быть допустимым значением <a href="simpletype-roamapplicabilitytype.md"><strong>роамаппликабилититипе</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="c4913-135">The value of this element must be a valid <a href="simpletype-roamapplicabilitytype.md"><strong>roamApplicabilityType</strong></a> value.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="c4913-136"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="c4913-136"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c4913-137">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="c4913-137">Parent Element</span></span></th>
<th><span data-ttu-id="c4913-138">Описание</span><span class="sxs-lookup"><span data-stu-id="c4913-138">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c4913-139"><a href="element-mbnprofileext.md">MBNProfileExt</a></span><span class="sxs-lookup"><span data-stu-id="c4913-139"><a href="element-mbnprofileext.md">MBNProfileExt</a></span></span></td>
<td><p><span data-ttu-id="c4913-140">Элемент <strong>мбнпрофиликст</strong> является расширением более раннего элемента мбнпрофиле.</span><span class="sxs-lookup"><span data-stu-id="c4913-140">The <strong>MBNProfileExt</strong> element is an extension of the earlier MBNProfile element.</span></span> <span data-ttu-id="c4913-141">Он определяет профиль мобильного широкополосного подключения с более широким набором параметров, чем элемент Мбнпрофиле.</span><span class="sxs-lookup"><span data-stu-id="c4913-141">It identifies a Mobile Broadband profile with a richer set of options than the MBNProfile element.</span></span></p>
<p><span data-ttu-id="c4913-142">В профиле может быть несколько элементов Мбнпрофиликст, описывающих параметры профиля для определенного набора условий.</span><span class="sxs-lookup"><span data-stu-id="c4913-142">There can be more than one MbnProfileExt element in a profile, describing profile settings for a particular set of operating conditions.</span></span> <span data-ttu-id="c4913-143">Используйте дочерний элемент <a href="element-profileconditionedon.md"><strong>профилекондитионедон</strong></a> из <strong>мбнпрофиликст</strong> , чтобы указать, какие операционные условия делают определенный профиль активным.</span><span class="sxs-lookup"><span data-stu-id="c4913-143">Use the <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> child element of <strong>MBNProfileExt</strong> to specify which operating conditions make a particular profile the active profile.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="c4913-144">Требования</span><span class="sxs-lookup"><span data-stu-id="c4913-144">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c4913-145">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c4913-145">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



