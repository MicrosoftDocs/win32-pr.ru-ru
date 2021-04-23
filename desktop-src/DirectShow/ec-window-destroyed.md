---
description: Модуль подготовки видео был уничтожен или удален из графа.
ms.assetid: facf35c2-d6a2-4373-bce5-171fd9325116
title: EC_WINDOW_DESTROYED (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdd3e641c7fb911a8da10a4c89682fa266e862de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675033"
---
# <a name="ec_window_destroyed"></a><span data-ttu-id="088a5-103">\_окно EC \_ уничтожено</span><span class="sxs-lookup"><span data-stu-id="088a5-103">EC\_WINDOW\_DESTROYED</span></span>

<span data-ttu-id="088a5-104">Модуль подготовки видео был уничтожен или удален из графа.</span><span class="sxs-lookup"><span data-stu-id="088a5-104">The video renderer was destroyed or removed from the graph.</span></span>

## <a name="parameters"></a><span data-ttu-id="088a5-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="088a5-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="088a5-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="088a5-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="088a5-107">(**IUnknown** \* ) Указатель на интерфейс [**ибасефилтер**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) модуля подготовки видео.</span><span class="sxs-lookup"><span data-stu-id="088a5-107">(**IUnknown**\*) Pointer to the video renderer's [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface.</span></span>

</dd> <dt>

<span data-ttu-id="088a5-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="088a5-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="088a5-109">Ноль.</span><span class="sxs-lookup"><span data-stu-id="088a5-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="088a5-110">Действие по умолчанию</span><span class="sxs-lookup"><span data-stu-id="088a5-110">Default Action</span></span>

<span data-ttu-id="088a5-111">Диспетчер графов фильтров освобождает это окно в качестве фокуса через интерфейс [**метод IResourceManager**](/windows/desktop/api/Strmif/nn-strmif-iresourcemanager) .</span><span class="sxs-lookup"><span data-stu-id="088a5-111">The filter graph manager releases this window as the focus, through the [**IResourceManager**](/windows/desktop/api/Strmif/nn-strmif-iresourcemanager) interface.</span></span> <span data-ttu-id="088a5-112">Он не отправляет уведомление о событии в приложение.</span><span class="sxs-lookup"><span data-stu-id="088a5-112">It does not send the event notification to the application.</span></span>

## <a name="remarks"></a><span data-ttu-id="088a5-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="088a5-113">Remarks</span></span>

<span data-ttu-id="088a5-114">Модуль подготовки видео отправляет это событие, когда оно покидает граф фильтра в своем методе [**ибасефилтер:: жоинфилтерграф**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) .</span><span class="sxs-lookup"><span data-stu-id="088a5-114">The video renderer sends this event when it leaves the filter graph, in its [**IBaseFilter::JoinFilterGraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) method.</span></span> <span data-ttu-id="088a5-115">(Отправка события при уничтожении фильтра может быть слишком поздно, так как в этом случае диспетчер графов фильтров также может быть уничтожен.)</span><span class="sxs-lookup"><span data-stu-id="088a5-115">(Sending the event when the filter is destroyed might be too late, because at that point the filter graph manager might also be destroyed.)</span></span>

<span data-ttu-id="088a5-116">Это событие позволяет другим фильтрам получать ресурсы, зависящие от фокуса окна, например звуковыми устройствами.</span><span class="sxs-lookup"><span data-stu-id="088a5-116">This event enables other filters to acquire resources that depend on window focus, such as audio devices.</span></span>

## <a name="requirements"></a><span data-ttu-id="088a5-117">Требования</span><span class="sxs-lookup"><span data-stu-id="088a5-117">Requirements</span></span>



| <span data-ttu-id="088a5-118">Требование</span><span class="sxs-lookup"><span data-stu-id="088a5-118">Requirement</span></span> | <span data-ttu-id="088a5-119">Значение</span><span class="sxs-lookup"><span data-stu-id="088a5-119">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="088a5-120">Header</span><span class="sxs-lookup"><span data-stu-id="088a5-120">Header</span></span><br/> | <dl> <span data-ttu-id="088a5-121"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="088a5-121"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="088a5-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="088a5-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="088a5-123">Коды уведомлений о событиях</span><span class="sxs-lookup"><span data-stu-id="088a5-123">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="088a5-124">Уведомление о событии в DirectShow</span><span class="sxs-lookup"><span data-stu-id="088a5-124">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




