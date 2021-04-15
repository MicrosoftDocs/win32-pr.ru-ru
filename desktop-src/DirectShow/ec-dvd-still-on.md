---
description: Сигнализирует началу все еще (PGC, Cell или ВОБУ).
ms.assetid: cf2b08c9-22fa-4559-9289-787eaec46c6c
title: EC_DVD_STILL_ON (Двдевкоде. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_STILL_ON
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 0e2f9fcfecc44ee6d0769e00805c0aee512b2e7c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651676"
---
# <a name="ec_dvd_still_on"></a><span data-ttu-id="da3f0-103">\_ \_ все еще на DVD-диске EC \_</span><span class="sxs-lookup"><span data-stu-id="da3f0-103">EC\_DVD\_STILL\_ON</span></span>

<span data-ttu-id="da3f0-104">Сигнализирует началу все еще (PGC, Cell или ВОБУ).</span><span class="sxs-lookup"><span data-stu-id="da3f0-104">Signals the beginning of any still (PGC, Cell, or VOBU).</span></span>

## <a name="parameters"></a><span data-ttu-id="da3f0-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="da3f0-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da3f0-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="da3f0-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="da3f0-107">Логическое значение (**bool**), указывающее, доступны ли кнопки.</span><span class="sxs-lookup"><span data-stu-id="da3f0-107">Boolean (**BOOL**) value indicating whether buttons are available.</span></span> <span data-ttu-id="da3f0-108">Ноль (0) означает, что кнопки доступны, поэтому метод [**IDvdControl2:: стиллофф**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-stilloff) не будет работать.</span><span class="sxs-lookup"><span data-stu-id="da3f0-108">Zero (0) indicates buttons are available so the [**IDvdControl2::StillOff**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-stilloff) method won't work.</span></span> <span data-ttu-id="da3f0-109">Один (1) означает, что кнопки недоступны, поэтому **IDvdControl2:: стиллофф** будет работать.</span><span class="sxs-lookup"><span data-stu-id="da3f0-109">One (1) indicates no buttons are available, so **IDvdControl2::StillOff** will work.</span></span>

</dd> <dt>

<span data-ttu-id="da3f0-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="da3f0-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="da3f0-111">Значение **типа DWORD** , указывающее время в секундах, по истечении которого будет выполняться последнее.</span><span class="sxs-lookup"><span data-stu-id="da3f0-111">**DWORD** value indicating the number of seconds the still will last.</span></span> <span data-ttu-id="da3f0-112">значение 0xFFFFFFFF указывает на бесконечность. Это означает Ожидание нажатия пользователем кнопки или до тех пор, пока приложение не вызовет [**IDvdControl2:: стиллофф**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-stilloff).</span><span class="sxs-lookup"><span data-stu-id="da3f0-112">0xFFFFFFFF indicates an infinite still, meaning wait until the user presses a button or until the application calls [**IDvdControl2::StillOff**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-stilloff).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="da3f0-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="da3f0-113">Remarks</span></span>

<span data-ttu-id="da3f0-114">Все сочетания кнопок и по-прежнему возможны (кнопки со всеми по-прежнему включены, кнопки с по-прежнему отключены, кнопка отключена, кнопка выключена.</span><span class="sxs-lookup"><span data-stu-id="da3f0-114">All combinations of buttons and still are possible (buttons on with still on, buttons on with still off, button off with still on, button off with still off).</span></span>

<span data-ttu-id="da3f0-115">Это событие возникает во всех доменах.</span><span class="sxs-lookup"><span data-stu-id="da3f0-115">This event is raised in all domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="da3f0-116">Требования</span><span class="sxs-lookup"><span data-stu-id="da3f0-116">Requirements</span></span>



| <span data-ttu-id="da3f0-117">Требование</span><span class="sxs-lookup"><span data-stu-id="da3f0-117">Requirement</span></span> | <span data-ttu-id="da3f0-118">Значение</span><span class="sxs-lookup"><span data-stu-id="da3f0-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da3f0-119">Header</span><span class="sxs-lookup"><span data-stu-id="da3f0-119">Header</span></span><br/> | <dl> <span data-ttu-id="da3f0-120"><dt>Двдевкоде. h (включение DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="da3f0-120"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da3f0-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="da3f0-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da3f0-122">DVD-приложения</span><span class="sxs-lookup"><span data-stu-id="da3f0-122">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="da3f0-123">Коды уведомлений о событиях DVD</span><span class="sxs-lookup"><span data-stu-id="da3f0-123">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="da3f0-124">Уведомление о событии в DirectShow</span><span class="sxs-lookup"><span data-stu-id="da3f0-124">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




