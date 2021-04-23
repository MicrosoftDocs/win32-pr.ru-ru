---
description: Окно видео активируется или деактивируется.
ms.assetid: 2e004899-bb2b-4127-b606-e2a979275836
title: EC_ACTIVATE (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81e48adb3ae98af172664b807386c615d34b6b22
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675579"
---
# <a name="ec_activate"></a><span data-ttu-id="6346c-103">\_Активация EC</span><span class="sxs-lookup"><span data-stu-id="6346c-103">EC\_ACTIVATE</span></span>

<span data-ttu-id="6346c-104">Окно видео активируется или деактивируется.</span><span class="sxs-lookup"><span data-stu-id="6346c-104">A video window is being activated or deactivated.</span></span>

## <a name="parameters"></a><span data-ttu-id="6346c-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="6346c-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6346c-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="6346c-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="6346c-107">(**Bool**) **Значение true** , если окно активируется, или **значение false** , если окно деактивировано.</span><span class="sxs-lookup"><span data-stu-id="6346c-107">(**BOOL**) **TRUE** if the window is activated, or **FALSE** if the window is deactivated.</span></span>

</dd> <dt>

<span data-ttu-id="6346c-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="6346c-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="6346c-109">(**IUnknown** \* ) Указатель на интерфейс [**ибасефилтер**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) визуализатора.</span><span class="sxs-lookup"><span data-stu-id="6346c-109">(**IUnknown**\*) Pointer to the renderer's [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="6346c-110">Действие по умолчанию</span><span class="sxs-lookup"><span data-stu-id="6346c-110">Default Action</span></span>

<span data-ttu-id="6346c-111">Диспетчер графов фильтров устанавливает фокус с помощью интерфейса [**метод IResourceManager**](/windows/desktop/api/Strmif/nn-strmif-iresourcemanager) .</span><span class="sxs-lookup"><span data-stu-id="6346c-111">The filter graph manager sets the focus, through the [**IResourceManager**](/windows/desktop/api/Strmif/nn-strmif-iresourcemanager) interface.</span></span> <span data-ttu-id="6346c-112">Он не отправляет уведомление о событии в приложение.</span><span class="sxs-lookup"><span data-stu-id="6346c-112">It does not send the event notification to the application.</span></span>

## <a name="remarks"></a><span data-ttu-id="6346c-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6346c-113">Remarks</span></span>

<span data-ttu-id="6346c-114">Модуль обработки видео отправляет это событие всякий раз, когда окно активируется или деактивируется (то есть при получении сообщения WM \_ активатеапп).</span><span class="sxs-lookup"><span data-stu-id="6346c-114">A video renderer sends this event whenever its window is activated or deactivated (that is, when it receives a WM\_ACTIVATEAPP message).</span></span> <span data-ttu-id="6346c-115">Активация или деактивация окна может быть вызвана тем, что окно получило или потеряло фокус, либо поскольку модуль подготовки отчетов переключен между полноэкранным режимом и оконным режимом.</span><span class="sxs-lookup"><span data-stu-id="6346c-115">Window activation or deactivation can occur because the window has gained or lost focus, or because the renderer has switched between full-screen mode and windowed mode.</span></span>

<span data-ttu-id="6346c-116">Это событие позволяет диспетчеру фильтров графа выделять ресурсы, зависящие от фокуса окна, например звуковыми устройствами.</span><span class="sxs-lookup"><span data-stu-id="6346c-116">This event enables the filter graph manager to allocate resources that depend on window focus, such as audio devices.</span></span>

## <a name="requirements"></a><span data-ttu-id="6346c-117">Требования</span><span class="sxs-lookup"><span data-stu-id="6346c-117">Requirements</span></span>



| <span data-ttu-id="6346c-118">Требование</span><span class="sxs-lookup"><span data-stu-id="6346c-118">Requirement</span></span> | <span data-ttu-id="6346c-119">Значение</span><span class="sxs-lookup"><span data-stu-id="6346c-119">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6346c-120">Header</span><span class="sxs-lookup"><span data-stu-id="6346c-120">Header</span></span><br/> | <dl> <span data-ttu-id="6346c-121"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="6346c-121"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6346c-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6346c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6346c-123">Коды уведомлений о событиях</span><span class="sxs-lookup"><span data-stu-id="6346c-123">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="6346c-124">Уведомление о событии в DirectShow</span><span class="sxs-lookup"><span data-stu-id="6346c-124">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




