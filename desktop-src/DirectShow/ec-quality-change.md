---
description: Граф удаляет образцы для контроля качества.
ms.assetid: a21fe766-58a5-4851-a282-883374287e18
title: EC_QUALITY_CHANGE (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5752db30c8ad6ed85655948cf2adb9ef7ac8078
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674818"
---
# <a name="ec_quality_change"></a><span data-ttu-id="ccd79-103">\_изменение качества \_ EC</span><span class="sxs-lookup"><span data-stu-id="ccd79-103">EC\_QUALITY\_CHANGE</span></span>

<span data-ttu-id="ccd79-104">Граф удаляет образцы для контроля качества.</span><span class="sxs-lookup"><span data-stu-id="ccd79-104">The graph is dropping samples, for quality control.</span></span>

## <a name="parameters"></a><span data-ttu-id="ccd79-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="ccd79-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ccd79-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="ccd79-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="ccd79-107">Ноль.</span><span class="sxs-lookup"><span data-stu-id="ccd79-107">Zero.</span></span>

</dd> <dt>

<span data-ttu-id="ccd79-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="ccd79-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="ccd79-109">Ноль.</span><span class="sxs-lookup"><span data-stu-id="ccd79-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="ccd79-110">Действие по умолчанию</span><span class="sxs-lookup"><span data-stu-id="ccd79-110">Default Action</span></span>

<span data-ttu-id="ccd79-111">Нет.</span><span class="sxs-lookup"><span data-stu-id="ccd79-111">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="ccd79-112">Remarks</span><span class="sxs-lookup"><span data-stu-id="ccd79-112">Remarks</span></span>

<span data-ttu-id="ccd79-113">Фильтр отправляет это событие, если оно удаляет образцы в ответ на сообщение контроля качества.</span><span class="sxs-lookup"><span data-stu-id="ccd79-113">A filter sends this event if it drops samples in response to a quality control message.</span></span> <span data-ttu-id="ccd79-114">Он отправляет событие только в том случае, если он корректирует уровень качества, а не для каждого из выдаваемых им примеров.</span><span class="sxs-lookup"><span data-stu-id="ccd79-114">It sends the event only when it adjusts the quality level, not for each sample that it drops.</span></span> <span data-ttu-id="ccd79-115">Дополнительные сведения см. в разделе [Управление качеством](quality-control-management.md).</span><span class="sxs-lookup"><span data-stu-id="ccd79-115">For more information, see [Quality-Control Management](quality-control-management.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ccd79-116">Требования</span><span class="sxs-lookup"><span data-stu-id="ccd79-116">Requirements</span></span>



| <span data-ttu-id="ccd79-117">Требование</span><span class="sxs-lookup"><span data-stu-id="ccd79-117">Requirement</span></span> | <span data-ttu-id="ccd79-118">Значение</span><span class="sxs-lookup"><span data-stu-id="ccd79-118">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ccd79-119">Header</span><span class="sxs-lookup"><span data-stu-id="ccd79-119">Header</span></span><br/> | <dl> <span data-ttu-id="ccd79-120"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="ccd79-120"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ccd79-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ccd79-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccd79-122">Коды уведомлений о событиях</span><span class="sxs-lookup"><span data-stu-id="ccd79-122">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="ccd79-123">Уведомление о событии в DirectShow</span><span class="sxs-lookup"><span data-stu-id="ccd79-123">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




