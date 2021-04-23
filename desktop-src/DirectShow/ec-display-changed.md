---
description: Режим экрана изменился.
ms.assetid: 1f5b066b-6d5d-44bb-851a-424b2bd389c0
title: EC_DISPLAY_CHANGED (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 549a4c5201906b692a1bd726e65269679705e9a5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679625"
---
# <a name="ec_display_changed"></a><span data-ttu-id="88f88-103">\_изменение дисплея \_ EC</span><span class="sxs-lookup"><span data-stu-id="88f88-103">EC\_DISPLAY\_CHANGED</span></span>

<span data-ttu-id="88f88-104">Режим экрана изменился.</span><span class="sxs-lookup"><span data-stu-id="88f88-104">The display mode has changed.</span></span>

## <a name="parameters"></a><span data-ttu-id="88f88-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="88f88-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88f88-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="88f88-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="88f88-107">(**IUnknown** \* ) Указатель на массив интерфейсов [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin) для входных контактов модуля подготовки видео.</span><span class="sxs-lookup"><span data-stu-id="88f88-107">(**IUnknown**\*) Pointer to an array of [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interfaces for the video renderer's input pins.</span></span> <span data-ttu-id="88f88-108">Если *lParam2* равен нулю, этот параметр может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="88f88-108">If *lParam2* is zero, this parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="88f88-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="88f88-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="88f88-110">Если *lParam2* равен нулю, *lParam1* содержит один указатель **Ипин** или равен **null**.</span><span class="sxs-lookup"><span data-stu-id="88f88-110">If *lParam2* is zero, *lParam1* contains a single **IPin** pointer or equals **NULL**.</span></span> <span data-ttu-id="88f88-111">Если *lParam2* больше нуля, *lParam1* содержит массив указателей **Ипин** , а число элементов в массиве — *lParam2*.</span><span class="sxs-lookup"><span data-stu-id="88f88-111">If *lParam2* is greater than zero, *lParam1* contains an array of **IPin** pointers, and the number of elements in the array is given by *lParam2*.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="88f88-112">Действие по умолчанию</span><span class="sxs-lookup"><span data-stu-id="88f88-112">Default Action</span></span>

<span data-ttu-id="88f88-113">Диспетчер графов фильтров временно останавливает граф, а затем отключает модуль подготовки видео.</span><span class="sxs-lookup"><span data-stu-id="88f88-113">The filter graph manager temporarily stops the graph, and then disconnects and reconnects the video renderer.</span></span> <span data-ttu-id="88f88-114">Он не передает событие в приложение.</span><span class="sxs-lookup"><span data-stu-id="88f88-114">It does not pass the event to the application.</span></span>

## <a name="remarks"></a><span data-ttu-id="88f88-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="88f88-115">Remarks</span></span>

<span data-ttu-id="88f88-116">Обработчики видео могут отправить это событие в ответ на сообщение [**\_ дисплайчанже WM**](/windows/desktop/gdi/wm-displaychange) .</span><span class="sxs-lookup"><span data-stu-id="88f88-116">Video renderers can send this event in response to a [**WM\_DISPLAYCHANGE**](/windows/desktop/gdi/wm-displaychange) message.</span></span> <span data-ttu-id="88f88-117">Сообщение **WM \_ дисплайчанже** указывает, что пользователь изменил разрешение экрана.</span><span class="sxs-lookup"><span data-stu-id="88f88-117">The **WM\_DISPLAYCHANGE** message indicates that the user has changed the display resolution.</span></span>

<span data-ttu-id="88f88-118">Во время подключения к закреплениям большинство модулей обработки видео выбирают формат на основе текущего режима отображения.</span><span class="sxs-lookup"><span data-stu-id="88f88-118">During pin connection, most video renderers pick a format based on the current display mode.</span></span> <span data-ttu-id="88f88-119">При изменении режима отображения для модуля подготовки отчетов может потребоваться выбрать другой формат.</span><span class="sxs-lookup"><span data-stu-id="88f88-119">If the display mode changes, the video renderer might need to choose another format.</span></span> <span data-ttu-id="88f88-120">Отправляя это сообщение, модуль подготовки отчетов сообщает диспетчеру графа фильтра о необходимости повторного подключения.</span><span class="sxs-lookup"><span data-stu-id="88f88-120">By sending this message, the renderer signals to the filter graph manager that it needs to be reconnected.</span></span> <span data-ttu-id="88f88-121">Во время повторного подключения модуль подготовки отчетов может выбрать новый формат.</span><span class="sxs-lookup"><span data-stu-id="88f88-121">During the reconnection, the renderer can select a new format.</span></span> <span data-ttu-id="88f88-122">В случае сбоя повторного подключения диспетчер графа фильтров отправляет в приложение событие [**EC \_ еррораборт**](ec-errorabort.md) .</span><span class="sxs-lookup"><span data-stu-id="88f88-122">If the reconnection fails, the filter graph manager sends an [**EC\_ERRORABORT**](ec-errorabort.md) event to the application.</span></span>

### <a name="enhanced-video-renderer"></a><span data-ttu-id="88f88-123">Улучшенный модуль подготовки видео</span><span class="sxs-lookup"><span data-stu-id="88f88-123">Enhanced Video Renderer</span></span>

<span data-ttu-id="88f88-124">Пользовательский выступающий для [**расширенного обработчика видео**](enhanced-video-renderer-filter.md) (Евр) должен отправить это событие в евр, если устройство Direct3D выступающего изменяется.</span><span class="sxs-lookup"><span data-stu-id="88f88-124">A custom presenter for the [**Enhanced Video Renderer**](enhanced-video-renderer-filter.md) (EVR) should send this event to the EVR if the presenter's Direct3D device changes.</span></span> <span data-ttu-id="88f88-125">Задайте *lParam1* и *lParam2* равными нулю; Евр игнорирует параметры события.</span><span class="sxs-lookup"><span data-stu-id="88f88-125">Set *lParam1* and *lParam2* to zero; the EVR ignores the event parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="88f88-126">Требования</span><span class="sxs-lookup"><span data-stu-id="88f88-126">Requirements</span></span>



| <span data-ttu-id="88f88-127">Требование</span><span class="sxs-lookup"><span data-stu-id="88f88-127">Requirement</span></span> | <span data-ttu-id="88f88-128">Значение</span><span class="sxs-lookup"><span data-stu-id="88f88-128">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="88f88-129">Header</span><span class="sxs-lookup"><span data-stu-id="88f88-129">Header</span></span><br/> | <dl> <span data-ttu-id="88f88-130"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="88f88-130"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88f88-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="88f88-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88f88-132">Коды уведомлений о событиях</span><span class="sxs-lookup"><span data-stu-id="88f88-132">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="88f88-133">Уведомление о событии в DirectShow</span><span class="sxs-lookup"><span data-stu-id="88f88-133">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

