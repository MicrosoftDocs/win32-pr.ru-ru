---
description: ивланаппликабилити
MS-HAID: WWAN\_profile\_v4.element\_IwlanApplicability
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: ивланаппликабилити
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6b8b0376f2ee882a57e4c71e392fb7b02f6eeb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701479"
---
# <a name="span-idwwan_profile_v4element_iwlanapplicabilityspaniwlanapplicability"></a><span data-ttu-id="e8eda-103"><span id="WWAN_profile_v4.element_IwlanApplicability"></span>ивланаппликабилити</span><span class="sxs-lookup"><span data-stu-id="e8eda-103"><span id="WWAN_profile_v4.element_IwlanApplicability"></span>IwlanApplicability</span></span>

<span data-ttu-id="e8eda-104">Указывает, что этот профиль активен только при подключении к сети ИВЛАН.</span><span class="sxs-lookup"><span data-stu-id="e8eda-104">Specifies that this profile is active only when connected to an IWLAN network.</span></span> <span data-ttu-id="e8eda-105">В противном случае профиль неприменим и не может использоваться для активации контекста протокола данных пакетов (PDP).</span><span class="sxs-lookup"><span data-stu-id="e8eda-105">Otherwise, the profile is not applicable, and cannot be used to activate a Packet Data Protocol (PDP) context.</span></span> <span data-ttu-id="e8eda-106">Значение этого элемента должно быть допустимым значением [**ивланаппликабилититипе**](simpletype-iwlanapplicabilitytype.md) .</span><span class="sxs-lookup"><span data-stu-id="e8eda-106">The value of this element must be a valid [**iwlanApplicabilityType**](simpletype-iwlanapplicabilitytype.md) value.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="e8eda-107">Иерархия элементов</span><span class="sxs-lookup"><span data-stu-id="e8eda-107">Element hierarchy</span></span>

[<MBNProfileExt>](element-mbnprofileext.md)  
[<ProfileConditionedOn>](element-profileconditionedon.md)  
**<IwlanApplicability>**

## <a name="syntax"></a><span data-ttu-id="e8eda-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e8eda-108">Syntax</span></span>

``` syntax
<IwlanApplicability>

  "CellularOnly" | "CellularAndIwlan" | "IwlanOnly"

</IwlanApplicability>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="e8eda-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Атрибуты и элементы</span><span class="sxs-lookup"><span data-stu-id="e8eda-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="e8eda-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Атрибуты</span><span class="sxs-lookup"><span data-stu-id="e8eda-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="e8eda-111">Нет.</span><span class="sxs-lookup"><span data-stu-id="e8eda-111">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="e8eda-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="e8eda-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="e8eda-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="e8eda-113">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="e8eda-114"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="e8eda-114"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e8eda-115">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="e8eda-115">Parent Element</span></span></th>
<th><span data-ttu-id="e8eda-116">Описание</span><span class="sxs-lookup"><span data-stu-id="e8eda-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e8eda-117"><a href="element-profileconditionedon.md">профилекондитионедон</a></span><span class="sxs-lookup"><span data-stu-id="e8eda-117"><a href="element-profileconditionedon.md">ProfileConditionedOn</a></span></span></td>
<td><p><span data-ttu-id="e8eda-118">Указывает условия, которые должны быть удовлетворены для применения профиля.</span><span class="sxs-lookup"><span data-stu-id="e8eda-118">Specifies the conditions which must be satisfied for a profile to be applicable.</span></span></p>
<p><span data-ttu-id="e8eda-119">Этот элемент является новым для v4.</span><span class="sxs-lookup"><span data-stu-id="e8eda-119">This element is new for v4.</span></span> <span data-ttu-id="e8eda-120">Он позволяет указать несколько профилей, которые применяются в различных условиях, а также для автоматического использования соответствующего профиля.</span><span class="sxs-lookup"><span data-stu-id="e8eda-120">It enables you to specify multiple profiles that apply in different conditions, and for the proper profile to be used automatically when it is applicable.</span></span> <span data-ttu-id="e8eda-121">Этот элемент является необязательным.</span><span class="sxs-lookup"><span data-stu-id="e8eda-121">This element is optional.</span></span> <span data-ttu-id="e8eda-122">Если его не указать, профиль всегда будет применяться в соответствии с указанными условиями.</span><span class="sxs-lookup"><span data-stu-id="e8eda-122">If you do not specify it, then the profile is always applicable with respect to the conditions listed.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="e8eda-123">Требования</span><span class="sxs-lookup"><span data-stu-id="e8eda-123">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e8eda-124">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e8eda-124">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



