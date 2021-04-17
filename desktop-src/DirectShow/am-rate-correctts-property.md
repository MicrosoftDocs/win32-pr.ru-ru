---
description: Навигатор DVD использует это свойство для информирования декодера о том, что навигатор устанавливает правильные отметки времени для образцов, которые он передает в декодер.
ms.assetid: f04e8291-734f-483e-b756-5362beb68d9c
title: Свойство AM_RATE_CorrectTS (Двдмедиа. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa410b079d3de63de364662c7d5465c82814d24a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689054"
---
# <a name="am_rate_correctts-property"></a><span data-ttu-id="c48e2-103">\_ \_ Свойство корректтс Rate</span><span class="sxs-lookup"><span data-stu-id="c48e2-103">AM\_RATE\_CorrectTS Property</span></span>

<span data-ttu-id="c48e2-104">Навигатор DVD использует это свойство для информирования декодера о том, что навигатор устанавливает правильные отметки времени для образцов, которые он передает в декодер.</span><span class="sxs-lookup"><span data-stu-id="c48e2-104">The DVD Navigator uses this property to inform the decoder that the Navigator is setting the correct time stamps on the samples it delivers to the decoder.</span></span>



|                   |                               |
|-------------------|-------------------------------|
| <span data-ttu-id="c48e2-105">Идентификатор GUID набора свойств</span><span class="sxs-lookup"><span data-stu-id="c48e2-105">Property Set GUID</span></span> | <span data-ttu-id="c48e2-106">\_Кспропсетид \_ тсратечанже</span><span class="sxs-lookup"><span data-stu-id="c48e2-106">AM\_KSPROPSETID\_TSRateChange</span></span> |
| <span data-ttu-id="c48e2-107">Идентификатор свойства</span><span class="sxs-lookup"><span data-stu-id="c48e2-107">Property ID</span></span>       | <span data-ttu-id="c48e2-108">\_Ставка \_ корректтс</span><span class="sxs-lookup"><span data-stu-id="c48e2-108">AM\_RATE\_CorrectTS</span></span>           |
| <span data-ttu-id="c48e2-109">Тип данных</span><span class="sxs-lookup"><span data-stu-id="c48e2-109">Data Type</span></span>         | <span data-ttu-id="c48e2-110">**LONG**</span><span class="sxs-lookup"><span data-stu-id="c48e2-110">**LONG**</span></span>                      |



 

## <a name="remarks"></a><span data-ttu-id="c48e2-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c48e2-111">Remarks</span></span>

<span data-ttu-id="c48e2-112">В более ранних версиях DVD-навигатора не были заданы правильные метки времени, когда скорость воспроизведения отличается от 1,0.</span><span class="sxs-lookup"><span data-stu-id="c48e2-112">Earlier versions of the DVD Navigator did not set the correct time stamps when the playback rate was something other than 1.0.</span></span> <span data-ttu-id="c48e2-113">Многие декодеры обдействуют эту проблему, игнорируя отметки времени во время перемотки назад или вперед и оценивая правильное время презентации.</span><span class="sxs-lookup"><span data-stu-id="c48e2-113">Many decoders work around this problem by ignoring the time stamps during rewind or fast forward, and estimating the correct presentation times.</span></span>

<span data-ttu-id="c48e2-114">Эти проблемы были исправлены в текущей версии навигатора по DVD.</span><span class="sxs-lookup"><span data-stu-id="c48e2-114">These problems have been corrected in the current version of the DVD Navigator.</span></span> <span data-ttu-id="c48e2-115">Чтобы обеспечить обратную совместимость с существующими декодерами, Навигатор DVD указывает, что штампы времени верны, установив \_ \_ свойство корректтс Rate в декодере со значением **true**.</span><span class="sxs-lookup"><span data-stu-id="c48e2-115">For backward compatibility with existing decoders, the DVD Navigator indicates that the time stamps are correct by setting the AM\_RATE\_CorrectTS property on the decoder with the value **TRUE**.</span></span> <span data-ttu-id="c48e2-116">Если это свойство задано, декодер должен использовать фактические штампы времени вместо оценки времени представления.</span><span class="sxs-lookup"><span data-stu-id="c48e2-116">When this property is set, the decoder should use the actual time stamps, instead of estimating the presentation times.</span></span>

## <a name="requirements"></a><span data-ttu-id="c48e2-117">Требования</span><span class="sxs-lookup"><span data-stu-id="c48e2-117">Requirements</span></span>



| <span data-ttu-id="c48e2-118">Требование</span><span class="sxs-lookup"><span data-stu-id="c48e2-118">Requirement</span></span> | <span data-ttu-id="c48e2-119">Значение</span><span class="sxs-lookup"><span data-stu-id="c48e2-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c48e2-120">Header</span><span class="sxs-lookup"><span data-stu-id="c48e2-120">Header</span></span><br/> | <dl> <span data-ttu-id="c48e2-121"><dt>Двдмедиа. h</dt></span><span class="sxs-lookup"><span data-stu-id="c48e2-121"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c48e2-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c48e2-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c48e2-123">**Набор свойств изменения скорости**</span><span class="sxs-lookup"><span data-stu-id="c48e2-123">**Rate Change Property Set**</span></span>](rate-change-property-set.md)
</dt> </dl>

 

 




