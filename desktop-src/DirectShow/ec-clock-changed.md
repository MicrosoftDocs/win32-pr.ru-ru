---
description: Время ссылки изменилось.
ms.assetid: f6de9e74-85fa-4f36-9d7d-3d95f2dbf873
title: EC_CLOCK_CHANGED (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f6a1346c4d445245e62c4823edb4f2cc5accfcf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675574"
---
# <a name="ec_clock_changed"></a><span data-ttu-id="c52db-103">\_изменение такта EC \_</span><span class="sxs-lookup"><span data-stu-id="c52db-103">EC\_CLOCK\_CHANGED</span></span>

<span data-ttu-id="c52db-104">Время ссылки изменилось.</span><span class="sxs-lookup"><span data-stu-id="c52db-104">The reference clock has changed.</span></span>

## <a name="parameters"></a><span data-ttu-id="c52db-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="c52db-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c52db-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="c52db-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="c52db-107">Ноль.</span><span class="sxs-lookup"><span data-stu-id="c52db-107">Zero.</span></span>

</dd> <dt>

<span data-ttu-id="c52db-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="c52db-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="c52db-109">Ноль.</span><span class="sxs-lookup"><span data-stu-id="c52db-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="c52db-110">Действие по умолчанию</span><span class="sxs-lookup"><span data-stu-id="c52db-110">Default Action</span></span>

<span data-ttu-id="c52db-111">Нет.</span><span class="sxs-lookup"><span data-stu-id="c52db-111">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="c52db-112">Remarks</span><span class="sxs-lookup"><span data-stu-id="c52db-112">Remarks</span></span>

<span data-ttu-id="c52db-113">Диспетчер графов фильтров отправляет это событие при вызове метода [**имедиафилтер:: сетсинксаурце**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) .</span><span class="sxs-lookup"><span data-stu-id="c52db-113">The filter graph manager sends this event when its [**IMediaFilter::SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) method is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="c52db-114">Требования</span><span class="sxs-lookup"><span data-stu-id="c52db-114">Requirements</span></span>



| <span data-ttu-id="c52db-115">Требование</span><span class="sxs-lookup"><span data-stu-id="c52db-115">Requirement</span></span> | <span data-ttu-id="c52db-116">Значение</span><span class="sxs-lookup"><span data-stu-id="c52db-116">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c52db-117">Header</span><span class="sxs-lookup"><span data-stu-id="c52db-117">Header</span></span><br/> | <dl> <span data-ttu-id="c52db-118"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="c52db-118"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c52db-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c52db-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c52db-120">Коды уведомлений о событиях</span><span class="sxs-lookup"><span data-stu-id="c52db-120">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="c52db-121">Уведомление о событии в DirectShow</span><span class="sxs-lookup"><span data-stu-id="c52db-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




