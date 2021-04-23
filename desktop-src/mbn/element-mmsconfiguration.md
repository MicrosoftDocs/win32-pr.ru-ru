---
description: ммсконфигуратион
MS-HAID: WWAN\_profile\_v4.element\_MmsConfiguration
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: ммсконфигуратион
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cb98506476558ed0e39df11bab4b9446de4fd3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263040"
---
# <a name="span-idwwan_profile_v4element_mmsconfigurationspanmmsconfiguration"></a><span data-ttu-id="874b3-103"><span id="WWAN_profile_v4.element_MmsConfiguration"></span>ммсконфигуратион</span><span class="sxs-lookup"><span data-stu-id="874b3-103"><span id="WWAN_profile_v4.element_MmsConfiguration"></span>MmsConfiguration</span></span>

<span data-ttu-id="874b3-104">Сведения о конфигурации для службы обмена сообщениями мультимедиа (MMS).</span><span class="sxs-lookup"><span data-stu-id="874b3-104">Configuration information for Multimedia Messaging Service (MMS).</span></span>

<span data-ttu-id="874b3-105">Помимо настройки элементов конфигурации в этом элементе, профиль MMS должен иметь следующие параметры.</span><span class="sxs-lookup"><span data-stu-id="874b3-105">In addition to setting the configuration elements within this element, an MMS profile must have the following settings.</span></span>

-   <span data-ttu-id="874b3-106">Его элемент [**Name**](element-name.md) должен содержать уникальное для всей системы имя.</span><span class="sxs-lookup"><span data-stu-id="874b3-106">Its [**Name**](element-name.md) element must contain a system-wide unique name.</span></span>
-   <span data-ttu-id="874b3-107">Его [**профилекреатионтипе**](./schema-profilecreationtype-mbnprofile-element.md) должен быть установлен в значение **усерпровисионед**.</span><span class="sxs-lookup"><span data-stu-id="874b3-107">Its [**ProfileCreationType**](./schema-profilecreationtype-mbnprofile-element.md) must be set to **UserProvisioned**.</span></span>
-   <span data-ttu-id="874b3-108">Его [**симикЦид**](/windows/win32/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid) должен содержать ICCID SIM-карты, для которой предназначен этот профиль.</span><span class="sxs-lookup"><span data-stu-id="874b3-108">Its [**SimIccID**](/windows/win32/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid) must contain the ICCID of the SIM that this profile is intended for.</span></span>
-   <span data-ttu-id="874b3-109">Его [**ConnectionMode**](./schema-connectionmode-mbnprofile-element.md) должен быть установлен в значение " **вручную**".</span><span class="sxs-lookup"><span data-stu-id="874b3-109">Its [**ConnectionMode**](./schema-connectionmode-mbnprofile-element.md) must be set to **Manual**.</span></span>
-   <span data-ttu-id="874b3-110">Его [**пурпосеграупгуид**](element-purposegroupguid.md) должен содержать GUID для группы целей MMS.</span><span class="sxs-lookup"><span data-stu-id="874b3-110">Its [**PurposeGroupGuid**](element-purposegroupguid.md) must contain the GUID for MMS purpose group.</span></span>
-   <span data-ttu-id="874b3-111">Его [**исаддитионалпдпконтекстпрофиле**](/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)) должен быть установлен в **значение true**.</span><span class="sxs-lookup"><span data-stu-id="874b3-111">Its [**IsAdditionalPdpContextProfile**](/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)) must be set to **true**.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="874b3-112">Иерархия элементов</span><span class="sxs-lookup"><span data-stu-id="874b3-112">Element hierarchy</span></span>

[<MBNProfileExt>](element-mbnprofileext.md)  
**<MmsConfiguration>**

## <a name="syntax"></a><span data-ttu-id="874b3-113">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="874b3-113">Syntax</span></span>

``` syntax
<MmsConfiguration>

  <!-- Child elements -->
  MmscUrl?,
  MmscPort?,
  MmsMaximumMessageSize?

</MmsConfiguration>
```

### <a name="key"></a><span data-ttu-id="874b3-114">Ключ</span><span class="sxs-lookup"><span data-stu-id="874b3-114">Key</span></span>

