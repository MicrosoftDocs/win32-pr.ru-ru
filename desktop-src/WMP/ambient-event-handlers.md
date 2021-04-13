---
title: Обработчики событий окружения
description: Обработчики событий окружения
ms.assetid: ec806b92-a66d-499d-9bb3-cea7e82676bb
keywords:
- Обложки проигрывателя Windows Media, обработчики событий окружения
- обложки, обработчики событий окружения
- Справочник по обложкам, обработчикам событий окружения
- обработчики событий окружения
- события, окружение
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dc05cf90956464afbb030f3cd5dc4af194b0da2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410727"
---
# <a name="ambient-event-handlers"></a><span data-ttu-id="b5e86-108">Обработчики событий окружения</span><span class="sxs-lookup"><span data-stu-id="b5e86-108">Ambient Event Handlers</span></span>

<span data-ttu-id="b5e86-109">Для большинства элементов обложки можно реализовать следующие обработчики событий.</span><span class="sxs-lookup"><span data-stu-id="b5e86-109">The following event handlers can be implemented for most skin elements.</span></span> <span data-ttu-id="b5e86-110">Атрибуты внешнего события, доступ к которым осуществляется с помощью ключевого слова **события** , можно использовать в обработчике событий для определения состояния клавиатуры и мыши во время события.</span><span class="sxs-lookup"><span data-stu-id="b5e86-110">The ambient event attributes accessed with the **event** keyword can be used within an event handler to determine the state of the keyboard and mouse at the time of the event.</span></span>



