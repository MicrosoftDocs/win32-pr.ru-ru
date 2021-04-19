---
description: Отправляется при изменении текущих цепочек программ (PGC).
ms.assetid: 80fcd059-6ab4-4116-ac3a-012c451237b3
title: EC_DVD_PROGRAM_CHAIN_CHANGE (Двдевкоде. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_PROGRAM_CHAIN_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: eefd45ac1d147a0409417f215e56a4db490dfdbe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675253"
---
# <a name="ec_dvd_program_chain_change"></a><span data-ttu-id="dd23b-103">\_ \_ \_ изменение цепочки DVD-дисков EC \_</span><span class="sxs-lookup"><span data-stu-id="dd23b-103">EC\_DVD\_PROGRAM\_CHAIN\_CHANGE</span></span>

<span data-ttu-id="dd23b-104">Отправляется при изменении текущих цепочек программ (PGC).</span><span class="sxs-lookup"><span data-stu-id="dd23b-104">Sent when current program chain (PGC) changes.</span></span>

## <a name="parameters"></a><span data-ttu-id="dd23b-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="dd23b-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd23b-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="dd23b-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="dd23b-107">Новый номер цепочки программ (ПГКН).</span><span class="sxs-lookup"><span data-stu-id="dd23b-107">The new program chain number (PGCN).</span></span>

</dd> <dt>

<span data-ttu-id="dd23b-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="dd23b-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="dd23b-109">Код локали (LCID) для языка аудио.</span><span class="sxs-lookup"><span data-stu-id="dd23b-109">The locale identifier (LCID) of the audio language.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dd23b-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dd23b-110">Remarks</span></span>

<span data-ttu-id="dd23b-111">По умолчанию это событие отключено.</span><span class="sxs-lookup"><span data-stu-id="dd23b-111">This event is disabled by default.</span></span> <span data-ttu-id="dd23b-112">Чтобы включить это событие, вызовите [**IDvdControl2:: SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) и установите для параметра **\_ нотифипоситиончанже DVD** значение **true**.</span><span class="sxs-lookup"><span data-stu-id="dd23b-112">To enable this event, call [**IDvdControl2::SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) and set the **DVD\_NotifyPositionChange** option to **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd23b-113">Требования</span><span class="sxs-lookup"><span data-stu-id="dd23b-113">Requirements</span></span>



| <span data-ttu-id="dd23b-114">Требование</span><span class="sxs-lookup"><span data-stu-id="dd23b-114">Requirement</span></span> | <span data-ttu-id="dd23b-115">Значение</span><span class="sxs-lookup"><span data-stu-id="dd23b-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd23b-116">Header</span><span class="sxs-lookup"><span data-stu-id="dd23b-116">Header</span></span><br/> | <dl> <span data-ttu-id="dd23b-117"><dt>Двдевкоде. h (включение DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dd23b-117"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd23b-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dd23b-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd23b-119">DVD-приложения</span><span class="sxs-lookup"><span data-stu-id="dd23b-119">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="dd23b-120">Коды уведомлений о событиях DVD</span><span class="sxs-lookup"><span data-stu-id="dd23b-120">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="dd23b-121">Уведомление о событии в DirectShow</span><span class="sxs-lookup"><span data-stu-id="dd23b-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




