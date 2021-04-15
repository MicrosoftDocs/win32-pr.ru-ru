---
title: VIEW, элемент
description: VIEW, элемент
ms.assetid: e1dfde08-33a0-4f12-8db0-ad62e4a1d467
keywords:
- Обложки проигрывателя Windows Media, элемент VIEW
- обложки, элемент VIEW
- VIEW, элемент
- Справочник по обложкам, элементу VIEW
- элементы, представление
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07e907cced22b4d1cd498054df06ac8677a7488b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411076"
---
# <a name="view-element"></a><span data-ttu-id="9da79-108">VIEW, элемент</span><span class="sxs-lookup"><span data-stu-id="9da79-108">VIEW Element</span></span>

<span data-ttu-id="9da79-109">Элемент **View** содержит сведения о пользовательском интерфейсе обложки и использует атрибуты, методы и обработчики событий, приведенные в следующих таблицах.</span><span class="sxs-lookup"><span data-stu-id="9da79-109">The **VIEW** element contains the user interface details of a skin, and uses the attributes, methods, and event handlers shown in the following tables.</span></span>

<span data-ttu-id="9da79-110">Несколько элементов **представления** могут быть определены как дочерние элементы **темы** обложки для предоставления различных интерфейсов в различных ситуациях.</span><span class="sxs-lookup"><span data-stu-id="9da79-110">Multiple **VIEW** elements can be defined as children of the **THEME** element of a skin to provide different interfaces for different situations.</span></span> <span data-ttu-id="9da79-111">Элементы **представления** не могут быть потомками любого другого элемента и содержат все остальные элементы обложки.</span><span class="sxs-lookup"><span data-stu-id="9da79-111">**VIEW** elements cannot be specified as children of any other element, and they contain all other skin elements.</span></span> <span data-ttu-id="9da79-112">Обратите внимание, что каждое представление имеет собственную область переменной, то есть не может совместно использовать значения атрибутов с другими представлениями.</span><span class="sxs-lookup"><span data-stu-id="9da79-112">Note that each view has its own variable scope, which means it cannot share attribute values with other views.</span></span>

<span data-ttu-id="9da79-113">Глобальный атрибут **View** можно использовать для ссылки на конкретный элемент **представления** из любого места внутри него.</span><span class="sxs-lookup"><span data-stu-id="9da79-113">The **view** global attribute can be used to reference a specific **VIEW** element from anywhere within it.</span></span> <span data-ttu-id="9da79-114">Это альтернатива использованию атрибута **ID** , который должен использоваться в других элементах **представления** или в элементе **Theme** .</span><span class="sxs-lookup"><span data-stu-id="9da79-114">This is an alternative to using its **id** attribute, which must be used from within other **VIEW** elements or from within the **THEME** element.</span></span>

<span data-ttu-id="9da79-115">Элемент **View** поддерживает следующие атрибуты.</span><span class="sxs-lookup"><span data-stu-id="9da79-115">The **VIEW** element supports the following attributes.</span></span> <span data-ttu-id="9da79-116">Атрибуты, отмеченные звездочкой ( \* ), также поддерживаются элементом вложенного **представления** .</span><span class="sxs-lookup"><span data-stu-id="9da79-116">Attributes marked with an asterisk (\*) are also supported by the **SUBVIEW** element.</span></span>



