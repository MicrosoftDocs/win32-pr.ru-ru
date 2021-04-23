---
title: Числа (мультимедиа Windows)
description: С помощью чисел
ms.assetid: d416c4c2-a3e1-45a2-9ae1-82050a5e471b
keywords:
- аудио миксерс, элементы управления
- аудио миксерс, числа
- миксерс, элементы управления
- миксерс, числа
- числовые элементы управления
- Структура MIXERCONTROLDETAILS_SIGNED
- Структура MIXERCONTROLDETAILS_UNSIGNED
- элемент управления шкала
- элемент управления в процентах
- подписанный элемент управления
- элемент управления без знака
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f02c4ffd40f1058fae51af3798135840394be918
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104134906"
---
# <a name="numbers-windows-multimedia"></a><span data-ttu-id="4ce78-114">Числа (мультимедиа Windows)</span><span class="sxs-lookup"><span data-stu-id="4ce78-114">Numbers (Windows Multimedia)</span></span>

<span data-ttu-id="4ce78-115">Элементы управления "число" позволяют пользователю вводить числовые данные, связанные со строкой.</span><span class="sxs-lookup"><span data-stu-id="4ce78-115">The number controls allow the user to enter numerical data associated with a line.</span></span> <span data-ttu-id="4ce78-116">Числовые данные выражаются как целые числа со знаком, целые числа без знака или целочисленные шкала значения.</span><span class="sxs-lookup"><span data-stu-id="4ce78-116">The numerical data is expressed as signed integers, unsigned integers, or integer decibel values.</span></span> <span data-ttu-id="4ce78-117">Эти элементы управления используют [**\_ неподписанные**](/previous-versions//dd757298(v=vs.85)) структуры [**миксерконтролдетаилс \_**](/previous-versions//dd757297(v=vs.85)) и миксерконтролдетаилс для получения и задания свойств элементов управления.</span><span class="sxs-lookup"><span data-stu-id="4ce78-117">These controls use the [**MIXERCONTROLDETAILS\_SIGNED**](/previous-versions//dd757297(v=vs.85)) and [**MIXERCONTROLDETAILS\_UNSIGNED**](/previous-versions//dd757298(v=vs.85)) structures to retrieve and set control properties.</span></span> <span data-ttu-id="4ce78-118">В следующей таблице описаны типы элементов управления "число".</span><span class="sxs-lookup"><span data-stu-id="4ce78-118">The following table describes the types of number controls.</span></span>



| <span data-ttu-id="4ce78-119">Control</span><span class="sxs-lookup"><span data-stu-id="4ce78-119">Control</span></span>  | <span data-ttu-id="4ce78-120">Описание</span><span class="sxs-lookup"><span data-stu-id="4ce78-120">Description</span></span>                                                                                                                         |
|----------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ce78-121">Со знаком</span><span class="sxs-lookup"><span data-stu-id="4ce78-121">Signed</span></span>   | <span data-ttu-id="4ce78-122">Позволяет указать целочисленные значения в диапазоне от – 231 до (231 – 1).</span><span class="sxs-lookup"><span data-stu-id="4ce78-122">Allows integer values entered in the range of – 231 through (231 –1).</span></span>                                                               |
| <span data-ttu-id="4ce78-123">Без знака</span><span class="sxs-lookup"><span data-stu-id="4ce78-123">Unsigned</span></span> | <span data-ttu-id="4ce78-124">Позволяет указать целочисленные значения в диапазоне от 0 до (232 – 1).</span><span class="sxs-lookup"><span data-stu-id="4ce78-124">Allows integer values entered in the range of 0 through (232 –1).</span></span>                                                                   |
| <span data-ttu-id="4ce78-125">Шкала</span><span class="sxs-lookup"><span data-stu-id="4ce78-125">Decibel</span></span>  | <span data-ttu-id="4ce78-126">Позволяет указать целочисленные шкала значения в десятых долях децибел.</span><span class="sxs-lookup"><span data-stu-id="4ce78-126">Allows integer decibel values to be entered, in tenths of decibels.</span></span> <span data-ttu-id="4ce78-127">Диапазон значений для этого элемента управления — от – 32 768 до 32 767.</span><span class="sxs-lookup"><span data-stu-id="4ce78-127">The range of values for this control is –32,768 through 32,767.</span></span> |
| <span data-ttu-id="4ce78-128">Процент</span><span class="sxs-lookup"><span data-stu-id="4ce78-128">Percent</span></span>  | <span data-ttu-id="4ce78-129">Позволяет указать значения в виде процентов.</span><span class="sxs-lookup"><span data-stu-id="4ce78-129">Allows values to be entered as percentages.</span></span>                                                                                         |



 

 

 
