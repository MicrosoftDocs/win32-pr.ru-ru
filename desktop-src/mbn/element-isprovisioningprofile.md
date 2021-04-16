---
description: испровисионингпрофиле
MS-HAID: WWAN\_profile\_v4.element\_IsProvisioningProfile
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: испровисионингпрофиле
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be857d96473fa81f0bf72580ced811de56eb2436
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692250"
---
# <a name="span-idwwan_profile_v4element_isprovisioningprofilespanisprovisioningprofile"></a><span data-ttu-id="f6a7a-103"><span id="WWAN_profile_v4.element_IsProvisioningProfile"></span>испровисионингпрофиле</span><span class="sxs-lookup"><span data-stu-id="f6a7a-103"><span id="WWAN_profile_v4.element_IsProvisioningProfile"></span>IsProvisioningProfile</span></span>

<span data-ttu-id="f6a7a-104">Указывает, что этот профиль должен использоваться только для подготовки. В противном случае профиль неприменим и не может использоваться для активации контекста протокола данных пакетов (PDP).</span><span class="sxs-lookup"><span data-stu-id="f6a7a-104">Specifies that this profile is to be used for provisioning only.Otherwise, the profile is not applicable, and cannot be used to activate a Packet Data Protocol (PDP) context.</span></span> <span data-ttu-id="f6a7a-105">Этот элемент является новым для v4.</span><span class="sxs-lookup"><span data-stu-id="f6a7a-105">This element is new for v4.</span></span>

<span data-ttu-id="f6a7a-106">Если **испровисионингпрофиле** имеет значение true, то значение [**по умолчанию**](element-isdefault.md) должно быть равно false, а [**ConnectionMode**](element-connectionmode.md) — вручную.</span><span class="sxs-lookup"><span data-stu-id="f6a7a-106">If **IsProvisioningProfile** is true, [**IsDefault**](element-isdefault.md) must be false, and [**ConnectionMode**](element-connectionmode.md) must be manual.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="f6a7a-107">Иерархия элементов</span><span class="sxs-lookup"><span data-stu-id="f6a7a-107">Element hierarchy</span></span>

[<MBNProfileExt>](element-mbnprofileext.md)  
**<IsProvisioningProfile>**

## <a name="syntax"></a><span data-ttu-id="f6a7a-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f6a7a-108">Syntax</span></span>

``` syntax
<IsProvisioningProfile>

  boolean

</IsProvisioningProfile>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="f6a7a-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Атрибуты и элементы</span><span class="sxs-lookup"><span data-stu-id="f6a7a-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="f6a7a-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Атрибуты</span><span class="sxs-lookup"><span data-stu-id="f6a7a-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="f6a7a-111">Нет.</span><span class="sxs-lookup"><span data-stu-id="f6a7a-111">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="f6a7a-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="f6a7a-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="f6a7a-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="f6a7a-113">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="f6a7a-114"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="f6a7a-114"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f6a7a-115">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="f6a7a-115">Parent Element</span></span></th>
<th><span data-ttu-id="f6a7a-116">Описание</span><span class="sxs-lookup"><span data-stu-id="f6a7a-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f6a7a-117"><a href="element-mbnprofileext.md">MBNProfileExt</a></span><span class="sxs-lookup"><span data-stu-id="f6a7a-117"><a href="element-mbnprofileext.md">MBNProfileExt</a></span></span></td>
<td><p><span data-ttu-id="f6a7a-118">Элемент <strong>мбнпрофиликст</strong> является расширением более раннего элемента мбнпрофиле.</span><span class="sxs-lookup"><span data-stu-id="f6a7a-118">The <strong>MBNProfileExt</strong> element is an extension of the earlier MBNProfile element.</span></span> <span data-ttu-id="f6a7a-119">Он определяет профиль мобильного широкополосного подключения с более широким набором параметров, чем элемент Мбнпрофиле.</span><span class="sxs-lookup"><span data-stu-id="f6a7a-119">It identifies a Mobile Broadband profile with a richer set of options than the MBNProfile element.</span></span></p>
<p><span data-ttu-id="f6a7a-120">В профиле может быть несколько элементов Мбнпрофиликст, описывающих параметры профиля для определенного набора условий.</span><span class="sxs-lookup"><span data-stu-id="f6a7a-120">There can be more than one MbnProfileExt element in a profile, describing profile settings for a particular set of operating conditions.</span></span> <span data-ttu-id="f6a7a-121">Используйте дочерний элемент <a href="element-profileconditionedon.md"><strong>профилекондитионедон</strong></a> из <strong>мбнпрофиликст</strong> , чтобы указать, какие операционные условия делают определенный профиль активным.</span><span class="sxs-lookup"><span data-stu-id="f6a7a-121">Use the <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> child element of <strong>MBNProfileExt</strong> to specify which operating conditions make a particular profile the active profile.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="f6a7a-122">Требования</span><span class="sxs-lookup"><span data-stu-id="f6a7a-122">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f6a7a-123">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f6a7a-123">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



