---
title: Флажки
description: С флажком пользователи принимают решение о двух четко противоположных вариантах.
ms.assetid: 7c39987d-807b-41c1-9788-65c3d468b976
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 20cf5bc4fd13b974f87fbb33a5fea9a365f99735
ms.sourcegitcommit: 8ebcf6cd36f67f8bcf78e76ae8923d65b8995c8a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/05/2021
ms.locfileid: "111524308"
---
# <a name="check-boxes"></a><span data-ttu-id="cfffe-103">Флажки</span><span class="sxs-lookup"><span data-stu-id="cfffe-103">Check Boxes</span></span>

> [!NOTE]
> <span data-ttu-id="cfffe-104">Это руководство по проектированию было создано для Windows 7 и не Обновлено для более новых версий Windows.</span><span class="sxs-lookup"><span data-stu-id="cfffe-104">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="cfffe-105">Многие рекомендации по-прежнему применяются в принципе, но презентация и примеры не соответствуют нашим [текущим руководствам по проектированию](/windows/uwp/design/).</span><span class="sxs-lookup"><span data-stu-id="cfffe-105">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="cfffe-106">С флажком пользователи принимают решение о двух четко противоположных вариантах.</span><span class="sxs-lookup"><span data-stu-id="cfffe-106">With a check box, users make a decision between two clearly opposite choices.</span></span> <span data-ttu-id="cfffe-107">Метка флажка указывает на выбранное состояние, тогда как значение выключенного состояния должно быть однозначным, противоположным выбранному состоянию.</span><span class="sxs-lookup"><span data-stu-id="cfffe-107">The check box label indicates the selected state, whereas the meaning of the cleared state must be the unambiguous opposite of the selected state.</span></span> <span data-ttu-id="cfffe-108">Следовательно, флажки **следует использовать только для включения или отключения параметра, а также для выбора или отостановки выбора элемента.**</span><span class="sxs-lookup"><span data-stu-id="cfffe-108">Consequently, **check boxes should be used only to toggle an option on or off or to select or deselect an item.**</span></span>

![<span data-ttu-id="cfffe-109">снимок экрана с одним из четырех выбранных флажков</span><span class="sxs-lookup"><span data-stu-id="cfffe-109">screen shot of one of four check boxes selected</span></span> ](images/ctrl-check-boxes-image1.png)

<span data-ttu-id="cfffe-110">Типичная группа флажков.</span><span class="sxs-lookup"><span data-stu-id="cfffe-110">A typical group of check boxes.</span></span>

> [!Note]  
> <span data-ttu-id="cfffe-111">Рекомендации, связанные с [макетом](vis-layout.md) , представлены в отдельной статье.</span><span class="sxs-lookup"><span data-stu-id="cfffe-111">Guidelines related to [layout](vis-layout.md) are presented in a separate article.</span></span>

 

## <a name="is-this-the-right-control"></a><span data-ttu-id="cfffe-112">Выбор правильного элемента управления</span><span class="sxs-lookup"><span data-stu-id="cfffe-112">Is this the right control?</span></span>

<span data-ttu-id="cfffe-113">Чтобы определиться, ответьте на вопросы:</span><span class="sxs-lookup"><span data-stu-id="cfffe-113">To decide, consider these questions:</span></span>

