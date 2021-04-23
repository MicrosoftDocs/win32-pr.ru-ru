---
description: MmscUrl
MS-HAID: WWAN\_profile\_v4.element\_MmscUrl
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: MmscUrl
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 319146573e4782365b7db67c453a0866f198d61b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991100"
---
# <a name="span-idwwan_profile_v4element_mmscurlspanmmscurl"></a><span data-ttu-id="991d6-103"><span id="WWAN_profile_v4.element_MmscUrl"></span>ммскурл</span><span class="sxs-lookup"><span data-stu-id="991d6-103"><span id="WWAN_profile_v4.element_MmscUrl"></span>MmscUrl</span></span>

<span data-ttu-id="991d6-104">Указывает URL-адрес сервера ММСК для устройства.</span><span class="sxs-lookup"><span data-stu-id="991d6-104">Specifies the URL of the MMSC server for the device.</span></span> <span data-ttu-id="991d6-105">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="991d6-105">Optional.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="991d6-106">Иерархия элементов</span><span class="sxs-lookup"><span data-stu-id="991d6-106">Element hierarchy</span></span>

[<MBNProfileExt>](element-mbnprofileext.md)  
[<MmsConfiguration>](element-mmsconfiguration.md)  
**<MmscUrl>**

## <a name="syntax"></a><span data-ttu-id="991d6-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="991d6-107">Syntax</span></span>

``` syntax
<MmscUrl>

  anyURI

</MmscUrl>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="991d6-108"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Атрибуты и элементы</span><span class="sxs-lookup"><span data-stu-id="991d6-108"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="991d6-109"><span id="attributes"></span><span id="ATTRIBUTES"></span>Атрибуты</span><span class="sxs-lookup"><span data-stu-id="991d6-109"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="991d6-110">Нет.</span><span class="sxs-lookup"><span data-stu-id="991d6-110">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="991d6-111"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="991d6-111"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="991d6-112">Нет.</span><span class="sxs-lookup"><span data-stu-id="991d6-112">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="991d6-113"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="991d6-113"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="991d6-114">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="991d6-114">Parent Element</span></span></th>
<th><span data-ttu-id="991d6-115">Описание</span><span class="sxs-lookup"><span data-stu-id="991d6-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="991d6-116"><a href="element-mmsconfiguration.md">ммсконфигуратион</a></span><span class="sxs-lookup"><span data-stu-id="991d6-116"><a href="element-mmsconfiguration.md">MmsConfiguration</a></span></span></td>
<td><p><span data-ttu-id="991d6-117">Сведения о конфигурации для службы обмена сообщениями мультимедиа (MMS).</span><span class="sxs-lookup"><span data-stu-id="991d6-117">Configuration information for Multimedia Messaging Service (MMS).</span></span></p>
<p><span data-ttu-id="991d6-118">Помимо настройки элементов конфигурации в этом элементе, профиль MMS должен иметь следующие параметры.</span><span class="sxs-lookup"><span data-stu-id="991d6-118">In addition to setting the configuration elements within this element, an MMS profile must have the following settings.</span></span></p>
<ul>
<li><span data-ttu-id="991d6-119">Его элемент <a href="element-name.md"><strong>Name</strong></a> должен содержать уникальное для всей системы имя.</span><span class="sxs-lookup"><span data-stu-id="991d6-119">Its <a href="element-name.md"><strong>Name</strong></a> element must contain a system-wide unique name.</span></span></li>
<li><span data-ttu-id="991d6-120">Его <a href="../mbn/schema-profilecreationtype-mbnprofile-element.md"><strong>профилекреатионтипе</strong></a> должен быть установлен в значение <strong>усерпровисионед</strong>.</span><span class="sxs-lookup"><span data-stu-id="991d6-120">Its <a href="../mbn/schema-profilecreationtype-mbnprofile-element.md"><strong>ProfileCreationType</strong></a> must be set to <strong>UserProvisioned</strong>.</span></span></li>
<li><span data-ttu-id="991d6-121">Его <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid"><strong>симикЦид</strong></a> должен содержать ICCID SIM-карты, для которой предназначен этот профиль.</span><span class="sxs-lookup"><span data-stu-id="991d6-121">Its <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid"><strong>SimIccID</strong></a> must contain the ICCID of the SIM that this profile is intended for.</span></span></li>
<li><span data-ttu-id="991d6-122">Его <a href="../mbn/schema-connectionmode-mbnprofile-element.md"><strong>ConnectionMode</strong></a> должен быть установлен в значение " <strong>вручную</strong>".</span><span class="sxs-lookup"><span data-stu-id="991d6-122">Its <a href="../mbn/schema-connectionmode-mbnprofile-element.md"><strong>ConnectionMode</strong></a> must be set to <strong>Manual</strong>.</span></span></li>
<li><span data-ttu-id="991d6-123">Его <a href="element-purposegroupguid.md"><strong>пурпосеграупгуид</strong></a> должен содержать GUID для группы целей MMS.</span><span class="sxs-lookup"><span data-stu-id="991d6-123">Its <a href="element-purposegroupguid.md"><strong>PurposeGroupGuid</strong></a> must contain the GUID for MMS purpose group.</span></span></li>
<li><span data-ttu-id="991d6-124">Его <a href="/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)"><strong>исаддитионалпдпконтекстпрофиле</strong></a> должен быть установлен в <strong>значение true</strong>.</span><span class="sxs-lookup"><span data-stu-id="991d6-124">Its <a href="/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)"><strong>IsAdditionalPdpContextProfile</strong></a> must be set to <strong>true</strong>.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="991d6-125">Требования</span><span class="sxs-lookup"><span data-stu-id="991d6-125">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="991d6-126">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="991d6-126">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 
