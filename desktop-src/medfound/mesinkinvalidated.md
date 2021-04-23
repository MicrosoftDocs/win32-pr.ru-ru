---
description: Возникает, когда приемник мультимедиа станет недействительным.
ms.assetid: fa75926e-7cef-44da-9efe-f2f86fd4fd45
title: Событие Месинкинвалидатед (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46807a45e907999b34190f9678bd3dc0051680ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263257"
---
# <a name="mesinkinvalidated-event"></a><span data-ttu-id="d3baf-103">Событие Месинкинвалидатед</span><span class="sxs-lookup"><span data-stu-id="d3baf-103">MESinkInvalidated event</span></span>

<span data-ttu-id="d3baf-104">Возникает, когда приемник мультимедиа станет недействительным.</span><span class="sxs-lookup"><span data-stu-id="d3baf-104">Raised when a media sink becomes invalid.</span></span>

## <a name="event-values"></a><span data-ttu-id="d3baf-105">Значения событий</span><span class="sxs-lookup"><span data-stu-id="d3baf-105">Event values</span></span>

<span data-ttu-id="d3baf-106">Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="d3baf-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="d3baf-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="d3baf-107">VARTYPE</span></span>              | <span data-ttu-id="d3baf-108">Описание</span><span class="sxs-lookup"><span data-stu-id="d3baf-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="d3baf-109">VT \_ пуст</span><span class="sxs-lookup"><span data-stu-id="d3baf-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="d3baf-110">Нет данных события.</span><span class="sxs-lookup"><span data-stu-id="d3baf-110">No event data.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="d3baf-111">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="d3baf-111">Attributes</span></span>

<span data-ttu-id="d3baf-112">Для этого события определены следующие атрибуты.</span><span class="sxs-lookup"><span data-stu-id="d3baf-112">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="d3baf-113">attribute</span><span class="sxs-lookup"><span data-stu-id="d3baf-113">Attribute</span></span>                                                                    | <span data-ttu-id="d3baf-114">Описание</span><span class="sxs-lookup"><span data-stu-id="d3baf-114">Description</span></span>                                                              |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [<span data-ttu-id="d3baf-115">**\_ \_ узел вывода событий \_ MF**</span><span class="sxs-lookup"><span data-stu-id="d3baf-115">**MF\_EVENT\_OUTPUT\_NODE**</span></span>](mf-event-output-node-attribute.md)<br/> | <span data-ttu-id="d3baf-116">Определяет узел топологии для этого приемника мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="d3baf-116">Identifies the topology node for this media sink.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="d3baf-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d3baf-117">Remarks</span></span>

<span data-ttu-id="d3baf-118">Сеанс мультимедиа вызывает это событие, если оно получает одно из следующих событий из приемника мультимедиа:</span><span class="sxs-lookup"><span data-stu-id="d3baf-118">The Media Session raises this event if it receives any of the following events from the media sink:</span></span>

-   [<span data-ttu-id="d3baf-119">меаудиосессиондевицеремовед</span><span class="sxs-lookup"><span data-stu-id="d3baf-119">MEAudioSessionDeviceRemoved</span></span>](meaudiosessiondeviceremoved.md)

-   [<span data-ttu-id="d3baf-120">меаудиосессиондисконнектед</span><span class="sxs-lookup"><span data-stu-id="d3baf-120">MEAudioSessionDisconnected</span></span>](meaudiosessiondisconnected.md)

-   [<span data-ttu-id="d3baf-121">меаудиосессионексклусивемодеоверриде</span><span class="sxs-lookup"><span data-stu-id="d3baf-121">MEAudioSessionExclusiveModeOverride</span></span>](meaudiosessionexclusivemodeoverride.md)

-   [<span data-ttu-id="d3baf-122">меаудиосессионформатчанжед</span><span class="sxs-lookup"><span data-stu-id="d3baf-122">MEAudioSessionFormatChanged</span></span>](meaudiosessionformatchanged.md)

-   [<span data-ttu-id="d3baf-123">меаудиосессионсервершутдовн</span><span class="sxs-lookup"><span data-stu-id="d3baf-123">MEAudioSessionServerShutdown</span></span>](meaudiosessionservershutdown.md)

<span data-ttu-id="d3baf-124">Приемник мультимедиа также может вызвать это событие. в этом случае сеанс мультимедиа задает атрибут [**\_ \_ \_ узла вывода события MF**](mf-event-output-node-attribute.md) для события и перенаправляет событие в приложение.</span><span class="sxs-lookup"><span data-stu-id="d3baf-124">A media sink can also raise this event, in which case the Media Session sets the [**MF\_EVENT\_OUTPUT\_NODE**](mf-event-output-node-attribute.md) attribute on the event and forwards the event to the application.</span></span>

<span data-ttu-id="d3baf-125">Если приложение получает это событие, оно должно заново создать приемник мультимедиа и поставить топологию повторно.</span><span class="sxs-lookup"><span data-stu-id="d3baf-125">If the application receives this event, it needs to recreate the media sink and queue the topology again.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3baf-126">Требования</span><span class="sxs-lookup"><span data-stu-id="d3baf-126">Requirements</span></span>



| <span data-ttu-id="d3baf-127">Требование</span><span class="sxs-lookup"><span data-stu-id="d3baf-127">Requirement</span></span> | <span data-ttu-id="d3baf-128">Значение</span><span class="sxs-lookup"><span data-stu-id="d3baf-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3baf-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d3baf-129">Minimum supported client</span></span><br/> | <span data-ttu-id="d3baf-130">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d3baf-130">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d3baf-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d3baf-131">Minimum supported server</span></span><br/> | <span data-ttu-id="d3baf-132">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d3baf-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d3baf-133">Header</span><span class="sxs-lookup"><span data-stu-id="d3baf-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3baf-134"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d3baf-134"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3baf-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d3baf-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3baf-136">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d3baf-136">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




