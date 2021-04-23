---
description: Модуль подготовки видео переключается в полноэкранный режим.
ms.assetid: f720a9b6-930a-4ed7-9798-1c72fa7a11ff
title: EC_FULLSCREEN_LOST (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf36b5652ea5f7cde26950a18de086af0862dac7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675625"
---
# <a name="ec_fullscreen_lost"></a><span data-ttu-id="62df0-103">неполноэкранный режим EC \_ \_</span><span class="sxs-lookup"><span data-stu-id="62df0-103">EC\_FULLSCREEN\_LOST</span></span>

<span data-ttu-id="62df0-104">Модуль подготовки видео переключается в полноэкранный режим.</span><span class="sxs-lookup"><span data-stu-id="62df0-104">The video renderer is switching out of full-screen mode.</span></span>

## <a name="parameters"></a><span data-ttu-id="62df0-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="62df0-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62df0-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="62df0-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="62df0-107">Ноль.</span><span class="sxs-lookup"><span data-stu-id="62df0-107">Zero.</span></span>

</dd> <dt>

<span data-ttu-id="62df0-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="62df0-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="62df0-109">(**IUnknown** \* ) Указатель на интерфейс [**ибасефилтер**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) модуля подготовки видео или **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="62df0-109">(**IUnknown**\*) Pointer to the video renderer's [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface, or **NULL**.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="62df0-110">Действие по умолчанию</span><span class="sxs-lookup"><span data-stu-id="62df0-110">Default Action</span></span>

<span data-ttu-id="62df0-111">Нет.</span><span class="sxs-lookup"><span data-stu-id="62df0-111">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="62df0-112">Remarks</span><span class="sxs-lookup"><span data-stu-id="62df0-112">Remarks</span></span>

<span data-ttu-id="62df0-113">Когда модуль [подготовки отчетов к просмотру](full-screen-renderer-filter.md) теряет активацию, он отправляет это событие.</span><span class="sxs-lookup"><span data-stu-id="62df0-113">When the [Full Screen Renderer](full-screen-renderer-filter.md) loses activation, it sends this event.</span></span> <span data-ttu-id="62df0-114">Когда модуль подготовки видео переключается из полноэкранного режима, диспетчер графа фильтров отправляет это событие в ответ на событие [**\_ активации EC**](ec-activate.md) из модуля подготовки отчетов.</span><span class="sxs-lookup"><span data-stu-id="62df0-114">When another video renderer switches out of full-screen mode, the filter graph manager sends this event, in response to an [**EC\_ACTIVATE**](ec-activate.md) event from the renderer.</span></span>

## <a name="requirements"></a><span data-ttu-id="62df0-115">Требования</span><span class="sxs-lookup"><span data-stu-id="62df0-115">Requirements</span></span>



| <span data-ttu-id="62df0-116">Требование</span><span class="sxs-lookup"><span data-stu-id="62df0-116">Requirement</span></span> | <span data-ttu-id="62df0-117">Значение</span><span class="sxs-lookup"><span data-stu-id="62df0-117">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="62df0-118">Header</span><span class="sxs-lookup"><span data-stu-id="62df0-118">Header</span></span><br/> | <dl> <span data-ttu-id="62df0-119"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="62df0-119"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62df0-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="62df0-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62df0-121">Коды уведомлений о событиях</span><span class="sxs-lookup"><span data-stu-id="62df0-121">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="62df0-122">Уведомление о событии в DirectShow</span><span class="sxs-lookup"><span data-stu-id="62df0-122">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