| <span data-ttu-id="9da79-117">attribute</span><span class="sxs-lookup"><span data-stu-id="9da79-117">Attribute</span></span>                                                       | <span data-ttu-id="9da79-118">Описание</span><span class="sxs-lookup"><span data-stu-id="9da79-118">Description</span></span>                                                                                                             |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9da79-119">[backgroundColor](view-backgroundcolor.md)\*</span><span class="sxs-lookup"><span data-stu-id="9da79-119">[backgroundColor](view-backgroundcolor.md) \*</span></span>                  | <span data-ttu-id="9da79-120">Указывает или получает цвет фона для **представления** или **подпредставления**.</span><span class="sxs-lookup"><span data-stu-id="9da79-120">Specifies or retrieves the background color of the **VIEW** or **SUBVIEW**.</span></span>                                             |
| <span data-ttu-id="9da79-121">[backgroundImage](view-backgroundimage.md) \*</span><span class="sxs-lookup"><span data-stu-id="9da79-121">[backgroundImage](view-backgroundimage.md) \*</span></span>                  | <span data-ttu-id="9da79-122">Указывает или получает фоновое изображение **представления** или **подпредставления**.</span><span class="sxs-lookup"><span data-stu-id="9da79-122">Specifies or retrieves the background image of the **VIEW** or **SUBVIEW**.</span></span>                                             |
| [<span data-ttu-id="9da79-123">баккграундимажехуешифт</span><span class="sxs-lookup"><span data-stu-id="9da79-123">backgroundImageHueShift</span></span>](view-backgroundimagehueshift.md)     | <span data-ttu-id="9da79-124">Указывает или получает величину, на которую смещается цветовой тон фонового изображения.</span><span class="sxs-lookup"><span data-stu-id="9da79-124">Specifies or retrieves the amount by which the hue of the background image is shifted.</span></span>                                  |
| [<span data-ttu-id="9da79-125">баккграундимажесатуратион</span><span class="sxs-lookup"><span data-stu-id="9da79-125">backgroundImageSaturation</span></span>](view-backgroundimagesaturation.md) | <span data-ttu-id="9da79-126">Указывает или получает значение насыщенности фонового изображения.</span><span class="sxs-lookup"><span data-stu-id="9da79-126">Specifies or retrieves the saturation value of the background image.</span></span>                                                    |
| <span data-ttu-id="9da79-127">[баккграундтилед](view-backgroundtiled.md)\*</span><span class="sxs-lookup"><span data-stu-id="9da79-127">[backgroundTiled](view-backgroundtiled.md) \*</span></span>                  | <span data-ttu-id="9da79-128">Указывает или получает значение, указывающее, производится ли мозаичное заполнение фонового изображения **представления** или **подпредставления** .</span><span class="sxs-lookup"><span data-stu-id="9da79-128">Specifies or retrieves a value indicating whether the background image of the **VIEW** or **SUBVIEW** is tiled.</span></span>         |
| [<span data-ttu-id="9da79-129">category</span><span class="sxs-lookup"><span data-stu-id="9da79-129">category</span></span>](view-category.md)                                   | <span data-ttu-id="9da79-130">Указывает или получает категорию, для которой будет отображаться пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="9da79-130">Specifies or retrieves the category for which the user interface will appear.</span></span>                                           |
| [<span data-ttu-id="9da79-131">фокусобжектид</span><span class="sxs-lookup"><span data-stu-id="9da79-131">focusObjectID</span></span>](view-focusobjectid.md)                         | <span data-ttu-id="9da79-132">Указывает или получает значение, указывающее, какой элемент имеет фокус клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="9da79-132">Specifies or retrieves a value indicating which element has keyboard focus.</span></span>                                             |
| [<span data-ttu-id="9da79-133">maxHeight</span><span class="sxs-lookup"><span data-stu-id="9da79-133">maxHeight</span></span>](view-maxheight.md)                                 | <span data-ttu-id="9da79-134">Указывает или получает максимальную высоту **представления** при изменении размера.</span><span class="sxs-lookup"><span data-stu-id="9da79-134">Specifies or retrieves the maximum height of the **VIEW** when resizing.</span></span>                                                |
| [<span data-ttu-id="9da79-135">maxWidth</span><span class="sxs-lookup"><span data-stu-id="9da79-135">maxWidth</span></span>](view-maxwidth.md)                                   | <span data-ttu-id="9da79-136">Указывает или получает максимальную ширину **представления** при изменении размера.</span><span class="sxs-lookup"><span data-stu-id="9da79-136">Specifies or retrieves the maximum width of the **VIEW** when resizing.</span></span>                                                 |
| [<span data-ttu-id="9da79-137">minHeight</span><span class="sxs-lookup"><span data-stu-id="9da79-137">minHeight</span></span>](view-minheight.md)                                 | <span data-ttu-id="9da79-138">Указывает или получает минимальную высоту **представления** при изменении размера.</span><span class="sxs-lookup"><span data-stu-id="9da79-138">Specifies or retrieves the minimum height of the **VIEW** when resizing.</span></span>                                                |
| [<span data-ttu-id="9da79-139">minWidth</span><span class="sxs-lookup"><span data-stu-id="9da79-139">minWidth</span></span>](view-minwidth.md)                                   | <span data-ttu-id="9da79-140">Указывает или получает минимальную ширину **представления** при изменении размера.</span><span class="sxs-lookup"><span data-stu-id="9da79-140">Specifies or retrieves the minimum width of the **VIEW** when resizing.</span></span>                                                 |
| [<span data-ttu-id="9da79-141">изменяемым размером</span><span class="sxs-lookup"><span data-stu-id="9da79-141">resizable</span></span>](view-resizable.md)                                 | <span data-ttu-id="9da79-142">Указывает или получает значение, указывающее, можно ли изменить размер **представления** .</span><span class="sxs-lookup"><span data-stu-id="9da79-142">Specifies or retrieves a value indicating whether the **VIEW** can be resized.</span></span>                                          |
| [<span data-ttu-id="9da79-143">ресизебаккграундимаже</span><span class="sxs-lookup"><span data-stu-id="9da79-143">resizeBackgroundImage</span></span>](view-resizebackgroundimage.md)         | <span data-ttu-id="9da79-144">Указывает или получает значение, указывающее, можно ли изменить размер фонового изображения.</span><span class="sxs-lookup"><span data-stu-id="9da79-144">Specifies or retrieves a value indicating whether the background image can be resized.</span></span>                                  |
| [<span data-ttu-id="9da79-145">scriptFile</span><span class="sxs-lookup"><span data-stu-id="9da79-145">scriptFile</span></span>](view-scriptfile.md)                               | <span data-ttu-id="9da79-146">Указывает имена файлов сопутствующих файлов JScript.</span><span class="sxs-lookup"><span data-stu-id="9da79-146">Specifies the file names of accompanying JScript files.</span></span>                                                                 |
| [<span data-ttu-id="9da79-147">тимеринтервал</span><span class="sxs-lookup"><span data-stu-id="9da79-147">timerInterval</span></span>](view-timerinterval.md)                         | <span data-ttu-id="9da79-148">Указывает или получает интервал (в миллисекундах), в течение которого таймер запускает события в обработчик событий **OnTime** .</span><span class="sxs-lookup"><span data-stu-id="9da79-148">Specifies or retrieves the interval, in milliseconds, at which the timer fires events to the **ontimer** event handler.</span></span> |
| [<span data-ttu-id="9da79-149">title</span><span class="sxs-lookup"><span data-stu-id="9da79-149">title</span></span>](view-title.md)                                         | <span data-ttu-id="9da79-150">Указывает или получает заголовок **представления**.</span><span class="sxs-lookup"><span data-stu-id="9da79-150">Specifies or retrieves the title of the **VIEW**.</span></span> <span data-ttu-id="9da79-151">Можно задать только во время разработки.</span><span class="sxs-lookup"><span data-stu-id="9da79-151">Can only be set at design time.</span></span>                                       |
| [<span data-ttu-id="9da79-152">titleBar</span><span class="sxs-lookup"><span data-stu-id="9da79-152">titleBar</span></span>](view-titlebar.md)                                   | <span data-ttu-id="9da79-153">Указывает или получает значение, указывающее, отображается ли заголовок окна.</span><span class="sxs-lookup"><span data-stu-id="9da79-153">Specifies or retrieves a value indicating whether the window title bar is shown.</span></span>                                        |
| <span data-ttu-id="9da79-154">[транспаренциколор](view-transparencycolor.md)\*</span><span class="sxs-lookup"><span data-stu-id="9da79-154">[transparencyColor](view-transparencycolor.md) \*</span></span>              | <span data-ttu-id="9da79-155">Указывает или получает цвет прозрачности фонового изображения.</span><span class="sxs-lookup"><span data-stu-id="9da79-155">Specifies or retrieves the transparency color of the background image.</span></span>                                                  |



 

