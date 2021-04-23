---
description: Модемдмконфигпрофиле \/ апнид (v4)
MS-HAID: WWAN\_profile\_v4.element\_1\_ApnID
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Апнид (v4)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a3838a632359fcdf7bc32004103f6f90163d988
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/05/2021
ms.locfileid: "106388865"
---
# <a name="span-idwwan_profile_v4element_1_apnidspanmodemdmconfigprofileapnid-v4"></a><span data-ttu-id="e3b5d-103"><span id="WWAN_profile_v4.element_1_ApnID"></span>Модемдмконфигпрофиле \/ апнид (v4)</span><span class="sxs-lookup"><span data-stu-id="e3b5d-103"><span id="WWAN_profile_v4.element_1_ApnID"></span>ModemDMConfigProfile\/ApnID (v4)</span></span>

<span data-ttu-id="e3b5d-104">Идентификатор APN, связанный с этим профилем. Этот элемент является новым в v4 и является необязательным.</span><span class="sxs-lookup"><span data-stu-id="e3b5d-104">An APN ID associated with this profile.This element is new in v4, and it is optional.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="e3b5d-105">Иерархия элементов</span><span class="sxs-lookup"><span data-stu-id="e3b5d-105">Element hierarchy</span></span>

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;**\<ApnID\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;**\<ApnID\>**

## <a name="syntax"></a><span data-ttu-id="e3b5d-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e3b5d-106">Syntax</span></span>

``` syntax
<ApnID>

  decimal

</ApnID>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="e3b5d-107"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Атрибуты и элементы</span><span class="sxs-lookup"><span data-stu-id="e3b5d-107"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="e3b5d-108"><span id="attributes"></span><span id="ATTRIBUTES"></span>Атрибуты</span><span class="sxs-lookup"><span data-stu-id="e3b5d-108"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="e3b5d-109">Отсутствует.</span><span class="sxs-lookup"><span data-stu-id="e3b5d-109">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="e3b5d-110"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="e3b5d-110"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="e3b5d-111">Отсутствует.</span><span class="sxs-lookup"><span data-stu-id="e3b5d-111">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="e3b5d-112"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="e3b5d-112"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e3b5d-113">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="e3b5d-113">Parent Element</span></span></th>
<th><span data-ttu-id="e3b5d-114">Описание</span><span class="sxs-lookup"><span data-stu-id="e3b5d-114">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e3b5d-115"><a href="element-mbnprofileext.md">MBNProfileExt</a></span><span class="sxs-lookup"><span data-stu-id="e3b5d-115"><a href="element-mbnprofileext.md">MBNProfileExt</a></span></span></td>
<td><p><span data-ttu-id="e3b5d-116">Элемент <strong>мбнпрофиликст</strong> является расширением более раннего элемента мбнпрофиле.</span><span class="sxs-lookup"><span data-stu-id="e3b5d-116">The <strong>MBNProfileExt</strong> element is an extension of the earlier MBNProfile element.</span></span> <span data-ttu-id="e3b5d-117">Он определяет профиль мобильного широкополосного подключения с более широким набором параметров, чем элемент Мбнпрофиле.</span><span class="sxs-lookup"><span data-stu-id="e3b5d-117">It identifies a Mobile Broadband profile with a richer set of options than the MBNProfile element.</span></span></p>
<p><span data-ttu-id="e3b5d-118">В профиле может быть несколько элементов Мбнпрофиликст, описывающих параметры профиля для определенного набора условий.</span><span class="sxs-lookup"><span data-stu-id="e3b5d-118">There can be more than one MbnProfileExt element in a profile, describing profile settings for a particular set of operating conditions.</span></span> <span data-ttu-id="e3b5d-119">Используйте дочерний элемент <a href="element-profileconditionedon.md"><strong>профилекондитионедон</strong></a> из <strong>мбнпрофиликст</strong> , чтобы указать, какие операционные условия делают определенный профиль активным.</span><span class="sxs-lookup"><span data-stu-id="e3b5d-119">Use the <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> child element of <strong>MBNProfileExt</strong> to specify which operating conditions make a particular profile the active profile.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e3b5d-120"><a href="element-modemdmconfigprofile.md">ModemDMConfigProfile</a></span><span class="sxs-lookup"><span data-stu-id="e3b5d-120"><a href="element-modemdmconfigprofile.md">ModemDMConfigProfile</a></span></span></td>
<td><p><span data-ttu-id="e3b5d-121">Профиль конфигурации DM для модема.</span><span class="sxs-lookup"><span data-stu-id="e3b5d-121">Modem DM configuration profile.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="e3b5d-122">Требования</span><span class="sxs-lookup"><span data-stu-id="e3b5d-122">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e3b5d-123">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e3b5d-123">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



