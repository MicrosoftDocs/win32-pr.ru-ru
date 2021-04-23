---
description: исексклусиветусер
MS-HAID: WWAN\_profile\_v4.element\_IsExclusiveToOther
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: исексклусиветусер
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a948ad9b6a457f74e98eab745d851bdd2399c67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701480"
---
# <a name="span-idwwan_profile_v4element_isexclusivetootherspanisexclusivetoother"></a><span data-ttu-id="c481a-103"><span id="WWAN_profile_v4.element_IsExclusiveToOther"></span>исексклусиветусер</span><span class="sxs-lookup"><span data-stu-id="c481a-103"><span id="WWAN_profile_v4.element_IsExclusiveToOther"></span>IsExclusiveToOther</span></span>

<span data-ttu-id="c481a-104">Указывает, что этот профиль является эксклюзивным для других профилей того же набора профилей. Этот элемент является новым для v4.</span><span class="sxs-lookup"><span data-stu-id="c481a-104">Specifies that this profile is exclusive to other profiles of the same profile set(s).This element is new for v4.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="c481a-105">Иерархия элементов</span><span class="sxs-lookup"><span data-stu-id="c481a-105">Element hierarchy</span></span>

[<MBNProfileExt>](element-mbnprofileext.md)  
**<IsExclusiveToOther>**

## <a name="syntax"></a><span data-ttu-id="c481a-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c481a-106">Syntax</span></span>

``` syntax
<IsExclusiveToOther>

  boolean

</IsExclusiveToOther>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="c481a-107"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Атрибуты и элементы</span><span class="sxs-lookup"><span data-stu-id="c481a-107"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="c481a-108"><span id="attributes"></span><span id="ATTRIBUTES"></span>Атрибуты</span><span class="sxs-lookup"><span data-stu-id="c481a-108"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="c481a-109">Нет.</span><span class="sxs-lookup"><span data-stu-id="c481a-109">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="c481a-110"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="c481a-110"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="c481a-111">Нет.</span><span class="sxs-lookup"><span data-stu-id="c481a-111">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="c481a-112"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="c481a-112"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c481a-113">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="c481a-113">Parent Element</span></span></th>
<th><span data-ttu-id="c481a-114">Описание</span><span class="sxs-lookup"><span data-stu-id="c481a-114">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c481a-115"><a href="element-mbnprofileext.md">MBNProfileExt</a></span><span class="sxs-lookup"><span data-stu-id="c481a-115"><a href="element-mbnprofileext.md">MBNProfileExt</a></span></span></td>
<td><p><span data-ttu-id="c481a-116">Элемент <strong>мбнпрофиликст</strong> является расширением более раннего элемента мбнпрофиле.</span><span class="sxs-lookup"><span data-stu-id="c481a-116">The <strong>MBNProfileExt</strong> element is an extension of the earlier MBNProfile element.</span></span> <span data-ttu-id="c481a-117">Он определяет профиль мобильного широкополосного подключения с более широким набором параметров, чем элемент Мбнпрофиле.</span><span class="sxs-lookup"><span data-stu-id="c481a-117">It identifies a Mobile Broadband profile with a richer set of options than the MBNProfile element.</span></span></p>
<p><span data-ttu-id="c481a-118">В профиле может быть несколько элементов Мбнпрофиликст, описывающих параметры профиля для определенного набора условий.</span><span class="sxs-lookup"><span data-stu-id="c481a-118">There can be more than one MbnProfileExt element in a profile, describing profile settings for a particular set of operating conditions.</span></span> <span data-ttu-id="c481a-119">Используйте дочерний элемент <a href="element-profileconditionedon.md"><strong>профилекондитионедон</strong></a> из <strong>мбнпрофиликст</strong> , чтобы указать, какие операционные условия делают определенный профиль активным.</span><span class="sxs-lookup"><span data-stu-id="c481a-119">Use the <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> child element of <strong>MBNProfileExt</strong> to specify which operating conditions make a particular profile the active profile.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="c481a-120">Требования</span><span class="sxs-lookup"><span data-stu-id="c481a-120">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c481a-121">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c481a-121">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



