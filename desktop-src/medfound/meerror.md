---
description: 'Сигнализирует о серьезной ошибке. Любой компонент Media Foundation может отправить это событие в любое время. Вызовите Имфмедиаевент:: Status, чтобы получить код ошибки операции, которая завершилась ошибкой.'
ms.assetid: bff80041-77d8-43b1-a410-9cefaf45eb2c
title: Событие Миррор (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0eb557dffb2c73a63031a193c331edabe470db7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692676"
---
# <a name="meerror-event"></a><span data-ttu-id="42e2c-105">Событие Миррор</span><span class="sxs-lookup"><span data-stu-id="42e2c-105">MEError event</span></span>

<span data-ttu-id="42e2c-106">Сигнализирует о серьезной ошибке.</span><span class="sxs-lookup"><span data-stu-id="42e2c-106">Signals a serious error.</span></span> <span data-ttu-id="42e2c-107">Любой компонент Media Foundation может отправить это событие в любое время.</span><span class="sxs-lookup"><span data-stu-id="42e2c-107">Any Media Foundation component can send this event at any time.</span></span> <span data-ttu-id="42e2c-108">Вызовите [**имфмедиаевент:: Status**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) , чтобы получить код ошибки операции, которая завершилась ошибкой.</span><span class="sxs-lookup"><span data-stu-id="42e2c-108">Call [**IMFMediaEvent::GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) to get the error code of the operation that failed.</span></span>

## <a name="event-values"></a><span data-ttu-id="42e2c-109">Значения событий</span><span class="sxs-lookup"><span data-stu-id="42e2c-109">Event values</span></span>

<span data-ttu-id="42e2c-110">Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="42e2c-110">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="42e2c-111">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="42e2c-111">VARTYPE</span></span>              | <span data-ttu-id="42e2c-112">Описание</span><span class="sxs-lookup"><span data-stu-id="42e2c-112">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="42e2c-113">VT \_ пуст</span><span class="sxs-lookup"><span data-stu-id="42e2c-113">VT\_EMPTY</span></span><br/> | <span data-ttu-id="42e2c-114">Нет данных события.</span><span class="sxs-lookup"><span data-stu-id="42e2c-114">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="42e2c-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="42e2c-115">Remarks</span></span>

<span data-ttu-id="42e2c-116">Это событие следует использовать только для непредвиденных ошибок.</span><span class="sxs-lookup"><span data-stu-id="42e2c-116">This event should be used only for unexpected errors.</span></span> <span data-ttu-id="42e2c-117">Не отправляйте это событие, чтобы сообщить о сбое асинхронного метода.</span><span class="sxs-lookup"><span data-stu-id="42e2c-117">Do not send this event to signal that an asynchronous method failed.</span></span> <span data-ttu-id="42e2c-118">В случае сбоя асинхронного метода код ошибки возвращается в виде обычного события для этого метода.</span><span class="sxs-lookup"><span data-stu-id="42e2c-118">If an asynchronous method fails, the error code is returned in the normal event for that method.</span></span>

<span data-ttu-id="42e2c-119">Если во время потоковой передачи возникает устранимая ошибка, отправьте событие [менонфаталеррор](menonfatalerror.md) .</span><span class="sxs-lookup"><span data-stu-id="42e2c-119">If a recoverable error occurs during streaming, send the [MENonFatalError](menonfatalerror.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="42e2c-120">Требования</span><span class="sxs-lookup"><span data-stu-id="42e2c-120">Requirements</span></span>



| <span data-ttu-id="42e2c-121">Требование</span><span class="sxs-lookup"><span data-stu-id="42e2c-121">Requirement</span></span> | <span data-ttu-id="42e2c-122">Значение</span><span class="sxs-lookup"><span data-stu-id="42e2c-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42e2c-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="42e2c-123">Minimum supported client</span></span><br/> | <span data-ttu-id="42e2c-124">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="42e2c-124">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="42e2c-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="42e2c-125">Minimum supported server</span></span><br/> | <span data-ttu-id="42e2c-126">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="42e2c-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="42e2c-127">Header</span><span class="sxs-lookup"><span data-stu-id="42e2c-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="42e2c-128"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="42e2c-128"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42e2c-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="42e2c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42e2c-130">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="42e2c-130">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




