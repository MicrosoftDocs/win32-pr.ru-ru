---
description: Посылается, когда VMR выбрал механизм рендеринга.
ms.assetid: 815d1254-c6e3-4a6c-ba4a-bf3da7d35d1f
title: EC_VMR_RENDERDEVICE_SET (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9855b23e25a2c3b955c1499b9505efffcc5637e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675781"
---
# <a name="ec_vmr_renderdevice_set"></a><span data-ttu-id="1a25b-103">\_ \_ набор рендердевицеов EC VMR \_</span><span class="sxs-lookup"><span data-stu-id="1a25b-103">EC\_VMR\_RENDERDEVICE\_SET</span></span>

<span data-ttu-id="1a25b-104">Посылается, когда VMR выбрал механизм рендеринга.</span><span class="sxs-lookup"><span data-stu-id="1a25b-104">Sent when the VMR has selected its rendering mechanism.</span></span>

## <a name="parameters"></a><span data-ttu-id="1a25b-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="1a25b-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a25b-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="1a25b-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="1a25b-107">Может иметь одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="1a25b-107">May be one of the following values:</span></span>



| <span data-ttu-id="1a25b-108">Значение</span><span class="sxs-lookup"><span data-stu-id="1a25b-108">Value</span></span>                        | <span data-ttu-id="1a25b-109">Значение</span><span class="sxs-lookup"><span data-stu-id="1a25b-109">Meaning</span></span>                                                  |
|------------------------------|----------------------------------------------------------|
| <span data-ttu-id="1a25b-110">\_ \_ наложение устройства VMR \_</span><span class="sxs-lookup"><span data-stu-id="1a25b-110">VMR\_RENDER\_DEVICE\_OVERLAY</span></span> | <span data-ttu-id="1a25b-111">VMR будет отображаться на поверхности наложения (только VMR-7).</span><span class="sxs-lookup"><span data-stu-id="1a25b-111">The VMR will render to the overlay surface (VMR-7 only).</span></span> |
| <span data-ttu-id="1a25b-112">VMR \_ отрисовывает \_ устройство \_ видмем</span><span class="sxs-lookup"><span data-stu-id="1a25b-112">VMR\_RENDER\_DEVICE\_VIDMEM</span></span>  | <span data-ttu-id="1a25b-113">Фильтр VMR будет отображаться в видеопамяти.</span><span class="sxs-lookup"><span data-stu-id="1a25b-113">The VMR will render to video memory.</span></span>                     |
| <span data-ttu-id="1a25b-114">VMR \_ отрисовывает \_ устройство \_ сисмем</span><span class="sxs-lookup"><span data-stu-id="1a25b-114">VMR\_RENDER\_DEVICE\_SYSMEM</span></span>  | <span data-ttu-id="1a25b-115">Фильтр VMR будет отображаться в системной памяти (только VMR-7).</span><span class="sxs-lookup"><span data-stu-id="1a25b-115">The VMR will render to system memory (VMR-7 only).</span></span>       |



 

</dd> <dt>

<span data-ttu-id="1a25b-116"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="1a25b-116"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="1a25b-117">Не используется.</span><span class="sxs-lookup"><span data-stu-id="1a25b-117">Not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1a25b-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1a25b-118">Remarks</span></span>

<span data-ttu-id="1a25b-119">Это событие отправляется с помощью VMR-7 и VMR-9 и перенаправляется в приложения.</span><span class="sxs-lookup"><span data-stu-id="1a25b-119">This event is sent by both the VMR-7 and the VMR-9 and it is forwarded to applications.</span></span> <span data-ttu-id="1a25b-120">Обратите внимание, что VMR-9 поддерживает только целевые объекты отрисовки видео в памяти.</span><span class="sxs-lookup"><span data-stu-id="1a25b-120">Note that the VMR-9 only supports video memory render targets.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a25b-121">Требования</span><span class="sxs-lookup"><span data-stu-id="1a25b-121">Requirements</span></span>



| <span data-ttu-id="1a25b-122">Требование</span><span class="sxs-lookup"><span data-stu-id="1a25b-122">Requirement</span></span> | <span data-ttu-id="1a25b-123">Значение</span><span class="sxs-lookup"><span data-stu-id="1a25b-123">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1a25b-124">Header</span><span class="sxs-lookup"><span data-stu-id="1a25b-124">Header</span></span><br/> | <dl> <span data-ttu-id="1a25b-125"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="1a25b-125"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a25b-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1a25b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a25b-127">Коды уведомлений о событиях</span><span class="sxs-lookup"><span data-stu-id="1a25b-127">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="1a25b-128">Уведомление о событии в DirectShow</span><span class="sxs-lookup"><span data-stu-id="1a25b-128">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




