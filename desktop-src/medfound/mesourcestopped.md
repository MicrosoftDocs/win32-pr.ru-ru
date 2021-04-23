---
description: 'Вызывается источником мультимедиа, когда метод Имфмедиасаурце:: останавливаться завершается асинхронно.'
ms.assetid: 0eda9aa1-3aad-43ac-9d87-ab96e4ac319d
title: Событие Месаурцестоппед (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d08909a95cf1c867c5d8392425f25565b5a2728d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711217"
---
# <a name="mesourcestopped-event"></a><span data-ttu-id="d34d7-103">Событие Месаурцестоппед</span><span class="sxs-lookup"><span data-stu-id="d34d7-103">MESourceStopped event</span></span>

<span data-ttu-id="d34d7-104">Вызывается источником мультимедиа, когда метод [**имфмедиасаурце:: останавливаться**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop) завершается асинхронно.</span><span class="sxs-lookup"><span data-stu-id="d34d7-104">Raised by a media source when the [**IMFMediaSource::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop) method completes asynchronously.</span></span>

## <a name="event-values"></a><span data-ttu-id="d34d7-105">Значения событий</span><span class="sxs-lookup"><span data-stu-id="d34d7-105">Event values</span></span>

<span data-ttu-id="d34d7-106">Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="d34d7-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="d34d7-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="d34d7-107">VARTYPE</span></span>              | <span data-ttu-id="d34d7-108">Описание</span><span class="sxs-lookup"><span data-stu-id="d34d7-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="d34d7-109">VT \_ пуст</span><span class="sxs-lookup"><span data-stu-id="d34d7-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="d34d7-110">Нет данных события.</span><span class="sxs-lookup"><span data-stu-id="d34d7-110">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="d34d7-111">Требования</span><span class="sxs-lookup"><span data-stu-id="d34d7-111">Requirements</span></span>



| <span data-ttu-id="d34d7-112">Требование</span><span class="sxs-lookup"><span data-stu-id="d34d7-112">Requirement</span></span> | <span data-ttu-id="d34d7-113">Значение</span><span class="sxs-lookup"><span data-stu-id="d34d7-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d34d7-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d34d7-114">Minimum supported client</span></span><br/> | <span data-ttu-id="d34d7-115">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d34d7-115">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d34d7-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d34d7-116">Minimum supported server</span></span><br/> | <span data-ttu-id="d34d7-117">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d34d7-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d34d7-118">Header</span><span class="sxs-lookup"><span data-stu-id="d34d7-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="d34d7-119"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d34d7-119"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d34d7-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d34d7-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d34d7-121">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d34d7-121">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




