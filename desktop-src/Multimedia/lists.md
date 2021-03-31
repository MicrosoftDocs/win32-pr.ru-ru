---
title: Списки
description: Списки
ms.assetid: 89fb4457-307a-4693-94d4-57f57c422d1e
keywords:
- аудио миксерс, элементы управления
- аудио миксерс, списки
- миксерс, элементы управления
- миксерс, списки
- Список - элементы управления
- Структура MIXERCONTROLDETAILS_BOOLEAN
- Структура MIXERCONTROLDETAILS_LISTTEXT
- элемент управления с одним выделением
- элемент управления с множественным выделением
- элемент управления микшера
- мультиплексор (МУЛЬТИПЛЕКСОР)
- МУЛЬТИПЛЕКСОР (мультиплексор)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d475816d7090ee241a1508cc054b12742c4ab27
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337001"
---
# <a name="lists"></a><span data-ttu-id="ac6b0-115">Списки</span><span class="sxs-lookup"><span data-stu-id="ac6b0-115">Lists</span></span>

<span data-ttu-id="ac6b0-116">Элементы управления "список" предоставляют одновыборные или множественные состояния для сложных звуковых линий.</span><span class="sxs-lookup"><span data-stu-id="ac6b0-116">The list controls provide single-select or multiple-select states for complex audio lines.</span></span> <span data-ttu-id="ac6b0-117">Эти элементы управления используют [**\_ логическую структуру миксерконтролдетаилс**](/previous-versions//dd757295(v=vs.85)) для извлечения и установки свойств элементов управления.</span><span class="sxs-lookup"><span data-stu-id="ac6b0-117">These controls use the [**MIXERCONTROLDETAILS\_BOOLEAN**](/previous-versions//dd757295(v=vs.85)) structure to retrieve and set control properties.</span></span> <span data-ttu-id="ac6b0-118">Структура [**миксерконтролдетаилс \_ листтекст**](/previous-versions//dd757296(v=vs.85)) также используется для получения всех текстовых описаний элемента управления с несколькими элементами.</span><span class="sxs-lookup"><span data-stu-id="ac6b0-118">The [**MIXERCONTROLDETAILS\_LISTTEXT**](/previous-versions//dd757296(v=vs.85)) structure is also used to retrieve all text descriptions of a multiple-item control.</span></span> <span data-ttu-id="ac6b0-119">В следующей таблице описаны типы элементов управления "список".</span><span class="sxs-lookup"><span data-stu-id="ac6b0-119">The following table describes the types of list controls.</span></span>



| <span data-ttu-id="ac6b0-120">Control</span><span class="sxs-lookup"><span data-stu-id="ac6b0-120">Control</span></span>           | <span data-ttu-id="ac6b0-121">Описание</span><span class="sxs-lookup"><span data-stu-id="ac6b0-121">Description</span></span>                                                                                                                                                                                                                                                                      |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac6b0-122">Один выбор</span><span class="sxs-lookup"><span data-stu-id="ac6b0-122">Single-select</span></span>     | <span data-ttu-id="ac6b0-123">Разрешает выбор элемента управления только по одному элементу за раз.</span><span class="sxs-lookup"><span data-stu-id="ac6b0-123">Restricts the control selection to one item at a time.</span></span> <span data-ttu-id="ac6b0-124">В отличие от элемента управления мультиплексирования, этот элемент управления можно использовать для управления более чем строками исходного кода.</span><span class="sxs-lookup"><span data-stu-id="ac6b0-124">Unlike the multiplexer control, this control can be used to control more than audio source lines.</span></span> <span data-ttu-id="ac6b0-125">Например, этот элемент управления можно использовать для выбора фильтра с низким уровнем передачи из списка фильтров, поддерживаемых устройством микшера.</span><span class="sxs-lookup"><span data-stu-id="ac6b0-125">For example, you could use this control to select a low-pass filter from a list of filters supported by a mixer device.</span></span> |
| <span data-ttu-id="ac6b0-126">Мультиплексор (МУЛЬТИПЛЕКСОР)</span><span class="sxs-lookup"><span data-stu-id="ac6b0-126">Multiplexer (MUX)</span></span> | <span data-ttu-id="ac6b0-127">Ограничит выбор строки до одной строки исходного кода за раз.</span><span class="sxs-lookup"><span data-stu-id="ac6b0-127">Restricts the line selection to one source line at a time.</span></span>                                                                                                                                                                                                                       |
| <span data-ttu-id="ac6b0-128">Множественный выбор</span><span class="sxs-lookup"><span data-stu-id="ac6b0-128">Multiple-select</span></span>   | <span data-ttu-id="ac6b0-129">Позволяет пользователю выбрать несколько элементов из списка одновременно.</span><span class="sxs-lookup"><span data-stu-id="ac6b0-129">Allows the user to select multiple items from a list simultaneously.</span></span> <span data-ttu-id="ac6b0-130">В отличие от элемента управления микшера, элемент управления множественного выбора можно использовать для управления более чем строками исходного кода.</span><span class="sxs-lookup"><span data-stu-id="ac6b0-130">Unlike the mixer control, the multiple-select control can be used to control more than audio source lines.</span></span>                                                                                                  |
| <span data-ttu-id="ac6b0-131">Громк</span><span class="sxs-lookup"><span data-stu-id="ac6b0-131">Mixer</span></span>             | <span data-ttu-id="ac6b0-132">Позволяет пользователю выбирать исходные строки из списка одновременно.</span><span class="sxs-lookup"><span data-stu-id="ac6b0-132">Allows the user to select source lines from a list simultaneously.</span></span>                                                                                                                                                                                                               |



 

 

 