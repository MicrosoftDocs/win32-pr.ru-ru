---
description: Вызывается приемниками потоков расширенного модуля подготовки видео (Евр) при изменении видеоустройства.
ms.assetid: 5b663d6b-5df8-4321-a6a5-a21b9810065a
title: Событие Местреамсинкдевицечанжед (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 651fc34a56ca52cfb9e0b3f20e6e4d6b5366f541
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711216"
---
# <a name="mestreamsinkdevicechanged-event"></a><span data-ttu-id="79171-103">Событие Местреамсинкдевицечанжед</span><span class="sxs-lookup"><span data-stu-id="79171-103">MEStreamSinkDeviceChanged event</span></span>

<span data-ttu-id="79171-104">Вызывается приемниками потоков расширенного модуля подготовки видео (Евр) при изменении видеоустройства.</span><span class="sxs-lookup"><span data-stu-id="79171-104">Raised by the stream sinks of the enhanced video renderer (EVR) if the video device changes.</span></span> <span data-ttu-id="79171-105">Например, ЕВР вызывает это событие при получении события [**\_ \_ изменения дисплея EC**](../directshow/ec-display-changed.md) .</span><span class="sxs-lookup"><span data-stu-id="79171-105">For example, the EVR raises this event when it receives an [**EC\_DISPLAY\_CHANGED**](../directshow/ec-display-changed.md) event.</span></span>

<span data-ttu-id="79171-106">Конвейер Media Foundation отвечает на это событие, повторно отправляя все примеры запросов, которые завершились сбоем во время изменения устройства.</span><span class="sxs-lookup"><span data-stu-id="79171-106">The Media Foundation pipeline responds to this event by resubmitting all sample requests that failed while the device was changing.</span></span>

## <a name="event-values"></a><span data-ttu-id="79171-107">Значения событий</span><span class="sxs-lookup"><span data-stu-id="79171-107">Event values</span></span>

<span data-ttu-id="79171-108">Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="79171-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="79171-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="79171-109">VARTYPE</span></span>              | <span data-ttu-id="79171-110">Описание</span><span class="sxs-lookup"><span data-stu-id="79171-110">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="79171-111">VT \_ пуст</span><span class="sxs-lookup"><span data-stu-id="79171-111">VT\_EMPTY</span></span><br/> | <span data-ttu-id="79171-112">Нет данных события.</span><span class="sxs-lookup"><span data-stu-id="79171-112">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="79171-113">Требования</span><span class="sxs-lookup"><span data-stu-id="79171-113">Requirements</span></span>



| <span data-ttu-id="79171-114">Требование</span><span class="sxs-lookup"><span data-stu-id="79171-114">Requirement</span></span> | <span data-ttu-id="79171-115">Значение</span><span class="sxs-lookup"><span data-stu-id="79171-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79171-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="79171-116">Minimum supported client</span></span><br/> | <span data-ttu-id="79171-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="79171-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="79171-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="79171-118">Minimum supported server</span></span><br/> | <span data-ttu-id="79171-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="79171-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="79171-120">Header</span><span class="sxs-lookup"><span data-stu-id="79171-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="79171-121"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="79171-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79171-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="79171-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79171-123">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="79171-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="79171-124">Приемники носителей</span><span class="sxs-lookup"><span data-stu-id="79171-124">Media Sinks</span></span>](media-sinks.md)
</dt> </dl>

 

 
