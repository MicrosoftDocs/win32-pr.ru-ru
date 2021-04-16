---
description: Сообщает, что источник мультимедиа начал работу с данными буфера.
ms.assetid: 8637dfcd-2e0c-4cf4-a216-4089c201bfc6
title: Событие Мебуфферингстартед (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8eb3baf8e66d44eb67ee4c1bbc54ae2e197db081
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105719407"
---
# <a name="mebufferingstarted-event"></a><span data-ttu-id="21bb7-103">Событие Мебуфферингстартед</span><span class="sxs-lookup"><span data-stu-id="21bb7-103">MEBufferingStarted event</span></span>

<span data-ttu-id="21bb7-104">Сообщает, что источник мультимедиа начал работу с данными буфера.</span><span class="sxs-lookup"><span data-stu-id="21bb7-104">Signals that a media source has started to buffer data.</span></span>

<span data-ttu-id="21bb7-105">Источник мультимедиа может отправить это событие, если исходные буферы находятся во время выполнения сеанса мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="21bb7-105">A media source can send this event if the source buffers data while the Media Session is running.</span></span> <span data-ttu-id="21bb7-106">Когда сеанс мультимедиа получает это событие, он приостанавливает время презентации, пока источник мультимедиа не отправит событие [мебуфферингстоппед](mebufferingstopped.md) .</span><span class="sxs-lookup"><span data-stu-id="21bb7-106">When the Media Session receives this event, it pauses the presentation clock until the media source sends the [MEBufferingStopped](mebufferingstopped.md) event.</span></span> <span data-ttu-id="21bb7-107">Сеанс мультимедиа также перенаправляет событие Мебуфферингстартед в приложение.</span><span class="sxs-lookup"><span data-stu-id="21bb7-107">The Media Session also forwards the MEBufferingStarted event to the application.</span></span>

<span data-ttu-id="21bb7-108">Потоковые потоки, которые реализуют интерфейс [**имфбитестреамбуфферинг**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreambuffering) , также отправляют это событие.</span><span class="sxs-lookup"><span data-stu-id="21bb7-108">Byte streams that implement the [**IMFByteStreamBuffering**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreambuffering) interface also send this event.</span></span>

## <a name="event-values"></a><span data-ttu-id="21bb7-109">Значения событий</span><span class="sxs-lookup"><span data-stu-id="21bb7-109">Event values</span></span>

<span data-ttu-id="21bb7-110">Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="21bb7-110">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="21bb7-111">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="21bb7-111">VARTYPE</span></span>              | <span data-ttu-id="21bb7-112">Описание</span><span class="sxs-lookup"><span data-stu-id="21bb7-112">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="21bb7-113">VT \_ пуст</span><span class="sxs-lookup"><span data-stu-id="21bb7-113">VT\_EMPTY</span></span><br/> | <span data-ttu-id="21bb7-114">Нет данных события.</span><span class="sxs-lookup"><span data-stu-id="21bb7-114">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="21bb7-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="21bb7-115">Remarks</span></span>

<span data-ttu-id="21bb7-116">Если источник мультимедиа отправляет событие Мебуфферингстартед, он должен отправить событие [мебуфферингстоппед](mebufferingstopped.md) при остановке буферизации данных.</span><span class="sxs-lookup"><span data-stu-id="21bb7-116">If a media source sends the MEBufferingStarted event, it must send the [MEBufferingStopped](mebufferingstopped.md) event when it stops buffering data.</span></span> <span data-ttu-id="21bb7-117">Источник мультимедиа должен отправить соответствующее событие Мебуфферингстоппед для каждого события Мебуфферингстартед.</span><span class="sxs-lookup"><span data-stu-id="21bb7-117">The media source must send a matching MEBufferingStopped event for every MEBufferingStarted event.</span></span> <span data-ttu-id="21bb7-118">Источник мультимедиа не должен пересылать эти события перед вызовом метода [**имфмедиасаурце:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) источника или после вызова метода [**Имфмедиасаурце:: останавливаться**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop) источника.</span><span class="sxs-lookup"><span data-stu-id="21bb7-118">The media source should not forward these events before the source's [**IMFMediaSource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) method is called, or after the source's [**IMFMediaSource::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop) method is called.</span></span>

<span data-ttu-id="21bb7-119">При потоковой передаче из Media Foundation сетевого источника можно получить ход буферизации, запросив статистику по **\_ \_ идентификатору буфферпрогресс мфнетсаурце** .</span><span class="sxs-lookup"><span data-stu-id="21bb7-119">If you are streaming from the Media Foundation network source, you can get the buffering progress by querying the **MFNETSOURCE\_BUFFERPROGRESS\_ID** statistic.</span></span> <span data-ttu-id="21bb7-120">Дополнительные сведения см. в разделе [**мфнетсаурце \_ Statistics \_ IDS**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids).</span><span class="sxs-lookup"><span data-stu-id="21bb7-120">For more information, see [**MFNETSOURCE\_STATISTICS\_IDS**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids).</span></span>

## <a name="examples"></a><span data-ttu-id="21bb7-121">Примеры</span><span class="sxs-lookup"><span data-stu-id="21bb7-121">Examples</span></span>


```C++
HRESULT GetBufferProgress(IMFMediaSession *pSession, DWORD *pProgress)
{
    IPropertyStore *pProp = NULL;
    PROPVARIANT var;

    // Get the property store from the media session.
    HRESULT hr = MFGetService(
        pSession, 
        MFNETSOURCE_STATISTICS_SERVICE, 
        IID_PPV_ARGS(&pProp)
        );

    if (SUCCEEDED(hr))
    {
        PROPERTYKEY key;
        key.fmtid = MFNETSOURCE_STATISTICS;
        key.pid = MFNETSOURCE_BUFFERPROGRESS_ID;

        hr = pProp->GetValue(key, &var);
    }

    if (SUCCEEDED(hr))
    {
        *pProgress = var.lVal;
    }

    PropVariantClear(&var);
    SafeRelease(&pProp);
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="21bb7-122">Требования</span><span class="sxs-lookup"><span data-stu-id="21bb7-122">Requirements</span></span>



| <span data-ttu-id="21bb7-123">Требование</span><span class="sxs-lookup"><span data-stu-id="21bb7-123">Requirement</span></span> | <span data-ttu-id="21bb7-124">Значение</span><span class="sxs-lookup"><span data-stu-id="21bb7-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21bb7-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="21bb7-125">Minimum supported client</span></span><br/> | <span data-ttu-id="21bb7-126">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="21bb7-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="21bb7-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="21bb7-127">Minimum supported server</span></span><br/> | <span data-ttu-id="21bb7-128">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="21bb7-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="21bb7-129">Header</span><span class="sxs-lookup"><span data-stu-id="21bb7-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="21bb7-130"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="21bb7-130"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21bb7-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="21bb7-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21bb7-132">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="21bb7-132">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="21bb7-133">Сетевые подключения в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="21bb7-133">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




