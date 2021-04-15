---
description: Это свойство запрашивает у декодера максимальную частоту полных кадров, поддерживаемую декодером. Типом данных этого свойства является \_ Структура AM куерирате.
ms.assetid: 98808ed4-6d34-437b-9729-9cc805bc81f0
title: Свойство AM_RATE_QueryFullFrameRate (Двдмедиа. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab2c99564caa09253198b101a3e2467ec88c7e34
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689053"
---
# <a name="am_rate_queryfullframerate-property"></a><span data-ttu-id="6f87f-104">\_ \_ Свойство куерифуллфрамерате Rate</span><span class="sxs-lookup"><span data-stu-id="6f87f-104">AM\_RATE\_QueryFullFrameRate Property</span></span>

<span data-ttu-id="6f87f-105">Это свойство запрашивает у декодера максимальную частоту полных кадров, поддерживаемую декодером.</span><span class="sxs-lookup"><span data-stu-id="6f87f-105">This property queries the decoder for the maximum full-frame rate that the decoder supports.</span></span> <span data-ttu-id="6f87f-106">Типом данных этого свойства является структура **AM \_ куерирате** .</span><span class="sxs-lookup"><span data-stu-id="6f87f-106">The data type for this property is an **AM\_QueryRate** structure.</span></span>

<span data-ttu-id="6f87f-107">Это свойство определено для версии 1,1 этого набора свойств. см [**. \_ \_ усератеверсион Rate**](am-rate-userateversion-property.md).</span><span class="sxs-lookup"><span data-stu-id="6f87f-107">This property is defined for version 1.1 of this property set; see [**AM\_RATE\_UseRateVersion**](am-rate-userateversion-property.md).</span></span>



|                   |                                       |
|-------------------|---------------------------------------|
| <span data-ttu-id="6f87f-108">Идентификатор GUID набора свойств</span><span class="sxs-lookup"><span data-stu-id="6f87f-108">Property Set GUID</span></span> | <span data-ttu-id="6f87f-109">\_Кспропсетид \_ тсратечанже</span><span class="sxs-lookup"><span data-stu-id="6f87f-109">AM\_KSPROPSETID\_TSRateChange</span></span>         |
| <span data-ttu-id="6f87f-110">Идентификатор свойства</span><span class="sxs-lookup"><span data-stu-id="6f87f-110">Property ID</span></span>       | <span data-ttu-id="6f87f-111">\_ \_ Свойство куерифуллфрамерате Rate</span><span class="sxs-lookup"><span data-stu-id="6f87f-111">AM\_RATE\_QueryFullFrameRate Property</span></span> |
| <span data-ttu-id="6f87f-112">Тип данных</span><span class="sxs-lookup"><span data-stu-id="6f87f-112">Data Type</span></span>         | [<span data-ttu-id="6f87f-113">**\_Куерирате**</span><span class="sxs-lookup"><span data-stu-id="6f87f-113">**AM\_QueryRate**</span></span>](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_queryrate) |



 

## <a name="remarks"></a><span data-ttu-id="6f87f-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6f87f-114">Remarks</span></span>

<span data-ttu-id="6f87f-115">Если скорость воспроизведения превышает максимальную скорость декодера, фильтр источника отправляет группы непрерывных выборок, разделенные небесперебойностью.</span><span class="sxs-lookup"><span data-stu-id="6f87f-115">If the playback rate exceeds the decoder's maximum rate, the source filter sends groups of continuous samples separated by discontinuities.</span></span> <span data-ttu-id="6f87f-116">Метки времени переходят между прекращениями.</span><span class="sxs-lookup"><span data-stu-id="6f87f-116">The time stamps jump across the discontinuities.</span></span> <span data-ttu-id="6f87f-117">Фильтр источника может сделать это, даже если скорость воспроизведения находится в пределах максимальной скорости декодера, так как могут существовать другие факторы, такие как ввод-вывод на диск, которые ограничивают максимальную скорость воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="6f87f-117">The source filter might do this even if the playback rate is within the decoder's maximum rate, because there may be other factors, such as disk IO, that limit the full playback rate.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f87f-118">Требования</span><span class="sxs-lookup"><span data-stu-id="6f87f-118">Requirements</span></span>



| <span data-ttu-id="6f87f-119">Требование</span><span class="sxs-lookup"><span data-stu-id="6f87f-119">Requirement</span></span> | <span data-ttu-id="6f87f-120">Значение</span><span class="sxs-lookup"><span data-stu-id="6f87f-120">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6f87f-121">Header</span><span class="sxs-lookup"><span data-stu-id="6f87f-121">Header</span></span><br/> | <dl> <span data-ttu-id="6f87f-122"><dt>Двдмедиа. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f87f-122"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f87f-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6f87f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f87f-124">**Набор свойств изменения скорости**</span><span class="sxs-lookup"><span data-stu-id="6f87f-124">**Rate Change Property Set**</span></span>](rate-change-property-set.md)
</dt> </dl>

 

 




