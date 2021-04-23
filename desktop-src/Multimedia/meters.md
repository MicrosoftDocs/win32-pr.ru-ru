---
title: Приборов
description: Приборов
ms.assetid: 11a98d2a-7cdd-4249-bba9-7edc51d7f8b0
keywords:
- аудио миксерс, элементы управления
- звуковые миксерсы, измерительные приборы
- миксерс, элементы управления
- миксерс, метрах
- элементы управления "Счетчик"
- Структура MIXERCONTROLDETAILS_BOOLEAN
- Структура MIXERCONTROLDETAILS_SIGNED
- Структура MIXERCONTROLDETAILS_UNSIGNED
- Логический элемент управления
- Пиковое управление
- подписанный элемент управления
- элемент управления без знака
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f36f1bebfca22b963e5c1eb6fede3f2786b35199
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487720"
---
# <a name="meters"></a><span data-ttu-id="77b01-115">Приборов</span><span class="sxs-lookup"><span data-stu-id="77b01-115">Meters</span></span>

<span data-ttu-id="77b01-116">Элемент управления "Счетчик" измеряет данные, передаваемые через звуковую линию.</span><span class="sxs-lookup"><span data-stu-id="77b01-116">The meter controls measure data passing through an audio line.</span></span> <span data-ttu-id="77b01-117">Эти элементы управления используют [**\_ неподписанные**](/previous-versions//dd757298(v=vs.85)) структуры [**миксерконтролдетаилс \_ Boolean**](/previous-versions//dd757295(v=vs.85)), [**миксерконтролдетаилс \_ со знаком**](/previous-versions//dd757297(v=vs.85))и миксерконтролдетаилс для получения и задания свойств элемента управления.</span><span class="sxs-lookup"><span data-stu-id="77b01-117">These controls use the [**MIXERCONTROLDETAILS\_BOOLEAN**](/previous-versions//dd757295(v=vs.85)), [**MIXERCONTROLDETAILS\_SIGNED**](/previous-versions//dd757297(v=vs.85)), and [**MIXERCONTROLDETAILS\_UNSIGNED**](/previous-versions//dd757298(v=vs.85)) structures to retrieve and set control properties.</span></span> <span data-ttu-id="77b01-118">В следующей таблице описаны типы счетчиков.</span><span class="sxs-lookup"><span data-stu-id="77b01-118">The following table describes the types of meters.</span></span>



| <span data-ttu-id="77b01-119">Control</span><span class="sxs-lookup"><span data-stu-id="77b01-119">Control</span></span>  | <span data-ttu-id="77b01-120">Описание</span><span class="sxs-lookup"><span data-stu-id="77b01-120">Description</span></span>                                                                                                                                            |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77b01-121">логический</span><span class="sxs-lookup"><span data-stu-id="77b01-121">Boolean</span></span>  | <span data-ttu-id="77b01-122">Измеряет, является ли целочисленное значение ЛОЖНЫм (нулем) или TRUE/ON (отличное от нуля).</span><span class="sxs-lookup"><span data-stu-id="77b01-122">Measures whether an integer value is FALSE/OFF (zero) or TRUE/ON (nonzero).</span></span>                                                                            |
| <span data-ttu-id="77b01-123">Peak</span><span class="sxs-lookup"><span data-stu-id="77b01-123">Peak</span></span>     | <span data-ttu-id="77b01-124">Измеряет отклонения от 0 как в положительных, так и в отрицательных направлениях.</span><span class="sxs-lookup"><span data-stu-id="77b01-124">Measures the deflection from 0 in both the positive and negative directions.</span></span> <span data-ttu-id="77b01-125">Диапазон целочисленных значений для счетчика пиковой нагрузки составляет от – 32 768 до 32 767.</span><span class="sxs-lookup"><span data-stu-id="77b01-125">The range of integer values for the peak meter is –32,768 through 32,767.</span></span> |
| <span data-ttu-id="77b01-126">Со знаком</span><span class="sxs-lookup"><span data-stu-id="77b01-126">Signed</span></span>   | <span data-ttu-id="77b01-127">Измеряет целочисленные значения в диапазоне от – 231 до (231 – 1).</span><span class="sxs-lookup"><span data-stu-id="77b01-127">Measures integer values in the range of –231 through (231 – 1).</span></span> <span data-ttu-id="77b01-128">Драйвер микшера определяет ограничения этого счетчика.</span><span class="sxs-lookup"><span data-stu-id="77b01-128">The mixer driver defines the limits of this meter.</span></span>                                     |
| <span data-ttu-id="77b01-129">Без знака</span><span class="sxs-lookup"><span data-stu-id="77b01-129">Unsigned</span></span> | <span data-ttu-id="77b01-130">Измеряет целочисленные значения в диапазоне от 0 до (232 – 1).</span><span class="sxs-lookup"><span data-stu-id="77b01-130">Measures integer values in the range of 0 through (232 – 1).</span></span> <span data-ttu-id="77b01-131">Драйвер микшера определяет ограничения этого счетчика.</span><span class="sxs-lookup"><span data-stu-id="77b01-131">The mixer driver defines the limits of this meter.</span></span>                                        |



 

 

 