<span data-ttu-id="9da79-156">Элемент **View** поддерживает следующие методы.</span><span class="sxs-lookup"><span data-stu-id="9da79-156">The **VIEW** element supports the following methods.</span></span>



| <span data-ttu-id="9da79-157">Метод</span><span class="sxs-lookup"><span data-stu-id="9da79-157">Method</span></span>                                              | <span data-ttu-id="9da79-158">Описание</span><span class="sxs-lookup"><span data-stu-id="9da79-158">Description</span></span>                                                |
|-----------------------------------------------------|------------------------------------------------------------|
| [<span data-ttu-id="9da79-159">close</span><span class="sxs-lookup"><span data-stu-id="9da79-159">close</span></span>](view-close.md)                             | <span data-ttu-id="9da79-160">Закрывает **представление**.</span><span class="sxs-lookup"><span data-stu-id="9da79-160">Closes the **VIEW**.</span></span>                                       |
| [<span data-ttu-id="9da79-161">ни</span><span class="sxs-lookup"><span data-stu-id="9da79-161">maximize</span></span>](view-maximize.md)                       | <span data-ttu-id="9da79-162">Разворачивает **представление**.</span><span class="sxs-lookup"><span data-stu-id="9da79-162">Maximizes the **VIEW**.</span></span>                                    |
| [<span data-ttu-id="9da79-163">свести к минимуму</span><span class="sxs-lookup"><span data-stu-id="9da79-163">minimize</span></span>](view-minimize.md)                       | <span data-ttu-id="9da79-164">Свертывает **представление**.</span><span class="sxs-lookup"><span data-stu-id="9da79-164">Minimizes the **VIEW**.</span></span>                                    |
| [<span data-ttu-id="9da79-165">restore</span><span class="sxs-lookup"><span data-stu-id="9da79-165">restore</span></span>](view-restore.md)                         | <span data-ttu-id="9da79-166">Восстанавливает **представление**.</span><span class="sxs-lookup"><span data-stu-id="9da79-166">Restores the **VIEW**.</span></span>                                     |
| [<span data-ttu-id="9da79-167">ретурнтомедиацентер</span><span class="sxs-lookup"><span data-stu-id="9da79-167">returnToMediaCenter</span></span>](view-returntomediacenter.md) | <span data-ttu-id="9da79-168">Возвращает пользователя в полноэкранный режим проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="9da79-168">Returns the user to the full mode of Windows Media Player.</span></span> |
| [<span data-ttu-id="9da79-169">size</span><span class="sxs-lookup"><span data-stu-id="9da79-169">size</span></span>](view-size.md)                               | <span data-ttu-id="9da79-170">Изменяет размер **представления** на указанном крае.</span><span class="sxs-lookup"><span data-stu-id="9da79-170">Resizes the **VIEW** on a specified edge.</span></span>                  |



 

