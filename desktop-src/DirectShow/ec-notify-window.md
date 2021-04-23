---
description: Уведомляет фильтр окна модуля подготовки видео.
ms.assetid: 65d2f40e-c42c-4d71-b9b3-7662a8be0953
title: EC_NOTIFY_WINDOW (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3165247f05e2fb945f02fee43149b84480bd4b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679804"
---
# <a name="ec_notify_window"></a><span data-ttu-id="54bf2-103">\_окно уведомления \_ EC</span><span class="sxs-lookup"><span data-stu-id="54bf2-103">EC\_NOTIFY\_WINDOW</span></span>

<span data-ttu-id="54bf2-104">Уведомляет фильтр окна модуля подготовки видео.</span><span class="sxs-lookup"><span data-stu-id="54bf2-104">Notifies a filter of the video renderer's window.</span></span>

## <a name="parameters"></a><span data-ttu-id="54bf2-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="54bf2-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54bf2-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="54bf2-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="54bf2-107">(**HWND**) Обработчик для окна.</span><span class="sxs-lookup"><span data-stu-id="54bf2-107">(**HWND**) Handle to the window.</span></span>

</dd> <dt>

<span data-ttu-id="54bf2-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="54bf2-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="54bf2-109">Ноль.</span><span class="sxs-lookup"><span data-stu-id="54bf2-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="54bf2-110">Действие по умолчанию</span><span class="sxs-lookup"><span data-stu-id="54bf2-110">Default Action</span></span>

<span data-ttu-id="54bf2-111">Это событие используется модулем DirectShow для внутренних целей.</span><span class="sxs-lookup"><span data-stu-id="54bf2-111">This event is used internally by DirectShow.</span></span> <span data-ttu-id="54bf2-112">Диспетчер графов фильтров не передает это событие в приложение.</span><span class="sxs-lookup"><span data-stu-id="54bf2-112">The filter graph manager does not pass this event to the application.</span></span> <span data-ttu-id="54bf2-113">Приложения не могут переопределять действие по умолчанию для этого события.</span><span class="sxs-lookup"><span data-stu-id="54bf2-113">Applications cannot override the default action for this event.</span></span>

## <a name="remarks"></a><span data-ttu-id="54bf2-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="54bf2-114">Remarks</span></span>

<span data-ttu-id="54bf2-115">При подключении модуля обработки видео он проверяет, поддерживает ли выходной ПИН-код вышестоящего выхода интерфейс [**имедиаевентсинк**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) .</span><span class="sxs-lookup"><span data-stu-id="54bf2-115">When a video renderer is connected, it checks whether the upstream output pin supports the [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) interface.</span></span> <span data-ttu-id="54bf2-116">Если это так, модуль подготовки отчетов отправляет это событие в вышестоящий фильтр.</span><span class="sxs-lookup"><span data-stu-id="54bf2-116">If so, the renderer sends this event to the upstream filter.</span></span>

## <a name="requirements"></a><span data-ttu-id="54bf2-117">Требования</span><span class="sxs-lookup"><span data-stu-id="54bf2-117">Requirements</span></span>



| <span data-ttu-id="54bf2-118">Требование</span><span class="sxs-lookup"><span data-stu-id="54bf2-118">Requirement</span></span> | <span data-ttu-id="54bf2-119">Значение</span><span class="sxs-lookup"><span data-stu-id="54bf2-119">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="54bf2-120">Header</span><span class="sxs-lookup"><span data-stu-id="54bf2-120">Header</span></span><br/> | <dl> <span data-ttu-id="54bf2-121"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="54bf2-121"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54bf2-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="54bf2-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54bf2-123">Коды уведомлений о событиях</span><span class="sxs-lookup"><span data-stu-id="54bf2-123">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="54bf2-124">Уведомление о событии в DirectShow</span><span class="sxs-lookup"><span data-stu-id="54bf2-124">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




