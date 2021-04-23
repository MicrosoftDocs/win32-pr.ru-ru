---
description: Отправляется Имфмедиасаурце, который инкапсулирует устройство, чтобы указать, что устройство удалено.
ms.assetid: 107AFF19-B444-4B62-9217-46A99AC3632C
title: Событие Мевидеокаптуредевицеремовед (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e3276f53f86bdce78825b94828577eab9e40954
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674067"
---
# <a name="mevideocapturedeviceremoved-event"></a><span data-ttu-id="5651a-103">Событие Мевидеокаптуредевицеремовед</span><span class="sxs-lookup"><span data-stu-id="5651a-103">MEVideoCaptureDeviceRemoved event</span></span>

<span data-ttu-id="5651a-104">Отправляется [**имфмедиасаурце**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) , который инкапсулирует устройство, чтобы указать, что устройство удалено.</span><span class="sxs-lookup"><span data-stu-id="5651a-104">Sent by the [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) that encapsulates the device to indicate that the device has been removed.</span></span>

## <a name="event-values"></a><span data-ttu-id="5651a-105">Значения событий</span><span class="sxs-lookup"><span data-stu-id="5651a-105">Event values</span></span>

<span data-ttu-id="5651a-106">Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="5651a-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="5651a-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="5651a-107">VARTYPE</span></span>               | <span data-ttu-id="5651a-108">Описание</span><span class="sxs-lookup"><span data-stu-id="5651a-108">Description</span></span>                           |
|-----------------------|---------------------------------------|
| <span data-ttu-id="5651a-109">VT \_ пуст</span><span class="sxs-lookup"><span data-stu-id="5651a-109">VT\_EMPTY</span></span> <br/> | <span data-ttu-id="5651a-110">Нет данных события.</span><span class="sxs-lookup"><span data-stu-id="5651a-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="5651a-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5651a-111">Remarks</span></span>

<span data-ttu-id="5651a-112">Это событие отправляется [**имфмедиасаурце**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) , который инкапсулирует устройство.</span><span class="sxs-lookup"><span data-stu-id="5651a-112">This event is sent by the [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) that encapsulates the device.</span></span>

## <a name="requirements"></a><span data-ttu-id="5651a-113">Требования</span><span class="sxs-lookup"><span data-stu-id="5651a-113">Requirements</span></span>



| <span data-ttu-id="5651a-114">Требование</span><span class="sxs-lookup"><span data-stu-id="5651a-114">Requirement</span></span> | <span data-ttu-id="5651a-115">Значение</span><span class="sxs-lookup"><span data-stu-id="5651a-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5651a-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5651a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5651a-117">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="5651a-117">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="5651a-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5651a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5651a-119">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="5651a-119">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5651a-120">Header</span><span class="sxs-lookup"><span data-stu-id="5651a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="5651a-121"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5651a-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5651a-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5651a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5651a-123">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5651a-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




