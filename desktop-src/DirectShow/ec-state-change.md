---
description: Состояние графа фильтра изменилось.
ms.assetid: f77b4c06-46a5-4912-adb0-0fa8cb7769aa
title: EC_STATE_CHANGE (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf64cc62ba15f77370e52821c3335f9a22f573d3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685439"
---
# <a name="ec_state_change"></a><span data-ttu-id="66d32-103">\_изменение состояния \_ EC</span><span class="sxs-lookup"><span data-stu-id="66d32-103">EC\_STATE\_CHANGE</span></span>

<span data-ttu-id="66d32-104">Состояние графа фильтра изменилось.</span><span class="sxs-lookup"><span data-stu-id="66d32-104">The filter graph has changed state.</span></span>

## <a name="parameters"></a><span data-ttu-id="66d32-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="66d32-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66d32-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="66d32-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="66d32-107">(**DWORD**) Член перечисляемого [**типа \_ состояния фильтра**](/windows/win32/api/strmif/ne-strmif-filter_state) , указывающий новое состояние диаграммы.</span><span class="sxs-lookup"><span data-stu-id="66d32-107">(**DWORD**) Member of the [**FILTER\_STATE**](/windows/win32/api/strmif/ne-strmif-filter_state) enumerated type, indicating the new graph state.</span></span>

</dd> <dt>

<span data-ttu-id="66d32-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="66d32-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="66d32-109">Ноль.</span><span class="sxs-lookup"><span data-stu-id="66d32-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="66d32-110">Действие по умолчанию</span><span class="sxs-lookup"><span data-stu-id="66d32-110">Default Action</span></span>

<span data-ttu-id="66d32-111">Нет действия по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="66d32-111">No default action.</span></span> <span data-ttu-id="66d32-112">Событие не отправляется в приложение.</span><span class="sxs-lookup"><span data-stu-id="66d32-112">The event is not sent to the application.</span></span>

> [!Note]  
> <span data-ttu-id="66d32-113">Это событие может возникать при завершении работы графа.</span><span class="sxs-lookup"><span data-stu-id="66d32-113">This event can occur when the graph shuts down.</span></span> <span data-ttu-id="66d32-114">Если вы Переопределите действие по умолчанию и прослушиваете это событие, необходимо быть особенно осторожным, чтобы не обрабатывать события после выпуска диспетчера графа фильтров.</span><span class="sxs-lookup"><span data-stu-id="66d32-114">If you override the default action and listen for this event, you must be especially careful not to process events after releasing the Filter Graph Manager.</span></span> <span data-ttu-id="66d32-115">В противном случае приложение может ссылаться на недопустимый указатель [**имедиаевент**](/windows/desktop/api/Control/nn-control-imediaevent) и на сбой.</span><span class="sxs-lookup"><span data-stu-id="66d32-115">Otherwise, your application might reference an invalid [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) pointer and crash.</span></span> <span data-ttu-id="66d32-116">Дополнительные сведения см. [в разделе реагирование на события](responding-to-events.md).</span><span class="sxs-lookup"><span data-stu-id="66d32-116">For more information, see [Responding to Events](responding-to-events.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="66d32-117">Требования</span><span class="sxs-lookup"><span data-stu-id="66d32-117">Requirements</span></span>



| <span data-ttu-id="66d32-118">Требование</span><span class="sxs-lookup"><span data-stu-id="66d32-118">Requirement</span></span> | <span data-ttu-id="66d32-119">Значение</span><span class="sxs-lookup"><span data-stu-id="66d32-119">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="66d32-120">Header</span><span class="sxs-lookup"><span data-stu-id="66d32-120">Header</span></span><br/> | <dl> <span data-ttu-id="66d32-121"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="66d32-121"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66d32-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="66d32-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66d32-123">Коды уведомлений о событиях</span><span class="sxs-lookup"><span data-stu-id="66d32-123">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="66d32-124">Уведомление о событии в DirectShow</span><span class="sxs-lookup"><span data-stu-id="66d32-124">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




