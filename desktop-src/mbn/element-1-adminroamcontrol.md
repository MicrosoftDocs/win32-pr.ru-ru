---
description: Модемдмконфигпрофиле \/ админроамконтрол (v4)
MS-HAID: WWAN\_profile\_v4.element\_1\_AdminRoamControl
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: админроамконтрол
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbaece25829412f04f6f82226b8edd274f4aaef9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144842"
---
# <a name="span-idwwan_profile_v4element_1_adminroamcontrolspanmodemdmconfigprofileadminroamcontrol-v4"></a><span data-ttu-id="a4d9a-103"><span id="WWAN_profile_v4.element_1_AdminRoamControl"></span>Модемдмконфигпрофиле \/ админроамконтрол (v4)</span><span class="sxs-lookup"><span data-stu-id="a4d9a-103"><span id="WWAN_profile_v4.element_1_AdminRoamControl"></span>ModemDMConfigProfile\/AdminRoamControl (v4)</span></span>

<span data-ttu-id="a4d9a-104">Указывает, управляется ли профиль административным роумингом.</span><span class="sxs-lookup"><span data-stu-id="a4d9a-104">Specifies whether the profile is administratively roam controlled.</span></span> <span data-ttu-id="a4d9a-105">Этот элемент является новым для v4.</span><span class="sxs-lookup"><span data-stu-id="a4d9a-105">This element is new for v4.</span></span> <span data-ttu-id="a4d9a-106">Значением этого элемента является значение [**роамконтролтипе**](simpletype-roamcontroltype.md) .</span><span class="sxs-lookup"><span data-stu-id="a4d9a-106">The value of this element is a [**roamControlType**](simpletype-roamcontroltype.md) value.</span></span> <span data-ttu-id="a4d9a-107">Это необязательный элемент. Если значение не указано, по умолчанию используется **аллроамалловед** .</span><span class="sxs-lookup"><span data-stu-id="a4d9a-107">This is an optional element; if no value is specified, then **AllRoamAllowed** is the default.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="a4d9a-108">Иерархия элементов</span><span class="sxs-lookup"><span data-stu-id="a4d9a-108">Element hierarchy</span></span>

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;**\<AdminRoamControl\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;**\<AdminRoamControl\>**

## <a name="syntax"></a><span data-ttu-id="a4d9a-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a4d9a-109">Syntax</span></span>

``` syntax
<AdminRoamControl>

  "AllRoamAllowed" | "PartnerRoamAllowed" | "NoRoamAllowed"

</AdminRoamControl>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="a4d9a-110"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Атрибуты и элементы</span><span class="sxs-lookup"><span data-stu-id="a4d9a-110"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="a4d9a-111"><span id="attributes"></span><span id="ATTRIBUTES"></span>Атрибуты</span><span class="sxs-lookup"><span data-stu-id="a4d9a-111"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="a4d9a-112">Нет.</span><span class="sxs-lookup"><span data-stu-id="a4d9a-112">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="a4d9a-113"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="a4d9a-113"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="a4d9a-114">Нет.</span><span class="sxs-lookup"><span data-stu-id="a4d9a-114">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="a4d9a-115"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="a4d9a-115"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a4d9a-116">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="a4d9a-116">Parent Element</span></span></th>
<th><span data-ttu-id="a4d9a-117">Описание</span><span class="sxs-lookup"><span data-stu-id="a4d9a-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a4d9a-118"><a href="element-mbnprofileext.md">MBNProfileExt</a></span><span class="sxs-lookup"><span data-stu-id="a4d9a-118"><a href="element-mbnprofileext.md">MBNProfileExt</a></span></span></td>
<td><p><span data-ttu-id="a4d9a-119">Элемент <strong>мбнпрофиликст</strong> является расширением более раннего элемента мбнпрофиле.</span><span class="sxs-lookup"><span data-stu-id="a4d9a-119">The <strong>MBNProfileExt</strong> element is an extension of the earlier MBNProfile element.</span></span> <span data-ttu-id="a4d9a-120">Он определяет профиль мобильного широкополосного подключения с более широким набором параметров, чем элемент Мбнпрофиле.</span><span class="sxs-lookup"><span data-stu-id="a4d9a-120">It identifies a Mobile Broadband profile with a richer set of options than the MBNProfile element.</span></span></p>
<p><span data-ttu-id="a4d9a-121">В профиле может быть несколько элементов Мбнпрофиликст, описывающих параметры профиля для определенного набора условий.</span><span class="sxs-lookup"><span data-stu-id="a4d9a-121">There can be more than one MbnProfileExt element in a profile, describing profile settings for a particular set of operating conditions.</span></span> <span data-ttu-id="a4d9a-122">Используйте дочерний элемент <a href="element-profileconditionedon.md"><strong>профилекондитионедон</strong></a> из <strong>мбнпрофиликст</strong> , чтобы указать, какие операционные условия делают определенный профиль активным.</span><span class="sxs-lookup"><span data-stu-id="a4d9a-122">Use the <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> child element of <strong>MBNProfileExt</strong> to specify which operating conditions make a particular profile the active profile.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d9a-123"><a href="element-modemdmconfigprofile.md">ModemDMConfigProfile</a></span><span class="sxs-lookup"><span data-stu-id="a4d9a-123"><a href="element-modemdmconfigprofile.md">ModemDMConfigProfile</a></span></span></td>
<td><p><span data-ttu-id="a4d9a-124">Профиль конфигурации DM для модема.</span><span class="sxs-lookup"><span data-stu-id="a4d9a-124">Modem DM configuration profile.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="a4d9a-125">Требования</span><span class="sxs-lookup"><span data-stu-id="a4d9a-125">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a4d9a-126">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="a4d9a-126">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



