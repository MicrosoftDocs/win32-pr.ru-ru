---
description: Отправляется асинхронным Media Foundation преобразованием (MFT) в ответ на \_ \_ \_ сообщение маркера команды сообщения MFT.
ms.assetid: d0c0d62d-9133-4d4b-8606-c2ae1d4c9f0a
title: Событие Метрансформмаркер (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab79c47e2ddb26f2366aff075548f7905807df1e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673499"
---
# <a name="metransformmarker-event"></a><span data-ttu-id="02da0-103">Событие Метрансформмаркер</span><span class="sxs-lookup"><span data-stu-id="02da0-103">METransformMarker event</span></span>

<span data-ttu-id="02da0-104">Отправляется асинхронным Media Foundation преобразованием (MFT) в ответ на сообщение **\_ \_ \_ маркера команды сообщения MFT** .</span><span class="sxs-lookup"><span data-stu-id="02da0-104">Sent by an asynchronous Media Foundation transform (MFT) in response to an **MFT\_MESSAGE\_COMMAND\_MARKER** message.</span></span>

## <a name="event-values"></a><span data-ttu-id="02da0-105">Значения событий</span><span class="sxs-lookup"><span data-stu-id="02da0-105">Event values</span></span>

<span data-ttu-id="02da0-106">Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="02da0-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="02da0-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="02da0-107">VARTYPE</span></span>              | <span data-ttu-id="02da0-108">Описание</span><span class="sxs-lookup"><span data-stu-id="02da0-108">Description</span></span>               |
|----------------------|---------------------------|
| <span data-ttu-id="02da0-109">VT \_ пуст</span><span class="sxs-lookup"><span data-stu-id="02da0-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="02da0-110">Нет данных события.</span><span class="sxs-lookup"><span data-stu-id="02da0-110">No event data.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="02da0-111">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="02da0-111">Attributes</span></span>

<span data-ttu-id="02da0-112">Для этого события определены следующие атрибуты.</span><span class="sxs-lookup"><span data-stu-id="02da0-112">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="02da0-113">attribute</span><span class="sxs-lookup"><span data-stu-id="02da0-113">Attribute</span></span>                                                      | <span data-ttu-id="02da0-114">Описание</span><span class="sxs-lookup"><span data-stu-id="02da0-114">Description</span></span>                                                                                                                |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="02da0-115">\_ \_ контекст MFT события \_ MF</span><span class="sxs-lookup"><span data-stu-id="02da0-115">MF\_EVENT\_MFT\_CONTEXT</span></span>](mf-event-mft-context.md)<br/> | <span data-ttu-id="02da0-116">Значение параметра *улпарам* из сообщения **\_ \_ \_ метки команды сообщения MFT** .</span><span class="sxs-lookup"><span data-stu-id="02da0-116">The value of the *ulParam* parameter from the **MFT\_MESSAGE\_COMMAND\_MARKER** message.</span></span><br/><span data-ttu-id="02da0-117">*Необходимости*</span><span class="sxs-lookup"><span data-stu-id="02da0-117">*(Required)*</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="02da0-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="02da0-118">Remarks</span></span>

<span data-ttu-id="02da0-119">Асинхронный МФТС отправляет это событие через интерфейс [**имфмедиаевентженератор**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) .</span><span class="sxs-lookup"><span data-stu-id="02da0-119">Asynchronous MFTs send this event through the [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface.</span></span> <span data-ttu-id="02da0-120">Синхронное МФТС никогда не отправляет это событие.</span><span class="sxs-lookup"><span data-stu-id="02da0-120">Synchronous MFTs never send this event.</span></span>

<span data-ttu-id="02da0-121">Клиент асинхронной таблицы MFT может поместить маркер в поток, вызвав [**имфтрансформ::P роцессмессаже**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) с сообщением **\_ \_ \_ маркера команды сообщения MFT** .</span><span class="sxs-lookup"><span data-stu-id="02da0-121">The client of an asynchronous MFT can place a marker in the stream by calling [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) with the **MFT\_MESSAGE\_COMMAND\_MARKER** message.</span></span> <span data-ttu-id="02da0-122">Параметр *улпарам* содержит данные, определяемые приложением.</span><span class="sxs-lookup"><span data-stu-id="02da0-122">The *ulParam* parameter contains application-defined data.</span></span>

<span data-ttu-id="02da0-123">Когда MFT заканчивает обработку всех входных данных, которые были доступны во время вызова [**ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) , MFT ставит в очередь событие метрансформмаркер.</span><span class="sxs-lookup"><span data-stu-id="02da0-123">When the MFT finishes processing all of the input data that was available at the time of the [**ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) call, the MFT queues an METransformMarker event.</span></span> <span data-ttu-id="02da0-124">Атрибут [ \_ \_ \_ context события MF в MFT](mf-event-mft-context.md) события содержит значение параметра *улпарам* .</span><span class="sxs-lookup"><span data-stu-id="02da0-124">The [MF\_EVENT\_MFT\_CONTEXT](mf-event-mft-context.md) attribute of the event contains the value of the *ulParam* parameter.</span></span> <span data-ttu-id="02da0-125">Дополнительные сведения см. в разделе [асинхронная МФТС](asynchronous-mfts.md).</span><span class="sxs-lookup"><span data-stu-id="02da0-125">For more information, see [Asynchronous MFTs](asynchronous-mfts.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="02da0-126">Требования</span><span class="sxs-lookup"><span data-stu-id="02da0-126">Requirements</span></span>



| <span data-ttu-id="02da0-127">Требование</span><span class="sxs-lookup"><span data-stu-id="02da0-127">Requirement</span></span> | <span data-ttu-id="02da0-128">Значение</span><span class="sxs-lookup"><span data-stu-id="02da0-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02da0-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="02da0-129">Minimum supported client</span></span><br/> | <span data-ttu-id="02da0-130">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="02da0-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="02da0-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="02da0-131">Minimum supported server</span></span><br/> | <span data-ttu-id="02da0-132">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="02da0-132">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                  |
| <span data-ttu-id="02da0-133">Header</span><span class="sxs-lookup"><span data-stu-id="02da0-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="02da0-134"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="02da0-134"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02da0-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="02da0-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02da0-136">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="02da0-136">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="02da0-137">Асинхронный МФТС</span><span class="sxs-lookup"><span data-stu-id="02da0-137">Asynchronous MFTs</span></span>](asynchronous-mfts.md)
</dt> </dl>

 

 




