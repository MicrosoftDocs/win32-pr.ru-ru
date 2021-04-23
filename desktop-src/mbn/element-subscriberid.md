---
description: субскриберид
MS-HAID: WWAN\_profile\_v4.element\_SubscriberID
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: субскриберид
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 525cd75dbf1ab752ab17ea32d566e57977ab74a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682663"
---
# <a name="span-idwwan_profile_v4element_subscriberidspansubscriberid"></a><span data-ttu-id="6fe0a-103"><span id="WWAN_profile_v4.element_SubscriberID"></span>субскриберид</span><span class="sxs-lookup"><span data-stu-id="6fe0a-103"><span id="WWAN_profile_v4.element_SubscriberID"></span>SubscriberID</span></span>

<span data-ttu-id="6fe0a-104">Определяет уникальный идентификатор профиля.</span><span class="sxs-lookup"><span data-stu-id="6fe0a-104">Identifies the unique identifier of the profile.</span></span>

<span data-ttu-id="6fe0a-105">Для сети GSM оно должно содержать IMSI (Международный идентификатор мобильного подписчика) SIM-карты и устройства CDMA, которые должны содержать минимальное значение (мобильный идентификационный номер) устройства.</span><span class="sxs-lookup"><span data-stu-id="6fe0a-105">For a GSM network this should contain the IMSI (International Mobile Subscriber Identity) of the SIM and for CDMA devices it should contain the MIN (Mobile Identification Number) of the device.</span></span>

<span data-ttu-id="6fe0a-106">Дополнительные сведения см. в документации по элементу [**субскриберид**](./schema-subscriberid-mbnprofile-element.md) v1.</span><span class="sxs-lookup"><span data-stu-id="6fe0a-106">For more information, see the documentation for the v1 [**SubscriberID**](./schema-subscriberid-mbnprofile-element.md) element.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="6fe0a-107">Иерархия элементов</span><span class="sxs-lookup"><span data-stu-id="6fe0a-107">Element hierarchy</span></span>

[<MBNProfileExt>](element-mbnprofileext.md)  
**<SubscriberID>**

## <a name="syntax"></a><span data-ttu-id="6fe0a-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6fe0a-108">Syntax</span></span>

``` syntax
<SubscriberID>

  subscriberIdType

</SubscriberID>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="6fe0a-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Атрибуты и элементы</span><span class="sxs-lookup"><span data-stu-id="6fe0a-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="6fe0a-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Атрибуты</span><span class="sxs-lookup"><span data-stu-id="6fe0a-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="6fe0a-111">Нет.</span><span class="sxs-lookup"><span data-stu-id="6fe0a-111">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="6fe0a-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="6fe0a-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="6fe0a-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="6fe0a-113">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="6fe0a-114"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="6fe0a-114"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6fe0a-115">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="6fe0a-115">Parent Element</span></span></th>
<th><span data-ttu-id="6fe0a-116">Описание</span><span class="sxs-lookup"><span data-stu-id="6fe0a-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6fe0a-117"><a href="element-mbnprofileext.md">MBNProfileExt</a></span><span class="sxs-lookup"><span data-stu-id="6fe0a-117"><a href="element-mbnprofileext.md">MBNProfileExt</a></span></span></td>
<td><p><span data-ttu-id="6fe0a-118">Элемент <strong>мбнпрофиликст</strong> является расширением более раннего элемента мбнпрофиле.</span><span class="sxs-lookup"><span data-stu-id="6fe0a-118">The <strong>MBNProfileExt</strong> element is an extension of the earlier MBNProfile element.</span></span> <span data-ttu-id="6fe0a-119">Он определяет профиль мобильного широкополосного подключения с более широким набором параметров, чем элемент Мбнпрофиле.</span><span class="sxs-lookup"><span data-stu-id="6fe0a-119">It identifies a Mobile Broadband profile with a richer set of options than the MBNProfile element.</span></span></p>
<p><span data-ttu-id="6fe0a-120">В профиле может быть несколько элементов Мбнпрофиликст, описывающих параметры профиля для определенного набора условий.</span><span class="sxs-lookup"><span data-stu-id="6fe0a-120">There can be more than one MbnProfileExt element in a profile, describing profile settings for a particular set of operating conditions.</span></span> <span data-ttu-id="6fe0a-121">Используйте дочерний элемент <a href="element-profileconditionedon.md"><strong>профилекондитионедон</strong></a> из <strong>мбнпрофиликст</strong> , чтобы указать, какие операционные условия делают определенный профиль активным.</span><span class="sxs-lookup"><span data-stu-id="6fe0a-121">Use the <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> child element of <strong>MBNProfileExt</strong> to specify which operating conditions make a particular profile the active profile.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="6fe0a-122">Требования</span><span class="sxs-lookup"><span data-stu-id="6fe0a-122">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6fe0a-123">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="6fe0a-123">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 
