---
description: Отправляется Имфмедиасаурце, который инкапсулирует устройство, чтобы указать, что устройство было вытеснено.
ms.assetid: 85EE663C-94B7-47EA-ABBA-A8371342EEB2
title: Событие Мевидеокаптуредевицепримптед (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3968c0641d954741474b1d5ec7ffaa11dcad5f15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683130"
---
# <a name="mevideocapturedevicepreempted-event"></a><span data-ttu-id="6b898-103">Событие Мевидеокаптуредевицепримптед</span><span class="sxs-lookup"><span data-stu-id="6b898-103">MEVideoCaptureDevicePreempted event</span></span>

<span data-ttu-id="6b898-104">Отправляется [**имфмедиасаурце**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) , который инкапсулирует устройство, чтобы указать, что устройство было вытеснено.</span><span class="sxs-lookup"><span data-stu-id="6b898-104">Sent by the [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) that encapsulates the device to indicate that the device has been preempted.</span></span>

## <a name="event-values"></a><span data-ttu-id="6b898-105">Значения событий</span><span class="sxs-lookup"><span data-stu-id="6b898-105">Event values</span></span>

<span data-ttu-id="6b898-106">Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="6b898-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="6b898-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="6b898-107">VARTYPE</span></span>               | <span data-ttu-id="6b898-108">Описание</span><span class="sxs-lookup"><span data-stu-id="6b898-108">Description</span></span>                           |
|-----------------------|---------------------------------------|
| <span data-ttu-id="6b898-109">VT \_ пуст</span><span class="sxs-lookup"><span data-stu-id="6b898-109">VT\_EMPTY</span></span> <br/> | <span data-ttu-id="6b898-110">Нет данных события.</span><span class="sxs-lookup"><span data-stu-id="6b898-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="6b898-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6b898-111">Remarks</span></span>

<span data-ttu-id="6b898-112">Это событие отправляется [**имфмедиасаурце**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) , который инкапсулирует устройство.</span><span class="sxs-lookup"><span data-stu-id="6b898-112">This event is sent by the [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) that encapsulates the device.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b898-113">Требования</span><span class="sxs-lookup"><span data-stu-id="6b898-113">Requirements</span></span>



| <span data-ttu-id="6b898-114">Требование</span><span class="sxs-lookup"><span data-stu-id="6b898-114">Requirement</span></span> | <span data-ttu-id="6b898-115">Значение</span><span class="sxs-lookup"><span data-stu-id="6b898-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b898-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6b898-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6b898-117">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="6b898-117">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="6b898-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6b898-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6b898-119">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="6b898-119">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6b898-120">Header</span><span class="sxs-lookup"><span data-stu-id="6b898-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b898-121"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6b898-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b898-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6b898-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b898-123">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6b898-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




