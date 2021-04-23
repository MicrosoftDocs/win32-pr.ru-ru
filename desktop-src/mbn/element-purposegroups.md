---
description: пурпосеграупс
MS-HAID: WWAN\_profile\_v4.element\_PurposeGroups
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: пурпосеграупс
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 370cf6b0dc13848ca21a2a06e0b9806d753878c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692248"
---
# <a name="span-idwwan_profile_v4element_purposegroupsspanpurposegroups"></a><span data-ttu-id="95943-103"><span id="WWAN_profile_v4.element_PurposeGroups"></span>пурпосеграупс</span><span class="sxs-lookup"><span data-stu-id="95943-103"><span id="WWAN_profile_v4.element_PurposeGroups"></span>PurposeGroups</span></span>

<span data-ttu-id="95943-104">Необязательный список групп профилей, где каждая группа включает профили, используемые для общего назначения.</span><span class="sxs-lookup"><span data-stu-id="95943-104">An optional list of groups of profiles, where each group includes profiles used for a common purpose.</span></span>

<span data-ttu-id="95943-105">Этот элемент является новым для V4 схемы.</span><span class="sxs-lookup"><span data-stu-id="95943-105">This element is new for v4 of the schema.</span></span>

<span data-ttu-id="95943-106">Один профиль может быть указан в нескольких группах.</span><span class="sxs-lookup"><span data-stu-id="95943-106">One profile can be listed in multiple groups.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="95943-107">Иерархия элементов</span><span class="sxs-lookup"><span data-stu-id="95943-107">Element hierarchy</span></span>

[<MBNProfileExt>](element-mbnprofileext.md)  
**<PurposeGroups>**

## <a name="syntax"></a><span data-ttu-id="95943-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="95943-108">Syntax</span></span>

``` syntax
<PurposeGroups>

  <!-- Child elements -->
  PurposeGroupGuid{1,10}

</PurposeGroups>
```

### <a name="key"></a><span data-ttu-id="95943-109">Ключ</span><span class="sxs-lookup"><span data-stu-id="95943-109">Key</span></span>

<span data-ttu-id="95943-110">`{}`   конкретный диапазон вхождений</span><span class="sxs-lookup"><span data-stu-id="95943-110">`{}`   specific range of occurrences</span></span>

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="95943-111"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Атрибуты и элементы</span><span class="sxs-lookup"><span data-stu-id="95943-111"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="95943-112"><span id="attributes"></span><span id="ATTRIBUTES"></span>Атрибуты</span><span class="sxs-lookup"><span data-stu-id="95943-112"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="95943-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="95943-113">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="95943-114"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="95943-114"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="95943-115">Дочерний элемент</span><span class="sxs-lookup"><span data-stu-id="95943-115">Child Element</span></span></th>
<th><span data-ttu-id="95943-116">Описание</span><span class="sxs-lookup"><span data-stu-id="95943-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="95943-117"><a href="element-purposegroupguid.md">пурпосеграупгуид</a></span><span class="sxs-lookup"><span data-stu-id="95943-117"><a href="element-purposegroupguid.md">PurposeGroupGuid</a></span></span></td>
<td><p><span data-ttu-id="95943-118">Представляет один профиль в Пурпосеграуп профилей.</span><span class="sxs-lookup"><span data-stu-id="95943-118">Represents one profile in a PurposeGroup of profiles.</span></span></p>
<p><span data-ttu-id="95943-119">Профили указываются по значению <a href="simpletype-guidtype.md"><strong>гуидтипе</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="95943-119">Profiles are specified by their <a href="simpletype-guidtype.md"><strong>guidType</strong></a> value.</span></span></p>
<p><span data-ttu-id="95943-120">Определены четыре значения GUID, перечисленные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="95943-120">Four GUID values are defined, as listed in the following table.</span></span></p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="95943-121">Целевая группа</span><span class="sxs-lookup"><span data-stu-id="95943-121">Purpose group</span></span></th>
<th><span data-ttu-id="95943-122">Код GUID</span><span class="sxs-lookup"><span data-stu-id="95943-122">GUID</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="95943-123">Интернет</span><span class="sxs-lookup"><span data-stu-id="95943-123">Internet</span></span></td>
<td><span data-ttu-id="95943-124">3E5545D2-1137-4DC8-A198-33F1C657515F</span><span class="sxs-lookup"><span data-stu-id="95943-124">3E5545D2-1137-4DC8-A198-33F1C657515F</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95943-125">MMS</span><span class="sxs-lookup"><span data-stu-id="95943-125">MMS</span></span></td>
<td><span data-ttu-id="95943-126">53E2C5D3-D13C-4068-AA38-9C48FF2E55A8</span><span class="sxs-lookup"><span data-stu-id="95943-126">53E2C5D3-D13C-4068-AA38-9C48FF2E55A8</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95943-127">IMS</span><span class="sxs-lookup"><span data-stu-id="95943-127">IMS</span></span></td>
<td><span data-ttu-id="95943-128">474D66ED-0E4B-476B-A455-19BB1239ED13</span><span class="sxs-lookup"><span data-stu-id="95943-128">474D66ED-0E4B-476B-A455-19BB1239ED13</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95943-129">супл</span><span class="sxs-lookup"><span data-stu-id="95943-129">SUPL</span></span></td>
<td><span data-ttu-id="95943-130">6D42669F-52A9-408E-9493-1071DCC437BD</span><span class="sxs-lookup"><span data-stu-id="95943-130">6D42669F-52A9-408E-9493-1071DCC437BD</span></span></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>

 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="95943-131"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="95943-131"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="95943-132">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="95943-132">Parent Element</span></span></th>
<th><span data-ttu-id="95943-133">Описание</span><span class="sxs-lookup"><span data-stu-id="95943-133">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="95943-134"><a href="element-mbnprofileext.md">MBNProfileExt</a></span><span class="sxs-lookup"><span data-stu-id="95943-134"><a href="element-mbnprofileext.md">MBNProfileExt</a></span></span></td>
<td><p><span data-ttu-id="95943-135">Элемент <strong>мбнпрофиликст</strong> является расширением более раннего элемента мбнпрофиле.</span><span class="sxs-lookup"><span data-stu-id="95943-135">The <strong>MBNProfileExt</strong> element is an extension of the earlier MBNProfile element.</span></span> <span data-ttu-id="95943-136">Он определяет профиль мобильного широкополосного подключения с более широким набором параметров, чем элемент Мбнпрофиле.</span><span class="sxs-lookup"><span data-stu-id="95943-136">It identifies a Mobile Broadband profile with a richer set of options than the MBNProfile element.</span></span></p>
<p><span data-ttu-id="95943-137">В профиле может быть несколько элементов Мбнпрофиликст, описывающих параметры профиля для определенного набора условий.</span><span class="sxs-lookup"><span data-stu-id="95943-137">There can be more than one MbnProfileExt element in a profile, describing profile settings for a particular set of operating conditions.</span></span> <span data-ttu-id="95943-138">Используйте дочерний элемент <a href="element-profileconditionedon.md"><strong>профилекондитионедон</strong></a> из <strong>мбнпрофиликст</strong> , чтобы указать, какие операционные условия делают определенный профиль активным.</span><span class="sxs-lookup"><span data-stu-id="95943-138">Use the <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> child element of <strong>MBNProfileExt</strong> to specify which operating conditions make a particular profile the active profile.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="95943-139">Требования</span><span class="sxs-lookup"><span data-stu-id="95943-139">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="95943-140">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="95943-140">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