<span data-ttu-id="874b3-115">`?`   необязательно (ноль или один)</span><span class="sxs-lookup"><span data-stu-id="874b3-115">`?`   optional (zero or one)</span></span>

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="874b3-116"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Атрибуты и элементы</span><span class="sxs-lookup"><span data-stu-id="874b3-116"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="874b3-117"><span id="attributes"></span><span id="ATTRIBUTES"></span>Атрибуты</span><span class="sxs-lookup"><span data-stu-id="874b3-117"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="874b3-118">Нет.</span><span class="sxs-lookup"><span data-stu-id="874b3-118">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="874b3-119"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="874b3-119"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="874b3-120">Дочерний элемент</span><span class="sxs-lookup"><span data-stu-id="874b3-120">Child Element</span></span></th>
<th><span data-ttu-id="874b3-121">Описание</span><span class="sxs-lookup"><span data-stu-id="874b3-121">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="874b3-122"><a href="element-mmsmaximummessagesize.md">MmsMaximumMessageSize</a></span><span class="sxs-lookup"><span data-stu-id="874b3-122"><a href="element-mmsmaximummessagesize.md">MmsMaximumMessageSize</a></span></span></td>
<td><p><span data-ttu-id="874b3-123">Указывает максимальный размер MMS сообщений в килобайтах.</span><span class="sxs-lookup"><span data-stu-id="874b3-123">Specifies the maximum size of MMS messages, in kilobytes.</span></span> <span data-ttu-id="874b3-124">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="874b3-124">Optional.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="874b3-125"><a href="element-mmscport.md">MmscPort</a></span><span class="sxs-lookup"><span data-stu-id="874b3-125"><a href="element-mmscport.md">MmscPort</a></span></span></td>
<td><p><span data-ttu-id="874b3-126">Указывает номер порта сервера ММСК для устройства.</span><span class="sxs-lookup"><span data-stu-id="874b3-126">Specifies the port number of the MMSC server for the device.</span></span> <span data-ttu-id="874b3-127">Укажите значение 0, чтобы указать, что конкретный порт не указан.</span><span class="sxs-lookup"><span data-stu-id="874b3-127">Specify 0 to indicate that no specific port is specified.</span></span> <span data-ttu-id="874b3-128">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="874b3-128">Optional.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="874b3-129"><a href="element-mmscurl.md">MmscUrl</a></span><span class="sxs-lookup"><span data-stu-id="874b3-129"><a href="element-mmscurl.md">MmscUrl</a></span></span></td>
<td><p><span data-ttu-id="874b3-130">Указывает URL-адрес сервера ММСК для устройства.</span><span class="sxs-lookup"><span data-stu-id="874b3-130">Specifies the URL of the MMSC server for the device.</span></span> <span data-ttu-id="874b3-131">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="874b3-131">Optional.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="874b3-132"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="874b3-132"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="874b3-133">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="874b3-133">Parent Element</span></span></th>
<th><span data-ttu-id="874b3-134">Описание</span><span class="sxs-lookup"><span data-stu-id="874b3-134">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="874b3-135"><a href="element-mbnprofileext.md">MBNProfileExt</a></span><span class="sxs-lookup"><span data-stu-id="874b3-135"><a href="element-mbnprofileext.md">MBNProfileExt</a></span></span></td>
<td><p><span data-ttu-id="874b3-136">Элемент <strong>мбнпрофиликст</strong> является расширением более раннего элемента мбнпрофиле.</span><span class="sxs-lookup"><span data-stu-id="874b3-136">The <strong>MBNProfileExt</strong> element is an extension of the earlier MBNProfile element.</span></span> <span data-ttu-id="874b3-137">Он определяет профиль мобильного широкополосного подключения с более широким набором параметров, чем элемент Мбнпрофиле.</span><span class="sxs-lookup"><span data-stu-id="874b3-137">It identifies a Mobile Broadband profile with a richer set of options than the MBNProfile element.</span></span></p>
<p><span data-ttu-id="874b3-138">В профиле может быть несколько элементов Мбнпрофиликст, описывающих параметры профиля для определенного набора условий.</span><span class="sxs-lookup"><span data-stu-id="874b3-138">There can be more than one MbnProfileExt element in a profile, describing profile settings for a particular set of operating conditions.</span></span> <span data-ttu-id="874b3-139">Используйте дочерний элемент <a href="element-profileconditionedon.md"><strong>профилекондитионедон</strong></a> из <strong>мбнпрофиликст</strong> , чтобы указать, какие операционные условия делают определенный профиль активным.</span><span class="sxs-lookup"><span data-stu-id="874b3-139">Use the <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> child element of <strong>MBNProfileExt</strong> to specify which operating conditions make a particular profile the active profile.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="874b3-140">Требования</span><span class="sxs-lookup"><span data-stu-id="874b3-140">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="874b3-141">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="874b3-141">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 
