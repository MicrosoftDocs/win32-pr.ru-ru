---
description: Отправляется асинхронным Media Foundation преобразованием (MFT) по завершении операции очистки.
ms.assetid: 923055e5-a09a-402e-983b-6fa3cebb1b3a
title: Событие Метрансформдраинкомплете (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed291f9edacb11ba6edf7f5bd50a0715ae61a281
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348745"
---
# <a name="metransformdraincomplete-event"></a><span data-ttu-id="473cf-103">Событие Метрансформдраинкомплете</span><span class="sxs-lookup"><span data-stu-id="473cf-103">METransformDrainComplete event</span></span>

<span data-ttu-id="473cf-104">Отправляется асинхронным Media Foundation преобразованием (MFT) по завершении операции очистки.</span><span class="sxs-lookup"><span data-stu-id="473cf-104">Sent by an asynchronous Media Foundation transform (MFT) when a drain operation is complete.</span></span>

## <a name="event-values"></a><span data-ttu-id="473cf-105">Значения событий</span><span class="sxs-lookup"><span data-stu-id="473cf-105">Event values</span></span>

<span data-ttu-id="473cf-106">Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="473cf-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="473cf-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="473cf-107">VARTYPE</span></span>              | <span data-ttu-id="473cf-108">Описание</span><span class="sxs-lookup"><span data-stu-id="473cf-108">Description</span></span>               |
|----------------------|---------------------------|
| <span data-ttu-id="473cf-109">VT \_ пуст</span><span class="sxs-lookup"><span data-stu-id="473cf-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="473cf-110">Нет данных события.</span><span class="sxs-lookup"><span data-stu-id="473cf-110">No event data.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="473cf-111">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="473cf-111">Attributes</span></span>

<span data-ttu-id="473cf-112">Для этого события определены следующие атрибуты.</span><span class="sxs-lookup"><span data-stu-id="473cf-112">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="473cf-113">attribute</span><span class="sxs-lookup"><span data-stu-id="473cf-113">Attribute</span></span>                                                                        | <span data-ttu-id="473cf-114">Описание</span><span class="sxs-lookup"><span data-stu-id="473cf-114">Description</span></span>                                                                      |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [<span data-ttu-id="473cf-115">\_ \_ \_ ИД входного \_ потока MFT события \_ MF</span><span class="sxs-lookup"><span data-stu-id="473cf-115">MF\_EVENT\_MFT\_INPUT\_STREAM\_ID</span></span>](mf-event-mft-input-stream-id.md)<br/> | <span data-ttu-id="473cf-116">Идентификатор потока, который был остановлен.</span><span class="sxs-lookup"><span data-stu-id="473cf-116">The identifier of the stream that was drained.</span></span><br/><span data-ttu-id="473cf-117">*Необходимости*</span><span class="sxs-lookup"><span data-stu-id="473cf-117">*(Required)*</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="473cf-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="473cf-118">Remarks</span></span>

<span data-ttu-id="473cf-119">Асинхронный МФТС отправляет это событие через интерфейс [**имфмедиаевентженератор**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) .</span><span class="sxs-lookup"><span data-stu-id="473cf-119">Asynchronous MFTs send this event through the [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface.</span></span> <span data-ttu-id="473cf-120">Синхронное МФТС никогда не отправляет это событие.</span><span class="sxs-lookup"><span data-stu-id="473cf-120">Synchronous MFTs never send this event.</span></span>

<span data-ttu-id="473cf-121">Чтобы очистить MFT, вызовите [**имфтрансформ::P роцессмессаже**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) с сообщением о **\_ \_ \_ стоке команды сообщения MFT** .</span><span class="sxs-lookup"><span data-stu-id="473cf-121">To drain an MFT, call [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) with the **MFT\_MESSAGE\_COMMAND\_DRAIN** message.</span></span> <span data-ttu-id="473cf-122">Укажите входной поток для очистки в параметре *улпарам* .</span><span class="sxs-lookup"><span data-stu-id="473cf-122">Specify the input stream to drain in the *ulParam* parameter.</span></span> <span data-ttu-id="473cf-123">По завершении операции очистки асинхронная MFT отправляет событие Метрансформдраинкомплете.</span><span class="sxs-lookup"><span data-stu-id="473cf-123">When the drain operation is completed, an asynchronous MFT sends the METransformDrainComplete event.</span></span> <span data-ttu-id="473cf-124">Атрибут [ \_ \_ \_ \_ \_ идентификатора входного потока для события MF](mf-event-mft-input-stream-id.md) содержит идентификатор потока, заданный в параметре *улпарам* .</span><span class="sxs-lookup"><span data-stu-id="473cf-124">The [MF\_EVENT\_MFT\_INPUT\_STREAM\_ID](mf-event-mft-input-stream-id.md) attribute of the event contains the stream identifier given in the *ulParam* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="473cf-125">Требования</span><span class="sxs-lookup"><span data-stu-id="473cf-125">Requirements</span></span>



| <span data-ttu-id="473cf-126">Требование</span><span class="sxs-lookup"><span data-stu-id="473cf-126">Requirement</span></span> | <span data-ttu-id="473cf-127">Значение</span><span class="sxs-lookup"><span data-stu-id="473cf-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="473cf-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="473cf-128">Minimum supported client</span></span><br/> | <span data-ttu-id="473cf-129">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="473cf-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="473cf-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="473cf-130">Minimum supported server</span></span><br/> | <span data-ttu-id="473cf-131">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="473cf-131">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                  |
| <span data-ttu-id="473cf-132">Header</span><span class="sxs-lookup"><span data-stu-id="473cf-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="473cf-133"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="473cf-133"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="473cf-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="473cf-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="473cf-135">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="473cf-135">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="473cf-136">Асинхронный МФТС</span><span class="sxs-lookup"><span data-stu-id="473cf-136">Asynchronous MFTs</span></span>](asynchronous-mfts.md)
</dt> </dl>

 

 




