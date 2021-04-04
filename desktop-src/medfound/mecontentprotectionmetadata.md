---
description: Поток мультимедиа использует это событие для отправки в декодер метаданных, относящихся к системе защиты.
ms.assetid: 249446CA-AEF7-41A1-98EB-0B9392AE4AD8
title: Событие Меконтентпротектионметадата (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1dd72289a900b9c9b96fe9a64d427dab13110d66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897946"
---
# <a name="mecontentprotectionmetadata-event"></a><span data-ttu-id="3f1c6-103">Событие Меконтентпротектионметадата</span><span class="sxs-lookup"><span data-stu-id="3f1c6-103">MEContentProtectionMetadata event</span></span>

<span data-ttu-id="3f1c6-104">Поток мультимедиа использует это событие для отправки в декодер метаданных, относящихся к системе защиты.</span><span class="sxs-lookup"><span data-stu-id="3f1c6-104">Media Stream uses this event to send protection system specific metadata to the decoder.</span></span>

## <a name="event-values"></a><span data-ttu-id="3f1c6-105">Значения событий</span><span class="sxs-lookup"><span data-stu-id="3f1c6-105">Event values</span></span>

<span data-ttu-id="3f1c6-106">Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="3f1c6-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="3f1c6-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="3f1c6-107">VARTYPE</span></span>              | <span data-ttu-id="3f1c6-108">Описание</span><span class="sxs-lookup"><span data-stu-id="3f1c6-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="3f1c6-109">VT \_ пуст</span><span class="sxs-lookup"><span data-stu-id="3f1c6-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="3f1c6-110">Нет данных события.</span><span class="sxs-lookup"><span data-stu-id="3f1c6-110">No event data.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="3f1c6-111">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="3f1c6-111">Attributes</span></span>

<span data-ttu-id="3f1c6-112">Для этого события определены следующие атрибуты.</span><span class="sxs-lookup"><span data-stu-id="3f1c6-112">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="3f1c6-113">attribute</span><span class="sxs-lookup"><span data-stu-id="3f1c6-113">Attribute</span></span>                                                                                              | <span data-ttu-id="3f1c6-114">Описание</span><span class="sxs-lookup"><span data-stu-id="3f1c6-114">Description</span></span>                                                                                         |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3f1c6-115">\_ \_ \_ KEYDATA МЕТАДАННЫХ потока событий \_ MF</span><span class="sxs-lookup"><span data-stu-id="3f1c6-115">MF\_EVENT\_STREAM\_METADATA\_KEYDATA</span></span>](mf-event-stream-metadata-keydata.md)<br/>                | <span data-ttu-id="3f1c6-116">Этот атрибут является необязательным.</span><span class="sxs-lookup"><span data-stu-id="3f1c6-116">This is an optional attribute.</span></span> <span data-ttu-id="3f1c6-117">Данные, относящиеся к системе защиты.</span><span class="sxs-lookup"><span data-stu-id="3f1c6-117">Protection system specific data.</span></span><br/> <br/>              |
| [<span data-ttu-id="3f1c6-118">\_ \_ \_ \_ кэйидс содержимого МЕТАДАННЫХ для потока событий MF \_</span><span class="sxs-lookup"><span data-stu-id="3f1c6-118">MF\_EVENT\_STREAM\_METADATA\_CONTENT\_KEYIDS</span></span>](mf-event-stream-metadata-content-keyids.md)<br/> | <span data-ttu-id="3f1c6-119">Идентификаторы ключей содержимого, с которыми связано событие.</span><span class="sxs-lookup"><span data-stu-id="3f1c6-119">Content key IDs which the event is associated with.</span></span><br/> <br/>                          |
| [<span data-ttu-id="3f1c6-120">\_ \_ \_ SYSTEMID метаданные потока событий \_ MF</span><span class="sxs-lookup"><span data-stu-id="3f1c6-120">MF\_EVENT\_STREAM\_METADATA\_SYSTEMID</span></span>](mf-event-stream-metadata-systemid.md)<br/>              | <span data-ttu-id="3f1c6-121">Этот атрибут является необязательным.</span><span class="sxs-lookup"><span data-stu-id="3f1c6-121">This is an optional attribute.</span></span> <span data-ttu-id="3f1c6-122">Идентификатор системы, для которого предназначены ключевые данные.</span><span class="sxs-lookup"><span data-stu-id="3f1c6-122">System ID for which the key data is intended.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="3f1c6-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3f1c6-123">Remarks</span></span>

<span data-ttu-id="3f1c6-124">Это событие используется, например, для взаимодействия с событием смены ключа.</span><span class="sxs-lookup"><span data-stu-id="3f1c6-124">This event is used, for example, for communicating key rotation event.</span></span> <span data-ttu-id="3f1c6-125">В этом случае его следует отправить как можно раньше, чтобы обеспечить время декодера для подготовки перед выполнением примеров, зашифрованных с помощью нового идентификатора ключа.</span><span class="sxs-lookup"><span data-stu-id="3f1c6-125">In this case it should be sent as early as possible to give the decoder time to prepare itself before samples encrypted with the new key ID start arriving.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f1c6-126">Требования</span><span class="sxs-lookup"><span data-stu-id="3f1c6-126">Requirements</span></span>



| <span data-ttu-id="3f1c6-127">Требование</span><span class="sxs-lookup"><span data-stu-id="3f1c6-127">Requirement</span></span> | <span data-ttu-id="3f1c6-128">Значение</span><span class="sxs-lookup"><span data-stu-id="3f1c6-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f1c6-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3f1c6-129">Minimum supported client</span></span><br/> | <span data-ttu-id="3f1c6-130">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3f1c6-130">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="3f1c6-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3f1c6-131">Minimum supported server</span></span><br/> | <span data-ttu-id="3f1c6-132">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="3f1c6-132">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                  |
| <span data-ttu-id="3f1c6-133">Header</span><span class="sxs-lookup"><span data-stu-id="3f1c6-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="3f1c6-134"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3f1c6-134"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f1c6-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3f1c6-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f1c6-136">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3f1c6-136">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




