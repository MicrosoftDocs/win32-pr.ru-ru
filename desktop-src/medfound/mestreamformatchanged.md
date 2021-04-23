---
description: Вызывается потоком мультимедиа при изменении типа мультимедиа потока.
ms.assetid: 14786a9b-413e-4fb4-b267-bfd0ccd4631b
title: Событие Местреамформатчанжед (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd48e7abc8121707b150af5bc8968a50c1eb44e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898370"
---
# <a name="mestreamformatchanged-event"></a><span data-ttu-id="1acad-103">Событие Местреамформатчанжед</span><span class="sxs-lookup"><span data-stu-id="1acad-103">MEStreamFormatChanged event</span></span>

<span data-ttu-id="1acad-104">Вызывается потоком мультимедиа при изменении типа мультимедиа потока.</span><span class="sxs-lookup"><span data-stu-id="1acad-104">Raised by a media stream when the media type of the stream changes.</span></span>

## <a name="event-values"></a><span data-ttu-id="1acad-105">Значения событий</span><span class="sxs-lookup"><span data-stu-id="1acad-105">Event values</span></span>

<span data-ttu-id="1acad-106">Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="1acad-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="1acad-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="1acad-107">VARTYPE</span></span>                | <span data-ttu-id="1acad-108">Описание</span><span class="sxs-lookup"><span data-stu-id="1acad-108">Description</span></span>                                                                                                 |
|------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1acad-109">VT \_ Unknown</span><span class="sxs-lookup"><span data-stu-id="1acad-109">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="1acad-110">Указатель на интерфейс [**имфмедиатипе**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) нового типа носителя.</span><span class="sxs-lookup"><span data-stu-id="1acad-110">Pointer to the [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface of the new media type.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="1acad-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1acad-111">Remarks</span></span>

<span data-ttu-id="1acad-112">Это событие используется для сигнализации изменений формата в потоке.</span><span class="sxs-lookup"><span data-stu-id="1acad-112">Use this event to signal format changes in the stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="1acad-113">Требования</span><span class="sxs-lookup"><span data-stu-id="1acad-113">Requirements</span></span>



| <span data-ttu-id="1acad-114">Требование</span><span class="sxs-lookup"><span data-stu-id="1acad-114">Requirement</span></span> | <span data-ttu-id="1acad-115">Значение</span><span class="sxs-lookup"><span data-stu-id="1acad-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1acad-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1acad-116">Minimum supported client</span></span><br/> | <span data-ttu-id="1acad-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1acad-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="1acad-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1acad-118">Minimum supported server</span></span><br/> | <span data-ttu-id="1acad-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1acad-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1acad-120">Header</span><span class="sxs-lookup"><span data-stu-id="1acad-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="1acad-121"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1acad-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1acad-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1acad-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1acad-123">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1acad-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




