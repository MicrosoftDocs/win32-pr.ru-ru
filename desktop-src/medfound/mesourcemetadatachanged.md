---
description: Вызывается источником мультимедиа при обновлении его метаданных.
ms.assetid: 6818b0c9-9628-41e6-8dc6-dff26f4fcfd2
title: Событие Месаурцеметадатачанжед (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b72463d145d7b4b4b14ac3c321f19a7f9a4c2178
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991239"
---
# <a name="mesourcemetadatachanged-event"></a><span data-ttu-id="be310-103">Событие Месаурцеметадатачанжед</span><span class="sxs-lookup"><span data-stu-id="be310-103">MESourceMetadataChanged event</span></span>

<span data-ttu-id="be310-104">Вызывается источником мультимедиа при обновлении его метаданных.</span><span class="sxs-lookup"><span data-stu-id="be310-104">Raised by a media source when it updates its metadata.</span></span>

## <a name="event-values"></a><span data-ttu-id="be310-105">Значения событий</span><span class="sxs-lookup"><span data-stu-id="be310-105">Event values</span></span>

<span data-ttu-id="be310-106">Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="be310-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="be310-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="be310-107">VARTYPE</span></span>              | <span data-ttu-id="be310-108">Описание</span><span class="sxs-lookup"><span data-stu-id="be310-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="be310-109">VT \_ пуст</span><span class="sxs-lookup"><span data-stu-id="be310-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="be310-110">Нет данных события.</span><span class="sxs-lookup"><span data-stu-id="be310-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="be310-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="be310-111">Remarks</span></span>

<span data-ttu-id="be310-112">Если источник мультимедиа не может предоставить все метаданные при первоначальном создании источника, он должен вызвать это событие после того, как метаданные будут доступны.</span><span class="sxs-lookup"><span data-stu-id="be310-112">If the media source cannot provide all of the metadata when the source is first created, it should raise this event after the metadata is available.</span></span>

<span data-ttu-id="be310-113">Источник мультимедиа должен создать новый дескриптор представления и скопировать все атрибуты из дескриптора презентации (PD) в объект события.</span><span class="sxs-lookup"><span data-stu-id="be310-113">The media source should create a new presentation descriptor and copy all of the attributes from the presentation descriptor (PD) to the event object.</span></span> <span data-ttu-id="be310-114">Приложение может использовать объект события для перечисления новых атрибутов PD.</span><span class="sxs-lookup"><span data-stu-id="be310-114">The application can use the event object to enumerate the new PD attributes.</span></span> <span data-ttu-id="be310-115">В частности, значения для файла [с \_ \_ продолжительностью MF PD](mf-pd-duration-attribute.md) и [MF \_ PD \_ общего \_ \_ размера](mf-pd-total-file-size-attribute.md) могут быть неизвестны до тех пор, пока файл не будет полностью скачан.</span><span class="sxs-lookup"><span data-stu-id="be310-115">In particular, the values for [MF\_PD\_DURATION](mf-pd-duration-attribute.md) and [MF\_PD\_TOTAL\_FILE\_SIZE](mf-pd-total-file-size-attribute.md) might be unknown until the file is completely downloaded.</span></span>

## <a name="requirements"></a><span data-ttu-id="be310-116">Требования</span><span class="sxs-lookup"><span data-stu-id="be310-116">Requirements</span></span>



| <span data-ttu-id="be310-117">Требование</span><span class="sxs-lookup"><span data-stu-id="be310-117">Requirement</span></span> | <span data-ttu-id="be310-118">Значение</span><span class="sxs-lookup"><span data-stu-id="be310-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be310-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="be310-119">Minimum supported client</span></span><br/> | <span data-ttu-id="be310-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="be310-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="be310-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="be310-121">Minimum supported server</span></span><br/> | <span data-ttu-id="be310-122">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="be310-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="be310-123">Header</span><span class="sxs-lookup"><span data-stu-id="be310-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="be310-124"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="be310-124"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be310-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="be310-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be310-126">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="be310-126">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="be310-127">Атрибуты дескриптора представления</span><span class="sxs-lookup"><span data-stu-id="be310-127">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




