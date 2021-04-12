---
description: MmsMaximumMessageSize
MS-HAID: WWAN\_profile\_v4.element\_MmsMaximumMessageSize
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: MmsMaximumMessageSize
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c5b020e7fd6ad4f39bd488c3af0ef14a3aab1eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263183"
---
# <a name="span-idwwan_profile_v4element_mmsmaximummessagesizespanmmsmaximummessagesize"></a><span data-ttu-id="917b5-103"><span id="WWAN_profile_v4.element_MmsMaximumMessageSize"></span>ммсмаксимуммессажесизе</span><span class="sxs-lookup"><span data-stu-id="917b5-103"><span id="WWAN_profile_v4.element_MmsMaximumMessageSize"></span>MmsMaximumMessageSize</span></span>

<span data-ttu-id="917b5-104">Указывает максимальный размер MMS сообщений в килобайтах.</span><span class="sxs-lookup"><span data-stu-id="917b5-104">Specifies the maximum size of MMS messages, in kilobytes.</span></span> <span data-ttu-id="917b5-105">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="917b5-105">Optional.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="917b5-106">Иерархия элементов</span><span class="sxs-lookup"><span data-stu-id="917b5-106">Element hierarchy</span></span>

[<MBNProfileExt>](element-mbnprofileext.md)  
[<MmsConfiguration>](element-mmsconfiguration.md)  
**<MmsMaximumMessageSize>**

## <a name="syntax"></a><span data-ttu-id="917b5-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="917b5-107">Syntax</span></span>

``` syntax
<MmsMaximumMessageSize>

  nonNegativeInteger

</MmsMaximumMessageSize>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="917b5-108"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Атрибуты и элементы</span><span class="sxs-lookup"><span data-stu-id="917b5-108"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="917b5-109"><span id="attributes"></span><span id="ATTRIBUTES"></span>Атрибуты</span><span class="sxs-lookup"><span data-stu-id="917b5-109"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="917b5-110">Нет.</span><span class="sxs-lookup"><span data-stu-id="917b5-110">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="917b5-111"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="917b5-111"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="917b5-112">Нет.</span><span class="sxs-lookup"><span data-stu-id="917b5-112">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="917b5-113"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="917b5-113"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="917b5-114">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="917b5-114">Parent Element</span></span></th>
<th><span data-ttu-id="917b5-115">Описание</span><span class="sxs-lookup"><span data-stu-id="917b5-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="917b5-116"><a href="element-mmsconfiguration.md">ммсконфигуратион</a></span><span class="sxs-lookup"><span data-stu-id="917b5-116"><a href="element-mmsconfiguration.md">MmsConfiguration</a></span></span></td>
<td><p><span data-ttu-id="917b5-117">Сведения о конфигурации для службы обмена сообщениями мультимедиа (MMS).</span><span class="sxs-lookup"><span data-stu-id="917b5-117">Configuration information for Multimedia Messaging Service (MMS).</span></span></p>
<p><span data-ttu-id="917b5-118">Помимо настройки элементов конфигурации в этом элементе, профиль MMS должен иметь следующие параметры.</span><span class="sxs-lookup"><span data-stu-id="917b5-118">In addition to setting the configuration elements within this element, an MMS profile must have the following settings.</span></span></p>
<ul>
<li><span data-ttu-id="917b5-119">Его элемент <a href="element-name.md"><strong>Name</strong></a> должен содержать уникальное для всей системы имя.</span><span class="sxs-lookup"><span data-stu-id="917b5-119">Its <a href="element-name.md"><strong>Name</strong></a> element must contain a system-wide unique name.</span></span></li>
<li><span data-ttu-id="917b5-120">Его <a href="../mbn/schema-profilecreationtype-mbnprofile-element.md"><strong>профилекреатионтипе</strong></a> должен быть установлен в значение <strong>усерпровисионед</strong>.</span><span class="sxs-lookup"><span data-stu-id="917b5-120">Its <a href="../mbn/schema-profilecreationtype-mbnprofile-element.md"><strong>ProfileCreationType</strong></a> must be set to <strong>UserProvisioned</strong>.</span></span></li>
<li><span data-ttu-id="917b5-121">Его <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid"><strong>симикЦид</strong></a> должен содержать ICCID SIM-карты, для которой предназначен этот профиль.</span><span class="sxs-lookup"><span data-stu-id="917b5-121">Its <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid"><strong>SimIccID</strong></a> must contain the ICCID of the SIM that this profile is intended for.</span></span></li>
<li><span data-ttu-id="917b5-122">Его <a href="../mbn/schema-connectionmode-mbnprofile-element.md"><strong>ConnectionMode</strong></a> должен быть установлен в значение " <strong>вручную</strong>".</span><span class="sxs-lookup"><span data-stu-id="917b5-122">Its <a href="../mbn/schema-connectionmode-mbnprofile-element.md"><strong>ConnectionMode</strong></a> must be set to <strong>Manual</strong>.</span></span></li>
<li><span data-ttu-id="917b5-123">Его <a href="element-purposegroupguid.md"><strong>пурпосеграупгуид</strong></a> должен содержать GUID для группы целей MMS.</span><span class="sxs-lookup"><span data-stu-id="917b5-123">Its <a href="element-purposegroupguid.md"><strong>PurposeGroupGuid</strong></a> must contain the GUID for MMS purpose group.</span></span></li>
<li><span data-ttu-id="917b5-124">Его <a href="/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)"><strong>исаддитионалпдпконтекстпрофиле</strong></a> должен быть установлен в <strong>значение true</strong>.</span><span class="sxs-lookup"><span data-stu-id="917b5-124">Its <a href="/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)"><strong>IsAdditionalPdpContextProfile</strong></a> must be set to <strong>true</strong>.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="917b5-125">Требования</span><span class="sxs-lookup"><span data-stu-id="917b5-125">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="917b5-126">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="917b5-126">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 
