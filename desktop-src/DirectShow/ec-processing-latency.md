---
description: Указывает количество времени, которое компонент принимает для обработки каждого образца.
ms.assetid: 84f81ee1-76d8-46fb-86ef-2500f8f4ef36
title: EC_PROCESSING_LATENCY (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d97514b4d2851f619f89f42e644766d50b7d25f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674819"
---
# <a name="ec_processing_latency"></a><span data-ttu-id="eab5b-103">\_Задержка обработки \_ EC</span><span class="sxs-lookup"><span data-stu-id="eab5b-103">EC\_PROCESSING\_LATENCY</span></span>

<span data-ttu-id="eab5b-104">Указывает количество времени, которое компонент принимает для обработки каждого образца.</span><span class="sxs-lookup"><span data-stu-id="eab5b-104">Indicates the amount of time that a component is taking to process each sample.</span></span>

## <a name="parameters"></a><span data-ttu-id="eab5b-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="eab5b-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eab5b-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="eab5b-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="eab5b-107">(**\_ время ссылки на константу** \* ) количество времени для обработки каждого образца в единицах с 100 до единицы.</span><span class="sxs-lookup"><span data-stu-id="eab5b-107">(**const REFERENCE\_TIME**\*) The amount of time to process each sample, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="eab5b-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="eab5b-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="eab5b-109">Ноль.</span><span class="sxs-lookup"><span data-stu-id="eab5b-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="eab5b-110">Действие по умолчанию</span><span class="sxs-lookup"><span data-stu-id="eab5b-110">Default Action</span></span>

<span data-ttu-id="eab5b-111">Нет.</span><span class="sxs-lookup"><span data-stu-id="eab5b-111">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="eab5b-112">Remarks</span><span class="sxs-lookup"><span data-stu-id="eab5b-112">Remarks</span></span>

<span data-ttu-id="eab5b-113">Выступающий для [**расширенного фильтра модуля подготовки видео**](enhanced-video-renderer-filter.md) (Евр) может отправить это сообщение в евр, чтобы уведомить Евр о задержке обработки в выступающем.</span><span class="sxs-lookup"><span data-stu-id="eab5b-113">A presenter for the [**Enhanced Video Renderer**](enhanced-video-renderer-filter.md) (EVR) filter can send this message to the EVR to notify the EVR about the presenter's processing latency.</span></span>

## <a name="requirements"></a><span data-ttu-id="eab5b-114">Требования</span><span class="sxs-lookup"><span data-stu-id="eab5b-114">Requirements</span></span>



| <span data-ttu-id="eab5b-115">Требование</span><span class="sxs-lookup"><span data-stu-id="eab5b-115">Requirement</span></span> | <span data-ttu-id="eab5b-116">Значение</span><span class="sxs-lookup"><span data-stu-id="eab5b-116">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="eab5b-117">Header</span><span class="sxs-lookup"><span data-stu-id="eab5b-117">Header</span></span><br/> | <dl> <span data-ttu-id="eab5b-118"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="eab5b-118"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eab5b-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="eab5b-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eab5b-120">Коды уведомлений о событиях</span><span class="sxs-lookup"><span data-stu-id="eab5b-120">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="eab5b-121">Уведомление о событии в DirectShow</span><span class="sxs-lookup"><span data-stu-id="eab5b-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