<span data-ttu-id="9da79-171">Элемент **View** может реализовывать следующие обработчики событий.</span><span class="sxs-lookup"><span data-stu-id="9da79-171">The **VIEW** element can implement the following event handlers.</span></span>



| <span data-ttu-id="9da79-172">Обработчик событий</span><span class="sxs-lookup"><span data-stu-id="9da79-172">Event handler</span></span>               | <span data-ttu-id="9da79-173">Описание</span><span class="sxs-lookup"><span data-stu-id="9da79-173">Description</span></span>                                                                |
|-----------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="9da79-174">OnClose</span><span class="sxs-lookup"><span data-stu-id="9da79-174">onclose</span></span>](view-onclose.md) | <span data-ttu-id="9da79-175">Обрабатывает событие, возникающее, когда **представление** собирается закрыться.</span><span class="sxs-lookup"><span data-stu-id="9da79-175">Handles an event that occurs when the **VIEW** is about to be closed.</span></span>      |
| [<span data-ttu-id="9da79-176">OnError</span><span class="sxs-lookup"><span data-stu-id="9da79-176">onerror</span></span>](view-onerror.md) | <span data-ttu-id="9da79-177">Обрабатывает событие ошибки, если **Settings. енаблиррордиалогс** имеет значение false.</span><span class="sxs-lookup"><span data-stu-id="9da79-177">Handles an error event if **Settings.enableErrorDialogs** is set to false.</span></span> |
| [<span data-ttu-id="9da79-178">OnLoad</span><span class="sxs-lookup"><span data-stu-id="9da79-178">onload</span></span>](view-onload.md)   | <span data-ttu-id="9da79-179">Обрабатывает событие, возникающее при первом отображении **представления** .</span><span class="sxs-lookup"><span data-stu-id="9da79-179">Handles an event that occurs when the **VIEW** is first displayed.</span></span>         |
| [<span data-ttu-id="9da79-180">время ожидания</span><span class="sxs-lookup"><span data-stu-id="9da79-180">ontimer</span></span>](view-ontimer.md) | <span data-ttu-id="9da79-181">Обрабатывает события таймера.</span><span class="sxs-lookup"><span data-stu-id="9da79-181">Handles timer events.</span></span>                                                      |



 

<span data-ttu-id="9da79-182">Элемент **View** поддерживает атрибуты окружения и может реализовывать обработчики событий окружения, за исключением случаев, когда отмечено.</span><span class="sxs-lookup"><span data-stu-id="9da79-182">The **VIEW** element supports the ambient attributes and can implement the ambient event handlers, except where noted.</span></span> <span data-ttu-id="9da79-183">Дополнительные сведения см. в разделе [атрибуты окружения](ambient-attributes.md) и [обработчики событий окружения](ambient-event-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="9da79-183">For more information, see [Ambient Attributes](ambient-attributes.md) and [Ambient Event Handlers](ambient-event-handlers.md),</span></span>

## <a name="related-topics"></a><span data-ttu-id="9da79-184">См. также</span><span class="sxs-lookup"><span data-stu-id="9da79-184">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9da79-185">**Справочник по программированию для обложки**</span><span class="sxs-lookup"><span data-stu-id="9da79-185">**Skin Programming Reference**</span></span>](skin-programming-reference.md)
</dt> </dl>

 

 




