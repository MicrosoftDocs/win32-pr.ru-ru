---
description: Поставщик часов был отключен.
ms.assetid: 0a885b7a-840d-4112-85f7-ff6f2d87bb75
title: EC_CLOCK_UNSET (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85ead35d89eee94bbffb38a96f658ccb2bb6e6e4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675572"
---
# <a name="ec_clock_unset"></a><span data-ttu-id="78248-103">неопределенное \_ время EC \_</span><span class="sxs-lookup"><span data-stu-id="78248-103">EC\_CLOCK\_UNSET</span></span>

<span data-ttu-id="78248-104">Поставщик часов был отключен.</span><span class="sxs-lookup"><span data-stu-id="78248-104">The clock provider was disconnected.</span></span>

## <a name="parameters"></a><span data-ttu-id="78248-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="78248-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78248-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="78248-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="78248-107">Ноль.</span><span class="sxs-lookup"><span data-stu-id="78248-107">Zero.</span></span>

</dd> <dt>

<span data-ttu-id="78248-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="78248-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="78248-109">Ноль.</span><span class="sxs-lookup"><span data-stu-id="78248-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="78248-110">Действие по умолчанию</span><span class="sxs-lookup"><span data-stu-id="78248-110">Default Action</span></span>

<span data-ttu-id="78248-111">Диспетчер графов фильтров выбирает новый эталонный таймер при следующей приостановке или выполнении команды.</span><span class="sxs-lookup"><span data-stu-id="78248-111">The Filter Graph Manager chooses a new reference clock on the next pause or run command.</span></span> <span data-ttu-id="78248-112">Он также перенаправляет событие в приложение.</span><span class="sxs-lookup"><span data-stu-id="78248-112">It also forwards the event to the application.</span></span>

## <a name="remarks"></a><span data-ttu-id="78248-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="78248-113">Remarks</span></span>

<span data-ttu-id="78248-114">Кспрокси сигнализирует об этом событии, когда закрепление фильтра, предоставляющего часы, отключено.</span><span class="sxs-lookup"><span data-stu-id="78248-114">KSProxy signals this event when the pin of a clock-providing filter is disconnected.</span></span>

## <a name="requirements"></a><span data-ttu-id="78248-115">Требования</span><span class="sxs-lookup"><span data-stu-id="78248-115">Requirements</span></span>



| <span data-ttu-id="78248-116">Требование</span><span class="sxs-lookup"><span data-stu-id="78248-116">Requirement</span></span> | <span data-ttu-id="78248-117">Значение</span><span class="sxs-lookup"><span data-stu-id="78248-117">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="78248-118">Header</span><span class="sxs-lookup"><span data-stu-id="78248-118">Header</span></span><br/> | <dl> <span data-ttu-id="78248-119"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="78248-119"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78248-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="78248-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78248-121">Коды уведомлений о событиях</span><span class="sxs-lookup"><span data-stu-id="78248-121">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="78248-122">Уведомление о событии в DirectShow</span><span class="sxs-lookup"><span data-stu-id="78248-122">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




