---
description: 'Вызывается потоком мультимедиа, когда метод Имфмедиасаурце:: останавливаться завершается асинхронно.'
ms.assetid: 80280820-b618-43d9-881e-6119dfa36e22
title: Событие Местреамстоппед (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3e28060505afc6b16aa6359af21c77cf92df972
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702551"
---
# <a name="mestreamstopped-event"></a><span data-ttu-id="ca6dc-103">Событие Местреамстоппед</span><span class="sxs-lookup"><span data-stu-id="ca6dc-103">MEStreamStopped event</span></span>

<span data-ttu-id="ca6dc-104">Вызывается потоком мультимедиа, когда метод [**имфмедиасаурце:: останавливаться**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop) завершается асинхронно.</span><span class="sxs-lookup"><span data-stu-id="ca6dc-104">Raised by a media stream when the [**IMFMediaSource::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop) method completes asynchronously.</span></span>

## <a name="event-values"></a><span data-ttu-id="ca6dc-105">Значения событий</span><span class="sxs-lookup"><span data-stu-id="ca6dc-105">Event values</span></span>

<span data-ttu-id="ca6dc-106">Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="ca6dc-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="ca6dc-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="ca6dc-107">VARTYPE</span></span>              | <span data-ttu-id="ca6dc-108">Описание</span><span class="sxs-lookup"><span data-stu-id="ca6dc-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="ca6dc-109">VT \_ пуст</span><span class="sxs-lookup"><span data-stu-id="ca6dc-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="ca6dc-110">Нет данных события.</span><span class="sxs-lookup"><span data-stu-id="ca6dc-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="ca6dc-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ca6dc-111">Remarks</span></span>

<span data-ttu-id="ca6dc-112">Каждый активный поток в презентации отправляет это событие.</span><span class="sxs-lookup"><span data-stu-id="ca6dc-112">Each active stream in the presentation sends this event.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca6dc-113">Требования</span><span class="sxs-lookup"><span data-stu-id="ca6dc-113">Requirements</span></span>



| <span data-ttu-id="ca6dc-114">Требование</span><span class="sxs-lookup"><span data-stu-id="ca6dc-114">Requirement</span></span> | <span data-ttu-id="ca6dc-115">Значение</span><span class="sxs-lookup"><span data-stu-id="ca6dc-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca6dc-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ca6dc-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ca6dc-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ca6dc-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ca6dc-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ca6dc-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ca6dc-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ca6dc-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ca6dc-120">Header</span><span class="sxs-lookup"><span data-stu-id="ca6dc-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca6dc-121"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ca6dc-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca6dc-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ca6dc-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca6dc-123">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ca6dc-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




