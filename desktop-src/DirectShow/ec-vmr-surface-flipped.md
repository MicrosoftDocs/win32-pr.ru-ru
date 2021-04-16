---
description: Посылается, когда на представляемой поверхности вызывается метод отражения VMR-7's распределителя. Таким образом, VMR должен синхронизировать свою таблицу Директксва поверхностей с цепочкой зеркального отображения DirectDraw.
ms.assetid: e298857b-0579-48b4-add0-72320bc52d63
title: EC_VMR_SURFACE_FLIPPED (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1feafaa58f0cacdafde04591d494dbb9a9eb258e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652027"
---
# <a name="ec_vmr_surface_flipped"></a><span data-ttu-id="2e2d2-104">\_перевернутая поверхность с фильтром EC \_ \_</span><span class="sxs-lookup"><span data-stu-id="2e2d2-104">EC\_VMR\_SURFACE\_FLIPPED</span></span>

<span data-ttu-id="2e2d2-105">Посылается, когда на представляемой поверхности вызывается метод отражения VMR-7's распределителя.</span><span class="sxs-lookup"><span data-stu-id="2e2d2-105">Sent when the VMR-7's allocator presenter has called the DirectDraw Flip method on the surface being presented.</span></span> <span data-ttu-id="2e2d2-106">Таким образом, VMR должен синхронизировать свою таблицу Директксва поверхностей с цепочкой зеркального отображения DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="2e2d2-106">This allows the VMR to keep its DirectXVA table of surfaces synchronized with DirectDraw's flipping chain.</span></span>

## <a name="parameters"></a><span data-ttu-id="2e2d2-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="2e2d2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e2d2-108"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="2e2d2-108"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="2e2d2-109">(**HRESULT**) Код состояния, возвращенный методом отражения DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="2e2d2-109">(**HRESULT**) Status code returned from the DirectDraw Flip method.</span></span>

</dd> <dt>

<span data-ttu-id="2e2d2-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="2e2d2-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="2e2d2-111">Не используется.</span><span class="sxs-lookup"><span data-stu-id="2e2d2-111">Not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2e2d2-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2e2d2-112">Remarks</span></span>

<span data-ttu-id="2e2d2-113">Пользовательский распределитель — выступающие для VMR-7 должны отправить это событие.</span><span class="sxs-lookup"><span data-stu-id="2e2d2-113">Custom allocator-presenters for the VMR-7 should send this event.</span></span> <span data-ttu-id="2e2d2-114">Это событие не пересылается в приложения и не используется с распределителя-Presenters для VMR-9.</span><span class="sxs-lookup"><span data-stu-id="2e2d2-114">This event is not forwarded to applications and it is not used with allocator-presenters for the VMR-9.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e2d2-115">Требования</span><span class="sxs-lookup"><span data-stu-id="2e2d2-115">Requirements</span></span>



| <span data-ttu-id="2e2d2-116">Требование</span><span class="sxs-lookup"><span data-stu-id="2e2d2-116">Requirement</span></span> | <span data-ttu-id="2e2d2-117">Значение</span><span class="sxs-lookup"><span data-stu-id="2e2d2-117">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2e2d2-118">Header</span><span class="sxs-lookup"><span data-stu-id="2e2d2-118">Header</span></span><br/> | <dl> <span data-ttu-id="2e2d2-119"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e2d2-119"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e2d2-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2e2d2-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e2d2-121">Коды уведомлений о событиях</span><span class="sxs-lookup"><span data-stu-id="2e2d2-121">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="2e2d2-122">Уведомление о событии в DirectShow</span><span class="sxs-lookup"><span data-stu-id="2e2d2-122">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