-   <span data-ttu-id="cfffe-114">**Установлен ли флажок для включения или отключения параметра или выбора или отменить выбор элемента?**</span><span class="sxs-lookup"><span data-stu-id="cfffe-114">**Is the check box used to toggle an option on or off or to select or deselect an item?**</span></span> <span data-ttu-id="cfffe-115">Если нет — используйте другой элемент управления.</span><span class="sxs-lookup"><span data-stu-id="cfffe-115">If not, use another control.</span></span>
-   <span data-ttu-id="cfffe-116">**Являются ли выбранные и очищенные состояния четкими и неоднозначными противоположными?**</span><span class="sxs-lookup"><span data-stu-id="cfffe-116">**Are the selected and cleared states clear and unambiguous opposites?**</span></span> <span data-ttu-id="cfffe-117">В противном случае используйте [переключатели](ctrl-radio-buttons.md) или [раскрывающийся список](/windows/desktop/uxguide/ctrl-drop) , чтобы можно было помечать состояния независимо друг от друга.</span><span class="sxs-lookup"><span data-stu-id="cfffe-117">If not, use [radio buttons](ctrl-radio-buttons.md) or a [drop-down list](/windows/desktop/uxguide/ctrl-drop) so that you can label the states independently.</span></span>
-   <span data-ttu-id="cfffe-118">**При использовании в группе делает группу независимым выбором, из которой пользователи могут выбрать ноль или более.**</span><span class="sxs-lookup"><span data-stu-id="cfffe-118">**When used in a group, does the group comprise independent choices, from which users may choose zero or more?**</span></span> <span data-ttu-id="cfffe-119">В противном случае рекомендуется использовать элементы управления для зависимых вариантов, таких как переключатели и [представления в виде дерева флажков](ctrl-tree-views.md).</span><span class="sxs-lookup"><span data-stu-id="cfffe-119">If not, consider controls for dependent choices, such as radio buttons and [check box tree views](ctrl-tree-views.md).</span></span>
-   <span data-ttu-id="cfffe-120">**Если используется в группе, группа включает зависимые варианты выбора, из которых пользователи должны выбрать один или несколько?**</span><span class="sxs-lookup"><span data-stu-id="cfffe-120">**When used in a group, does the group comprise dependent choices, from which users must choose one or more?**</span></span> <span data-ttu-id="cfffe-121">Если это так, используйте группу флажков и обрабатывайте ошибку, если ни один из параметров не выбран.</span><span class="sxs-lookup"><span data-stu-id="cfffe-121">If so, use a group of check boxes and handle the error when none of the options are selected.</span></span>
-   <span data-ttu-id="cfffe-122">**Число параметров в группе 10 или меньше?**</span><span class="sxs-lookup"><span data-stu-id="cfffe-122">**Is the number of options in a group 10 or fewer?**</span></span> <span data-ttu-id="cfffe-123">Так как используемое пространство экрана пропорционально количеству параметров, установите число флажков не меньше 10.</span><span class="sxs-lookup"><span data-stu-id="cfffe-123">Since the screen space used is proportional to the number of options, keep the number of check boxes to 10 or fewer.</span></span> <span data-ttu-id="cfffe-124">Для более чем 10 параметров используйте [список флажков](ctrl-list-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="cfffe-124">For more than 10 options, use a [check box list](ctrl-list-boxes.md).</span></span>
-   <span data-ttu-id="cfffe-125">**Является ли переключатель лучшим вариантом?**</span><span class="sxs-lookup"><span data-stu-id="cfffe-125">**Would a radio button be a better choice?**</span></span> <span data-ttu-id="cfffe-126">Когда флажки подходят только для включения или отключения параметра, переключатели можно использовать для совершенно разных параметров.</span><span class="sxs-lookup"><span data-stu-id="cfffe-126">Where check boxes are suitable only for turning an option on or off, radio buttons can be used for completely different options.</span></span> <span data-ttu-id="cfffe-127">Если возможны оба решения:</span><span class="sxs-lookup"><span data-stu-id="cfffe-127">If both solutions are possible:</span></span>
    -   <span data-ttu-id="cfffe-128">Используйте переключатели, если значение снятого флажка не полностью очевидно.</span><span class="sxs-lookup"><span data-stu-id="cfffe-128">Use radio buttons if the meaning of the cleared check box isn't completely obvious.</span></span>

        <span data-ttu-id="cfffe-129">**Неправильно**:</span><span class="sxs-lookup"><span data-stu-id="cfffe-129">**Incorrect:**</span></span>

        ![<span data-ttu-id="cfffe-130">снимок экрана с одним флажком с меткой "Альбомная"</span><span class="sxs-lookup"><span data-stu-id="cfffe-130">screen shot of one check box labeled landscape</span></span> ](images/ctrl-check-boxes-image2.png)

        <span data-ttu-id="cfffe-131">В этом примере противоположный выбор из альбомной ориентации не является четким, поэтому этот флажок не подходит.</span><span class="sxs-lookup"><span data-stu-id="cfffe-131">In this example, the opposite choice from Landscape isn't clear, so the check box isn't a good choice.</span></span>

        <span data-ttu-id="cfffe-132">**Правильно:**</span><span class="sxs-lookup"><span data-stu-id="cfffe-132">**Correct:**</span></span>

        ![<span data-ttu-id="cfffe-133">снимок экрана двух переключателей</span><span class="sxs-lookup"><span data-stu-id="cfffe-133">screen shot of two radio buttons</span></span> ](images/ctrl-check-boxes-image3.png)

        <span data-ttu-id="cfffe-134">В этом примере варианты выбора не противоположны, поэтому переключатели являются лучшим выбором.</span><span class="sxs-lookup"><span data-stu-id="cfffe-134">In this example, the choices are not opposites so radio buttons are the better choice.</span></span>

    -   <span data-ttu-id="cfffe-135">Используйте переключатели на страницах мастера, чтобы сделать их ясными, даже если флажок в противном случае приемлем.</span><span class="sxs-lookup"><span data-stu-id="cfffe-135">Use radio buttons on wizard pages to make the alternatives clear, even if a check box is otherwise acceptable.</span></span>
    -   <span data-ttu-id="cfffe-136">Используйте переключатели, если у вас достаточно места на экране, и параметры достаточно важны, чтобы быть хорошим использованием этого пространства экрана.</span><span class="sxs-lookup"><span data-stu-id="cfffe-136">Use radio buttons if you have enough screen space and the options are important enough to be a good use of that screen space.</span></span> <span data-ttu-id="cfffe-137">В противном случае используйте флажок или раскрывающийся список.</span><span class="sxs-lookup"><span data-stu-id="cfffe-137">Otherwise, use a check box or a drop-down list.</span></span>

        <span data-ttu-id="cfffe-138">**Неправильно**:</span><span class="sxs-lookup"><span data-stu-id="cfffe-138">**Incorrect:**</span></span>

        ![<span data-ttu-id="cfffe-139">снимок экрана "показывать и не показывать кнопки соотношения"</span><span class="sxs-lookup"><span data-stu-id="cfffe-139">screen shot of show and don't show ratio buttons</span></span> ](images/ctrl-check-boxes-image4.png)

        <span data-ttu-id="cfffe-140">В этом примере параметры не имеют достаточного значения для использования переключателей.</span><span class="sxs-lookup"><span data-stu-id="cfffe-140">In this example, the options aren't important enough to use radio buttons.</span></span>

        <span data-ttu-id="cfffe-141">**Правильно:**</span><span class="sxs-lookup"><span data-stu-id="cfffe-141">**Correct:**</span></span>

        ![<span data-ttu-id="cfffe-142">снимок экрана с флажком "не показывать сообщение"</span><span class="sxs-lookup"><span data-stu-id="cfffe-142">screen shot of check box with don't show message</span></span> ](images/ctrl-check-boxes-image5.png)

        <span data-ttu-id="cfffe-143">В этом примере флажок — это эффективное использование пространства экрана для этого варианта периферийного устройства.</span><span class="sxs-lookup"><span data-stu-id="cfffe-143">In this example, a check box is an efficient use of screen space for this peripheral option.</span></span>

-   <span data-ttu-id="cfffe-144">Установите флажок, если в окне имеются другие флажки.</span><span class="sxs-lookup"><span data-stu-id="cfffe-144">Use a check box if there other check boxes on the window.</span></span>
-   <span data-ttu-id="cfffe-145">**Параметр представляет параметр программы, а не данные?**</span><span class="sxs-lookup"><span data-stu-id="cfffe-145">**Does the option present a program option, rather than data?**</span></span> <span data-ttu-id="cfffe-146">Значения параметра не должны основываться на контексте или других данных.</span><span class="sxs-lookup"><span data-stu-id="cfffe-146">The option's values shouldn't be based on context or other data.</span></span> <span data-ttu-id="cfffe-147">Для данных используйте список флажков или [список с множественным выбором](ctrl-list-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="cfffe-147">For data, use a check box list or [multiple-selection list](ctrl-list-boxes.md).</span></span>

## <a name="usage-patterns"></a><span data-ttu-id="cfffe-148">Варианты использования</span><span class="sxs-lookup"><span data-stu-id="cfffe-148">Usage patterns</span></span>

<span data-ttu-id="cfffe-149">Флажки имеют несколько шаблонов использования:</span><span class="sxs-lookup"><span data-stu-id="cfffe-149">Check boxes have several usage patterns:</span></span>



|    <span data-ttu-id="cfffe-150">Использование</span><span class="sxs-lookup"><span data-stu-id="cfffe-150">Usage</span></span>                                                                          |         <span data-ttu-id="cfffe-151">Пример</span><span class="sxs-lookup"><span data-stu-id="cfffe-151">Example</span></span>                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cfffe-152">**Отдельный вариант** Для выбора отдельного варианта используется один флажок.</span><span class="sxs-lookup"><span data-stu-id="cfffe-152">**An individual choice** A single check box is used to select an individual choice.</span></span> <br/>                                                                                                             | ![<span data-ttu-id="cfffe-153">снимок экрана с одним флажком с меткой "напомнить мне"</span><span class="sxs-lookup"><span data-stu-id="cfffe-153">screen shot of one check box with remind me label</span></span> ](images/ctrl-check-boxes-image6.png)<br/> <span data-ttu-id="cfffe-154">Для отдельного выбора используется один флажок.</span><span class="sxs-lookup"><span data-stu-id="cfffe-154">A single check box is used for an individual choice.</span></span><br/>                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="cfffe-155">**Независимые варианты (ноль или более)** Группа флажков используется для выбора набора из нуля или более вариантов.</span><span class="sxs-lookup"><span data-stu-id="cfffe-155">**Independent choices (zero or more)** A group of check boxes is used to select from a set of zero or more choices.</span></span><br/>                                                                              | <span data-ttu-id="cfffe-156">в отличие от элементов управления с одним выбором, таких как [переключатели](ctrl-radio-buttons.md), пользователи могут выбрать любое сочетание параметров в группе флажков.</span><span class="sxs-lookup"><span data-stu-id="cfffe-156">unlike single-selection controls such as [radio buttons](ctrl-radio-buttons.md), users can select any combination of options in a group of check boxes.</span></span><br/> <span data-ttu-id="cfffe-157">![снимок экрана с двумя из трех выбранных флажков ](images/ctrl-check-boxes-image7.png)</span><span class="sxs-lookup"><span data-stu-id="cfffe-157">![screen shot of two of three check boxes selected ](images/ctrl-check-boxes-image7.png)</span></span><br/> <span data-ttu-id="cfffe-158">Группа флажков используется для независимых вариантов выбора.</span><span class="sxs-lookup"><span data-stu-id="cfffe-158">A group of check boxes is used for independent choices.</span></span><br/>                                                                                                                                                  |
| <span data-ttu-id="cfffe-159">**Зависимые варианты (один или несколько)** Группу флажков также можно использовать для выбора из набора из одного или нескольких вариантов.</span><span class="sxs-lookup"><span data-stu-id="cfffe-159">**Dependent choices (one or more)** A group of check boxes can also be used to select from a set of one or more choices.</span></span><br/>                                                                         | <span data-ttu-id="cfffe-160">**может потребоваться представить выбор одного или нескольких зависимых вариантов**.</span><span class="sxs-lookup"><span data-stu-id="cfffe-160">**you may need to represent a selection of one or more dependent choices**.</span></span> <span data-ttu-id="cfffe-161">Поскольку Microsoft? Windows не имеет элемента управления, который напрямую поддерживает этот тип входных данных, лучшим решением будет использование группы флажков и обработку ошибки, если ни один из параметров не выбран.</span><span class="sxs-lookup"><span data-stu-id="cfffe-161">because microsoft?windows doesn't have a control that directly supports this type of input, the best solution is to use a group of check boxes and handle the error when none of the options are selected.</span></span><br/> <span data-ttu-id="cfffe-162">![снимок экрана с одним из двух выбранных флажков ](images/ctrl-check-boxes-image8.png)</span><span class="sxs-lookup"><span data-stu-id="cfffe-162">![screen shot of one of two check boxes selected ](images/ctrl-check-boxes-image8.png)</span></span><br/> <span data-ttu-id="cfffe-163">Используется группа флажков, где должен быть выбран хотя бы один протокол.</span><span class="sxs-lookup"><span data-stu-id="cfffe-163">A group of check boxes is used where at least one protocol must be selected.</span></span><br/> |
| <span data-ttu-id="cfffe-164">**Смешанный вариант** Кроме выбранных и сброшенных состояний, флажки также имеют смешанное состояние для множественного выбора, чтобы указать, что параметр задан для некоторых, но не всех объектов.</span><span class="sxs-lookup"><span data-stu-id="cfffe-164">**Mixed choice** In addition to their selected and cleared states, check boxes also have a mixed state for multiple selection to indicate that the option is set for some, but not all, objects.</span></span><br/> | ![<span data-ttu-id="cfffe-165">снимок экрана со сплошным синим флажком "только для чтения"</span><span class="sxs-lookup"><span data-stu-id="cfffe-165">screen shot of a solid blue read-only check box</span></span> ](images/ctrl-check-boxes-image9.png)<br/> <span data-ttu-id="cfffe-166">Флажок смешанного состояния.</span><span class="sxs-lookup"><span data-stu-id="cfffe-166">A mixed-state check box.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                      |



 

## <a name="guidelines"></a><span data-ttu-id="cfffe-167">Рекомендации</span><span class="sxs-lookup"><span data-stu-id="cfffe-167">Guidelines</span></span>

### <a name="general"></a><span data-ttu-id="cfffe-168">Общее</span><span class="sxs-lookup"><span data-stu-id="cfffe-168">General</span></span>

-   <span data-ttu-id="cfffe-169">Флажки, **связанные с группировкой**.</span><span class="sxs-lookup"><span data-stu-id="cfffe-169">**Group related check boxes**.</span></span> <span data-ttu-id="cfffe-170">Объедините связанные параметры и разделите несвязанные параметры группами из 10 или менее, используя несколько групп, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="cfffe-170">Combine related options and separate unrelated options into groups of 10 or fewer, using multiple groups if necessary.</span></span>

    ![<span data-ttu-id="cfffe-171">снимок экрана со связанными и несвязанными флажками</span><span class="sxs-lookup"><span data-stu-id="cfffe-171">screen shot of related and unrelated check boxes</span></span> ](images/ctrl-check-boxes-image10.png)

    <span data-ttu-id="cfffe-172">Пример групп связанных независимых параметров.</span><span class="sxs-lookup"><span data-stu-id="cfffe-172">An example of groups of related, independent options.</span></span>

-   <span data-ttu-id="cfffe-173">Используйте **поля группы, чтобы упорядочить группы** флажков это часто приводит к ненужным помехам экрана.</span><span class="sxs-lookup"><span data-stu-id="cfffe-173">**Reconsider using group boxes to organize groups of check boxes** this often results in unnecessary screen clutter.</span></span>
-   <span data-ttu-id="cfffe-174">**Перечислите флажки в логическом порядке**, такие как группирование тесно связанных параметров или размещение большинства наиболее распространенных вариантов, или выполнение некоторых других естественных последовательностей.</span><span class="sxs-lookup"><span data-stu-id="cfffe-174">**List check boxes in a logical order**, such as grouping highly related options together or placing most common options first, or following some other natural progression.</span></span> <span data-ttu-id="cfffe-175">Не рекомендуется использовать алфавитный порядок, так как он зависит от языка и, следовательно, недоступен для локализации.</span><span class="sxs-lookup"><span data-stu-id="cfffe-175">Alphabetical ordering isn't recommended because it is language dependent, and therefore not localizable.</span></span>
-   <span data-ttu-id="cfffe-176">**Выравнивание флажков по вертикали, а не по горизонтали**.</span><span class="sxs-lookup"><span data-stu-id="cfffe-176">**Align check boxes vertically, not horizontally**.</span></span> <span data-ttu-id="cfffe-177">Выравнивание по горизонтали труднее для чтения.</span><span class="sxs-lookup"><span data-stu-id="cfffe-177">Horizontal alignment is harder to read.</span></span>

    <span data-ttu-id="cfffe-178">**Правильно:**</span><span class="sxs-lookup"><span data-stu-id="cfffe-178">**Correct:**</span></span>

    ![<span data-ttu-id="cfffe-179">снимок экрана с выравниванием флажков по вертикали</span><span class="sxs-lookup"><span data-stu-id="cfffe-179">screen shot of check boxes aligned vertically</span></span> ](images/ctrl-check-boxes-image11.png)

    <span data-ttu-id="cfffe-180">В этом примере флажки правильно согласованы.</span><span class="sxs-lookup"><span data-stu-id="cfffe-180">In this example, the check boxes are correctly aligned.</span></span>

    <span data-ttu-id="cfffe-181">**Неправильно**:</span><span class="sxs-lookup"><span data-stu-id="cfffe-181">**Incorrect:**</span></span>

    ![<span data-ttu-id="cfffe-182">снимок экрана с выведением флажков по горизонтали</span><span class="sxs-lookup"><span data-stu-id="cfffe-182">screen shot of check boxes aligned horizontally</span></span> ](images/ctrl-check-boxes-image12.png)

    <span data-ttu-id="cfffe-183">В этом примере выравнивание по горизонтали труднее для чтения.</span><span class="sxs-lookup"><span data-stu-id="cfffe-183">In this example, the horizontal alignment is harder to read.</span></span>

-   <span data-ttu-id="cfffe-184">**Не используйте смешанное состояние для представления третьего состояния.**</span><span class="sxs-lookup"><span data-stu-id="cfffe-184">**Don't use the mixed state to represent a third state.**</span></span> <span data-ttu-id="cfffe-185">Смешанное состояние используется для указания того, что параметр задан для некоторых, но не для всех дочерних объектов.</span><span class="sxs-lookup"><span data-stu-id="cfffe-185">The mixed state is used to indicate that an option is set for some, but not all, child objects.</span></span> <span data-ttu-id="cfffe-186">Пользователи не должны иметь возможность задавать смешанное состояние напрямую, а смешанное состояние — это отражение дочерних объектов.</span><span class="sxs-lookup"><span data-stu-id="cfffe-186">Users shouldn't be able to set a mixed state directly rather the mixed state is a reflection of the child objects.</span></span> <span data-ttu-id="cfffe-187">Смешанное состояние не используется в качестве третьего состояния для отдельного элемента.</span><span class="sxs-lookup"><span data-stu-id="cfffe-187">The mixed state isn't used as a third state for an individual item.</span></span> <span data-ttu-id="cfffe-188">Чтобы представить третье состояние, используйте переключатели или раскрывающийся список.</span><span class="sxs-lookup"><span data-stu-id="cfffe-188">To represent a third state, use radio buttons or a drop-down list instead.</span></span>

    <span data-ttu-id="cfffe-189">**Неправильно**:</span><span class="sxs-lookup"><span data-stu-id="cfffe-189">**Incorrect:**</span></span>

    ![<span data-ttu-id="cfffe-190">снимок экрана — флажок "сплошная синяя служба тем"</span><span class="sxs-lookup"><span data-stu-id="cfffe-190">screen shot of solid blue theme service check box</span></span> ](images/ctrl-check-boxes-image13.png)

    <span data-ttu-id="cfffe-191">В этом примере смешанное состояние должно указывать на то, что служба темы не установлена.</span><span class="sxs-lookup"><span data-stu-id="cfffe-191">In this example, the mixed state is supposed to indicate that the Theme service isn't installed.</span></span>

    <span data-ttu-id="cfffe-192">**Правильно:**</span><span class="sxs-lookup"><span data-stu-id="cfffe-192">**Correct:**</span></span>

    ![<span data-ttu-id="cfffe-193">снимок экрана с тремя параметрами в раскрывающемся списке</span><span class="sxs-lookup"><span data-stu-id="cfffe-193">screen shot of drop-down list with three options</span></span> ](images/ctrl-check-boxes-image14.png)

    <span data-ttu-id="cfffe-194">В этом примере пользователи могут выбрать из списка три параметра.</span><span class="sxs-lookup"><span data-stu-id="cfffe-194">In this example, users can choose from a list of three clear options.</span></span>

-   <span data-ttu-id="cfffe-195">**Если щелкнуть флажок смешанное состояние, все выбранные, очищенные и исходные смешанные состояния должны быть циклически перебираться.**</span><span class="sxs-lookup"><span data-stu-id="cfffe-195">**Clicking a mixed state check box should cycle through all selected, all cleared, and the original mixed states.**</span></span> <span data-ttu-id="cfffe-196">Для форгивенесс важно иметь возможность восстановить исходное смешанное состояние, поскольку параметры могут быть сложными или неизвестны для пользователя.</span><span class="sxs-lookup"><span data-stu-id="cfffe-196">For forgiveness, it's important to be able to restore the original mixed state because the settings might be complex or unknown to the user.</span></span> <span data-ttu-id="cfffe-197">В противном случае, единственный способ восстановить смешанное состояние с уверенностью — отменить задачу и начать заново.</span><span class="sxs-lookup"><span data-stu-id="cfffe-197">Otherwise, the only way to restore the mixed state with confidence would be to cancel the task and start over.</span></span>
-   <span data-ttu-id="cfffe-198">**Не используйте флажки в качестве индикатора хода выполнения**.</span><span class="sxs-lookup"><span data-stu-id="cfffe-198">**Don't use check boxes as a progress indicator**.</span></span> <span data-ttu-id="cfffe-199">Вместо этого используйте элемент управления [индикатора выполнения](progress-bars.md) .</span><span class="sxs-lookup"><span data-stu-id="cfffe-199">Use a [progress indicator](progress-bars.md) control instead.</span></span>

    <span data-ttu-id="cfffe-200">**Неправильно**:</span><span class="sxs-lookup"><span data-stu-id="cfffe-200">**Incorrect:**</span></span>

    ![<span data-ttu-id="cfffe-201">снимок экрана с четырьмя флажками, отображающими ход выполнения</span><span class="sxs-lookup"><span data-stu-id="cfffe-201">screen shot of four check boxes showing progress</span></span> ](images/ctrl-check-boxes-image15.png)

    <span data-ttu-id="cfffe-202">В этом примере флажки в качестве индикатора хода выполнения используются неправильно.</span><span class="sxs-lookup"><span data-stu-id="cfffe-202">In this example, check boxes are used incorrectly as a progress indicator.</span></span>

    <span data-ttu-id="cfffe-203">**Правильно:**</span><span class="sxs-lookup"><span data-stu-id="cfffe-203">**Correct:**</span></span>

    ![<span data-ttu-id="cfffe-204">снимок экрана с частично заполненным индикатором выполнения</span><span class="sxs-lookup"><span data-stu-id="cfffe-204">screen shot of a partially filled progress bar</span></span> ](images/ctrl-check-boxes-image16.png)

    <span data-ttu-id="cfffe-205">Пример типичного индикатора выполнения.</span><span class="sxs-lookup"><span data-stu-id="cfffe-205">Example of a typical progress bar.</span></span>

-   <span data-ttu-id="cfffe-206">**Отображать отключенные флажки, используя правильное состояние выбора.**</span><span class="sxs-lookup"><span data-stu-id="cfffe-206">**Show disabled check boxes using the correct selection state.**</span></span> <span data-ttu-id="cfffe-207">Несмотря на то, что пользователи не могут их изменять, отключенные флажки передают информацию, чтобы они соответствовали результатам.</span><span class="sxs-lookup"><span data-stu-id="cfffe-207">Even though users can't change them, disabled check boxes convey information so they should be consistent with results.</span></span>

    <span data-ttu-id="cfffe-208">**Неправильно**:</span><span class="sxs-lookup"><span data-stu-id="cfffe-208">**Incorrect:**</span></span>

    ![<span data-ttu-id="cfffe-209">снимок экрана одного из двух флажков, затененных</span><span class="sxs-lookup"><span data-stu-id="cfffe-209">screen shot of one of two check boxes dimmed</span></span> ](images/ctrl-check-boxes-image17.png)

    <span data-ttu-id="cfffe-210">В этом примере параметр "всегда читать этот раздел вслух" должен быть сброшен, так как раздел не читается, если этот параметр отключен.</span><span class="sxs-lookup"><span data-stu-id="cfffe-210">In this example, the "Always read this section aloud" option should be cleared because the section isn't read when the option is disabled.</span></span>

-   <span data-ttu-id="cfffe-211">**Не устанавливайте флажок для следующих элементов**:</span><span class="sxs-lookup"><span data-stu-id="cfffe-211">**Don't use the selection of a check box to**:</span></span>
    -   <span data-ttu-id="cfffe-212">Выполнение команд.</span><span class="sxs-lookup"><span data-stu-id="cfffe-212">Perform commands.</span></span>
    -   <span data-ttu-id="cfffe-213">Отображение других окон, таких как диалоговое окно для сбора дополнительных входных данных.</span><span class="sxs-lookup"><span data-stu-id="cfffe-213">Display other windows, such as a dialog box to gather more input.</span></span>
    -   <span data-ttu-id="cfffe-214">Динамическое отображение других элементов управления, связанных с выбранным элементом управления (средства чтения с экрана не могут обнаруживать такие события).</span><span class="sxs-lookup"><span data-stu-id="cfffe-214">Dynamically display other controls related to the selected control (screen readers cannot detect such events).</span></span>

### <a name="dont-show-this-item-again"></a><span data-ttu-id="cfffe-215">Не показывать</span><span class="sxs-lookup"><span data-stu-id="cfffe-215">Don't show this</span></span> <item> <span data-ttu-id="cfffe-216">повторить</span><span class="sxs-lookup"><span data-stu-id="cfffe-216">again</span></span>

-   <span data-ttu-id="cfffe-217">**Попробуйте использовать параметр больше не показывать, <item> чтобы разрешить пользователям подавлять повторяющиеся диалоговые окна, только если нет лучшей альтернативы.**</span><span class="sxs-lookup"><span data-stu-id="cfffe-217">**Consider using a Don't show this <item> again option to allow users to suppress a recurring dialog box only if there isn't a better alternative.**</span></span> <span data-ttu-id="cfffe-218">Если пользователям действительно требуется диалоговое окно, попробуйте заранее определить его. Если это так, всегда показывать диалоговое окно, а если нет, исключите диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="cfffe-218">Try to determine beforehand if users really need the dialog; if they do, always show the dialog, and if they don't, eliminate the dialog.</span></span>

<span data-ttu-id="cfffe-219">Дополнительные рекомендации и примеры см. в разделе [диалоговые окна](win-dialog-box.md).</span><span class="sxs-lookup"><span data-stu-id="cfffe-219">For more guidelines and examples, see [Dialog Boxes](win-dialog-box.md).</span></span>

### <a name="subordinate-controls"></a><span data-ttu-id="cfffe-220">Подчиненные элементы управления</span><span class="sxs-lookup"><span data-stu-id="cfffe-220">Subordinate controls</span></span>

-   <span data-ttu-id="cfffe-221">Разместите подчиненные элементы управления справа или ниже (с отступом, с помощью метки с флажком) флажка и его метки.</span><span class="sxs-lookup"><span data-stu-id="cfffe-221">Place subordinate controls to the right of or below (indented, flush with the check box label) the check box and its label.</span></span> <span data-ttu-id="cfffe-222">Установите флажок с двоеточием.</span><span class="sxs-lookup"><span data-stu-id="cfffe-222">End the check box label with a colon.</span></span>

    ![<span data-ttu-id="cfffe-223">снимок экрана с надписью под меткой "флажок"</span><span class="sxs-lookup"><span data-stu-id="cfffe-223">screen shot of text box below check box label</span></span> ](images/ctrl-check-boxes-image18.png)

    <span data-ttu-id="cfffe-224">В этом примере флажок и его подчиненный элемент управления совместно используют метку флажка и ее ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="cfffe-224">In this example, the check box and its subordinate control share the check box label and its access key.</span></span>

-   <span data-ttu-id="cfffe-225">**Оставьте зависимые редактируемые текстовые поля и раскрывающиеся списки включенными, если они совместно используют метку установленного флажка.**</span><span class="sxs-lookup"><span data-stu-id="cfffe-225">**Leave dependent editable text boxes and drop-down lists enabled if they share the check box's label.**</span></span> <span data-ttu-id="cfffe-226">При вводе или вставке любого элемента в поле выберите соответствующий параметр автоматически.</span><span class="sxs-lookup"><span data-stu-id="cfffe-226">When users type or paste anything into the box, select the corresponding option automatically.</span></span> <span data-ttu-id="cfffe-227">Это упрощает взаимодействие.</span><span class="sxs-lookup"><span data-stu-id="cfffe-227">Doing so simplifies the interaction.</span></span>

    ![<span data-ttu-id="cfffe-228">снимок экрана текстовых полей верхнего и нижнего колонтитулов</span><span class="sxs-lookup"><span data-stu-id="cfffe-228">screen shot of header and footer text boxes</span></span> ](images/ctrl-check-boxes-image19.png)

    <span data-ttu-id="cfffe-229">В этом примере при вводе верхнего или нижнего колонтитула автоматически выбирается параметр.</span><span class="sxs-lookup"><span data-stu-id="cfffe-229">In this example, entering a header or footer automatically selects the option.</span></span>

-   <span data-ttu-id="cfffe-230">Если вложены флажки с переключателями или другие флажки, **отключите эти подчиненные элементы управления, пока не будет выбран параметр высокого уровня**.</span><span class="sxs-lookup"><span data-stu-id="cfffe-230">If you nest check boxes with radio buttons or other check boxes, **disable these subordinate controls until the high-level option is selected**.</span></span> <span data-ttu-id="cfffe-231">Это позволяет избежать путаницы в значении подчиненных элементов управления.</span><span class="sxs-lookup"><span data-stu-id="cfffe-231">Doing so avoids confusion about the meaning of the subordinate controls.</span></span>
-   <span data-ttu-id="cfffe-232">Сделать подчиненные элементы управления флажком рядом с флажком в последовательности табуляции.</span><span class="sxs-lookup"><span data-stu-id="cfffe-232">Make subordinate controls to a check box contiguous with the check box in the tab order.</span></span>
-   <span data-ttu-id="cfffe-233">**Если выбор параметра подразумевает выбор подчиненных флажков, явно установите эти флажки, чтобы связь была очищена.**</span><span class="sxs-lookup"><span data-stu-id="cfffe-233">**If selecting an option implies selecting subordinate check boxes, explicitly select those check boxes to make the relationship clear.**</span></span>

    <span data-ttu-id="cfffe-234">**Неправильно**:</span><span class="sxs-lookup"><span data-stu-id="cfffe-234">**Incorrect:**</span></span>

    ![<span data-ttu-id="cfffe-235">снимок экрана: выбранная кнопка, сброшенные флажки</span><span class="sxs-lookup"><span data-stu-id="cfffe-235">screen shot: selected button, cleared check boxes</span></span> ](images/ctrl-check-boxes-image20.png)

    <span data-ttu-id="cfffe-236">В этом примере подчиненные флажки не выбраны.</span><span class="sxs-lookup"><span data-stu-id="cfffe-236">In this example, the subordinate check boxes aren't selected.</span></span>

    <span data-ttu-id="cfffe-237">**Правильно:**</span><span class="sxs-lookup"><span data-stu-id="cfffe-237">**Correct:**</span></span>

    ![<span data-ttu-id="cfffe-238">снимок экрана: выбранная кнопка, выбранные флажки</span><span class="sxs-lookup"><span data-stu-id="cfffe-238">screen shot: selected button, selected check boxes</span></span> ](images/ctrl-check-boxes-image21.png)

    <span data-ttu-id="cfffe-239">В этом примере выделены подчиненные флажки, что позволяет снять связь с выбранным параметром.</span><span class="sxs-lookup"><span data-stu-id="cfffe-239">In this example, the subordinate check boxes are selected, making their relationship to the selected option clear.</span></span>

-   <span data-ttu-id="cfffe-240">**Используйте зависимые флажки, если альтернативы добавляют ненужные сложности**.</span><span class="sxs-lookup"><span data-stu-id="cfffe-240">**Use dependent check boxes if the alternatives add unnecessary complexity**.</span></span> <span data-ttu-id="cfffe-241">Хотя флажки должны быть независимыми, иногда такие варианты, как переключатели, добавляют ненужные сложности.</span><span class="sxs-lookup"><span data-stu-id="cfffe-241">While check boxes should be independent options, sometimes alternatives such as radio buttons add unnecessary complexity.</span></span>

    <span data-ttu-id="cfffe-242">**Правильно:**</span><span class="sxs-lookup"><span data-stu-id="cfffe-242">**Correct:**</span></span>

    ![<span data-ttu-id="cfffe-243">снимок экрана с путаницой кнопок и флажков</span><span class="sxs-lookup"><span data-stu-id="cfffe-243">screen shot of confusing buttons and check boxes</span></span> ](images/ctrl-check-boxes-image22.png)

    <span data-ttu-id="cfffe-244">В этом примере Использование переключателей является точным, но создает ненужные сложности.</span><span class="sxs-lookup"><span data-stu-id="cfffe-244">In this example, the use of radio buttons is accurate, but creates unnecessary complexity.</span></span>

    <span data-ttu-id="cfffe-245">**Лучше:**</span><span class="sxs-lookup"><span data-stu-id="cfffe-245">**Better:**</span></span>

    ![<span data-ttu-id="cfffe-246">снимок экрана только флажков</span><span class="sxs-lookup"><span data-stu-id="cfffe-246">screen shot of check boxes only</span></span> ](images/ctrl-check-boxes-image23.png)

    <span data-ttu-id="cfffe-247">В этом примере использование флажков упрощается и позволяет пользователям сосредоточиться на выборе требуемых параметров, а не на их сложной связи.</span><span class="sxs-lookup"><span data-stu-id="cfffe-247">In this example, the use of check boxes is simpler and allows users to focus on selecting the desired options instead of on their complex relationship.</span></span>

    <span data-ttu-id="cfffe-248">**Важно. применить эту рекомендацию только в редких обстоятельствах**, при отображении зависимостей существенно усложняется, не добавив ясности.</span><span class="sxs-lookup"><span data-stu-id="cfffe-248">**Important: Apply this guideline only in extremely rare circumstances**, when showing the dependencies adds significant complexity without adding clarity.</span></span> <span data-ttu-id="cfffe-249">В предыдущем примере маловероятно, что пользователи попытаются выбрать и надстрочные, и подстрочные индексы, и если бы они были, было бы легко понять, что они были эксклюзивными вариантами.</span><span class="sxs-lookup"><span data-stu-id="cfffe-249">In the previous example, it is unlikely that users would attempt to choose both superscript and subscript, and if they did, it would be easy to understand that they were exclusive options.</span></span>

### <a name="default-values"></a><span data-ttu-id="cfffe-250">Значения по умолчанию</span><span class="sxs-lookup"><span data-stu-id="cfffe-250">Default values</span></span>

-   <span data-ttu-id="cfffe-251">Если флажок предназначен для пользовательского параметра, **Установите безопасный режим (чтобы предотвратить потери данных или доступ к системе), наиболее безопасное и закрытое состояние по умолчанию.**</span><span class="sxs-lookup"><span data-stu-id="cfffe-251">If a check box is for a user option, **set the safest (to prevent loss of data or system access), most secure and private state by default.**</span></span> <span data-ttu-id="cfffe-252">Если безопасность и безопасность не являются факторами, выберите наиболее вероятное или удобное значение.</span><span class="sxs-lookup"><span data-stu-id="cfffe-252">If safety and security aren't factors, select the most likely or convenient value.</span></span>

## <a name="recommended-sizing-and-spacing"></a><span data-ttu-id="cfffe-253">Рекомендуемое изменение размера и расстояния</span><span class="sxs-lookup"><span data-stu-id="cfffe-253">Recommended sizing and spacing</span></span>

![<span data-ttu-id="cfffe-254">Рисунок рекомендуемого размера и промежутков между флажками</span><span class="sxs-lookup"><span data-stu-id="cfffe-254">figure of suggested check box sizing and spacing</span></span> ](images/ctrl-check-boxes-image24.png)

<span data-ttu-id="cfffe-255">Рекомендуемое изменение размера и расстояния для флажков.</span><span class="sxs-lookup"><span data-stu-id="cfffe-255">Recommended sizing and spacing for check boxes.</span></span>

## <a name="labels"></a><span data-ttu-id="cfffe-256">Метки</span><span class="sxs-lookup"><span data-stu-id="cfffe-256">Labels</span></span>

<span data-ttu-id="cfffe-257">**Метки флажков**</span><span class="sxs-lookup"><span data-stu-id="cfffe-257">**Check box labels**</span></span>

-   <span data-ttu-id="cfffe-258">Метка для каждого флажка.</span><span class="sxs-lookup"><span data-stu-id="cfffe-258">Label every check box.</span></span>
-   <span data-ttu-id="cfffe-259">Присвойте каждой метке уникальный [ключ доступа](glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="cfffe-259">Assign a unique [access key](glossary.md) to each label.</span></span> <span data-ttu-id="cfffe-260">Инструкции см. в разделе [Клавиатура](inter-keyboard.md).</span><span class="sxs-lookup"><span data-stu-id="cfffe-260">For guidelines, see [Keyboard](inter-keyboard.md).</span></span>
-   <span data-ttu-id="cfffe-261">Используйте [прописные буквы в стиле предложения](glossary.md).</span><span class="sxs-lookup"><span data-stu-id="cfffe-261">Use [sentence-style capitalization](glossary.md).</span></span>
-   <span data-ttu-id="cfffe-262">Напишите метку в виде фразы или императивного предложения и не используйте закрывающие знаки препинания.</span><span class="sxs-lookup"><span data-stu-id="cfffe-262">Write the label as a phrase or an imperative sentence, and use no ending punctuation.</span></span>
    -   <span data-ttu-id="cfffe-263">**Исключение:** Если метка флажка также помечает подчиненный элемент управления, следующий за ним, следует завершить метку с помощью двоеточия.</span><span class="sxs-lookup"><span data-stu-id="cfffe-263">**Exception:** If a check box label also labels a subordinate control that follows it, end the label with a colon.</span></span>
-   <span data-ttu-id="cfffe-264">Запишите метку, которая описывает выбранное состояние флажка.</span><span class="sxs-lookup"><span data-stu-id="cfffe-264">Write the label so that it describes the selected state of the check box.</span></span>
-   <span data-ttu-id="cfffe-265">Для группы флажков используйте параллельные выражения и старайтесь попытаться удержать одинаковую длину для всех меток.</span><span class="sxs-lookup"><span data-stu-id="cfffe-265">For a group of check boxes, use parallel phrasing and try to keep the length about the same for all labels.</span></span>
-   <span data-ttu-id="cfffe-266">Для группы флажков сосредоточьте текст метки на различиях между параметрами.</span><span class="sxs-lookup"><span data-stu-id="cfffe-266">For a group of check boxes, focus the label text on the differences among the options.</span></span> <span data-ttu-id="cfffe-267">Если все параметры имеют одинаковый вводный текст, переместите этот текст в метку группы.</span><span class="sxs-lookup"><span data-stu-id="cfffe-267">If all the options have the same introductory text, move that text to the group label.</span></span>
-   <span data-ttu-id="cfffe-268">Используйте положительные выражения.</span><span class="sxs-lookup"><span data-stu-id="cfffe-268">Use positive phrasing.</span></span> <span data-ttu-id="cfffe-269">Не заменяйте метку, чтобы установка флажка не выполняла никаких действий.</span><span class="sxs-lookup"><span data-stu-id="cfffe-269">Don't phrase a label so that selecting a check box means not to perform an action.</span></span>

    -   <span data-ttu-id="cfffe-270">**Исключение: не показывать флажки <item> снова** .</span><span class="sxs-lookup"><span data-stu-id="cfffe-270">**Exception:Don't show this <item> again** check boxes.</span></span>

    <span data-ttu-id="cfffe-271">**Неправильно**:</span><span class="sxs-lookup"><span data-stu-id="cfffe-271">**Incorrect:**</span></span>

    ![снимок экрана с отрицательной меткой "отключить"](images/ctrl-check-boxes-image25.png)

    <span data-ttu-id="cfffe-273">В этом примере параметр не использует положительные выражения.</span><span class="sxs-lookup"><span data-stu-id="cfffe-273">In this example, the option doesn't use positive phrasing.</span></span>

-   <span data-ttu-id="cfffe-274">Опишите только параметр с меткой.</span><span class="sxs-lookup"><span data-stu-id="cfffe-274">Describe just the option with the label.</span></span> <span data-ttu-id="cfffe-275">Короткие метки позволяют легко ссылаться на них в сообщениях и документации.</span><span class="sxs-lookup"><span data-stu-id="cfffe-275">Keep labels brief so it's easy to refer to them in messages and documentation.</span></span> <span data-ttu-id="cfffe-276">Если параметр требует дальнейшего объяснения, укажите пояснения в статическом элементе управления " [текст](./glossary.md) ", используя полные предложения и закрывающие знаки препинания.</span><span class="sxs-lookup"><span data-stu-id="cfffe-276">If the option requires further explanation, provide the explanation in a [static text](./glossary.md) control using complete sentences and ending punctuation.</span></span>

    > [!Note]
    >
    > <span data-ttu-id="cfffe-277">Добавление объяснения к одному флажку в группе не означает, что необходимо предоставить пояснения для всех флажков в группе.</span><span class="sxs-lookup"><span data-stu-id="cfffe-277">Adding an explanation to one check box in a group doesn't mean that you have to provide explanations for all check boxes in the group.</span></span> <span data-ttu-id="cfffe-278">Укажите нужные сведения в метке, если это возможно, и используйте объяснения только при необходимости.</span><span class="sxs-lookup"><span data-stu-id="cfffe-278">Provide the relevant information in the label if you can, and use explanations only when necessary.</span></span> <span data-ttu-id="cfffe-279">Не просто переводите метку в состояние согласованности.</span><span class="sxs-lookup"><span data-stu-id="cfffe-279">Don't merely restate the label for consistency.</span></span>

     

    ![<span data-ttu-id="cfffe-280">снимок экрана: флажок, метка и описание</span><span class="sxs-lookup"><span data-stu-id="cfffe-280">screen shot of checkbox, label, and description</span></span> ](images/ctrl-check-boxes-image26.png)

    <span data-ttu-id="cfffe-281">В этом примере метка флажка содержит дополнительный пояснительный текст под ним.</span><span class="sxs-lookup"><span data-stu-id="cfffe-281">In this example, a check box label has additional explanatory text beneath it.</span></span>

-   <span data-ttu-id="cfffe-282">Если настоятельно рекомендуется использовать параметр, рекомендуется добавить к метке "(рекомендуется)".</span><span class="sxs-lookup"><span data-stu-id="cfffe-282">If an option is strongly recommended, consider adding "(recommended)" to the label.</span></span> <span data-ttu-id="cfffe-283">Не забудьте добавить к метке элемента управления, а не дополнительным примечаниям.</span><span class="sxs-lookup"><span data-stu-id="cfffe-283">Be sure to add to the control label, not the supplemental notes.</span></span>
-   <span data-ttu-id="cfffe-284">Если необходимо использовать многострочные метки, Выровняйте верхнюю часть метки с флажком.</span><span class="sxs-lookup"><span data-stu-id="cfffe-284">If you must use multi-line labels, align the top of the label with the check box.</span></span>
-   <span data-ttu-id="cfffe-285">Не используйте подчиненный элемент управления, содержащиеся в нем значения или метку Units, чтобы создать предложение или фразу.</span><span class="sxs-lookup"><span data-stu-id="cfffe-285">Don't use a subordinate control, the values it contains, or its units label to create a sentence or phrase.</span></span> <span data-ttu-id="cfffe-286">Такой проект не локализуется, так как структура предложения зависит от языка.</span><span class="sxs-lookup"><span data-stu-id="cfffe-286">Such a design isn't localizable because sentence structure varies with language.</span></span>

    <span data-ttu-id="cfffe-287">**Неправильно**:</span><span class="sxs-lookup"><span data-stu-id="cfffe-287">**Incorrect:**</span></span>

    ![<span data-ttu-id="cfffe-288">снимок экрана метки флажка с текстовым полем в нем</span><span class="sxs-lookup"><span data-stu-id="cfffe-288">screen shot of checkbox label with text box in it</span></span> ](images/ctrl-check-boxes-image27.png)

    <span data-ttu-id="cfffe-289">В этом примере текстовое поле неверно помещается в метку флажка.</span><span class="sxs-lookup"><span data-stu-id="cfffe-289">In this example, the text box is incorrectly placed inside the check box label.</span></span>

<span data-ttu-id="cfffe-290">**Метки групп флажков**</span><span class="sxs-lookup"><span data-stu-id="cfffe-290">**Check box group labels**</span></span>

-   <span data-ttu-id="cfffe-291">Используйте метку группы, чтобы объяснить назначение группы, а не как сделать выбор.</span><span class="sxs-lookup"><span data-stu-id="cfffe-291">Use the group label to explain the purpose of the group, not how to make the selection.</span></span> <span data-ttu-id="cfffe-292">Предположим, что пользователи узнают, как использовать флажки.</span><span class="sxs-lookup"><span data-stu-id="cfffe-292">Assume that users know how to use check boxes.</span></span> <span data-ttu-id="cfffe-293">Например, не скажите «выбрать любой из следующих вариантов».</span><span class="sxs-lookup"><span data-stu-id="cfffe-293">For example, don't say "Select any of the following choices".</span></span>
-   <span data-ttu-id="cfffe-294">Завершайте каждую метку двоеточием.</span><span class="sxs-lookup"><span data-stu-id="cfffe-294">End each label with a colon.</span></span>
-   <span data-ttu-id="cfffe-295">Не присваивайте метке ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="cfffe-295">Don't assign an access key to the label.</span></span> <span data-ttu-id="cfffe-296">Это не обязательно, а другие ключи доступа сложнее назначить.</span><span class="sxs-lookup"><span data-stu-id="cfffe-296">Doing so isn't necessary and it makes the other access keys harder to assign.</span></span>
-   <span data-ttu-id="cfffe-297">Чтобы выбрать один или несколько зависимых вариантов, объясните требование к метке.</span><span class="sxs-lookup"><span data-stu-id="cfffe-297">For a selection of one or more dependent choices, explain the requirement on the label.</span></span>

    <span data-ttu-id="cfffe-298">**Правильно:**</span><span class="sxs-lookup"><span data-stu-id="cfffe-298">**Correct:**</span></span>

    ![<span data-ttu-id="cfffe-299">снимок экрана с меткой для двух элементов управления: протоколы</span><span class="sxs-lookup"><span data-stu-id="cfffe-299">screen shot of label for two controls: protocols</span></span> ](images/ctrl-check-boxes-image28.png)

    <span data-ttu-id="cfffe-300">В этом примере пользователи могут подумать, что они могут только выбрать один из вариантов.</span><span class="sxs-lookup"><span data-stu-id="cfffe-300">In this example, users might think that they can only make one selection.</span></span>

    <span data-ttu-id="cfffe-301">**Лучше:**</span><span class="sxs-lookup"><span data-stu-id="cfffe-301">**Better:**</span></span>

    ![<span data-ttu-id="cfffe-302">снимок экрана с меткой: Протокол выберите один или несколько</span><span class="sxs-lookup"><span data-stu-id="cfffe-302">screen shot of label: protocols select one or more</span></span> ](images/ctrl-check-boxes-image29.png)

    <span data-ttu-id="cfffe-303">В этом примере ясно, что пользователи могут выбрать несколько элементов.</span><span class="sxs-lookup"><span data-stu-id="cfffe-303">In this example, it's clear that users can make more than one selection.</span></span>

## <a name="documentation"></a><span data-ttu-id="cfffe-304">Документация</span><span class="sxs-lookup"><span data-stu-id="cfffe-304">Documentation</span></span>

<span data-ttu-id="cfffe-305">При ссылке на флажки:</span><span class="sxs-lookup"><span data-stu-id="cfffe-305">When referring to check boxes:</span></span>

-   <span data-ttu-id="cfffe-306">Используйте точный текст метки, включая прописную букву, но не включайте символ подчеркивания или двоеточие.</span><span class="sxs-lookup"><span data-stu-id="cfffe-306">Use the exact label text, including its capitalization, but don't include the access key underscore or colon.</span></span> <span data-ttu-id="cfffe-307">Включите флажок слово.</span><span class="sxs-lookup"><span data-stu-id="cfffe-307">Include the word check box.</span></span>
-   <span data-ttu-id="cfffe-308">Устанавливайте флажок, а не параметр, флажок или только поле, так как только поле однозначно для локализаторов.</span><span class="sxs-lookup"><span data-stu-id="cfffe-308">Refer to a check box as a check box, not option, checkbox, or just box, because box alone is ambiguous for localizers.</span></span>
-   <span data-ttu-id="cfffe-309">Чтобы описать взаимодействие с пользователем, используйте SELECT и Clear.</span><span class="sxs-lookup"><span data-stu-id="cfffe-309">To describe user interaction, use select and clear.</span></span>
-   <span data-ttu-id="cfffe-310">По возможности отформатируйте метку, используя полужирный текст.</span><span class="sxs-lookup"><span data-stu-id="cfffe-310">When possible, format the label using bold text.</span></span> <span data-ttu-id="cfffe-311">В противном случае заключите метку в кавычки, только если это необходимо для предотвращения путаницы.</span><span class="sxs-lookup"><span data-stu-id="cfffe-311">Otherwise, put the label in quotation marks only if required to prevent confusion.</span></span>

    <span data-ttu-id="cfffe-312">Пример. Установите флажок **Подчеркнутый** .</span><span class="sxs-lookup"><span data-stu-id="cfffe-312">Example: Select the **Underline** check box.</span></span>