| <span data-ttu-id="b5e86-111">Обработчик событий</span><span class="sxs-lookup"><span data-stu-id="b5e86-111">Event handler</span></span>                                   | <span data-ttu-id="b5e86-112">Описание</span><span class="sxs-lookup"><span data-stu-id="b5e86-112">Description</span></span>                                                                                                                                                                                                                   |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b5e86-113">*атрибут* \_ OnChange</span><span class="sxs-lookup"><span data-stu-id="b5e86-113">*attribute*\_onchange</span></span>](attribute-onchange.md) | <span data-ttu-id="b5e86-114">Когда атрибут обложки изменяет значение, возникает событие, которое может быть обработано обработчиком событий.</span><span class="sxs-lookup"><span data-stu-id="b5e86-114">When a skin attribute changes value, an event occurs that can be handled by an event handler.</span></span> <span data-ttu-id="b5e86-115">Имя обработчика событий — это имя атрибута, за которым следует символ подчеркивания и "OnChange", например "значение \_ onChange".</span><span class="sxs-lookup"><span data-stu-id="b5e86-115">The name of the event handler is the name of the attribute followed by an underscore and "onchange", such as "value\_onchange".</span></span> |
| [<span data-ttu-id="b5e86-116">onblurие</span><span class="sxs-lookup"><span data-stu-id="b5e86-116">onblur</span></span>](onblur.md)                            | <span data-ttu-id="b5e86-117">Обрабатывает событие, происходящее при потере элементом фокуса клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="b5e86-117">Handles an event that occurs when the element loses the keyboard focus.</span></span>                                                                                                                                                       |
| [<span data-ttu-id="b5e86-118">OnClick</span><span class="sxs-lookup"><span data-stu-id="b5e86-118">onclick</span></span>](onclick.md)                          | <span data-ttu-id="b5e86-119">Обрабатывает событие, возникающее, когда пользователь щелкает элемент.</span><span class="sxs-lookup"><span data-stu-id="b5e86-119">Handles an event that occurs when the user clicks the element.</span></span>                                                                                                                                                                |
| [<span data-ttu-id="b5e86-120">ондблкликк</span><span class="sxs-lookup"><span data-stu-id="b5e86-120">ondblclick</span></span>](ondblclick.md)                    | <span data-ttu-id="b5e86-121">Обрабатывает событие, возникающее при двойном щелчке элемента пользователем.</span><span class="sxs-lookup"><span data-stu-id="b5e86-121">Handles an event that occurs when the user double-clicks the element.</span></span>                                                                                                                                                         |
| [<span data-ttu-id="b5e86-122">онендалфабленд</span><span class="sxs-lookup"><span data-stu-id="b5e86-122">onendalphablend</span></span>](onendalphablend.md)          | <span data-ttu-id="b5e86-123">Обрабатывает событие, возникающее, когда элемент завершает операцию **алфаблендто** .</span><span class="sxs-lookup"><span data-stu-id="b5e86-123">Handles an event that occurs when an element completes an **alphaBlendTo** operation.</span></span>                                                                                                                                         |
| [<span data-ttu-id="b5e86-124">онендмове</span><span class="sxs-lookup"><span data-stu-id="b5e86-124">onendmove</span></span>](onendmove.md)                      | <span data-ttu-id="b5e86-125">Обрабатывает событие, возникающее, когда элемент завершает операцию **MoveTo** .</span><span class="sxs-lookup"><span data-stu-id="b5e86-125">Handles an event that occurs when an element completes a **moveTo** operation.</span></span>                                                                                                                                                |
| [<span data-ttu-id="b5e86-126">onfocus</span><span class="sxs-lookup"><span data-stu-id="b5e86-126">onfocus</span></span>](onfocus.md)                          | <span data-ttu-id="b5e86-127">Обрабатывает событие, происходящее при получении элементом фокуса клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="b5e86-127">Handles an event that occurs when the element receives the keyboard focus.</span></span>                                                                                                                                                    |
| [<span data-ttu-id="b5e86-128">KeyDown</span><span class="sxs-lookup"><span data-stu-id="b5e86-128">onkeydown</span></span>](onkeydown.md)                      | <span data-ttu-id="b5e86-129">Обрабатывает событие, возникающее при нажатии клавиши.</span><span class="sxs-lookup"><span data-stu-id="b5e86-129">Handles an event that occurs when a key is pressed.</span></span>                                                                                                                                                                           |
| [<span data-ttu-id="b5e86-130">OnKeyPress</span><span class="sxs-lookup"><span data-stu-id="b5e86-130">onkeypress</span></span>](onkeypress.md)                    | <span data-ttu-id="b5e86-131">Обрабатывает событие, возникающее при нажатии пользователем буквенно-цифрового ключа.</span><span class="sxs-lookup"><span data-stu-id="b5e86-131">Handles an event that occurs when the user presses an alphanumeric key.</span></span>                                                                                                                                                       |
| [<span data-ttu-id="b5e86-132">онкэйуп</span><span class="sxs-lookup"><span data-stu-id="b5e86-132">onkeyup</span></span>](onkeyup.md)                          | <span data-ttu-id="b5e86-133">Обрабатывает событие, возникающее при отпускании клавиши.</span><span class="sxs-lookup"><span data-stu-id="b5e86-133">Handles an event that occurs when a key is released.</span></span>                                                                                                                                                                          |
| [<span data-ttu-id="b5e86-134">OnMouseDown</span><span class="sxs-lookup"><span data-stu-id="b5e86-134">onmousedown</span></span>](onmousedown.md)                  | <span data-ttu-id="b5e86-135">Обрабатывает событие, происходящее при нажатии пользователем кнопки мыши.</span><span class="sxs-lookup"><span data-stu-id="b5e86-135">Handles an event that occurs when the user clicks a mouse button.</span></span>                                                                                                                                                             |
| [<span data-ttu-id="b5e86-136">OnMouseMove</span><span class="sxs-lookup"><span data-stu-id="b5e86-136">onmousemove</span></span>](onmousemove.md)                  | <span data-ttu-id="b5e86-137">Обрабатывает событие, возникающее, когда пользователь перемещает указатель мыши на элемент.</span><span class="sxs-lookup"><span data-stu-id="b5e86-137">Handles an event that occurs when the user moves the mouse pointer while it is over an element.</span></span>                                                                                                                               |
| [<span data-ttu-id="b5e86-138">onMouseout</span><span class="sxs-lookup"><span data-stu-id="b5e86-138">onmouseout</span></span>](onmouseout.md)                    | <span data-ttu-id="b5e86-139">Обрабатывает событие, происходящее, когда пользователь перемещает указатель мыши за пределы элемента.</span><span class="sxs-lookup"><span data-stu-id="b5e86-139">Handles an event that occurs when the user moves the pointer off the element.</span></span>                                                                                                                                                 |
| [<span data-ttu-id="b5e86-140">onmouseover</span><span class="sxs-lookup"><span data-stu-id="b5e86-140">onmouseover</span></span>](onmouseover.md)                  | <span data-ttu-id="b5e86-141">Обрабатывает событие, возникающее, когда пользователь впервые помещает указатель мыши на элемент.</span><span class="sxs-lookup"><span data-stu-id="b5e86-141">Handles an event that occurs when the user first places the pointer over the element.</span></span>                                                                                                                                         |
| [<span data-ttu-id="b5e86-142">OnMouseUp</span><span class="sxs-lookup"><span data-stu-id="b5e86-142">onmouseup</span></span>](onmouseup.md)                      | <span data-ttu-id="b5e86-143">Обрабатывает событие, возникающее, когда пользователь отпускает кнопку мыши, когда указатель находится над элементом.</span><span class="sxs-lookup"><span data-stu-id="b5e86-143">Handles an event that occurs when the user releases a mouse button while the pointer is over the element.</span></span>                                                                                                                     |
| [<span data-ttu-id="b5e86-144">онресизе</span><span class="sxs-lookup"><span data-stu-id="b5e86-144">onresize</span></span>](onresize.md)                        | <span data-ttu-id="b5e86-145">Обрабатывает событие, возникающее при изменении размера элемента управления.</span><span class="sxs-lookup"><span data-stu-id="b5e86-145">Handles an event that occurs when a control resizes.</span></span>                                                                                                                                                                          |



 

## <a name="related-topics"></a><span data-ttu-id="b5e86-146">См. также</span><span class="sxs-lookup"><span data-stu-id="b5e86-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b5e86-147">**Атрибуты внешнего события**</span><span class="sxs-lookup"><span data-stu-id="b5e86-147">**Ambient Event Attributes**</span></span>](ambient-event-attributes.md)
</dt> <dt>

[<span data-ttu-id="b5e86-148">**Справочник по программированию для обложки**</span><span class="sxs-lookup"><span data-stu-id="b5e86-148">**Skin Programming Reference**</span></span>](skin-programming-reference.md)
</dt> </dl>

 

 




