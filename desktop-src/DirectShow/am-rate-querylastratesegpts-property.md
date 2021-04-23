---
description: Это свойство запрашивает у декодера время начала изменения скорости, которое было поставлено в очередь недавно, независимо от его расположения в очереди изменения скорости.
ms.assetid: 3c7006e7-48fd-4df8-b446-8ee2b024278b
title: Свойство AM_RATE_QueryLastRateSegPTS (Двдмедиа. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72c6e3e00985ba6e714bf48d349fd5af5c9593b9
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910272"
---
# <a name="am_rate_querylastratesegpts-property"></a><span data-ttu-id="f7376-103">\_ \_ Свойство куериластратесегптс Rate</span><span class="sxs-lookup"><span data-stu-id="f7376-103">AM\_RATE\_QueryLastRateSegPTS Property</span></span>

<span data-ttu-id="f7376-104">Это свойство запрашивает у декодера время начала изменения скорости, которое было поставлено в очередь недавно, независимо от его расположения в очереди изменения скорости.</span><span class="sxs-lookup"><span data-stu-id="f7376-104">This property queries the decoder for the start time of the rate change that was queued most recently, regardless of its position in the rate-change queue.</span></span>

<span data-ttu-id="f7376-105">Это свойство определено для версии 1,1 этого набора свойств. см [**. \_ \_ усератеверсион Rate**](am-rate-userateversion-property.md).</span><span class="sxs-lookup"><span data-stu-id="f7376-105">This property is defined for version 1.1 of this property set; see [**AM\_RATE\_UseRateVersion**](am-rate-userateversion-property.md).</span></span>



| <span data-ttu-id="f7376-106">Метка</span><span class="sxs-lookup"><span data-stu-id="f7376-106">Label</span></span> | <span data-ttu-id="f7376-107">Значение</span><span class="sxs-lookup"><span data-stu-id="f7376-107">Value</span></span> |
|-------------------|-------------------------------|
| <span data-ttu-id="f7376-108">Идентификатор GUID набора свойств</span><span class="sxs-lookup"><span data-stu-id="f7376-108">Property Set GUID</span></span> | <span data-ttu-id="f7376-109">\_Кспропсетид \_ тсратечанже</span><span class="sxs-lookup"><span data-stu-id="f7376-109">AM\_KSPROPSETID\_TSRateChange</span></span> |
| <span data-ttu-id="f7376-110">Идентификатор свойства</span><span class="sxs-lookup"><span data-stu-id="f7376-110">Property ID</span></span>       | <span data-ttu-id="f7376-111">\_Ставка \_ куериластратесегптс</span><span class="sxs-lookup"><span data-stu-id="f7376-111">AM\_RATE\_QueryLastRateSegPTS</span></span> |
| <span data-ttu-id="f7376-112">Тип данных</span><span class="sxs-lookup"><span data-stu-id="f7376-112">Data Type</span></span>         | <span data-ttu-id="f7376-113">**\_время ссылки**</span><span class="sxs-lookup"><span data-stu-id="f7376-113">**REFERENCE\_TIME**</span></span>           |



 

## <a name="remarks"></a><span data-ttu-id="f7376-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f7376-114">Remarks</span></span>

<span data-ttu-id="f7376-115">Фильтр источника может использовать это свойство для синхронизации изменений скорости в нескольких потоках аудио и видео.</span><span class="sxs-lookup"><span data-stu-id="f7376-115">The source filter can use this property to synchronize rate changes across several audio and video streams.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7376-116">Requirements (Требования)</span><span class="sxs-lookup"><span data-stu-id="f7376-116">Requirements</span></span>



| <span data-ttu-id="f7376-117">Требование</span><span class="sxs-lookup"><span data-stu-id="f7376-117">Requirement</span></span> | <span data-ttu-id="f7376-118">Значение</span><span class="sxs-lookup"><span data-stu-id="f7376-118">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f7376-119">Заголовок</span><span class="sxs-lookup"><span data-stu-id="f7376-119">Header</span></span><br/> | <dl> <span data-ttu-id="f7376-120"><dt>Двдмедиа. h</dt></span><span class="sxs-lookup"><span data-stu-id="f7376-120"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7376-121">См. также</span><span class="sxs-lookup"><span data-stu-id="f7376-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7376-122">**Набор свойств изменения скорости**</span><span class="sxs-lookup"><span data-stu-id="f7376-122">**Rate Change Property Set**</span></span>](rate-change-property-set.md)
</dt> </dl>

 

 




