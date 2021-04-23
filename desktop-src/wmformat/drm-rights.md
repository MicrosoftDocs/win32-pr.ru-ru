---
title: DRM_Rights
description: '\_Свойство Rights DRM определяет права, которые будут необходимы приложению при следующей попытке открыть защищенный файл.'
ms.assetid: fbf62e8d-069e-427b-9093-6c579cdaa96a
keywords:
- DRM_Rights формат Windows Media
topic_type:
- apiref
api_name:
- DRM_Rights
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 542e511c11111bb2698d9c936a1f0973a2145c9b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104069548"
---
# <a name="drm_rights"></a><span data-ttu-id="11548-104">\_Права DRM</span><span class="sxs-lookup"><span data-stu-id="11548-104">DRM\_Rights</span></span>

<span data-ttu-id="11548-105">Свойство **\_ Rights DRM** определяет права, которые будут необходимы приложению при следующей попытке открыть защищенный файл.</span><span class="sxs-lookup"><span data-stu-id="11548-105">The **DRM\_Rights** property specifies the rights that the application will require in the next attempt to open a protected file.</span></span>

## <a name="global-constant"></a><span data-ttu-id="11548-106">Глобальная константа</span><span class="sxs-lookup"><span data-stu-id="11548-106">Global Constant</span></span>

<span data-ttu-id="11548-107">g \_ всзвмдрм \_ права</span><span class="sxs-lookup"><span data-stu-id="11548-107">g\_wszWMDRM\_Rights</span></span>

## <a name="data-type"></a><span data-ttu-id="11548-108">Тип данных</span><span class="sxs-lookup"><span data-stu-id="11548-108">Data Type</span></span>

<span data-ttu-id="11548-109">**\_Строка типа \_ ВМТ**</span><span class="sxs-lookup"><span data-stu-id="11548-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="11548-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="11548-110">Remarks</span></span>

<span data-ttu-id="11548-111">Это свойство, доступное для чтения и записи, которое извлекается с помощью [**ивмдрмреадер:: жетдрмпроперти**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty) и задается с помощью [**Ивмдрмреадер:: сетдрмпроперти**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-setdrmproperty) или [**ивмдрмвритер:: сетдрматтрибуте**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute).</span><span class="sxs-lookup"><span data-stu-id="11548-111">This is a read-write property that is retrieved using [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty) and set using either [**IWMDRMReader::SetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-setdrmproperty) or [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute).</span></span>

<span data-ttu-id="11548-112">В следующей таблице перечислены поддерживаемые права.</span><span class="sxs-lookup"><span data-stu-id="11548-112">The following table lists the supported rights.</span></span>



