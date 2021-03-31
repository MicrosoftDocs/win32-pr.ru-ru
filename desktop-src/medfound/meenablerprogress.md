---
description: Сообщает о ходе выполнения объекта включения содержимого. Объекты, которые предоставляют интерфейс Имфконтентенаблер, могут вызвать это событие, чтобы уведомить приложение о ходе выполнения действий созидателями содержимого.
ms.assetid: ec14ba9b-cfb6-4e32-870e-2436e11c308b
title: Событие Минаблерпрогресс (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58303835113408a7fe09436967286d5ff988acdc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263650"
---
# <a name="meenablerprogress-event"></a><span data-ttu-id="7656b-104">Событие Минаблерпрогресс</span><span class="sxs-lookup"><span data-stu-id="7656b-104">MEEnablerProgress event</span></span>

<span data-ttu-id="7656b-105">Сообщает о ходе выполнения объекта включения содержимого.</span><span class="sxs-lookup"><span data-stu-id="7656b-105">Signals the progress of a content enabler object.</span></span> <span data-ttu-id="7656b-106">Объекты, которые предоставляют интерфейс [**имфконтентенаблер**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) , могут вызвать это событие, чтобы уведомить приложение о ходе выполнения действий программы.</span><span class="sxs-lookup"><span data-stu-id="7656b-106">Objects that expose the [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) interface can raise this event to notify the application about the progress of the content enabler's actions.</span></span>

## <a name="event-values"></a><span data-ttu-id="7656b-107">Значения событий</span><span class="sxs-lookup"><span data-stu-id="7656b-107">Event values</span></span>

<span data-ttu-id="7656b-108">Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="7656b-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="7656b-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="7656b-109">VARTYPE</span></span>               | <span data-ttu-id="7656b-110">Описание</span><span class="sxs-lookup"><span data-stu-id="7656b-110">Description</span></span>                                                               |
|-----------------------|---------------------------------------------------------------------------|
| <span data-ttu-id="7656b-111">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="7656b-111">VT\_LPWSTR</span></span><br/> | <span data-ttu-id="7656b-112">Строка расширенных символов, описывающая ход выполнения.</span><span class="sxs-lookup"><span data-stu-id="7656b-112">Wide-character string that describes the progress.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="7656b-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7656b-113">Remarks</span></span>

<span data-ttu-id="7656b-114">Чтобы получить это событие, запросите интерфейс [**имфконтентенаблер**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) для интерфейса [**имфмедиаевентженератор**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) .</span><span class="sxs-lookup"><span data-stu-id="7656b-114">To receive this event, query the [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) interface for the [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface.</span></span> <span data-ttu-id="7656b-115">Затем вызовите [**имфмедиаевентженератор:: бегинжетевент**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent), как описано в разделе [генераторы событий мультимедиа](media-event-generators.md).</span><span class="sxs-lookup"><span data-stu-id="7656b-115">Then call [**IMFMediaEventGenerator::BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent), as described in the topic [Media Event Generators](media-event-generators.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7656b-116">Требования</span><span class="sxs-lookup"><span data-stu-id="7656b-116">Requirements</span></span>



| <span data-ttu-id="7656b-117">Требование</span><span class="sxs-lookup"><span data-stu-id="7656b-117">Requirement</span></span> | <span data-ttu-id="7656b-118">Значение</span><span class="sxs-lookup"><span data-stu-id="7656b-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7656b-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7656b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7656b-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7656b-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="7656b-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7656b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7656b-122">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7656b-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7656b-123">Header</span><span class="sxs-lookup"><span data-stu-id="7656b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="7656b-124"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7656b-124"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7656b-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7656b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7656b-126">**имфконтентенаблер**</span><span class="sxs-lookup"><span data-stu-id="7656b-126">**IMFContentEnabler**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler)
</dt> <dt>

[<span data-ttu-id="7656b-127">Генераторы событий мультимедиа</span><span class="sxs-lookup"><span data-stu-id="7656b-127">Media Event Generators</span></span>](media-event-generators.md)
</dt> <dt>

[<span data-ttu-id="7656b-128">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7656b-128">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




