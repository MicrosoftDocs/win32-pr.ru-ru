---
description: 'Возникает, когда метод Имфмедиасессион:: останавливаться завершается асинхронно.'
ms.assetid: 9cac9040-f652-4509-bbab-f2a41959d836
title: Событие Месессионстоппед (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e1bd74c168931cc4ac68ae3c990a156664e4b9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349432"
---
# <a name="mesessionstopped-event"></a><span data-ttu-id="07161-103">Событие Месессионстоппед</span><span class="sxs-lookup"><span data-stu-id="07161-103">MESessionStopped event</span></span>

<span data-ttu-id="07161-104">Возникает, когда метод [**имфмедиасессион:: останавливаться**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop) завершается асинхронно.</span><span class="sxs-lookup"><span data-stu-id="07161-104">Raised when the [**IMFMediaSession::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop) method completes asynchronously.</span></span>

## <a name="event-values"></a><span data-ttu-id="07161-105">Значения событий</span><span class="sxs-lookup"><span data-stu-id="07161-105">Event values</span></span>

<span data-ttu-id="07161-106">Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="07161-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="07161-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="07161-107">VARTYPE</span></span>              | <span data-ttu-id="07161-108">Описание</span><span class="sxs-lookup"><span data-stu-id="07161-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="07161-109">VT \_ пуст</span><span class="sxs-lookup"><span data-stu-id="07161-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="07161-110">Нет данных события.</span><span class="sxs-lookup"><span data-stu-id="07161-110">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="07161-111">Требования</span><span class="sxs-lookup"><span data-stu-id="07161-111">Requirements</span></span>



| <span data-ttu-id="07161-112">Требование</span><span class="sxs-lookup"><span data-stu-id="07161-112">Requirement</span></span> | <span data-ttu-id="07161-113">Значение</span><span class="sxs-lookup"><span data-stu-id="07161-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07161-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="07161-114">Minimum supported client</span></span><br/> | <span data-ttu-id="07161-115">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="07161-115">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="07161-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="07161-116">Minimum supported server</span></span><br/> | <span data-ttu-id="07161-117">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="07161-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="07161-118">Header</span><span class="sxs-lookup"><span data-stu-id="07161-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="07161-119"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="07161-119"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07161-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="07161-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07161-121">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="07161-121">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




