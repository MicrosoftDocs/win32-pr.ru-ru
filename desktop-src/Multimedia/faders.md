---
title: фадерс
description: фадерс
ms.assetid: 2ca6be9f-9825-44d9-99c1-abcf6f0b42f7
keywords:
- аудио миксерс, элементы управления
- Audio миксерс, фадерс
- миксерс, элементы управления
- миксерс, фадерс
- фадерс
- Структура MIXERCONTROLDETAILS_UNSIGNED
- элемент управления выцветание тома
- элемент управления затуханием громкости басов
- элемент управления выцветание громкости высоких частот
- элемент управления графического эквалайзера
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd2b560b61a694089b947b0cfda7a54b486f1e3a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103987406"
---
# <a name="faders"></a><span data-ttu-id="c8163-113">фадерс</span><span class="sxs-lookup"><span data-stu-id="c8163-113">Faders</span></span>

<span data-ttu-id="c8163-114">Элементы управления фадер обычно являются вертикальными элементами управления, которые могут быть скорректированы вверх или вниз.</span><span class="sxs-lookup"><span data-stu-id="c8163-114">The fader controls are typically vertical controls that can be adjusted up or down.</span></span> <span data-ttu-id="c8163-115">Эти элементы управления имеют линейную шкалу и [**используют \_ неподписанную структуру миксерконтролдетаилс**](/previous-versions//dd757298(v=vs.85)) для получения и задания сведений об элементе управления.</span><span class="sxs-lookup"><span data-stu-id="c8163-115">These controls have a linear scale and use the [**MIXERCONTROLDETAILS\_UNSIGNED**](/previous-versions//dd757298(v=vs.85)) structure to retrieve and set control details.</span></span> <span data-ttu-id="c8163-116">В следующей таблице описаны типы фадерс.</span><span class="sxs-lookup"><span data-stu-id="c8163-116">The following table describes the types of faders.</span></span>



| <span data-ttu-id="c8163-117">Control</span><span class="sxs-lookup"><span data-stu-id="c8163-117">Control</span></span>   | <span data-ttu-id="c8163-118">Описание</span><span class="sxs-lookup"><span data-stu-id="c8163-118">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                     |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8163-119">фадер</span><span class="sxs-lookup"><span data-stu-id="c8163-119">Fader</span></span>     | <span data-ttu-id="c8163-120">Общее управление затуханием.</span><span class="sxs-lookup"><span data-stu-id="c8163-120">General fade control.</span></span> <span data-ttu-id="c8163-121">Диапазон допустимых значений — от 0 до 65 535.</span><span class="sxs-lookup"><span data-stu-id="c8163-121">The range of acceptable values is 0 through 65,535.</span></span>                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="c8163-122">Том</span><span class="sxs-lookup"><span data-stu-id="c8163-122">Volume</span></span>    | <span data-ttu-id="c8163-123">Общий элемент управления выцветание тома.</span><span class="sxs-lookup"><span data-stu-id="c8163-123">General volume fade control.</span></span> <span data-ttu-id="c8163-124">Диапазон допустимых значений — от 0 до 65 535.</span><span class="sxs-lookup"><span data-stu-id="c8163-124">The range of acceptable values is 0 through 65,535.</span></span> <span data-ttu-id="c8163-125">Дополнительные сведения об изменении этого диапазона см. в документации по устройству микшера.</span><span class="sxs-lookup"><span data-stu-id="c8163-125">For information about changing this range, see the documentation for your mixer device.</span></span>                                                                                                                                                                                                                                        |
| <span data-ttu-id="c8163-126">Низким</span><span class="sxs-lookup"><span data-stu-id="c8163-126">Bass</span></span>      | <span data-ttu-id="c8163-127">Регулятор громкости басов.</span><span class="sxs-lookup"><span data-stu-id="c8163-127">Bass volume fade control.</span></span> <span data-ttu-id="c8163-128">Диапазон допустимых значений — от 0 до 65 535.</span><span class="sxs-lookup"><span data-stu-id="c8163-128">The range of acceptable values is 0 through 65,535.</span></span> <span data-ttu-id="c8163-129">Ограничения частоты басов зависят от оборудования.</span><span class="sxs-lookup"><span data-stu-id="c8163-129">The limits of the bass frequency band are hardware specific.</span></span> <span data-ttu-id="c8163-130">Сведения об ограничениях использования полос см. в документации по устройству микшера.</span><span class="sxs-lookup"><span data-stu-id="c8163-130">For information about band limits, see the documentation for your mixer device.</span></span>                                                                                                                                                                                      |
| <span data-ttu-id="c8163-131">Частот</span><span class="sxs-lookup"><span data-stu-id="c8163-131">Treble</span></span>    | <span data-ttu-id="c8163-132">Элемент управления выцветание громкости.</span><span class="sxs-lookup"><span data-stu-id="c8163-132">Treble volume fade control.</span></span> <span data-ttu-id="c8163-133">Диапазон допустимых значений — от 0 до 65 535.</span><span class="sxs-lookup"><span data-stu-id="c8163-133">The range of acceptable values is 0 through 65,535.</span></span> <span data-ttu-id="c8163-134">Ограничения частоты высоких частот зависят от оборудования.</span><span class="sxs-lookup"><span data-stu-id="c8163-134">The limits of the treble frequency band are hardware specific.</span></span> <span data-ttu-id="c8163-135">Дополнительные сведения об ограничениях диапазонов см. в документации по устройству микшера.</span><span class="sxs-lookup"><span data-stu-id="c8163-135">For information about the band limits, see the documentation for your mixer device.</span></span>                                                                                                                                                                              |
| <span data-ttu-id="c8163-136">Equalizer</span><span class="sxs-lookup"><span data-stu-id="c8163-136">Equalizer</span></span> | <span data-ttu-id="c8163-137">Элемент управления "графический эквалайзер".</span><span class="sxs-lookup"><span data-stu-id="c8163-137">Graphic equalizer control.</span></span> <span data-ttu-id="c8163-138">Диапазон допустимых значений для одной полосы эквалайзера — от 0 до 65 535.</span><span class="sxs-lookup"><span data-stu-id="c8163-138">The range of acceptable values for one band of the equalizer is 0 through 65,535.</span></span> <span data-ttu-id="c8163-139">Число делений эквалайзера и их ограничений зависит от оборудования.</span><span class="sxs-lookup"><span data-stu-id="c8163-139">The number of equalizer bands and their limits are hardware specific.</span></span> <span data-ttu-id="c8163-140">Сведения о эквалайзере см. в документации по устройству микшера.</span><span class="sxs-lookup"><span data-stu-id="c8163-140">For information about the equalizer, see the documentation for your mixer device.</span></span> <span data-ttu-id="c8163-141">Структуру [**миксерконтролдетаилс \_ листтекст**](/previous-versions//dd757296(v=vs.85)) можно использовать для получения текстовых меток эквалайзера.</span><span class="sxs-lookup"><span data-stu-id="c8163-141">You can use the [**MIXERCONTROLDETAILS\_LISTTEXT**](/previous-versions//dd757296(v=vs.85)) structure to retrieve text labels for the equalizer.</span></span> |



 

 

 