| <span data-ttu-id="11548-113">Правый</span><span class="sxs-lookup"><span data-stu-id="11548-113">Right</span></span>                                           | <span data-ttu-id="11548-114">Строковый литерал</span><span class="sxs-lookup"><span data-stu-id="11548-114">String literal</span></span>      | <span data-ttu-id="11548-115">Описание</span><span class="sxs-lookup"><span data-stu-id="11548-115">Description</span></span>                                                                                                                                                                                                          |
|-------------------------------------------------|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11548-116">g \_ всзвмдрм, \_ правое \_ резервное копирование</span><span class="sxs-lookup"><span data-stu-id="11548-116">g\_wszWMDRM\_RIGHT\_BACKUP</span></span>                      | <span data-ttu-id="11548-117">Копия</span><span class="sxs-lookup"><span data-stu-id="11548-117">"Backup"</span></span>            | <span data-ttu-id="11548-118">Право на резервное копирование лицензии.</span><span class="sxs-lookup"><span data-stu-id="11548-118">Right to back up the license.</span></span>                                                                                                                                                                                        |
| <span data-ttu-id="11548-119">g \_ всзвмдрм \_ право на \_ сотрудничество \_</span><span class="sxs-lookup"><span data-stu-id="11548-119">g\_wszWMDRM\_RIGHT\_COLLABORATIVE\_PLAY</span></span>         | <span data-ttu-id="11548-120">"Коллаборативеплай"</span><span class="sxs-lookup"><span data-stu-id="11548-120">"CollaborativePlay"</span></span> | <span data-ttu-id="11548-121">Право на воспроизведение файла как части списка воспроизведения для совместной работы.</span><span class="sxs-lookup"><span data-stu-id="11548-121">Right to play the file as part of a collaborative playlist.</span></span>                                                                                                                                                          |
| <span data-ttu-id="11548-122">g \_ всзвмдрм \_ , \_ копия справа</span><span class="sxs-lookup"><span data-stu-id="11548-122">g\_wszWMDRM\_RIGHT\_COPY</span></span>                        | <span data-ttu-id="11548-123">"Копировать"</span><span class="sxs-lookup"><span data-stu-id="11548-123">"Copy"</span></span>              | <span data-ttu-id="11548-124">Право на копирование файла на устройство.</span><span class="sxs-lookup"><span data-stu-id="11548-124">Right to copy the file to a device.</span></span> <span data-ttu-id="11548-125">Это право заменяет более старые права на копирование (g \_ всзвмдрм \_ справа \_ Копировать \_ на \_ компакт-диск, g \_ всзвмдрм \_ правую \_ копию \_ на \_ устройство, не защищенное от \_ SDMI \_ , и g \_ всзвмдрм \_ right \_ Copy \_ to \_ SDMI \_ Device).</span><span class="sxs-lookup"><span data-stu-id="11548-125">This right supersedes the older copy rights (g\_wszWMDRM\_RIGHT\_COPY\_TO\_CD, g\_wszWMDRM\_RIGHT\_COPY\_TO\_NON\_SDMI\_DEVICE, and g\_wszWMDRM\_RIGHT\_COPY\_TO\_SDMI\_DEVICE).</span></span> |
| <span data-ttu-id="11548-126">g \_ всзвмдрм \_ право \_ Копировать \_ на \_ компакт-диск</span><span class="sxs-lookup"><span data-stu-id="11548-126">g\_wszWMDRM\_RIGHT\_COPY\_TO\_CD</span></span>                | <span data-ttu-id="11548-127">"Print. редбук"</span><span class="sxs-lookup"><span data-stu-id="11548-127">"Print.redbook"</span></span>     | <span data-ttu-id="11548-128">Право копировать файл на компакт-диск (формат Red Book). В Windows Media DRM 10 это право заменяется на g \_ всзвмдрм \_ right \_ Copy.</span><span class="sxs-lookup"><span data-stu-id="11548-128">Right to copy the file to a CD (Red Book format).In Windows Media DRM 10, this right is replaced by g\_wszWMDRM\_RIGHT\_COPY.</span></span><br/>                                                                             |
| <span data-ttu-id="11548-129">g \_ всзвмдрм \_ right \_ Копировать \_ на \_ устройство, отличное от \_ SDMI \_</span><span class="sxs-lookup"><span data-stu-id="11548-129">g\_wszWMDRM\_RIGHT\_COPY\_TO\_NON\_SDMI\_DEVICE</span></span> | <span data-ttu-id="11548-130">"Перемещение. НОНСДМИ"</span><span class="sxs-lookup"><span data-stu-id="11548-130">"Transfer.NONSDMI"</span></span>  | <span data-ttu-id="11548-131">Право на копирование файла на устройство, не поддерживающее SDMI. В Windows Media DRM 10 это право заменяется на g \_ всзвмдрм \_ right \_ Copy.</span><span class="sxs-lookup"><span data-stu-id="11548-131">Right to copy the file to a non-SDMI device.In Windows Media DRM 10, this right is replaced by g\_wszWMDRM\_RIGHT\_COPY.</span></span><br/>                                                                                  |
| <span data-ttu-id="11548-132">g \_ всзвмдрм \_ право \_ Копировать \_ на \_ \_ устройство SDMI</span><span class="sxs-lookup"><span data-stu-id="11548-132">g\_wszWMDRM\_RIGHT\_COPY\_TO\_SDMI\_DEVICE</span></span>      | <span data-ttu-id="11548-133">"Перемещение. SDMI"</span><span class="sxs-lookup"><span data-stu-id="11548-133">"Transfer.SDMI"</span></span>     | <span data-ttu-id="11548-134">Право копировать файл на SDMI-совместимое устройство. В Windows Media DRM 10 это право заменяется на g \_ всзвмдрм \_ right \_ Copy.</span><span class="sxs-lookup"><span data-stu-id="11548-134">Right to copy the file to an SDMI-compliant device.In Windows Media DRM 10, this right is replaced by g\_wszWMDRM\_RIGHT\_COPY.</span></span><br/>                                                                           |
| <span data-ttu-id="11548-135">g \_ всзвмдрм \_ правое \_ Воспроизведение</span><span class="sxs-lookup"><span data-stu-id="11548-135">g\_wszWMDRM\_RIGHT\_PLAYBACK</span></span>                    | <span data-ttu-id="11548-136">Воспроизводит</span><span class="sxs-lookup"><span data-stu-id="11548-136">"Play"</span></span>              | <span data-ttu-id="11548-137">Право на воспроизведение файла мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="11548-137">Right to play the media file.</span></span>                                                                                                                                                                                        |



 

<span data-ttu-id="11548-138">Это свойство содержит строку расширенных символов с одним или несколькими правами, разделенных точкой с запятой, например: L. Воспроизведение; Копии Коллаборативеплай ".</span><span class="sxs-lookup"><span data-stu-id="11548-138">This property contains a wide-character string of one or more rights separated by semicolons, for example: L"Playback;Copy;CollaborativePlay".</span></span>

## <a name="see-also"></a><span data-ttu-id="11548-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="11548-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11548-140">**Свойства DRM**</span><span class="sxs-lookup"><span data-stu-id="11548-140">**DRM Properties**</span></span>](drm-properties.md)
</dt> </dl>

 

 





