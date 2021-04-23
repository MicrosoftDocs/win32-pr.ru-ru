---
description: Посылается при изменении номера ячейки или номера этой программы DVD.
ms.assetid: a500e86d-cd42-4716-9c57-828a72c4e1df
title: EC_DVD_PROGRAM_CELL_CHANGE (Двдевкоде. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_PROGRAM_CELL_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: d41f691016c3e41cfc3e14ed1ce6fff276dcc70e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651678"
---
# <a name="ec_dvd_program_cell_change"></a><span data-ttu-id="bb97a-103">\_ \_ \_ изменение ячейки DVD в программе EC \_</span><span class="sxs-lookup"><span data-stu-id="bb97a-103">EC\_DVD\_PROGRAM\_CELL\_CHANGE</span></span>

<span data-ttu-id="bb97a-104">Посылается при изменении номера ячейки или номера этой программы DVD.</span><span class="sxs-lookup"><span data-stu-id="bb97a-104">Sent when the DVD program number or cell number changes.</span></span>

## <a name="parameters"></a><span data-ttu-id="bb97a-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="bb97a-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb97a-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="bb97a-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="bb97a-107">Новый номер программы.</span><span class="sxs-lookup"><span data-stu-id="bb97a-107">The new program number.</span></span>

</dd> <dt>

<span data-ttu-id="bb97a-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="bb97a-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="bb97a-109">Новый номер ячейки.</span><span class="sxs-lookup"><span data-stu-id="bb97a-109">The new cell number.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bb97a-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bb97a-110">Remarks</span></span>

<span data-ttu-id="bb97a-111">По умолчанию это событие отключено.</span><span class="sxs-lookup"><span data-stu-id="bb97a-111">This event is disabled by default.</span></span> <span data-ttu-id="bb97a-112">Чтобы включить это событие, вызовите [**IDvdControl2:: SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) и установите для параметра **\_ нотифипоситиончанже DVD** значение **true**.</span><span class="sxs-lookup"><span data-stu-id="bb97a-112">To enable this event, call [**IDvdControl2::SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) and set the **DVD\_NotifyPositionChange** option to **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb97a-113">Требования</span><span class="sxs-lookup"><span data-stu-id="bb97a-113">Requirements</span></span>



| <span data-ttu-id="bb97a-114">Требование</span><span class="sxs-lookup"><span data-stu-id="bb97a-114">Requirement</span></span> | <span data-ttu-id="bb97a-115">Значение</span><span class="sxs-lookup"><span data-stu-id="bb97a-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb97a-116">Header</span><span class="sxs-lookup"><span data-stu-id="bb97a-116">Header</span></span><br/> | <dl> <span data-ttu-id="bb97a-117"><dt>Двдевкоде. h (включение DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bb97a-117"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb97a-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bb97a-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb97a-119">DVD-приложения</span><span class="sxs-lookup"><span data-stu-id="bb97a-119">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="bb97a-120">Коды уведомлений о событиях DVD</span><span class="sxs-lookup"><span data-stu-id="bb97a-120">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="bb97a-121">Уведомление о событии в DirectShow</span><span class="sxs-lookup"><span data-stu-id="bb97a-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




