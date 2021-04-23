---
description: Сигнализирует, что инициировано изменение скорости воспроизведения DVD.
ms.assetid: 2a1e3c21-1623-4e43-8c7b-1a34514442c9
title: EC_DVD_PLAYBACK_RATE_CHANGE (Двдевкоде. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_PLAYBACK_RATE_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 20ddc41fd70906fabc522daa4dcb7714b71e4251
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675255"
---
# <a name="ec_dvd_playback_rate_change"></a><span data-ttu-id="21ba1-103">\_ \_ \_ изменение скорости воспроизведения на DVD-диске EC \_</span><span class="sxs-lookup"><span data-stu-id="21ba1-103">EC\_DVD\_PLAYBACK\_RATE\_CHANGE</span></span>

<span data-ttu-id="21ba1-104">Сигнализирует, что инициировано изменение скорости воспроизведения DVD.</span><span class="sxs-lookup"><span data-stu-id="21ba1-104">Signals that a rate change in DVD playback has been initiated.</span></span>

## <a name="parameters"></a><span data-ttu-id="21ba1-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="21ba1-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21ba1-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="21ba1-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="21ba1-107">Значение типа LONG, указывающее новую скорость воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="21ba1-107">LONG indicating the new playback rate.</span></span> <span data-ttu-id="21ba1-108">Значение — это фактический темп воспроизведения, умноженный на 10 000, поэтому скорость воспроизведения равна 10000,0/ *lParam1*.</span><span class="sxs-lookup"><span data-stu-id="21ba1-108">The value is the actual playback rate multiplied by 10,000, so the playback rate equals 10000.0 / *lParam1*.</span></span> <span data-ttu-id="21ba1-109">Значения меньше нуля указывают на режим обратных воспроизведений, а значения больше нуля обозначают режим прямого воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="21ba1-109">Values less than zero indicate reverse playback mode, and values greater than zero indicate forward playback mode.</span></span>

</dd> <dt>

<span data-ttu-id="21ba1-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="21ba1-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="21ba1-111">Ноль.</span><span class="sxs-lookup"><span data-stu-id="21ba1-111">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="21ba1-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="21ba1-112">Remarks</span></span>

<span data-ttu-id="21ba1-113">Это событие возникает в домене Title.</span><span class="sxs-lookup"><span data-stu-id="21ba1-113">This event is raised in the title domain.</span></span>

<span data-ttu-id="21ba1-114">*Скорость* воспроизведения — это обратная *скорость* воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="21ba1-114">Playback *rate* is the inverse of playback *speed*.</span></span> <span data-ttu-id="21ba1-115">Например, если скорость воспроизведения составляет 2x, то ставка будет 0,5.</span><span class="sxs-lookup"><span data-stu-id="21ba1-115">For example, if playback speed is 2x, the rate is 0.5.</span></span>

## <a name="requirements"></a><span data-ttu-id="21ba1-116">Требования</span><span class="sxs-lookup"><span data-stu-id="21ba1-116">Requirements</span></span>



| <span data-ttu-id="21ba1-117">Требование</span><span class="sxs-lookup"><span data-stu-id="21ba1-117">Requirement</span></span> | <span data-ttu-id="21ba1-118">Значение</span><span class="sxs-lookup"><span data-stu-id="21ba1-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21ba1-119">Header</span><span class="sxs-lookup"><span data-stu-id="21ba1-119">Header</span></span><br/> | <dl> <span data-ttu-id="21ba1-120"><dt>Двдевкоде. h (включение DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="21ba1-120"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21ba1-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="21ba1-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21ba1-122">DVD-приложения</span><span class="sxs-lookup"><span data-stu-id="21ba1-122">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="21ba1-123">Коды уведомлений о событиях DVD</span><span class="sxs-lookup"><span data-stu-id="21ba1-123">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="21ba1-124">Уведомление о событии в DirectShow</span><span class="sxs-lookup"><span data-stu-id="21ba1-124">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




