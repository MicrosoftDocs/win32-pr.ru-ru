---
title: Атрибуты внешнего события
description: Атрибуты внешнего события
ms.assetid: 56cd2701-53b3-4456-8fcd-d65f8a6aefd7
keywords:
- Обложки проигрывателя Windows Media, атрибуты событий окружения
- обложки, атрибуты событий окружения
- Справочник по обложкам, атрибутам событий окружения
- атрибуты внешнего события
- атрибуты, событие окружения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a40522a741509e56d2e4c9201c305126067a0fe3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774270"
---
# <a name="ambient-event-attributes"></a><span data-ttu-id="b24cc-108">Атрибуты внешнего события</span><span class="sxs-lookup"><span data-stu-id="b24cc-108">Ambient Event Attributes</span></span>

<span data-ttu-id="b24cc-109">Следующие атрибуты являются общими для всех событий обложки.</span><span class="sxs-lookup"><span data-stu-id="b24cc-109">The following attributes are common to all skin events.</span></span> <span data-ttu-id="b24cc-110">Доступ к ним осуществляется с помощью ключевого слова **event** в обработчике событий для элемента.</span><span class="sxs-lookup"><span data-stu-id="b24cc-110">They are accessed with the **event** keyword within an event handler for the element.</span></span>



| <span data-ttu-id="b24cc-111">attribute</span><span class="sxs-lookup"><span data-stu-id="b24cc-111">Attribute</span></span>                              | <span data-ttu-id="b24cc-112">Описание</span><span class="sxs-lookup"><span data-stu-id="b24cc-112">Description</span></span>                                                                                                  |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b24cc-113">алткэй</span><span class="sxs-lookup"><span data-stu-id="b24cc-113">altKey</span></span>](event-altkey.md)             | <span data-ttu-id="b24cc-114">Получает значение, указывающее, была ли нажата клавиша ALT при возникновении события.</span><span class="sxs-lookup"><span data-stu-id="b24cc-114">Retrieves a value indicating whether the ALT key was down when the event occurred.</span></span>                           |
| [<span data-ttu-id="b24cc-115">переключатель</span><span class="sxs-lookup"><span data-stu-id="b24cc-115">button</span></span>](event-button.md)             | <span data-ttu-id="b24cc-116">Извлекает значение, указывающее, какая кнопка мыши была нажата при возникновении события.</span><span class="sxs-lookup"><span data-stu-id="b24cc-116">Retrieves a value indicating which mouse buttons were down when the event occurred.</span></span>                          |
| [<span data-ttu-id="b24cc-117">клиенткс</span><span class="sxs-lookup"><span data-stu-id="b24cc-117">clientX</span></span>](event-clientx.md)           | <span data-ttu-id="b24cc-118">Извлекает координату по оси x указателя мыши относительно области клиента окна приложения.</span><span class="sxs-lookup"><span data-stu-id="b24cc-118">Retrieves the x-coordinate of the mouse pointer with respect to the client region of the application window.</span></span> |
| [<span data-ttu-id="b24cc-119">Клиентская</span><span class="sxs-lookup"><span data-stu-id="b24cc-119">clientY</span></span>](event-clienty.md)           | <span data-ttu-id="b24cc-120">Получает координату y указателя мыши относительно клиентской области окна приложения.</span><span class="sxs-lookup"><span data-stu-id="b24cc-120">Retrieves the y-coordinate of the mouse pointer with respect to the client region of the application window.</span></span> |
| [<span data-ttu-id="b24cc-121">ктрлкэй</span><span class="sxs-lookup"><span data-stu-id="b24cc-121">ctrlKey</span></span>](event-ctrlkey.md)           | <span data-ttu-id="b24cc-122">Получает значение, указывающее, была ли нажата клавиша CTRL при возникновении события.</span><span class="sxs-lookup"><span data-stu-id="b24cc-122">Retrieves a value indicating whether the CTRL key was down when the event occurred.</span></span>                          |
| [<span data-ttu-id="b24cc-123">фромелемент</span><span class="sxs-lookup"><span data-stu-id="b24cc-123">fromElement</span></span>](event-fromelement.md)   | <span data-ttu-id="b24cc-124">Извлекает элемент, полученный от события.</span><span class="sxs-lookup"><span data-stu-id="b24cc-124">Retrieves the element the event came from.</span></span>                                                                   |
| [<span data-ttu-id="b24cc-125">keyCode</span><span class="sxs-lookup"><span data-stu-id="b24cc-125">keyCode</span></span>](event-keycode.md)           | <span data-ttu-id="b24cc-126">Извлекает код ключа ASCII, если при возникновении события была нажата клавиша.</span><span class="sxs-lookup"><span data-stu-id="b24cc-126">Retrieves the ASCII key code if a key was pressed when the event occurred.</span></span>                                   |
| [<span data-ttu-id="b24cc-127">оффсеткс</span><span class="sxs-lookup"><span data-stu-id="b24cc-127">offsetX</span></span>](event-offsetx.md)           | <span data-ttu-id="b24cc-128">Извлекает координату по оси x указателя мыши относительно элемента, вызывающего событие.</span><span class="sxs-lookup"><span data-stu-id="b24cc-128">Retrieves the x-coordinate of the mouse pointer with respect to the element firing the event.</span></span>                |
| [<span data-ttu-id="b24cc-129">смещение</span><span class="sxs-lookup"><span data-stu-id="b24cc-129">offsetY</span></span>](event-offsety.md)           | <span data-ttu-id="b24cc-130">Получает координату y указателя мыши относительно элемента, вызывающего событие.</span><span class="sxs-lookup"><span data-stu-id="b24cc-130">Retrieves the y-coordinate of the mouse pointer with respect to the element firing the event.</span></span>                |
| [<span data-ttu-id="b24cc-131">скринхеигхт</span><span class="sxs-lookup"><span data-stu-id="b24cc-131">screenHeight</span></span>](event-screenheight.md) | <span data-ttu-id="b24cc-132">Получает высоту доступного размера экрана в пикселях.</span><span class="sxs-lookup"><span data-stu-id="b24cc-132">Retrieves the height of the available screen size in pixels.</span></span>                                                 |
| [<span data-ttu-id="b24cc-133">скринвидс</span><span class="sxs-lookup"><span data-stu-id="b24cc-133">screenWidth</span></span>](event-screenwidth.md)   | <span data-ttu-id="b24cc-134">Получает ширину доступного размера экрана в пикселях.</span><span class="sxs-lookup"><span data-stu-id="b24cc-134">Retrieves the width of the available screen size in pixels.</span></span>                                                  |
| [<span data-ttu-id="b24cc-135">скринкс</span><span class="sxs-lookup"><span data-stu-id="b24cc-135">screenX</span></span>](event-screenx.md)           | <span data-ttu-id="b24cc-136">Получает абсолютную координату по оси x указателя мыши относительно экрана.</span><span class="sxs-lookup"><span data-stu-id="b24cc-136">Retrieves the absolute x-coordinate of the mouse pointer with respect to the screen.</span></span>                         |
| [<span data-ttu-id="b24cc-137">экран</span><span class="sxs-lookup"><span data-stu-id="b24cc-137">screenY</span></span>](event-screeny.md)           | <span data-ttu-id="b24cc-138">Получает абсолютную координату y указателя мыши относительно экрана.</span><span class="sxs-lookup"><span data-stu-id="b24cc-138">Retrieves the absolute y-coordinate of the mouse pointer with respect to the screen.</span></span>                         |
| [<span data-ttu-id="b24cc-139">шифткэй</span><span class="sxs-lookup"><span data-stu-id="b24cc-139">shiftKey</span></span>](event-shiftkey.md)         | <span data-ttu-id="b24cc-140">Получает значение, указывающее, была ли нажата клавиша SHIFT при возникновении события.</span><span class="sxs-lookup"><span data-stu-id="b24cc-140">Retrieves a value indicating whether the SHIFT key was down when the event occurred.</span></span>                         |
| [<span data-ttu-id="b24cc-141">срцелемент</span><span class="sxs-lookup"><span data-stu-id="b24cc-141">srcElement</span></span>](event-srcelement.md)     | <span data-ttu-id="b24cc-142">Извлекает элемент, который вызвал событие.</span><span class="sxs-lookup"><span data-stu-id="b24cc-142">Retrieves the element that fired the event.</span></span>                                                                  |
| [<span data-ttu-id="b24cc-143">тоелемент</span><span class="sxs-lookup"><span data-stu-id="b24cc-143">toElement</span></span>](event-toelement.md)       | <span data-ttu-id="b24cc-144">Извлекает элемент, в который переместился фокус клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="b24cc-144">Retrieves the element the keyboard focus moved to.</span></span>                                                           |
| [<span data-ttu-id="b24cc-145">x</span><span class="sxs-lookup"><span data-stu-id="b24cc-145">x</span></span>](event-x.md)                       | <span data-ttu-id="b24cc-146">Извлекает координату указателя мыши по оси x в соответствии с окном приложения.</span><span class="sxs-lookup"><span data-stu-id="b24cc-146">Retrieves the x-coordinate of the mouse pointer with respect to the application window.</span></span>                      |
| [<span data-ttu-id="b24cc-147">y</span><span class="sxs-lookup"><span data-stu-id="b24cc-147">y</span></span>](event-y.md)                       | <span data-ttu-id="b24cc-148">Получает координату y указателя мыши относительно окна приложения.</span><span class="sxs-lookup"><span data-stu-id="b24cc-148">Retrieves the y-coordinate of the mouse pointer with respect to the application window.</span></span>                      |



 

## <a name="related-topics"></a><span data-ttu-id="b24cc-149">См. также</span><span class="sxs-lookup"><span data-stu-id="b24cc-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b24cc-150">**Справочник по программированию для обложки**</span><span class="sxs-lookup"><span data-stu-id="b24cc-150">**Skin Programming Reference**</span></span>](skin-programming-reference.md)
</dt> </dl>

 

 




