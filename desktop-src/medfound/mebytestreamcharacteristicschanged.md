---
description: Отправляется потоком байтов при изменении характеристик потока байтов.
ms.assetid: EC34A7A3-BF01-4F9E-BA79-131B76D4C58F
title: Событие Мебитестреамчарактеристиксчанжед (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e626f510927970aad3c51182fca3a6dfddb0009
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105719406"
---
# <a name="mebytestreamcharacteristicschanged-event"></a><span data-ttu-id="e75e6-103">Событие Мебитестреамчарактеристиксчанжед</span><span class="sxs-lookup"><span data-stu-id="e75e6-103">MEByteStreamCharacteristicsChanged event</span></span>

<span data-ttu-id="e75e6-104">Отправляется потоком байтов при изменении характеристик потока байтов.</span><span class="sxs-lookup"><span data-stu-id="e75e6-104">Sent by a byte stream when the characteristics of the byte stream have changed.</span></span>

## <a name="event-values"></a><span data-ttu-id="e75e6-105">Значения событий</span><span class="sxs-lookup"><span data-stu-id="e75e6-105">Event values</span></span>

<span data-ttu-id="e75e6-106">Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="e75e6-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="e75e6-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="e75e6-107">VARTYPE</span></span>               | <span data-ttu-id="e75e6-108">Описание</span><span class="sxs-lookup"><span data-stu-id="e75e6-108">Description</span></span>                           |
|-----------------------|---------------------------------------|
| <span data-ttu-id="e75e6-109">VT \_ пуст</span><span class="sxs-lookup"><span data-stu-id="e75e6-109">VT\_EMPTY</span></span> <br/> | <span data-ttu-id="e75e6-110">Нет данных события.</span><span class="sxs-lookup"><span data-stu-id="e75e6-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="e75e6-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e75e6-111">Remarks</span></span>

<span data-ttu-id="e75e6-112">Это событие означает, что изменилась одна или несколько из следующих характеристик:</span><span class="sxs-lookup"><span data-stu-id="e75e6-112">This event indicates that one or more of the following characteristics has changed:</span></span>

-   <span data-ttu-id="e75e6-113">Флаги возможностей ([**имфбитестреам:: Capabilities**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-getcapabilities))</span><span class="sxs-lookup"><span data-stu-id="e75e6-113">Capability flags ([**IMFByteStream::GetCapabilities**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-getcapabilities))</span></span>
-   <span data-ttu-id="e75e6-114">Флаг конца потока ([**имфбитестреам:: исендофстреам**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-isendofstream))</span><span class="sxs-lookup"><span data-stu-id="e75e6-114">End-of-stream flag ([**IMFByteStream::IsEndOfStream**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-isendofstream))</span></span>
-   <span data-ttu-id="e75e6-115">Length ([**имфбитестреам:: DATALENGTH**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-getlength))</span><span class="sxs-lookup"><span data-stu-id="e75e6-115">Length ([**IMFByteStream::GetLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-getlength))</span></span>

<span data-ttu-id="e75e6-116">Это событие поддерживают не все реализации [**имфбитестреам**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) .</span><span class="sxs-lookup"><span data-stu-id="e75e6-116">Not all [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) implementations support this event.</span></span> <span data-ttu-id="e75e6-117">Чтобы получить событие, запросите объект байтового потока для интерфейса [**имфмедиаевентженератор**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) .</span><span class="sxs-lookup"><span data-stu-id="e75e6-117">To receive the event, query the byte-stream object for the [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="e75e6-118">Требования</span><span class="sxs-lookup"><span data-stu-id="e75e6-118">Requirements</span></span>



| <span data-ttu-id="e75e6-119">Требование</span><span class="sxs-lookup"><span data-stu-id="e75e6-119">Requirement</span></span> | <span data-ttu-id="e75e6-120">Значение</span><span class="sxs-lookup"><span data-stu-id="e75e6-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e75e6-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e75e6-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e75e6-122">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="e75e6-122">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="e75e6-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e75e6-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e75e6-124">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="e75e6-124">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e75e6-125">Header</span><span class="sxs-lookup"><span data-stu-id="e75e6-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="e75e6-126"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e75e6-126"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e75e6-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e75e6-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e75e6-128">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e75e6-128">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




