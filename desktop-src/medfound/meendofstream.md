---
description: Вызывается потоком мультимедиа при завершении потока.
ms.assetid: e793131a-f737-411f-a9fc-03b5b3d09aea
title: Событие Миндофстреам (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9eb70af021c1a35af829df9b3c80c0c2b71aa120
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898386"
---
# <a name="meendofstream-event"></a><span data-ttu-id="7b56c-103">Событие Миндофстреам</span><span class="sxs-lookup"><span data-stu-id="7b56c-103">MEEndOfStream event</span></span>

<span data-ttu-id="7b56c-104">Вызывается потоком мультимедиа при завершении потока.</span><span class="sxs-lookup"><span data-stu-id="7b56c-104">Raised by a media stream when the stream ends.</span></span>

## <a name="event-values"></a><span data-ttu-id="7b56c-105">Значения событий</span><span class="sxs-lookup"><span data-stu-id="7b56c-105">Event values</span></span>

<span data-ttu-id="7b56c-106">Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="7b56c-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="7b56c-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="7b56c-107">VARTYPE</span></span>              | <span data-ttu-id="7b56c-108">Описание</span><span class="sxs-lookup"><span data-stu-id="7b56c-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="7b56c-109">VT \_ пуст</span><span class="sxs-lookup"><span data-stu-id="7b56c-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="7b56c-110">Нет данных события.</span><span class="sxs-lookup"><span data-stu-id="7b56c-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="7b56c-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7b56c-111">Remarks</span></span>

<span data-ttu-id="7b56c-112">Когда [сеанс мультимедиа](media-session.md) получает событие миндофстреам, он вызывает [**Имфстреамсинк::P лацемаркер**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) в соответствующем приемнике носителя с типом маркера **мфстреамсинк \_ маркеров \_ ендофсегмент** .</span><span class="sxs-lookup"><span data-stu-id="7b56c-112">When the [Media Session](media-session.md) receives the MEEndOfStream event, it calls [**IMFStreamSink::PlaceMarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) on the corresponding media sink, with the **MFSTREAMSINK\_MARKER\_ENDOFSEGMENT** marker type.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b56c-113">Требования</span><span class="sxs-lookup"><span data-stu-id="7b56c-113">Requirements</span></span>



| <span data-ttu-id="7b56c-114">Требование</span><span class="sxs-lookup"><span data-stu-id="7b56c-114">Requirement</span></span> | <span data-ttu-id="7b56c-115">Значение</span><span class="sxs-lookup"><span data-stu-id="7b56c-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b56c-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7b56c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="7b56c-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7b56c-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="7b56c-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7b56c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="7b56c-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7b56c-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7b56c-120">Header</span><span class="sxs-lookup"><span data-stu-id="7b56c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b56c-121"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7b56c-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b56c-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7b56c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b56c-123">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7b56c-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




