---
description: Посылается при изменении значения регистра системного параметра (СПРМ).
ms.assetid: 266b6de1-740d-4b3d-8487-5a9570d6c852
title: EC_DVD_SPRM_Change (Двдевкоде. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_SPRM_Change
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 1af5b8637a197973bca2129a8b8a0198d20248eb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651677"
---
# <a name="ec_dvd_sprm_change"></a><span data-ttu-id="ff232-103">\_Изменение СПРМ DVD-диска EC \_ \_</span><span class="sxs-lookup"><span data-stu-id="ff232-103">EC\_DVD\_SPRM\_Change</span></span>

<span data-ttu-id="ff232-104">Посылается при изменении значения регистра системного параметра (СПРМ).</span><span class="sxs-lookup"><span data-stu-id="ff232-104">Sent when the value of a system parameter register (SPRM) changes.</span></span>

## <a name="parameters"></a><span data-ttu-id="ff232-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="ff232-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff232-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="ff232-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="ff232-107">Отсчитываемый от нуля индекс измененного значения СПРМ.</span><span class="sxs-lookup"><span data-stu-id="ff232-107">The zero-based index of the SPRM value that changed.</span></span>

</dd> <dt>

<span data-ttu-id="ff232-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="ff232-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="ff232-109">Младшие 16 разрядов содержат новое значение СПРМ.</span><span class="sxs-lookup"><span data-stu-id="ff232-109">The lower 16 bits contains the new SPRM value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ff232-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ff232-110">Remarks</span></span>

<span data-ttu-id="ff232-111">По умолчанию это событие отключено.</span><span class="sxs-lookup"><span data-stu-id="ff232-111">This event is disabled by default.</span></span> <span data-ttu-id="ff232-112">Чтобы включить это событие, вызовите [**IDvdControl2:: SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) и установите для параметра **\_ енаблелоггинжевентс DVD** значение **true**.</span><span class="sxs-lookup"><span data-stu-id="ff232-112">To enable this event, call [**IDvdControl2::SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) and set the **DVD\_EnableLoggingEvents** option to **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff232-113">Требования</span><span class="sxs-lookup"><span data-stu-id="ff232-113">Requirements</span></span>



| <span data-ttu-id="ff232-114">Требование</span><span class="sxs-lookup"><span data-stu-id="ff232-114">Requirement</span></span> | <span data-ttu-id="ff232-115">Значение</span><span class="sxs-lookup"><span data-stu-id="ff232-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff232-116">Header</span><span class="sxs-lookup"><span data-stu-id="ff232-116">Header</span></span><br/> | <dl> <span data-ttu-id="ff232-117"><dt>Двдевкоде. h (включение DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ff232-117"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff232-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ff232-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff232-119">DVD-приложения</span><span class="sxs-lookup"><span data-stu-id="ff232-119">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="ff232-120">Коды уведомлений о событиях DVD</span><span class="sxs-lookup"><span data-stu-id="ff232-120">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="ff232-121">Уведомление о событии в DirectShow</span><span class="sxs-lookup"><span data-stu-id="ff232-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="ff232-122">**IDvdInfo2:: Жеталлспрмс**</span><span class="sxs-lookup"><span data-stu-id="ff232-122">**IDvdInfo2::GetAllSPRMs**</span></span>](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getallsprms)
</dt> </dl>

 

 




