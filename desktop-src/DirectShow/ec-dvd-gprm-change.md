---
description: Отправляется при изменении значения регистра общего параметра (ГПРМ).
ms.assetid: 3e0c400e-9ea5-458c-9eca-97d66a440590
title: EC_DVD_GPRM_Change (Двдевкоде. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_GPRM_Change
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: f67a8646a72689c2570462f7dc4aeee6b2474136
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651679"
---
# <a name="ec_dvd_gprm_change"></a><span data-ttu-id="1826c-103">\_Изменение гпрм DVD-диска EC \_ \_</span><span class="sxs-lookup"><span data-stu-id="1826c-103">EC\_DVD\_GPRM\_Change</span></span>

<span data-ttu-id="1826c-104">Отправляется при изменении значения регистра общего параметра (ГПРМ).</span><span class="sxs-lookup"><span data-stu-id="1826c-104">Sent when the value of a general parameter register (GPRM) changes.</span></span>

## <a name="parameters"></a><span data-ttu-id="1826c-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="1826c-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1826c-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="1826c-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="1826c-107">Отсчитываемый от нуля индекс измененного значения ГПРМ.</span><span class="sxs-lookup"><span data-stu-id="1826c-107">The zero-based index of the GPRM value that changed.</span></span>

</dd> <dt>

<span data-ttu-id="1826c-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="1826c-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="1826c-109">Младшие 16 разрядов содержат новое значение ГПРМ.</span><span class="sxs-lookup"><span data-stu-id="1826c-109">The lower 16 bits contains the new GPRM value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1826c-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1826c-110">Remarks</span></span>

<span data-ttu-id="1826c-111">По умолчанию это событие отключено.</span><span class="sxs-lookup"><span data-stu-id="1826c-111">This event is disabled by default.</span></span> <span data-ttu-id="1826c-112">Чтобы включить это событие, вызовите [**IDvdControl2:: SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) и установите для параметра **\_ енаблелоггинжевентс DVD** значение **true**.</span><span class="sxs-lookup"><span data-stu-id="1826c-112">To enable this event, call [**IDvdControl2::SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) and set the **DVD\_EnableLoggingEvents** option to **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="1826c-113">Требования</span><span class="sxs-lookup"><span data-stu-id="1826c-113">Requirements</span></span>



| <span data-ttu-id="1826c-114">Требование</span><span class="sxs-lookup"><span data-stu-id="1826c-114">Requirement</span></span> | <span data-ttu-id="1826c-115">Значение</span><span class="sxs-lookup"><span data-stu-id="1826c-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1826c-116">Header</span><span class="sxs-lookup"><span data-stu-id="1826c-116">Header</span></span><br/> | <dl> <span data-ttu-id="1826c-117"><dt>Двдевкоде. h (включение DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1826c-117"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1826c-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1826c-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1826c-119">DVD-приложения</span><span class="sxs-lookup"><span data-stu-id="1826c-119">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="1826c-120">Коды уведомлений о событиях DVD</span><span class="sxs-lookup"><span data-stu-id="1826c-120">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="1826c-121">Уведомление о событии в DirectShow</span><span class="sxs-lookup"><span data-stu-id="1826c-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="1826c-122">**IDvdInfo2:: Жеталлгпрмс**</span><span class="sxs-lookup"><span data-stu-id="1826c-122">**IDvdInfo2::GetAllGPRMs**</span></span>](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getallgprms)
</dt> </dl>

 

 




