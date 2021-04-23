---
description: Вызывается источником мультимедиа, предоставляющим топологии через интерфейс Имфмедиасаурцетопологипровидер, например источник Sequencer. Источник создает событие, когда в нем есть новая презентация. Сеанс мультимедиа перенаправляет это событие в приложение.
ms.assetid: c669b2c9-5ece-4045-b691-8a71bbf491e1
title: Событие Меневпресентатион (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70265a84cc7724fc6f5b6a77be2181149bd82176
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263647"
---
# <a name="menewpresentation-event"></a><span data-ttu-id="fba2f-105">Событие Меневпресентатион</span><span class="sxs-lookup"><span data-stu-id="fba2f-105">MENewPresentation event</span></span>

<span data-ttu-id="fba2f-106">Вызывается источником мультимедиа, предоставляющим топологии через интерфейс [**имфмедиасаурцетопологипровидер**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) , например источник Sequencer.</span><span class="sxs-lookup"><span data-stu-id="fba2f-106">Raised by a media source that provides topologies through the [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) interface, such as the sequencer source.</span></span> <span data-ttu-id="fba2f-107">Источник создает событие, когда в нем есть новая презентация.</span><span class="sxs-lookup"><span data-stu-id="fba2f-107">The source raises the event when it has a new presentation.</span></span> <span data-ttu-id="fba2f-108">Сеанс мультимедиа перенаправляет это событие в приложение.</span><span class="sxs-lookup"><span data-stu-id="fba2f-108">The Media Session forwards this event to the application.</span></span>

## <a name="event-values"></a><span data-ttu-id="fba2f-109">Значения событий</span><span class="sxs-lookup"><span data-stu-id="fba2f-109">Event values</span></span>

<span data-ttu-id="fba2f-110">Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="fba2f-110">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="fba2f-111">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="fba2f-111">VARTYPE</span></span>                | <span data-ttu-id="fba2f-112">Описание</span><span class="sxs-lookup"><span data-stu-id="fba2f-112">Description</span></span>                                                                                                                                                             |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fba2f-113">VT \_ Unknown</span><span class="sxs-lookup"><span data-stu-id="fba2f-113">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="fba2f-114">Указатель на интерфейс [**имфпресентатиондескриптор**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) дескриптора презентации для новой презентации.</span><span class="sxs-lookup"><span data-stu-id="fba2f-114">Pointer to the [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) interface of the presentation descriptor for the new presentation.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="fba2f-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fba2f-115">Remarks</span></span>

<span data-ttu-id="fba2f-116">Приложение может получить топологию, соответствующую дескриптору презентации, вызвав [**имфмедиасаурцетопологипровидер:: жетмедиасаурцетопологи**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) в источнике мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="fba2f-116">The application can get the topology that corresponds to the presentation descriptor by calling [**IMFMediaSourceTopologyProvider::GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) on the media source.</span></span> <span data-ttu-id="fba2f-117">Приложение может затем поставить новую топологию в очередь в сеансе мультимедиа, вызвав [**имфмедиасессион:: сеттопологи**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).</span><span class="sxs-lookup"><span data-stu-id="fba2f-117">The application can then queue the new topology on the Media Session by calling [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).</span></span>

## <a name="requirements"></a><span data-ttu-id="fba2f-118">Требования</span><span class="sxs-lookup"><span data-stu-id="fba2f-118">Requirements</span></span>



| <span data-ttu-id="fba2f-119">Требование</span><span class="sxs-lookup"><span data-stu-id="fba2f-119">Requirement</span></span> | <span data-ttu-id="fba2f-120">Значение</span><span class="sxs-lookup"><span data-stu-id="fba2f-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fba2f-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fba2f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="fba2f-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fba2f-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="fba2f-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fba2f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="fba2f-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fba2f-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="fba2f-125">Header</span><span class="sxs-lookup"><span data-stu-id="fba2f-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="fba2f-126"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fba2f-126"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fba2f-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fba2f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fba2f-128">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="fba2f-128">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="fba2f-129">Источник Sequencer</span><span class="sxs-lookup"><span data-stu-id="fba2f-129">Sequencer Source</span></span>](sequencer-source.md)
</dt> </dl>

 

 




