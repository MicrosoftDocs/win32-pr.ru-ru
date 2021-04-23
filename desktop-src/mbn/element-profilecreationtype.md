---
description: Профилекреатионтипе (в Мбнпрофиликст)
MS-HAID: WWAN\_profile\_v4.element\_ProfileCreationType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Профилекреатионтипе (в Мбнпрофиликст)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b56e09a18721bfa7d5f33d8e7511122f3d731f4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810115"
---
# <a name="span-idwwan_profile_v4element_profilecreationtypespanprofilecreationtype-in-mbnprofileext"></a><span data-ttu-id="35ffc-103"><span id="WWAN_profile_v4.element_ProfileCreationType"></span>Профилекреатионтипе (в Мбнпрофиликст)</span><span class="sxs-lookup"><span data-stu-id="35ffc-103"><span id="WWAN_profile_v4.element_ProfileCreationType"></span>ProfileCreationType (in MBNProfileExt)</span></span>

<span data-ttu-id="35ffc-104">Указывает создателя профиля.</span><span class="sxs-lookup"><span data-stu-id="35ffc-104">Specifies the creator of the profile.</span></span>

<span data-ttu-id="35ffc-105">Дополнительные сведения об этом элементе см. в документации по элементу [**профилекреатионтипе**](./schema-profilecreationtype-mbnprofile-element.md) v1.</span><span class="sxs-lookup"><span data-stu-id="35ffc-105">For more information about this element, see the documentation for the v1 [**ProfileCreationType**](./schema-profilecreationtype-mbnprofile-element.md) element.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="35ffc-106">Иерархия элементов</span><span class="sxs-lookup"><span data-stu-id="35ffc-106">Element hierarchy</span></span>

[<MBNProfileExt>](element-mbnprofileext.md)  
**<ProfileCreationType>**

## <a name="syntax"></a><span data-ttu-id="35ffc-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="35ffc-107">Syntax</span></span>

``` syntax
<ProfileCreationType>

  "UserProvisioned" | "AdminProvisioned" | "OperatorProvisioned" | "DeviceProvisioned"

</ProfileCreationType>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="35ffc-108"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Атрибуты и элементы</span><span class="sxs-lookup"><span data-stu-id="35ffc-108"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="35ffc-109"><span id="attributes"></span><span id="ATTRIBUTES"></span>Атрибуты</span><span class="sxs-lookup"><span data-stu-id="35ffc-109"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="35ffc-110">Нет.</span><span class="sxs-lookup"><span data-stu-id="35ffc-110">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="35ffc-111"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="35ffc-111"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="35ffc-112">Нет.</span><span class="sxs-lookup"><span data-stu-id="35ffc-112">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="35ffc-113"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="35ffc-113"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="35ffc-114">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="35ffc-114">Parent Element</span></span></th>
<th><span data-ttu-id="35ffc-115">Описание</span><span class="sxs-lookup"><span data-stu-id="35ffc-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="35ffc-116"><a href="element-mbnprofileext.md">MBNProfileExt</a></span><span class="sxs-lookup"><span data-stu-id="35ffc-116"><a href="element-mbnprofileext.md">MBNProfileExt</a></span></span></td>
<td><p><span data-ttu-id="35ffc-117">Элемент <strong>мбнпрофиликст</strong> является расширением более раннего элемента мбнпрофиле.</span><span class="sxs-lookup"><span data-stu-id="35ffc-117">The <strong>MBNProfileExt</strong> element is an extension of the earlier MBNProfile element.</span></span> <span data-ttu-id="35ffc-118">Он определяет профиль мобильного широкополосного подключения с более широким набором параметров, чем элемент Мбнпрофиле.</span><span class="sxs-lookup"><span data-stu-id="35ffc-118">It identifies a Mobile Broadband profile with a richer set of options than the MBNProfile element.</span></span></p>
<p><span data-ttu-id="35ffc-119">В профиле может быть несколько элементов Мбнпрофиликст, описывающих параметры профиля для определенного набора условий.</span><span class="sxs-lookup"><span data-stu-id="35ffc-119">There can be more than one MbnProfileExt element in a profile, describing profile settings for a particular set of operating conditions.</span></span> <span data-ttu-id="35ffc-120">Используйте дочерний элемент <a href="element-profileconditionedon.md"><strong>профилекондитионедон</strong></a> из <strong>мбнпрофиликст</strong> , чтобы указать, какие операционные условия делают определенный профиль активным.</span><span class="sxs-lookup"><span data-stu-id="35ffc-120">Use the <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> child element of <strong>MBNProfileExt</strong> to specify which operating conditions make a particular profile the active profile.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="related-elements"></a><span data-ttu-id="35ffc-121">Связанные элементы</span><span class="sxs-lookup"><span data-stu-id="35ffc-121">Related elements</span></span>

<span data-ttu-id="35ffc-122">Следующие элементы имеют то же имя, что и это одно, но различное содержимое или атрибуты:</span><span class="sxs-lookup"><span data-stu-id="35ffc-122">The following elements have the same name as this one, but different content or attributes:</span></span>

-   <span data-ttu-id="35ffc-123">**[Профилекреатионтипе (в Модемдмконфигпрофиле)](element-1-profilecreationtype.md)**</span><span class="sxs-lookup"><span data-stu-id="35ffc-123">**[ProfileCreationType (in ModemDMConfigProfile)](element-1-profilecreationtype.md)**</span></span>

## <a name="requirements"></a><span data-ttu-id="35ffc-124">Требования</span><span class="sxs-lookup"><span data-stu-id="35ffc-124">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="35ffc-125">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="35ffc-125">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 
