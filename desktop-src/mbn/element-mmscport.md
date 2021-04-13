---
description: MmscPort
MS-HAID: WWAN\_profile\_v4.element\_MmscPort
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: MmscPort
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08812a87b404cdec3caab43d56d4b9afdca9212b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343775"
---
# <a name="span-idwwan_profile_v4element_mmscportspanmmscport"></a><span data-ttu-id="0809f-103"><span id="WWAN_profile_v4.element_MmscPort"></span>ммскпорт</span><span class="sxs-lookup"><span data-stu-id="0809f-103"><span id="WWAN_profile_v4.element_MmscPort"></span>MmscPort</span></span>

<span data-ttu-id="0809f-104">Указывает номер порта сервера ММСК для устройства.</span><span class="sxs-lookup"><span data-stu-id="0809f-104">Specifies the port number of the MMSC server for the device.</span></span> <span data-ttu-id="0809f-105">Укажите значение 0, чтобы указать, что конкретный порт не указан.</span><span class="sxs-lookup"><span data-stu-id="0809f-105">Specify 0 to indicate that no specific port is specified.</span></span> <span data-ttu-id="0809f-106">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="0809f-106">Optional.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="0809f-107">Иерархия элементов</span><span class="sxs-lookup"><span data-stu-id="0809f-107">Element hierarchy</span></span>

[<MBNProfileExt>](element-mbnprofileext.md)  
[<MmsConfiguration>](element-mmsconfiguration.md)  
**<MmscPort>**

## <a name="syntax"></a><span data-ttu-id="0809f-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0809f-108">Syntax</span></span>

``` syntax
<MmscPort>

  [TBD (missing description)]

</MmscPort>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="0809f-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Атрибуты и элементы</span><span class="sxs-lookup"><span data-stu-id="0809f-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="0809f-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Атрибуты</span><span class="sxs-lookup"><span data-stu-id="0809f-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="0809f-111">Нет.</span><span class="sxs-lookup"><span data-stu-id="0809f-111">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="0809f-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="0809f-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="0809f-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="0809f-113">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="0809f-114"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="0809f-114"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0809f-115">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="0809f-115">Parent Element</span></span></th>
<th><span data-ttu-id="0809f-116">Описание</span><span class="sxs-lookup"><span data-stu-id="0809f-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0809f-117"><a href="element-mmsconfiguration.md">ммсконфигуратион</a></span><span class="sxs-lookup"><span data-stu-id="0809f-117"><a href="element-mmsconfiguration.md">MmsConfiguration</a></span></span></td>
<td><p><span data-ttu-id="0809f-118">Сведения о конфигурации для службы обмена сообщениями мультимедиа (MMS).</span><span class="sxs-lookup"><span data-stu-id="0809f-118">Configuration information for Multimedia Messaging Service (MMS).</span></span></p>
<p><span data-ttu-id="0809f-119">Помимо настройки элементов конфигурации в этом элементе, профиль MMS должен иметь следующие параметры.</span><span class="sxs-lookup"><span data-stu-id="0809f-119">In addition to setting the configuration elements within this element, an MMS profile must have the following settings.</span></span></p>
<ul>
<li><span data-ttu-id="0809f-120">Его элемент <a href="element-name.md"><strong>Name</strong></a> должен содержать уникальное для всей системы имя.</span><span class="sxs-lookup"><span data-stu-id="0809f-120">Its <a href="element-name.md"><strong>Name</strong></a> element must contain a system-wide unique name.</span></span></li>
<li><span data-ttu-id="0809f-121">Его <a href="../mbn/schema-profilecreationtype-mbnprofile-element.md"><strong>профилекреатионтипе</strong></a> должен быть установлен в значение <strong>усерпровисионед</strong>.</span><span class="sxs-lookup"><span data-stu-id="0809f-121">Its <a href="../mbn/schema-profilecreationtype-mbnprofile-element.md"><strong>ProfileCreationType</strong></a> must be set to <strong>UserProvisioned</strong>.</span></span></li>
<li><span data-ttu-id="0809f-122">Его <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid"><strong>симикЦид</strong></a> должен содержать ICCID SIM-карты, для которой предназначен этот профиль.</span><span class="sxs-lookup"><span data-stu-id="0809f-122">Its <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid"><strong>SimIccID</strong></a> must contain the ICCID of the SIM that this profile is intended for.</span></span></li>
<li><span data-ttu-id="0809f-123">Его <a href="../mbn/schema-connectionmode-mbnprofile-element.md"><strong>ConnectionMode</strong></a> должен быть установлен в значение " <strong>вручную</strong>".</span><span class="sxs-lookup"><span data-stu-id="0809f-123">Its <a href="../mbn/schema-connectionmode-mbnprofile-element.md"><strong>ConnectionMode</strong></a> must be set to <strong>Manual</strong>.</span></span></li>
<li><span data-ttu-id="0809f-124">Его <a href="element-purposegroupguid.md"><strong>пурпосеграупгуид</strong></a> должен содержать GUID для группы целей MMS.</span><span class="sxs-lookup"><span data-stu-id="0809f-124">Its <a href="element-purposegroupguid.md"><strong>PurposeGroupGuid</strong></a> must contain the GUID for MMS purpose group.</span></span></li>
<li><span data-ttu-id="0809f-125">Его <a href="/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)"><strong>исаддитионалпдпконтекстпрофиле</strong></a> должен быть установлен в <strong>значение true</strong>.</span><span class="sxs-lookup"><span data-stu-id="0809f-125">Its <a href="/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)"><strong>IsAdditionalPdpContextProfile</strong></a> must be set to <strong>true</strong>.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="0809f-126">Требования</span><span class="sxs-lookup"><span data-stu-id="0809f-126">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0809f-127">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="0809f-127">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 
