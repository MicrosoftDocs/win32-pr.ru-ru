---
description: 'Вызывается источником Sequencer, когда метод Имфсекуенцерсаурце:: Упдатетопологи завершается асинхронно.'
ms.assetid: f573cbd0-689c-4bfe-846b-6fc8008101c8
title: Событие Месекуенцерсаурцетопологюпдатед (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: baaf03119832937a584178b9f5958b066046c633
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711568"
---
# <a name="mesequencersourcetopologyupdated-event"></a><span data-ttu-id="b7a2f-103">Событие Месекуенцерсаурцетопологюпдатед</span><span class="sxs-lookup"><span data-stu-id="b7a2f-103">MESequencerSourceTopologyUpdated event</span></span>

<span data-ttu-id="b7a2f-104">Вызывается источником Sequencer, когда метод [**имфсекуенцерсаурце:: упдатетопологи**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopology) завершается асинхронно.</span><span class="sxs-lookup"><span data-stu-id="b7a2f-104">Raised by the sequencer source when the [**IMFSequencerSource::UpdateTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopology) method completes asynchronously.</span></span>

## <a name="event-values"></a><span data-ttu-id="b7a2f-105">Значения событий</span><span class="sxs-lookup"><span data-stu-id="b7a2f-105">Event values</span></span>

<span data-ttu-id="b7a2f-106">Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="b7a2f-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="b7a2f-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="b7a2f-107">VARTYPE</span></span>            | <span data-ttu-id="b7a2f-108">Описание</span><span class="sxs-lookup"><span data-stu-id="b7a2f-108">Description</span></span>                                                                                                                                                                                                                        |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7a2f-109">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="b7a2f-109">VT\_UI4</span></span><br/> | <span data-ttu-id="b7a2f-110">Идентификатор элемента Sequencer для обновляемой топологии.</span><span class="sxs-lookup"><span data-stu-id="b7a2f-110">Sequencer element identifier of the topology that is being updated.</span></span> <span data-ttu-id="b7a2f-111">Приложение задает это значение в параметре *ДВИД* метода [**упдатетопологи**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopology) .</span><span class="sxs-lookup"><span data-stu-id="b7a2f-111">The application specifies this value in the *dwId* parameter of the [**UpdateTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopology) method.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="b7a2f-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b7a2f-112">Remarks</span></span>

<span data-ttu-id="b7a2f-113">Это событие сигнализирует, что источник Sequencer обновил топологию, но не означает, что топология готова к воспроизведению.</span><span class="sxs-lookup"><span data-stu-id="b7a2f-113">This event signals that the sequencer source has updated the topology, but does not mean that the topology is ready for playback.</span></span> <span data-ttu-id="b7a2f-114">Приложение должно ожидать события [месессионтопологистатус](mesessiontopologystatus.md) .</span><span class="sxs-lookup"><span data-stu-id="b7a2f-114">The application should wait for the [MESessionTopologyStatus](mesessiontopologystatus.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7a2f-115">Требования</span><span class="sxs-lookup"><span data-stu-id="b7a2f-115">Requirements</span></span>



| <span data-ttu-id="b7a2f-116">Требование</span><span class="sxs-lookup"><span data-stu-id="b7a2f-116">Requirement</span></span> | <span data-ttu-id="b7a2f-117">Значение</span><span class="sxs-lookup"><span data-stu-id="b7a2f-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7a2f-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b7a2f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b7a2f-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b7a2f-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b7a2f-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b7a2f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b7a2f-121">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b7a2f-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b7a2f-122">Header</span><span class="sxs-lookup"><span data-stu-id="b7a2f-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7a2f-123"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b7a2f-123"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7a2f-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b7a2f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7a2f-125">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b7a2f-125">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="b7a2f-126">Источник Sequencer</span><span class="sxs-lookup"><span data-stu-id="b7a2f-126">Sequencer Source</span></span>](sequencer-source.md)
</dt> </dl>

 

 




