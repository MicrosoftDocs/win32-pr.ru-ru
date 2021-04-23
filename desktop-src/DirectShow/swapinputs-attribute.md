---
description: Атрибут свапинпутс указывает, следует ли поменять входные данные перехода. Если значение равно TRUE, входные данные меняются местами. Значение по умолчанию — FALSE.
ms.assetid: 2b8d95ec-2c6c-4bd8-83e9-7f72770449b5
title: Атрибут свапинпутс
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27e2f02c642283e90b994bcd1bfa9e05076a7bae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349065"
---
# <a name="swapinputs-attribute"></a><span data-ttu-id="5d125-105">Атрибут свапинпутс</span><span class="sxs-lookup"><span data-stu-id="5d125-105">swapinputs Attribute</span></span>

> [!Note]  
> <span data-ttu-id="5d125-106">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="5d125-106">\[Deprecated.</span></span> <span data-ttu-id="5d125-107">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5d125-107">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="5d125-108">`swapinputs`Атрибут указывает, следует ли поменять входные данные перехода.</span><span class="sxs-lookup"><span data-stu-id="5d125-108">The `swapinputs` attribute specifies whether to swap transition inputs.</span></span> <span data-ttu-id="5d125-109">Если значение равно **true**, входные данные меняются местами.</span><span class="sxs-lookup"><span data-stu-id="5d125-109">If the value is **TRUE**, the inputs are swapped.</span></span> <span data-ttu-id="5d125-110">Значение по умолчанию — **false**.</span><span class="sxs-lookup"><span data-stu-id="5d125-110">The default value is **FALSE**.</span></span>

## <a name="possible-values"></a><span data-ttu-id="5d125-111">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="5d125-111">Possible Values</span></span>

<span data-ttu-id="5d125-112">Следующие значения определены как TRUE: y, Y, t, T, 1.</span><span class="sxs-lookup"><span data-stu-id="5d125-112">The following values are defined as TRUE: y, Y, t, T, 1.</span></span> <span data-ttu-id="5d125-113">Следующие значения определены как FALSE: n, N, f, F, 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="5d125-113">The following values are defined as FALSE: n, N, f, F, 0 (zero).</span></span>

## <a name="applies-to"></a><span data-ttu-id="5d125-114">Применение</span><span class="sxs-lookup"><span data-stu-id="5d125-114">Applies To</span></span>

[<span data-ttu-id="5d125-115">**режима**</span><span class="sxs-lookup"><span data-stu-id="5d125-115">**transition**</span></span>](transition-element.md)

## <a name="remarks"></a><span data-ttu-id="5d125-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5d125-116">Remarks</span></span>

<span data-ttu-id="5d125-117">По умолчанию переход продолжается от составного набора всех уровней с низким приоритетом до слоя, на котором находится переход.</span><span class="sxs-lookup"><span data-stu-id="5d125-117">By default, a transition proceeds from the composite of all lower-priority layers to the layer on which the transition resides.</span></span> <span data-ttu-id="5d125-118">Если значение `swapinputs` атрибута равно 1, это направление изменяется на противоположное.</span><span class="sxs-lookup"><span data-stu-id="5d125-118">If the `swapinputs` attribute is 1, this direction is reversed.</span></span> <span data-ttu-id="5d125-119">Дополнительные сведения о модели многоуровневого слоя, используемой DES, см. [в разделе Модель временной шкалы](the-timeline-model.md).</span><span class="sxs-lookup"><span data-stu-id="5d125-119">For more information about the layering model used by DES, see [The Timeline Model](the-timeline-model.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="5d125-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5d125-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d125-121">Атрибуты КСТЛ</span><span class="sxs-lookup"><span data-stu-id="5d125-121">XTL Attributes</span></span>](xtl-attributes.md)
</dt> <dt>

[<span data-ttu-id="5d125-122">**Иамтимелинетранс:: Сетсвапинпутс**</span><span class="sxs-lookup"><span data-stu-id="5d125-122">**IAMTimelineTrans::SetSwapInputs**</span></span>](iamtimelinetrans-setswapinputs.md)
</dt> </dl>

 

 



