---
description: 'Возникает, когда метод Имфмедиасессион:: Close завершается асинхронно.'
ms.assetid: d1056ce7-5527-428a-8ace-e1c10a2124a5
title: Событие Месессионклосед (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49591e602c06a9beae616ff2a88a2a71241b6e9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701899"
---
# <a name="mesessionclosed-event"></a><span data-ttu-id="dc057-103">Событие Месессионклосед</span><span class="sxs-lookup"><span data-stu-id="dc057-103">MESessionClosed event</span></span>

<span data-ttu-id="dc057-104">Возникает, когда метод [**имфмедиасессион:: Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) завершается асинхронно.</span><span class="sxs-lookup"><span data-stu-id="dc057-104">Raised when the [**IMFMediaSession::Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) method completes asynchronously.</span></span>

## <a name="event-values"></a><span data-ttu-id="dc057-105">Значения событий</span><span class="sxs-lookup"><span data-stu-id="dc057-105">Event values</span></span>

<span data-ttu-id="dc057-106">Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="dc057-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="dc057-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="dc057-107">VARTYPE</span></span>              | <span data-ttu-id="dc057-108">Описание</span><span class="sxs-lookup"><span data-stu-id="dc057-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="dc057-109">VT \_ пуст</span><span class="sxs-lookup"><span data-stu-id="dc057-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="dc057-110">Нет данных события.</span><span class="sxs-lookup"><span data-stu-id="dc057-110">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="dc057-111">Требования</span><span class="sxs-lookup"><span data-stu-id="dc057-111">Requirements</span></span>



| <span data-ttu-id="dc057-112">Требование</span><span class="sxs-lookup"><span data-stu-id="dc057-112">Requirement</span></span> | <span data-ttu-id="dc057-113">Значение</span><span class="sxs-lookup"><span data-stu-id="dc057-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc057-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dc057-114">Minimum supported client</span></span><br/> | <span data-ttu-id="dc057-115">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="dc057-115">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="dc057-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dc057-116">Minimum supported server</span></span><br/> | <span data-ttu-id="dc057-117">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="dc057-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="dc057-118">Header</span><span class="sxs-lookup"><span data-stu-id="dc057-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="dc057-119"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dc057-119"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc057-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dc057-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc057-121">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="dc057-121">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




