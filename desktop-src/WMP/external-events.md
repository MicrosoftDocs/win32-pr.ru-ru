---
title: Внешние события
description: Внешние события
ms.assetid: d3fd8af6-8d7e-43b8-88fd-a59cf0cef609
keywords:
- Обложки проигрывателя Windows Media, внешние события
- обложки, внешние события
- события, внешние
- Написание кода для обложек, внешних событий
- внешние события
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfa09a01b709f0da51d09fc2bec70cba0a1b07d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105691354"
---
# <a name="external-events"></a><span data-ttu-id="e0f1e-108">Внешние события</span><span class="sxs-lookup"><span data-stu-id="e0f1e-108">External Events</span></span>

<span data-ttu-id="e0f1e-109">Когда пользователь нажимает кнопку или нажимает клавишу, вы можете реагировать на свои входные данные с помощью обработчиков событий.</span><span class="sxs-lookup"><span data-stu-id="e0f1e-109">When users click a button or press a key, you can respond to their input with event handlers.</span></span> <span data-ttu-id="e0f1e-110">Обработчик событий — это раздел кода, который выполняется при каждом срабатывании события.</span><span class="sxs-lookup"><span data-stu-id="e0f1e-110">An event handler is a section of code that runs whenever the event is triggered.</span></span>

<span data-ttu-id="e0f1e-111">Элементы обложки поддерживают следующие события:</span><span class="sxs-lookup"><span data-stu-id="e0f1e-111">The following events are supported by skin elements:</span></span>

-   <span data-ttu-id="e0f1e-112">**загрузка**</span><span class="sxs-lookup"><span data-stu-id="e0f1e-112">**load**</span></span>
-   <span data-ttu-id="e0f1e-113">**close**</span><span class="sxs-lookup"><span data-stu-id="e0f1e-113">**close**</span></span>
-   <span data-ttu-id="e0f1e-114">**изменить размер**</span><span class="sxs-lookup"><span data-stu-id="e0f1e-114">**resize**</span></span>
-   <span data-ttu-id="e0f1e-115">**активности**</span><span class="sxs-lookup"><span data-stu-id="e0f1e-115">**timer**</span></span>
-   <span data-ttu-id="e0f1e-116">**Откройте**</span><span class="sxs-lookup"><span data-stu-id="e0f1e-116">**click**</span></span>
-   <span data-ttu-id="e0f1e-117">**кнопки**</span><span class="sxs-lookup"><span data-stu-id="e0f1e-117">**dblclick**</span></span>
-   <span data-ttu-id="e0f1e-118">**error**</span><span class="sxs-lookup"><span data-stu-id="e0f1e-118">**error**</span></span>
-   <span data-ttu-id="e0f1e-119">**вниз**</span><span class="sxs-lookup"><span data-stu-id="e0f1e-119">**mousedown**</span></span>
-   <span data-ttu-id="e0f1e-120">**Кнопка**</span><span class="sxs-lookup"><span data-stu-id="e0f1e-120">**mouseup**</span></span>
-   <span data-ttu-id="e0f1e-121">**событие**</span><span class="sxs-lookup"><span data-stu-id="e0f1e-121">**mousemove**</span></span>
-   <span data-ttu-id="e0f1e-122">**MouseOver**</span><span class="sxs-lookup"><span data-stu-id="e0f1e-122">**mouseover**</span></span>
-   <span data-ttu-id="e0f1e-123">**мышь**</span><span class="sxs-lookup"><span data-stu-id="e0f1e-123">**mouseout**</span></span>
-   <span data-ttu-id="e0f1e-124">**бытии**</span><span class="sxs-lookup"><span data-stu-id="e0f1e-124">**keypress**</span></span>
-   <span data-ttu-id="e0f1e-125">**клавиш**</span><span class="sxs-lookup"><span data-stu-id="e0f1e-125">**keydown**</span></span>
-   <span data-ttu-id="e0f1e-126">**KeyUp**</span><span class="sxs-lookup"><span data-stu-id="e0f1e-126">**keyup**</span></span>

<span data-ttu-id="e0f1e-127">Дополнительные сведения о конкретных событиях см. в [справочнике по программированию обложки](skin-programming-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="e0f1e-127">See the [Skin Programming Reference](skin-programming-reference.md) for more details about specific events.</span></span>

<span data-ttu-id="e0f1e-128">Типичный обработчик внешних событий будет наименовать событие и определить код, который будет выполняться.</span><span class="sxs-lookup"><span data-stu-id="e0f1e-128">A typical external event handler would name the event and define the code that will run.</span></span> <span data-ttu-id="e0f1e-129">Например, если требуется создать код для запуска проигрывателя Windows Media при нажатии пользователем кнопки, в код кнопки следует поместить следующую строку.</span><span class="sxs-lookup"><span data-stu-id="e0f1e-129">For example, if you want to create code to start Windows Media Player when the user clicks on a button, you would put the following line in your button code.</span></span>


```C++
onclick = "JScript: player.URL = 'https://proseware.com/laure.wma' ; "

```



<span data-ttu-id="e0f1e-130">Будет воспроизведен файл с именем Лауре. WMA.</span><span class="sxs-lookup"><span data-stu-id="e0f1e-130">This will play the file named laure.wma.</span></span> <span data-ttu-id="e0f1e-131">Обратите внимание, что вы добавляете слово «on» к конкретным событиям.</span><span class="sxs-lookup"><span data-stu-id="e0f1e-131">Note that you add the word "on" to specific events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e0f1e-132">См. также</span><span class="sxs-lookup"><span data-stu-id="e0f1e-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0f1e-133">**Обработка событий**</span><span class="sxs-lookup"><span data-stu-id="e0f1e-133">**Handling Events**</span></span>](handling-events.md)
</dt> </dl>

 

 




