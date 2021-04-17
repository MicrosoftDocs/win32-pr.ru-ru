---
description: 'Посылается, когда поток мультимедиа доставляет новый пример в ответ на вызов Имфмедиастреам:: Рекуестсампле.'
ms.assetid: 01610053-786f-44b5-90d6-2cb2668cd632
title: Событие Мемедиасампле (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7de0cfcdbf943e0526d61a0c63424f7add078b2c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105713267"
---
# <a name="memediasample-event"></a><span data-ttu-id="01a6e-103">Событие Мемедиасампле</span><span class="sxs-lookup"><span data-stu-id="01a6e-103">MEMediaSample event</span></span>

<span data-ttu-id="01a6e-104">Посылается, когда поток мультимедиа доставляет новый пример в ответ на вызов [**имфмедиастреам:: рекуестсампле**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample).</span><span class="sxs-lookup"><span data-stu-id="01a6e-104">Sent when a media stream delivers a new sample in response to a call to [**IMFMediaStream::RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample).</span></span>

## <a name="event-values"></a><span data-ttu-id="01a6e-105">Значения событий</span><span class="sxs-lookup"><span data-stu-id="01a6e-105">Event values</span></span>

<span data-ttu-id="01a6e-106">Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="01a6e-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="01a6e-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="01a6e-107">VARTYPE</span></span>                | <span data-ttu-id="01a6e-108">Описание</span><span class="sxs-lookup"><span data-stu-id="01a6e-108">Description</span></span>                                                                                   |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="01a6e-109">VT \_ Unknown</span><span class="sxs-lookup"><span data-stu-id="01a6e-109">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="01a6e-110">Указатель на интерфейс [**имфсампле**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) образца.</span><span class="sxs-lookup"><span data-stu-id="01a6e-110">Pointer to the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface of the sample.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="01a6e-111">Требования</span><span class="sxs-lookup"><span data-stu-id="01a6e-111">Requirements</span></span>



| <span data-ttu-id="01a6e-112">Требование</span><span class="sxs-lookup"><span data-stu-id="01a6e-112">Requirement</span></span> | <span data-ttu-id="01a6e-113">Значение</span><span class="sxs-lookup"><span data-stu-id="01a6e-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01a6e-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="01a6e-114">Minimum supported client</span></span><br/> | <span data-ttu-id="01a6e-115">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="01a6e-115">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="01a6e-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="01a6e-116">Minimum supported server</span></span><br/> | <span data-ttu-id="01a6e-117">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="01a6e-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="01a6e-118">Header</span><span class="sxs-lookup"><span data-stu-id="01a6e-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="01a6e-119"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="01a6e-119"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01a6e-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="01a6e-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01a6e-121">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="01a6e-121">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="01a6e-122">Источники мультимедиа</span><span class="sxs-lookup"><span data-stu-id="01a6e-122">Media Sources</span></span>](media-sources.md)
</dt> </dl>

 

 




