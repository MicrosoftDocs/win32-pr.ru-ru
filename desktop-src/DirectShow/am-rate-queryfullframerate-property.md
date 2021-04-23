---
description: Это свойство запрашивает у декодера максимальную частоту полных кадров, поддерживаемую декодером. Типом данных этого свойства является \_ Структура AM куерирате.
ms.assetid: 98808ed4-6d34-437b-9729-9cc805bc81f0
title: Свойство AM_RATE_QueryFullFrameRate (Двдмедиа. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70bc096e5b68737ca877a037571223d673284dab
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910282"
---
# <a name="am_rate_queryfullframerate-property"></a><span data-ttu-id="c2027-104">\_ \_ Свойство куерифуллфрамерате Rate</span><span class="sxs-lookup"><span data-stu-id="c2027-104">AM\_RATE\_QueryFullFrameRate Property</span></span>

<span data-ttu-id="c2027-105">Это свойство запрашивает у декодера максимальную частоту полных кадров, поддерживаемую декодером.</span><span class="sxs-lookup"><span data-stu-id="c2027-105">This property queries the decoder for the maximum full-frame rate that the decoder supports.</span></span> <span data-ttu-id="c2027-106">Типом данных этого свойства является структура **AM \_ куерирате** .</span><span class="sxs-lookup"><span data-stu-id="c2027-106">The data type for this property is an **AM\_QueryRate** structure.</span></span>

<span data-ttu-id="c2027-107">Это свойство определено для версии 1,1 этого набора свойств. см [**. \_ \_ усератеверсион Rate**](am-rate-userateversion-property.md).</span><span class="sxs-lookup"><span data-stu-id="c2027-107">This property is defined for version 1.1 of this property set; see [**AM\_RATE\_UseRateVersion**](am-rate-userateversion-property.md).</span></span>



| <span data-ttu-id="c2027-108">Метка</span><span class="sxs-lookup"><span data-stu-id="c2027-108">Label</span></span> | <span data-ttu-id="c2027-109">Значение</span><span class="sxs-lookup"><span data-stu-id="c2027-109">Value</span></span> |
|-------------------|---------------------------------------|
| <span data-ttu-id="c2027-110">Идентификатор GUID набора свойств</span><span class="sxs-lookup"><span data-stu-id="c2027-110">Property Set GUID</span></span> | <span data-ttu-id="c2027-111">\_Кспропсетид \_ тсратечанже</span><span class="sxs-lookup"><span data-stu-id="c2027-111">AM\_KSPROPSETID\_TSRateChange</span></span>         |
| <span data-ttu-id="c2027-112">Идентификатор свойства</span><span class="sxs-lookup"><span data-stu-id="c2027-112">Property ID</span></span>       | <span data-ttu-id="c2027-113">\_ \_ Свойство куерифуллфрамерате Rate</span><span class="sxs-lookup"><span data-stu-id="c2027-113">AM\_RATE\_QueryFullFrameRate Property</span></span> |
| <span data-ttu-id="c2027-114">Тип данных</span><span class="sxs-lookup"><span data-stu-id="c2027-114">Data Type</span></span>         | [<span data-ttu-id="c2027-115">**\_Куерирате**</span><span class="sxs-lookup"><span data-stu-id="c2027-115">**AM\_QueryRate**</span></span>](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_queryrate) |



 

## <a name="remarks"></a><span data-ttu-id="c2027-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c2027-116">Remarks</span></span>

<span data-ttu-id="c2027-117">Если скорость воспроизведения превышает максимальную скорость декодера, фильтр источника отправляет группы непрерывных выборок, разделенные небесперебойностью.</span><span class="sxs-lookup"><span data-stu-id="c2027-117">If the playback rate exceeds the decoder's maximum rate, the source filter sends groups of continuous samples separated by discontinuities.</span></span> <span data-ttu-id="c2027-118">Метки времени переходят между прекращениями.</span><span class="sxs-lookup"><span data-stu-id="c2027-118">The time stamps jump across the discontinuities.</span></span> <span data-ttu-id="c2027-119">Фильтр источника может сделать это, даже если скорость воспроизведения находится в пределах максимальной скорости декодера, так как могут существовать другие факторы, такие как ввод-вывод на диск, которые ограничивают максимальную скорость воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="c2027-119">The source filter might do this even if the playback rate is within the decoder's maximum rate, because there may be other factors, such as disk IO, that limit the full playback rate.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2027-120">Requirements (Требования)</span><span class="sxs-lookup"><span data-stu-id="c2027-120">Requirements</span></span>



| <span data-ttu-id="c2027-121">Требование</span><span class="sxs-lookup"><span data-stu-id="c2027-121">Requirement</span></span> | <span data-ttu-id="c2027-122">Значение</span><span class="sxs-lookup"><span data-stu-id="c2027-122">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c2027-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="c2027-123">Header</span></span><br/> | <dl> <span data-ttu-id="c2027-124"><dt>Двдмедиа. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2027-124"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2027-125">См. также</span><span class="sxs-lookup"><span data-stu-id="c2027-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2027-126">**Набор свойств изменения скорости**</span><span class="sxs-lookup"><span data-stu-id="c2027-126">**Rate Change Property Set**</span></span>](rate-change-property-set.md)
</dt> </dl>

 

 




