---
description: Размер собственного видео изменился.
ms.assetid: 276f37b3-f981-4a01-bb37-1ee77248668f
title: EC_VIDEO_SIZE_CHANGED (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b29a70ceab583d8dfc51b417fb701a2988b2e96f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675547"
---
# <a name="ec_video_size_changed"></a><span data-ttu-id="64f5d-103">\_Размер видео \_ EC \_ изменен</span><span class="sxs-lookup"><span data-stu-id="64f5d-103">EC\_VIDEO\_SIZE\_CHANGED</span></span>

<span data-ttu-id="64f5d-104">Размер собственного видео изменился.</span><span class="sxs-lookup"><span data-stu-id="64f5d-104">The native video size has changed.</span></span>

## <a name="parameters"></a><span data-ttu-id="64f5d-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="64f5d-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64f5d-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="64f5d-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="64f5d-107">(**DWORD**) СЛОВО низкого порядка задает новую ширину в пикселях; в высоком порядке слово указывает новую высоту (в пикселях).</span><span class="sxs-lookup"><span data-stu-id="64f5d-107">(**DWORD**) Low-order WORD specifies the new width, in pixels; high-order WORD specifies the new height, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="64f5d-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="64f5d-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="64f5d-109">Ноль.</span><span class="sxs-lookup"><span data-stu-id="64f5d-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="64f5d-110">Действие по умолчанию</span><span class="sxs-lookup"><span data-stu-id="64f5d-110">Default Action</span></span>

<span data-ttu-id="64f5d-111">Нет.</span><span class="sxs-lookup"><span data-stu-id="64f5d-111">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="64f5d-112">Remarks</span><span class="sxs-lookup"><span data-stu-id="64f5d-112">Remarks</span></span>

<span data-ttu-id="64f5d-113">Модули подготовки видео могут отправить это событие, если они обнаруживают изменение в собственном размере видео.</span><span class="sxs-lookup"><span data-stu-id="64f5d-113">Video renderers may send this event if they detect a change in the native video size.</span></span>

<span data-ttu-id="64f5d-114">Модуль [подготовки видео 7](video-mixing-renderer-filter-7.md) (VMR-7) и [устройство микширования видео 9](video-mixing-renderer-filter-9.md) (VMR-9) отправляют это событие в оконном режиме, но не в режиме без окон или режиме отображения.</span><span class="sxs-lookup"><span data-stu-id="64f5d-114">The [Video Mixing Renderer 7](video-mixing-renderer-filter-7.md) (VMR-7) and the [Video Mixing Renderer 9](video-mixing-renderer-filter-9.md) (VMR-9) send this event in windowed mode, but not in windowless mode or renderless mode.</span></span> <span data-ttu-id="64f5d-115">Дополнительные сведения о режиме окон в фильтре VMR см. в разделе [визуализация видео](video-rendering.md).</span><span class="sxs-lookup"><span data-stu-id="64f5d-115">For more information about windowed mode in the VMR, see [Video Rendering](video-rendering.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="64f5d-116">Требования</span><span class="sxs-lookup"><span data-stu-id="64f5d-116">Requirements</span></span>



| <span data-ttu-id="64f5d-117">Требование</span><span class="sxs-lookup"><span data-stu-id="64f5d-117">Requirement</span></span> | <span data-ttu-id="64f5d-118">Значение</span><span class="sxs-lookup"><span data-stu-id="64f5d-118">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="64f5d-119">Header</span><span class="sxs-lookup"><span data-stu-id="64f5d-119">Header</span></span><br/> | <dl> <span data-ttu-id="64f5d-120"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="64f5d-120"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64f5d-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="64f5d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64f5d-122">Коды уведомлений о событиях</span><span class="sxs-lookup"><span data-stu-id="64f5d-122">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="64f5d-123">Уведомление о событии в DirectShow</span><span class="sxs-lookup"><span data-stu-id="64f5d-123">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




