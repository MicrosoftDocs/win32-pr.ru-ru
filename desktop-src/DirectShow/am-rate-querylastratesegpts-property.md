---
description: Это свойство запрашивает у декодера время начала изменения скорости, которое было поставлено в очередь недавно, независимо от его расположения в очереди изменения скорости.
ms.assetid: 3c7006e7-48fd-4df8-b446-8ee2b024278b
title: Свойство AM_RATE_QueryLastRateSegPTS (Двдмедиа. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 024ac26d8307dc9b8ff8e16603dfcc61b0704390
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657674"
---
# <a name="am_rate_querylastratesegpts-property"></a><span data-ttu-id="30118-103">\_ \_ Свойство куериластратесегптс Rate</span><span class="sxs-lookup"><span data-stu-id="30118-103">AM\_RATE\_QueryLastRateSegPTS Property</span></span>

<span data-ttu-id="30118-104">Это свойство запрашивает у декодера время начала изменения скорости, которое было поставлено в очередь недавно, независимо от его расположения в очереди изменения скорости.</span><span class="sxs-lookup"><span data-stu-id="30118-104">This property queries the decoder for the start time of the rate change that was queued most recently, regardless of its position in the rate-change queue.</span></span>

<span data-ttu-id="30118-105">Это свойство определено для версии 1,1 этого набора свойств. см [**. \_ \_ усератеверсион Rate**](am-rate-userateversion-property.md).</span><span class="sxs-lookup"><span data-stu-id="30118-105">This property is defined for version 1.1 of this property set; see [**AM\_RATE\_UseRateVersion**](am-rate-userateversion-property.md).</span></span>



|                   |                               |
|-------------------|-------------------------------|
| <span data-ttu-id="30118-106">Идентификатор GUID набора свойств</span><span class="sxs-lookup"><span data-stu-id="30118-106">Property Set GUID</span></span> | <span data-ttu-id="30118-107">\_Кспропсетид \_ тсратечанже</span><span class="sxs-lookup"><span data-stu-id="30118-107">AM\_KSPROPSETID\_TSRateChange</span></span> |
| <span data-ttu-id="30118-108">Идентификатор свойства</span><span class="sxs-lookup"><span data-stu-id="30118-108">Property ID</span></span>       | <span data-ttu-id="30118-109">\_Ставка \_ куериластратесегптс</span><span class="sxs-lookup"><span data-stu-id="30118-109">AM\_RATE\_QueryLastRateSegPTS</span></span> |
| <span data-ttu-id="30118-110">Тип данных</span><span class="sxs-lookup"><span data-stu-id="30118-110">Data Type</span></span>         | <span data-ttu-id="30118-111">**\_время ссылки**</span><span class="sxs-lookup"><span data-stu-id="30118-111">**REFERENCE\_TIME**</span></span>           |



 

## <a name="remarks"></a><span data-ttu-id="30118-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="30118-112">Remarks</span></span>

<span data-ttu-id="30118-113">Фильтр источника может использовать это свойство для синхронизации изменений скорости в нескольких потоках аудио и видео.</span><span class="sxs-lookup"><span data-stu-id="30118-113">The source filter can use this property to synchronize rate changes across several audio and video streams.</span></span>

## <a name="requirements"></a><span data-ttu-id="30118-114">Требования</span><span class="sxs-lookup"><span data-stu-id="30118-114">Requirements</span></span>



| <span data-ttu-id="30118-115">Требование</span><span class="sxs-lookup"><span data-stu-id="30118-115">Requirement</span></span> | <span data-ttu-id="30118-116">Значение</span><span class="sxs-lookup"><span data-stu-id="30118-116">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="30118-117">Header</span><span class="sxs-lookup"><span data-stu-id="30118-117">Header</span></span><br/> | <dl> <span data-ttu-id="30118-118"><dt>Двдмедиа. h</dt></span><span class="sxs-lookup"><span data-stu-id="30118-118"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30118-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="30118-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30118-120">**Набор свойств изменения скорости**</span><span class="sxs-lookup"><span data-stu-id="30118-120">**Rate Change Property Set**</span></span>](rate-change-property-set.md)
</dt> </dl>

 

 




