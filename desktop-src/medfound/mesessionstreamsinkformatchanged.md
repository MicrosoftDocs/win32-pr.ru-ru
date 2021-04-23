---
description: Вызывается сеансом мультимедиа при изменении формата в приемнике мультимедиа.
ms.assetid: f56419f8-7f50-4eda-bf4a-fcdbbe46e180
title: Событие Месессионстреамсинкформатчанжед (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bed59b9600cbaf8cb942a42beb6bed46d62fc15f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263642"
---
# <a name="mesessionstreamsinkformatchanged-event"></a><span data-ttu-id="b337b-103">Событие Месессионстреамсинкформатчанжед</span><span class="sxs-lookup"><span data-stu-id="b337b-103">MESessionStreamSinkFormatChanged event</span></span>

<span data-ttu-id="b337b-104">Вызывается сеансом мультимедиа при изменении формата в приемнике мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="b337b-104">Raised by the Media Session when the format changes on a media sink.</span></span>

## <a name="event-values"></a><span data-ttu-id="b337b-105">Значения событий</span><span class="sxs-lookup"><span data-stu-id="b337b-105">Event values</span></span>

<span data-ttu-id="b337b-106">Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="b337b-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="b337b-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="b337b-107">VARTYPE</span></span>              | <span data-ttu-id="b337b-108">Описание</span><span class="sxs-lookup"><span data-stu-id="b337b-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="b337b-109">VT \_ пуст</span><span class="sxs-lookup"><span data-stu-id="b337b-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="b337b-110">Нет данных события.</span><span class="sxs-lookup"><span data-stu-id="b337b-110">No event data.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="b337b-111">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="b337b-111">Attributes</span></span>

<span data-ttu-id="b337b-112">Для этого события определены следующие атрибуты.</span><span class="sxs-lookup"><span data-stu-id="b337b-112">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="b337b-113">attribute</span><span class="sxs-lookup"><span data-stu-id="b337b-113">Attribute</span></span>                                                                    | <span data-ttu-id="b337b-114">Описание</span><span class="sxs-lookup"><span data-stu-id="b337b-114">Description</span></span>                                                                                  |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b337b-115">**\_ \_ узел вывода событий \_ MF**</span><span class="sxs-lookup"><span data-stu-id="b337b-115">**MF\_EVENT\_OUTPUT\_NODE**</span></span>](mf-event-output-node-attribute.md)<br/> | <span data-ttu-id="b337b-116">Определяет узел топологии для приемника мультимедиа, формат которого изменился.</span><span class="sxs-lookup"><span data-stu-id="b337b-116">Identifies the topology node for the media sink whose format changed.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="b337b-117">Требования</span><span class="sxs-lookup"><span data-stu-id="b337b-117">Requirements</span></span>



| <span data-ttu-id="b337b-118">Требование</span><span class="sxs-lookup"><span data-stu-id="b337b-118">Requirement</span></span> | <span data-ttu-id="b337b-119">Значение</span><span class="sxs-lookup"><span data-stu-id="b337b-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b337b-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b337b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b337b-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b337b-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b337b-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b337b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b337b-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b337b-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b337b-124">Header</span><span class="sxs-lookup"><span data-stu-id="b337b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b337b-125"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b337b-125"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b337b-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b337b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b337b-127">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b337b-127">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




