---
description: ислонгстандингаддитионалпдпконтекстпрофиле
MS-HAID: WWAN\_profile\_v4.element\_IsLongStandingAdditionalPdpContextProfile
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: ислонгстандингаддитионалпдпконтекстпрофиле
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a6ab30af9e71b8e9bde8284137c6bff86355f67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897538"
---
# <a name="span-idwwan_profile_v4element_islongstandingadditionalpdpcontextprofilespanislongstandingadditionalpdpcontextprofile"></a><span data-ttu-id="a250c-103"><span id="WWAN_profile_v4.element_IsLongStandingAdditionalPdpContextProfile"></span>ислонгстандингаддитионалпдпконтекстпрофиле</span><span class="sxs-lookup"><span data-stu-id="a250c-103"><span id="WWAN_profile_v4.element_IsLongStandingAdditionalPdpContextProfile"></span>IsLongStandingAdditionalPdpContextProfile</span></span>

<span data-ttu-id="a250c-104">Указывает, что этот профиль является долгосрочным дополнительным профилем контекста PDP. Если значение этого элемента равно **true**, то для [**исаддитионалпдпконтекстпрофиле**](/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)) также должно быть задано значение **true**.</span><span class="sxs-lookup"><span data-stu-id="a250c-104">Specifies that this profile is a long-standing additional PDP context profile.If the value of this element is **true**, then [**IsAdditionalPdpContextProfile**](/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)) must also be set to **true**.</span></span> <span data-ttu-id="a250c-105">Это новый элемент для v4.</span><span class="sxs-lookup"><span data-stu-id="a250c-105">This is a new element for v4.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="a250c-106">Иерархия элементов</span><span class="sxs-lookup"><span data-stu-id="a250c-106">Element hierarchy</span></span>

[<MBNProfileExt>](element-mbnprofileext.md)  
**<IsLongStandingAdditionalPdpContextProfile>**

## <a name="syntax"></a><span data-ttu-id="a250c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a250c-107">Syntax</span></span>

``` syntax
<IsLongStandingAdditionalPdpContextProfile>

  boolean

</IsLongStandingAdditionalPdpContextProfile>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="a250c-108"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Атрибуты и элементы</span><span class="sxs-lookup"><span data-stu-id="a250c-108"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="a250c-109"><span id="attributes"></span><span id="ATTRIBUTES"></span>Атрибуты</span><span class="sxs-lookup"><span data-stu-id="a250c-109"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="a250c-110">Нет.</span><span class="sxs-lookup"><span data-stu-id="a250c-110">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="a250c-111"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="a250c-111"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="a250c-112">Нет.</span><span class="sxs-lookup"><span data-stu-id="a250c-112">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="a250c-113"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="a250c-113"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a250c-114">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="a250c-114">Parent Element</span></span></th>
<th><span data-ttu-id="a250c-115">Описание</span><span class="sxs-lookup"><span data-stu-id="a250c-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a250c-116"><a href="element-mbnprofileext.md">MBNProfileExt</a></span><span class="sxs-lookup"><span data-stu-id="a250c-116"><a href="element-mbnprofileext.md">MBNProfileExt</a></span></span></td>
<td><p><span data-ttu-id="a250c-117">Элемент <strong>мбнпрофиликст</strong> является расширением более раннего элемента мбнпрофиле.</span><span class="sxs-lookup"><span data-stu-id="a250c-117">The <strong>MBNProfileExt</strong> element is an extension of the earlier MBNProfile element.</span></span> <span data-ttu-id="a250c-118">Он определяет профиль мобильного широкополосного подключения с более широким набором параметров, чем элемент Мбнпрофиле.</span><span class="sxs-lookup"><span data-stu-id="a250c-118">It identifies a Mobile Broadband profile with a richer set of options than the MBNProfile element.</span></span></p>
<p><span data-ttu-id="a250c-119">В профиле может быть несколько элементов Мбнпрофиликст, описывающих параметры профиля для определенного набора условий.</span><span class="sxs-lookup"><span data-stu-id="a250c-119">There can be more than one MbnProfileExt element in a profile, describing profile settings for a particular set of operating conditions.</span></span> <span data-ttu-id="a250c-120">Используйте дочерний элемент <a href="element-profileconditionedon.md"><strong>профилекондитионедон</strong></a> из <strong>мбнпрофиликст</strong> , чтобы указать, какие операционные условия делают определенный профиль активным.</span><span class="sxs-lookup"><span data-stu-id="a250c-120">Use the <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> child element of <strong>MBNProfileExt</strong> to specify which operating conditions make a particular profile the active profile.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="a250c-121">Требования</span><span class="sxs-lookup"><span data-stu-id="a250c-121">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a250c-122">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="a250c-122">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 
