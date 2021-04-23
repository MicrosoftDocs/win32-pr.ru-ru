---
description: Указывает, что Навигатор DVD начал играть или завершил воспроизведение данных караоке.
ms.assetid: 910bf809-a56a-4d02-9c7e-429769a4ec2b
title: EC_DVD_KARAOKE_MODE (Двдевкоде. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_KARAOKE_MODE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: fb83bc1de9c2933b53935c056b192eca74c4245c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675263"
---
# <a name="ec_dvd_karaoke_mode"></a><span data-ttu-id="77f58-103">\_режим Караоке на DVD-диске EC \_ \_</span><span class="sxs-lookup"><span data-stu-id="77f58-103">EC\_DVD\_KARAOKE\_MODE</span></span>

<span data-ttu-id="77f58-104">Указывает, что [Навигатор DVD](data-flow-in-the-dvd-navigator.md) начал играть или завершил воспроизведение данных караоке.</span><span class="sxs-lookup"><span data-stu-id="77f58-104">Indicates that the [DVD Navigator](data-flow-in-the-dvd-navigator.md) has either begun playing or finished playing karaoke data.</span></span>

## <a name="parameters"></a><span data-ttu-id="77f58-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="77f58-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77f58-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="77f58-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="77f58-107">.</span><span class="sxs-lookup"><span data-stu-id="77f58-107">Boolean value.</span></span> <span data-ttu-id="77f58-108">Если задано **значение true**, проигрываться запись караоке.</span><span class="sxs-lookup"><span data-stu-id="77f58-108">If **TRUE**, a karaoke track is being played.</span></span> <span data-ttu-id="77f58-109">В противном случае запись караоке не будет воспроизводиться.</span><span class="sxs-lookup"><span data-stu-id="77f58-109">Otherwise, no karaoke track is being played.</span></span>

</dd> <dt>

<span data-ttu-id="77f58-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="77f58-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="77f58-111">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="77f58-111">Reserved.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="77f58-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="77f58-112">Remarks</span></span>

<span data-ttu-id="77f58-113">Проигрыватель DVD сигнализирует об этом событии при каждом изменении доменов.</span><span class="sxs-lookup"><span data-stu-id="77f58-113">The DVD player signals this event whenever it changes domains.</span></span>

<span data-ttu-id="77f58-114">Это событие возникает во всех доменах DVD.</span><span class="sxs-lookup"><span data-stu-id="77f58-114">This event is raised in all DVD domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="77f58-115">Требования</span><span class="sxs-lookup"><span data-stu-id="77f58-115">Requirements</span></span>



| <span data-ttu-id="77f58-116">Требование</span><span class="sxs-lookup"><span data-stu-id="77f58-116">Requirement</span></span> | <span data-ttu-id="77f58-117">Значение</span><span class="sxs-lookup"><span data-stu-id="77f58-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77f58-118">Header</span><span class="sxs-lookup"><span data-stu-id="77f58-118">Header</span></span><br/> | <dl> <span data-ttu-id="77f58-119"><dt>Двдевкоде. h (включение DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="77f58-119"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77f58-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="77f58-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77f58-121">DVD-приложения</span><span class="sxs-lookup"><span data-stu-id="77f58-121">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="77f58-122">Коды уведомлений о событиях DVD</span><span class="sxs-lookup"><span data-stu-id="77f58-122">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="77f58-123">Уведомление о событии в DirectShow</span><span class="sxs-lookup"><span data-stu-id="77f58-123">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




