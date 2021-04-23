---
description: Навигатор DVD использует это свойство для информирования декодера о том, что навигатор устанавливает правильные отметки времени для образцов, которые он передает в декодер.
ms.assetid: f04e8291-734f-483e-b756-5362beb68d9c
title: Свойство AM_RATE_CorrectTS (Двдмедиа. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15c65b613f892708dc210af2ca2a05efb74785fb
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910302"
---
# <a name="am_rate_correctts-property"></a><span data-ttu-id="8756a-103">\_ \_ Свойство корректтс Rate</span><span class="sxs-lookup"><span data-stu-id="8756a-103">AM\_RATE\_CorrectTS Property</span></span>

<span data-ttu-id="8756a-104">Навигатор DVD использует это свойство для информирования декодера о том, что навигатор устанавливает правильные отметки времени для образцов, которые он передает в декодер.</span><span class="sxs-lookup"><span data-stu-id="8756a-104">The DVD Navigator uses this property to inform the decoder that the Navigator is setting the correct time stamps on the samples it delivers to the decoder.</span></span>



| <span data-ttu-id="8756a-105">Метка</span><span class="sxs-lookup"><span data-stu-id="8756a-105">Label</span></span> | <span data-ttu-id="8756a-106">Значение</span><span class="sxs-lookup"><span data-stu-id="8756a-106">Value</span></span> |
|-------------------|-------------------------------|
| <span data-ttu-id="8756a-107">Идентификатор GUID набора свойств</span><span class="sxs-lookup"><span data-stu-id="8756a-107">Property Set GUID</span></span> | <span data-ttu-id="8756a-108">\_Кспропсетид \_ тсратечанже</span><span class="sxs-lookup"><span data-stu-id="8756a-108">AM\_KSPROPSETID\_TSRateChange</span></span> |
| <span data-ttu-id="8756a-109">Идентификатор свойства</span><span class="sxs-lookup"><span data-stu-id="8756a-109">Property ID</span></span>       | <span data-ttu-id="8756a-110">\_Ставка \_ корректтс</span><span class="sxs-lookup"><span data-stu-id="8756a-110">AM\_RATE\_CorrectTS</span></span>           |
| <span data-ttu-id="8756a-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="8756a-111">Data Type</span></span>         | <span data-ttu-id="8756a-112">**LONG**</span><span class="sxs-lookup"><span data-stu-id="8756a-112">**LONG**</span></span>                      |



 

## <a name="remarks"></a><span data-ttu-id="8756a-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8756a-113">Remarks</span></span>

<span data-ttu-id="8756a-114">В более ранних версиях DVD-навигатора не были заданы правильные метки времени, когда скорость воспроизведения отличается от 1,0.</span><span class="sxs-lookup"><span data-stu-id="8756a-114">Earlier versions of the DVD Navigator did not set the correct time stamps when the playback rate was something other than 1.0.</span></span> <span data-ttu-id="8756a-115">Многие декодеры обдействуют эту проблему, игнорируя отметки времени во время перемотки назад или вперед и оценивая правильное время презентации.</span><span class="sxs-lookup"><span data-stu-id="8756a-115">Many decoders work around this problem by ignoring the time stamps during rewind or fast forward, and estimating the correct presentation times.</span></span>

<span data-ttu-id="8756a-116">Эти проблемы были исправлены в текущей версии навигатора по DVD.</span><span class="sxs-lookup"><span data-stu-id="8756a-116">These problems have been corrected in the current version of the DVD Navigator.</span></span> <span data-ttu-id="8756a-117">Чтобы обеспечить обратную совместимость с существующими декодерами, Навигатор DVD указывает, что штампы времени верны, установив \_ \_ свойство корректтс Rate в декодере со значением **true**.</span><span class="sxs-lookup"><span data-stu-id="8756a-117">For backward compatibility with existing decoders, the DVD Navigator indicates that the time stamps are correct by setting the AM\_RATE\_CorrectTS property on the decoder with the value **TRUE**.</span></span> <span data-ttu-id="8756a-118">Если это свойство задано, декодер должен использовать фактические штампы времени вместо оценки времени представления.</span><span class="sxs-lookup"><span data-stu-id="8756a-118">When this property is set, the decoder should use the actual time stamps, instead of estimating the presentation times.</span></span>

## <a name="requirements"></a><span data-ttu-id="8756a-119">Requirements (Требования)</span><span class="sxs-lookup"><span data-stu-id="8756a-119">Requirements</span></span>



| <span data-ttu-id="8756a-120">Требование</span><span class="sxs-lookup"><span data-stu-id="8756a-120">Requirement</span></span> | <span data-ttu-id="8756a-121">Значение</span><span class="sxs-lookup"><span data-stu-id="8756a-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8756a-122">Заголовок</span><span class="sxs-lookup"><span data-stu-id="8756a-122">Header</span></span><br/> | <dl> <span data-ttu-id="8756a-123"><dt>Двдмедиа. h</dt></span><span class="sxs-lookup"><span data-stu-id="8756a-123"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8756a-124">См. также</span><span class="sxs-lookup"><span data-stu-id="8756a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8756a-125">**Набор свойств изменения скорости**</span><span class="sxs-lookup"><span data-stu-id="8756a-125">**Rate Change Property Set**</span></span>](rate-change-property-set.md)
</dt> </dl>

 

 




