---
description: Указывает, насколько далеко позади расписания компонент предназначен для обработки образцов.
ms.assetid: 8bd202fb-3015-41a2-ad14-862f64cb252f
title: EC_SAMPLE_LATENCY (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee90d42e6464eccc4bc93b1052e29392b74bb2d7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685068"
---
# <a name="ec_sample_latency"></a><span data-ttu-id="30988-103">\_пример \_ задержки для EC</span><span class="sxs-lookup"><span data-stu-id="30988-103">EC\_SAMPLE\_LATENCY</span></span>

<span data-ttu-id="30988-104">Указывает, насколько далеко позади расписания компонент предназначен для обработки образцов.</span><span class="sxs-lookup"><span data-stu-id="30988-104">Specifies how far behind schedule a component is for processing samples.</span></span>

## <a name="parameters"></a><span data-ttu-id="30988-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="30988-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30988-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="30988-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="30988-107">(**\_ время ссылки на константу** \* ) расстояние от компонента до, в 100-наносекундных единицах.</span><span class="sxs-lookup"><span data-stu-id="30988-107">(**const REFERENCE\_TIME**\*) How far behind the component is, in 100-nanosecond units.</span></span> <span data-ttu-id="30988-108">Если это значение положительное, компонент отстает от расписания.</span><span class="sxs-lookup"><span data-stu-id="30988-108">If this value is positive, the component is behind schedule.</span></span> <span data-ttu-id="30988-109">Если это значение отрицательное, компонент опережает расписание.</span><span class="sxs-lookup"><span data-stu-id="30988-109">If this value is negative, the component is ahead of schedule.</span></span>

</dd> <dt>

<span data-ttu-id="30988-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="30988-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="30988-111">Ноль.</span><span class="sxs-lookup"><span data-stu-id="30988-111">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="30988-112">Действие по умолчанию</span><span class="sxs-lookup"><span data-stu-id="30988-112">Default Action</span></span>

<span data-ttu-id="30988-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="30988-113">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="30988-114">Remarks</span><span class="sxs-lookup"><span data-stu-id="30988-114">Remarks</span></span>

<span data-ttu-id="30988-115">Пользовательский выступающий для фильтра [**расширенного обработчика видео**](enhanced-video-renderer-filter.md) (Евр) может отправить это сообщение в евр, чтобы уведомить Евр о том, что средство находится за расписанием или с опережением расписания.</span><span class="sxs-lookup"><span data-stu-id="30988-115">A custom presenter for the [**Enhanced Video Renderer**](enhanced-video-renderer-filter.md) (EVR) filter can send this message to the EVR, to notify the EVR whether the presenter is behind schedule or ahead of schedule.</span></span>

<span data-ttu-id="30988-116">Самый простой способ вычислить *lParam1* : *QPC Now*   *QPC Target*, где *QPC Now* — это время, а *QPC целевой объект* — время презентации.</span><span class="sxs-lookup"><span data-stu-id="30988-116">The simplest way to calculate *lParam1* is: *QPC now*   *QPC target*, where *QPC now* is the clock time now, and *QPC target* is the presentation time.</span></span>

## <a name="requirements"></a><span data-ttu-id="30988-117">Требования</span><span class="sxs-lookup"><span data-stu-id="30988-117">Requirements</span></span>



| <span data-ttu-id="30988-118">Требование</span><span class="sxs-lookup"><span data-stu-id="30988-118">Requirement</span></span> | <span data-ttu-id="30988-119">Значение</span><span class="sxs-lookup"><span data-stu-id="30988-119">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="30988-120">Header</span><span class="sxs-lookup"><span data-stu-id="30988-120">Header</span></span><br/> | <dl> <span data-ttu-id="30988-121"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="30988-121"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30988-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="30988-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30988-123">Коды уведомлений о событиях</span><span class="sxs-lookup"><span data-stu-id="30988-123">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="30988-124">Написание выступающего Евр</span><span class="sxs-lookup"><span data-stu-id="30988-124">How to Write an EVR Presenter</span></span>](/windows/desktop/medfound/how-to-write-an-evr-presenter)
</dt> </dl>

 

