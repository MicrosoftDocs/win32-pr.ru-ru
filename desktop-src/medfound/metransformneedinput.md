---
description: Отправляется асинхронным Media Foundation преобразованием (MFT) для запроса нового входного примера.
ms.assetid: 5d5c50d9-fe4e-47ff-ae09-980911ebfb22
title: Событие Метрансформнидинпут (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63cbdea648e4dc7d90b1321958eebb6c544ebb88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154651"
---
# <a name="metransformneedinput-event"></a><span data-ttu-id="e4f7e-103">Событие Метрансформнидинпут</span><span class="sxs-lookup"><span data-stu-id="e4f7e-103">METransformNeedInput event</span></span>

<span data-ttu-id="e4f7e-104">Отправляется асинхронным Media Foundation преобразованием (MFT) для запроса нового входного примера.</span><span class="sxs-lookup"><span data-stu-id="e4f7e-104">Sent by an asynchronous Media Foundation transform (MFT) to request a new input sample.</span></span>

## <a name="event-values"></a><span data-ttu-id="e4f7e-105">Значения событий</span><span class="sxs-lookup"><span data-stu-id="e4f7e-105">Event values</span></span>

<span data-ttu-id="e4f7e-106">Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="e4f7e-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="e4f7e-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="e4f7e-107">VARTYPE</span></span>              | <span data-ttu-id="e4f7e-108">Описание</span><span class="sxs-lookup"><span data-stu-id="e4f7e-108">Description</span></span>               |
|----------------------|---------------------------|
| <span data-ttu-id="e4f7e-109">VT \_ пуст</span><span class="sxs-lookup"><span data-stu-id="e4f7e-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="e4f7e-110">Нет данных события.</span><span class="sxs-lookup"><span data-stu-id="e4f7e-110">No event data.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="e4f7e-111">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="e4f7e-111">Attributes</span></span>

<span data-ttu-id="e4f7e-112">Для этого события определены следующие атрибуты.</span><span class="sxs-lookup"><span data-stu-id="e4f7e-112">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="e4f7e-113">attribute</span><span class="sxs-lookup"><span data-stu-id="e4f7e-113">Attribute</span></span>                                                                        | <span data-ttu-id="e4f7e-114">Описание</span><span class="sxs-lookup"><span data-stu-id="e4f7e-114">Description</span></span>                                                                           |
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [<span data-ttu-id="e4f7e-115">\_ \_ \_ ИД входного \_ потока MFT события \_ MF</span><span class="sxs-lookup"><span data-stu-id="e4f7e-115">MF\_EVENT\_MFT\_INPUT\_STREAM\_ID</span></span>](mf-event-mft-input-stream-id.md)<br/> | <span data-ttu-id="e4f7e-116">Идентификатор потока, для которого требуются входные данные.</span><span class="sxs-lookup"><span data-stu-id="e4f7e-116">The identifier of the stream that needs input data.</span></span><br/><span data-ttu-id="e4f7e-117">*Необходимости*</span><span class="sxs-lookup"><span data-stu-id="e4f7e-117">*(Required)*</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="e4f7e-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e4f7e-118">Remarks</span></span>

<span data-ttu-id="e4f7e-119">Асинхронный МФТС отправляет это событие через интерфейс [**имфмедиаевентженератор**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) .</span><span class="sxs-lookup"><span data-stu-id="e4f7e-119">Asynchronous MFTs send this event through the [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface.</span></span> <span data-ttu-id="e4f7e-120">Синхронное МФТС никогда не отправляет это событие.</span><span class="sxs-lookup"><span data-stu-id="e4f7e-120">Synchronous MFTs never send this event.</span></span>

<span data-ttu-id="e4f7e-121">Когда клиент MFT получает это событие, он должен вызвать [**имфтрансформ::P роцессинпут**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) , чтобы доставить следующий пример.</span><span class="sxs-lookup"><span data-stu-id="e4f7e-121">When the client of the MFT receives this event, it should call [**IMFTransform::ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) to deliver the next sample.</span></span> <span data-ttu-id="e4f7e-122">Атрибут [ \_ \_ \_ \_ \_ идентификатора входного потока события MF](mf-event-mft-input-stream-id.md) объекта события указывает, какой входной поток требует данные.</span><span class="sxs-lookup"><span data-stu-id="e4f7e-122">The [MF\_EVENT\_MFT\_INPUT\_STREAM\_ID](mf-event-mft-input-stream-id.md) attribute of the event object specifies which input stream requires data.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4f7e-123">Требования</span><span class="sxs-lookup"><span data-stu-id="e4f7e-123">Requirements</span></span>



| <span data-ttu-id="e4f7e-124">Требование</span><span class="sxs-lookup"><span data-stu-id="e4f7e-124">Requirement</span></span> | <span data-ttu-id="e4f7e-125">Значение</span><span class="sxs-lookup"><span data-stu-id="e4f7e-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4f7e-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e4f7e-126">Minimum supported client</span></span><br/> | <span data-ttu-id="e4f7e-127">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="e4f7e-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="e4f7e-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e4f7e-128">Minimum supported server</span></span><br/> | <span data-ttu-id="e4f7e-129">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="e4f7e-129">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                  |
| <span data-ttu-id="e4f7e-130">Header</span><span class="sxs-lookup"><span data-stu-id="e4f7e-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4f7e-131"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e4f7e-131"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4f7e-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e4f7e-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4f7e-133">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e4f7e-133">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="e4f7e-134">Асинхронный МФТС</span><span class="sxs-lookup"><span data-stu-id="e4f7e-134">Asynchronous MFTs</span></span>](asynchronous-mfts.md)
</dt> </dl>

 

 




