---
description: Указывает новый домен проигрывателя DVD.
ms.assetid: 4faa46d6-2ba2-44a3-b237-acac3b32f8b1
title: EC_DVD_DOMAIN_CHANGE (Двдевкоде. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_DOMAIN_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 815b6b2dd318d0b7716f4cf640ef3f83dacd0d60
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651772"
---
# <a name="ec_dvd_domain_change"></a><span data-ttu-id="f2b1b-103">\_изменение домена на DVD-диске EC \_ \_</span><span class="sxs-lookup"><span data-stu-id="f2b1b-103">EC\_DVD\_DOMAIN\_CHANGE</span></span>

<span data-ttu-id="f2b1b-104">Указывает новый домен проигрывателя DVD.</span><span class="sxs-lookup"><span data-stu-id="f2b1b-104">Indicates the DVD player's new domain.</span></span>

## <a name="parameters"></a><span data-ttu-id="f2b1b-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="f2b1b-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2b1b-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="f2b1b-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="f2b1b-107">Значение **типа DWORD** , указывающее новый домен.</span><span class="sxs-lookup"><span data-stu-id="f2b1b-107">**DWORD** value indicating the new domain.</span></span> <span data-ttu-id="f2b1b-108">Член типа данных "перечислимый [**\_ домен DVD-диска**](/windows/win32/api/strmif/ne-strmif-dvd_domain) ".</span><span class="sxs-lookup"><span data-stu-id="f2b1b-108">Member of the [**DVD\_DOMAIN**](/windows/win32/api/strmif/ne-strmif-dvd_domain) enumerated data type.</span></span>

</dd> <dt>

<span data-ttu-id="f2b1b-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="f2b1b-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="f2b1b-110">Ноль.</span><span class="sxs-lookup"><span data-stu-id="f2b1b-110">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f2b1b-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f2b1b-111">Remarks</span></span>

<span data-ttu-id="f2b1b-112">Проигрыватель DVD сигнализирует об этом событии при каждом изменении доменов.</span><span class="sxs-lookup"><span data-stu-id="f2b1b-112">The DVD player signals this event whenever it changes domains.</span></span>

<span data-ttu-id="f2b1b-113">Это событие возникает во всех доменах DVD.</span><span class="sxs-lookup"><span data-stu-id="f2b1b-113">This event is raised in all DVD domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2b1b-114">Требования</span><span class="sxs-lookup"><span data-stu-id="f2b1b-114">Requirements</span></span>



| <span data-ttu-id="f2b1b-115">Требование</span><span class="sxs-lookup"><span data-stu-id="f2b1b-115">Requirement</span></span> | <span data-ttu-id="f2b1b-116">Значение</span><span class="sxs-lookup"><span data-stu-id="f2b1b-116">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2b1b-117">Header</span><span class="sxs-lookup"><span data-stu-id="f2b1b-117">Header</span></span><br/> | <dl> <span data-ttu-id="f2b1b-118"><dt>Двдевкоде. h (включение DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f2b1b-118"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2b1b-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f2b1b-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2b1b-120">DVD-приложения</span><span class="sxs-lookup"><span data-stu-id="f2b1b-120">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="f2b1b-121">Коды уведомлений о событиях DVD</span><span class="sxs-lookup"><span data-stu-id="f2b1b-121">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="f2b1b-122">Уведомление о событии в DirectShow</span><span class="sxs-lookup"><span data-stu-id="f2b1b-122">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




