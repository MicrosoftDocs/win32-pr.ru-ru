---
title: Ползунки (основы проектирования)
description: С помощью ползунка пользователи могут выбирать из непрерывного диапазона значений.
ms.assetid: dee70fbc-6f18-43c7-9d41-4e97eac41e53
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 7ff9791ab49c338e4c11e014a3e996771571add9
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/10/2021
ms.locfileid: "104552752"
---
# <a name="sliders-design-basics"></a><span data-ttu-id="073f8-103">Ползунки (основы проектирования)</span><span class="sxs-lookup"><span data-stu-id="073f8-103">Sliders (Design basics)</span></span>

> [!NOTE]
> <span data-ttu-id="073f8-104">Это руководство по проектированию было создано для Windows 7 и не Обновлено для более новых версий Windows.</span><span class="sxs-lookup"><span data-stu-id="073f8-104">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="073f8-105">Многие рекомендации по-прежнему применяются в принципе, но презентация и примеры не соответствуют нашим [текущим руководствам по проектированию](/windows/uwp/design/).</span><span class="sxs-lookup"><span data-stu-id="073f8-105">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="073f8-106">С помощью ползунка пользователи могут выбирать из непрерывного диапазона значений.</span><span class="sxs-lookup"><span data-stu-id="073f8-106">With a slider, users can choose from a continuous range of values.</span></span> <span data-ttu-id="073f8-107">Ползунок имеет полоску, показывающую диапазон и индикатор, показывающий текущее значение.</span><span class="sxs-lookup"><span data-stu-id="073f8-107">A slider has a bar that shows the range and an indicator that shows the current value.</span></span> <span data-ttu-id="073f8-108">Необязательные деления отображают значения.</span><span class="sxs-lookup"><span data-stu-id="073f8-108">Optional tick marks show values.</span></span>

![<span data-ttu-id="073f8-109">Рисунок, показывающий полосу, ползунок и деления</span><span class="sxs-lookup"><span data-stu-id="073f8-109">figure showing bar, slider, and tick marks</span></span> ](images/ctrl-sliders-image1.png)

<span data-ttu-id="073f8-110">Типичный ползунок.</span><span class="sxs-lookup"><span data-stu-id="073f8-110">A typical slider.</span></span>

> [!Note]  
> <span data-ttu-id="073f8-111">Рекомендации, связанные с [макетом](vis-layout.md) , представлены в отдельной статье.</span><span class="sxs-lookup"><span data-stu-id="073f8-111">Guidelines related to [layout](vis-layout.md) are presented in a separate article.</span></span>

 

## <a name="is-this-the-right-control"></a><span data-ttu-id="073f8-112">Выбор правильного элемента управления</span><span class="sxs-lookup"><span data-stu-id="073f8-112">Is this the right control?</span></span>

<span data-ttu-id="073f8-113">Используйте ползунок, если необходимо, чтобы пользователи могли **задавать определенные, смежные значения (например, громкость или яркость) или диапазон дискретных значений (например, параметры разрешения экрана).**</span><span class="sxs-lookup"><span data-stu-id="073f8-113">Use a slider when you want your users to be able to **set defined, contiguous values (such as volume or brightness) or a range of discrete values (such as screen resolution settings).**</span></span>

<span data-ttu-id="073f8-114">Ползунок рекомендуется использовать, если вы уверены, что пользователи представляют значение в виде относительной величины, а не определенного числа.</span><span class="sxs-lookup"><span data-stu-id="073f8-114">A slider is a good choice when you know that users think of the value as a relative quantity, not a numeric value.</span></span> <span data-ttu-id="073f8-115">Например: как правило, пользователи хотят уменьшить громкость до минимума или наполовину, а не задать значение 2 или 5.</span><span class="sxs-lookup"><span data-stu-id="073f8-115">For example, users think about setting their audio volume to low or medium—not about setting the value to 2 or 5.</span></span>

<span data-ttu-id="073f8-116">Чтобы определиться, ответьте на вопросы:</span><span class="sxs-lookup"><span data-stu-id="073f8-116">To decide, consider these questions:</span></span>

-   <span data-ttu-id="073f8-117">**Можно ли представить значение параметра в виде относительной величины?**</span><span class="sxs-lookup"><span data-stu-id="073f8-117">**Does the setting seem like a relative quantity?**</span></span> <span data-ttu-id="073f8-118">В противном случае используйте [переключатели](ctrl-radio-buttons.md)или список [с](/windows/desktop/uxguide/ctrl-drop) [одним выбором](ctrl-list-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="073f8-118">If not, use [radio buttons](ctrl-radio-buttons.md), or a [drop-down](/windows/desktop/uxguide/ctrl-drop) or [single-selection list](ctrl-list-boxes.md).</span></span>
-   <span data-ttu-id="073f8-119">**У параметра есть точное и заранее известное числовое значение?**</span><span class="sxs-lookup"><span data-stu-id="073f8-119">**Is the setting an exact, known numeric value?**</span></span> <span data-ttu-id="073f8-120">Если это так, используйте [числовые текстовые поля](ctrl-text-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="073f8-120">If so, use a [numeric text boxes](ctrl-text-boxes.md).</span></span>
-   <span data-ttu-id="073f8-121">**Требуется ли пользователю мгновенная обратная связь при изменении значения параметра?**</span><span class="sxs-lookup"><span data-stu-id="073f8-121">**Would a user benefit from instant feedback on the effect of setting changes?**</span></span> <span data-ttu-id="073f8-122">Если да, то используйте ползунок.</span><span class="sxs-lookup"><span data-stu-id="073f8-122">If so, use a slider.</span></span> <span data-ttu-id="073f8-123">Например, пользователям будет проще выбрать цвет, если они сразу увидят эффект при изменении оттенка, насыщенности или яркости.</span><span class="sxs-lookup"><span data-stu-id="073f8-123">For example, users can choose a color more easily by immediately seeing the effect of changes to hue, saturation, or luminosity values.</span></span>
-   <span data-ttu-id="073f8-124">**Параметр может принимать 4 и более значений?**</span><span class="sxs-lookup"><span data-stu-id="073f8-124">**Does the setting have a range of four or more values?**</span></span> <span data-ttu-id="073f8-125">Если нет — используйте переключатели.</span><span class="sxs-lookup"><span data-stu-id="073f8-125">If not, use radio buttons.</span></span>
-   <span data-ttu-id="073f8-126">**Может ли пользователь изменить значение?**</span><span class="sxs-lookup"><span data-stu-id="073f8-126">**Can the user change the value?**</span></span> <span data-ttu-id="073f8-127">Ползунки подразумевают взаимодействие с пользователем.</span><span class="sxs-lookup"><span data-stu-id="073f8-127">Sliders are for user interaction.</span></span> <span data-ttu-id="073f8-128">Если пользователь вообще не может изменить это значение, используйте [текстовое поле](ctrl-text-boxes.md) только для чтения.</span><span class="sxs-lookup"><span data-stu-id="073f8-128">If a user can't ever change the value, use a read-only [text box](ctrl-text-boxes.md) instead.</span></span>

<span data-ttu-id="073f8-129">Если можно использовать ползунок или текстовое поле, используйте числовое текстовое поле, если:</span><span class="sxs-lookup"><span data-stu-id="073f8-129">If a slider or a numeric text box is possible, use a numeric text box if:</span></span>

-   <span data-ttu-id="073f8-130">На экране недостаточно свободного места.</span><span class="sxs-lookup"><span data-stu-id="073f8-130">Screen space is tight.</span></span>
-   <span data-ttu-id="073f8-131">Пользователь, скорее всего, предпочитает использовать клавиатуру.</span><span class="sxs-lookup"><span data-stu-id="073f8-131">A user is likely to prefer using the keyboard.</span></span>

<span data-ttu-id="073f8-132">Используйте ползунок, если:</span><span class="sxs-lookup"><span data-stu-id="073f8-132">Use a slider if:</span></span>

-   <span data-ttu-id="073f8-133">Пользователям требуется мгновенный эффект при изменении значения параметра.</span><span class="sxs-lookup"><span data-stu-id="073f8-133">Users will benefit from instant feedback.</span></span>

## <a name="guidelines"></a><span data-ttu-id="073f8-134">Рекомендации</span><span class="sxs-lookup"><span data-stu-id="073f8-134">Guidelines</span></span>

-   <span data-ttu-id="073f8-135">**Придерживайтесь естественного расположения.**</span><span class="sxs-lookup"><span data-stu-id="073f8-135">**Use a natural orientation.**</span></span> <span data-ttu-id="073f8-136">Например, если ползунок представляет значения, имеющие аналоги в реальном мире, которые обычно отображаются по вертикали (например, температура), то используйте вертикальную ориентацию.</span><span class="sxs-lookup"><span data-stu-id="073f8-136">For example, if the slider represents a real-world value that is normally shown vertically (such as temperature), use a vertical orientation.</span></span>
-   <span data-ttu-id="073f8-137">**Ориентация ползунка для отражения языка и региональных параметров пользователей.**</span><span class="sxs-lookup"><span data-stu-id="073f8-137">**Orient the slider to reflect the culture of your users.**</span></span> <span data-ttu-id="073f8-138">Например, западных языков и региональных параметров считываются слева направо, поэтому для горизонтальных ползунков Поместите нижний конец диапазона слева, а верхний элемент справа.</span><span class="sxs-lookup"><span data-stu-id="073f8-138">For example, Western cultures read from left to right, so for horizontal sliders, put the low end of the range on the left and the high end on the right.</span></span> <span data-ttu-id="073f8-139">Для языков и региональных параметров, считываемых справа налево, выполните обратное.</span><span class="sxs-lookup"><span data-stu-id="073f8-139">For cultures that read from right to left, do the opposite.</span></span>
-   <span data-ttu-id="073f8-140">**Задайте размер элемента управления, чтобы пользователь мог легко задать нужное значение.**</span><span class="sxs-lookup"><span data-stu-id="073f8-140">**Size the control so that a user can easily set the desired value.**</span></span> <span data-ttu-id="073f8-141">Для параметров с дискретными значениями убедитесь, что любое из значений легко выбрать с помощью мыши.</span><span class="sxs-lookup"><span data-stu-id="073f8-141">For settings with discrete values, make sure the user can easily select any value using the mouse.</span></span>
-   <span data-ttu-id="073f8-142">**Попробуйте использовать нелинейную шкалу, если диапазон значений велик и пользователи, скорее всего, выберет значения в одном конце диапазона.**</span><span class="sxs-lookup"><span data-stu-id="073f8-142">**Consider using a non-linear scale if the range of values is large and users will likely select values at one end of the range.**</span></span> <span data-ttu-id="073f8-143">Например, значение времени может быть равно 1 минуте, 1 часу, 1 день или 1 месяц.</span><span class="sxs-lookup"><span data-stu-id="073f8-143">For example, time value might be 1 minute, 1 hour, 1 day, or 1 month.</span></span>
-   <span data-ttu-id="073f8-144">**По возможности применяйте немедленную обратную связь во время или после того, как пользователь сделает выбор.**</span><span class="sxs-lookup"><span data-stu-id="073f8-144">**Whenever practical, give immediate feedback while or after a user makes a selection.**</span></span> <span data-ttu-id="073f8-145">Например, звуковый элемент управления громкостью Microsoft Windows указывает на получившийся звуковой том.</span><span class="sxs-lookup"><span data-stu-id="073f8-145">For example, the Microsoft Windows volume control beeps to indicate the resulting audio volume.</span></span>
-   <span data-ttu-id="073f8-146">**Используйте метки для показа диапазона значений.**</span><span class="sxs-lookup"><span data-stu-id="073f8-146">**Use labels to show the range of values.**</span></span>

    <span data-ttu-id="073f8-147">**Исключение:** Если ползунок ориентирован вертикально и верхняя метка является максимальной, высокой, более или эквивалентной, можно опустить другие метки, так как это значение ясно.</span><span class="sxs-lookup"><span data-stu-id="073f8-147">**Exception:** If the slider is vertically oriented and the top label is Maximum, High, More, or equivalent, you can omit the other labels since the meaning is clear.</span></span>

    ![<span data-ttu-id="073f8-148">Рисунок вертикального ползунка</span><span class="sxs-lookup"><span data-stu-id="073f8-148">figure of a vertical slider</span></span> ](images/ctrl-sliders-image2.png)

    <span data-ttu-id="073f8-149">В этом примере вертикальная ориентация ползунка делает метки диапазона ненужными.</span><span class="sxs-lookup"><span data-stu-id="073f8-149">In this example, the slider's vertical orientation makes the range labels unnecessary.</span></span>

-   <span data-ttu-id="073f8-150">**Используйте деления, если пользователям необходимо знать приблизительное значение параметра.**</span><span class="sxs-lookup"><span data-stu-id="073f8-150">**Use tick marks when users need to know the approximate value of the setting.**</span></span>
-   <span data-ttu-id="073f8-151">**Используйте деления и метку значения, если пользователям необходимо знать точное значение выбранного параметра.**</span><span class="sxs-lookup"><span data-stu-id="073f8-151">**Use tick marks and a value label when users need to know the exact value of the setting they choose.**</span></span> <span data-ttu-id="073f8-152">Всегда используйте метку значения, если пользователю необходимо получить сведения об этих единицах, чтобы иметь представление о параметре.</span><span class="sxs-lookup"><span data-stu-id="073f8-152">Always use a value label if a user needs to know the units to make sense of the setting.</span></span>

    ![<span data-ttu-id="073f8-153">Рисунок ползунка, показывающего число пикселов, выбранных</span><span class="sxs-lookup"><span data-stu-id="073f8-153">figure of slider showing number of pixels selected</span></span> ](images/ctrl-sliders-image3.png)

    <span data-ttu-id="073f8-154">В этом примере метка используется для четкого обозначения выбранного значения.</span><span class="sxs-lookup"><span data-stu-id="073f8-154">In this example, a label is used to clearly indicate the selected value.</span></span>

-   <span data-ttu-id="073f8-155">**Для горизонтально ориентированных ползунков поместите деления под ползунком.**</span><span class="sxs-lookup"><span data-stu-id="073f8-155">**For horizontally-oriented sliders, place tick marks under the slider.**</span></span> <span data-ttu-id="073f8-156">Для вертикально-ориентированных ползунков поместите деления вправо для западных языков и региональных параметров. для языков и региональных параметров, считываемых справа налево, выполните обратное.</span><span class="sxs-lookup"><span data-stu-id="073f8-156">For vertically-oriented sliders, place tick marks to the right for Western cultures; for cultures that read from right to left, do the opposite.</span></span>
-   <span data-ttu-id="073f8-157">**Поместите метку значения в элемент управления "ползунок", чтобы связь была четкой.**</span><span class="sxs-lookup"><span data-stu-id="073f8-157">**Place the value label completely under the slider control so that the relationship is clear.**</span></span>

    <span data-ttu-id="073f8-158">**Неправильно**:</span><span class="sxs-lookup"><span data-stu-id="073f8-158">**Incorrect:**</span></span>

    ![<span data-ttu-id="073f8-159">Рисунок метки, которая длиннее ее ползунка</span><span class="sxs-lookup"><span data-stu-id="073f8-159">figure of a label that is longer than its slider</span></span> ](images/ctrl-sliders-image4.png)

    <span data-ttu-id="073f8-160">В этом примере метка значения не согласуется под ползунком.</span><span class="sxs-lookup"><span data-stu-id="073f8-160">In this example, the value label isn't aligned under the slider.</span></span>

-   <span data-ttu-id="073f8-161">**При отключении ползунка также отключаются все связанные метки.**</span><span class="sxs-lookup"><span data-stu-id="073f8-161">**When disabling a slider, also disable any associated labels.**</span></span>
-   <span data-ttu-id="073f8-162">**Для одного и того же параметра не следует использовать как ползунок, так и числовое текстовое поле.**</span><span class="sxs-lookup"><span data-stu-id="073f8-162">**Don't use both a slider and a numeric text box for the same setting.**</span></span> <span data-ttu-id="073f8-163">Используйте только более подходящий элемент управления.</span><span class="sxs-lookup"><span data-stu-id="073f8-163">Use only the more appropriate control.</span></span>

    <span data-ttu-id="073f8-164">**Исключение:** Используйте оба элемента управления, когда пользователю нужно немедленно оставить отзыв и возможность задать точное числовое значение.</span><span class="sxs-lookup"><span data-stu-id="073f8-164">**Exception:** Use both controls when the user needs both immediate feedback and the ability to set an exact numeric value.</span></span>

-   <span data-ttu-id="073f8-165">**Не используйте ползунок в качестве индикатора хода выполнения.**</span><span class="sxs-lookup"><span data-stu-id="073f8-165">**Don't use a slider as a progress indicator.**</span></span>
-   <span data-ttu-id="073f8-166">**Не меняйте размер индикатора ползунка от размера по умолчанию.**</span><span class="sxs-lookup"><span data-stu-id="073f8-166">**Don't change the size of the slider indicator from the default size.**</span></span>

    <span data-ttu-id="073f8-167">**Неправильно**:</span><span class="sxs-lookup"><span data-stu-id="073f8-167">**Incorrect:**</span></span>

    ![<span data-ttu-id="073f8-168">Рисунок ползунка, размер которого меньше значения по умолчанию</span><span class="sxs-lookup"><span data-stu-id="073f8-168">figure of slider that is smaller than the default</span></span> ](images/ctrl-sliders-image5.png)

    <span data-ttu-id="073f8-169">В этом примере используется размер, меньший, чем используемый по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="073f8-169">In this example, a size smaller than the default is used.</span></span>

    <span data-ttu-id="073f8-170">**Правильно:**</span><span class="sxs-lookup"><span data-stu-id="073f8-170">**Correct:**</span></span>

    ![<span data-ttu-id="073f8-171">Рисунок, показывающий ползунок по умолчанию</span><span class="sxs-lookup"><span data-stu-id="073f8-171">figure showing the default slider</span></span> ](images/ctrl-sliders-image6.png)

    <span data-ttu-id="073f8-172">В этом примере используется размер по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="073f8-172">In this example, the default size is used.</span></span>

-   <span data-ttu-id="073f8-173">**Не помечать каждую деление.**</span><span class="sxs-lookup"><span data-stu-id="073f8-173">**Don't label every tick mark.**</span></span>

## <a name="recommended-sizing-and-spacing"></a><span data-ttu-id="073f8-174">Рекомендуемое изменение размера и расстояния</span><span class="sxs-lookup"><span data-stu-id="073f8-174">Recommended sizing and spacing</span></span>

![<span data-ttu-id="073f8-175">Рисунок рекомендуемого размера и интервала ползунка</span><span class="sxs-lookup"><span data-stu-id="073f8-175">figure of recommended slider sizing and spacing</span></span> ](images/ctrl-sliders-image7.png)

<span data-ttu-id="073f8-176">Рекомендуемый размер и интервал для ползунков.</span><span class="sxs-lookup"><span data-stu-id="073f8-176">Recommended sizing and spacing for sliders.</span></span>

## <a name="labels"></a><span data-ttu-id="073f8-177">Метки</span><span class="sxs-lookup"><span data-stu-id="073f8-177">Labels</span></span>

### <a name="slider-labels"></a><span data-ttu-id="073f8-178">Метки ползунка</span><span class="sxs-lookup"><span data-stu-id="073f8-178">Slider labels</span></span>

-   <span data-ttu-id="073f8-179">Используйте статическую текстовую метку, завершающуюся двоеточием, или метку поля группы без закрывающих знаков препинания.</span><span class="sxs-lookup"><span data-stu-id="073f8-179">Use a static text label ending with a colon, or a group box label with no ending punctuation.</span></span>
-   <span data-ttu-id="073f8-180">Присвойте каждой метке уникальный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="073f8-180">Assign a unique access key to each label.</span></span> <span data-ttu-id="073f8-181">Рекомендации по назначению см. в разделе [Клавиатура](inter-keyboard.md).</span><span class="sxs-lookup"><span data-stu-id="073f8-181">For assignment guidelines, see [Keyboard](inter-keyboard.md).</span></span>
-   <span data-ttu-id="073f8-182">Используйте выделение прописных букв, как в предложении.</span><span class="sxs-lookup"><span data-stu-id="073f8-182">Use sentence-style capitalization.</span></span>
-   <span data-ttu-id="073f8-183">Поместите метку ползунка либо слева от ползунка, либо выше и выровняйте ее по левому краю ползунка (или его левого идентификатора диапазона, если он есть).</span><span class="sxs-lookup"><span data-stu-id="073f8-183">Position the slider label either to the left of the slider, or above and aligned with the left edge of the slider (or its left range identifier, if present).</span></span>

### <a name="range-labels"></a><span data-ttu-id="073f8-184">Метки диапазона</span><span class="sxs-lookup"><span data-stu-id="073f8-184">Range labels</span></span>

-   <span data-ttu-id="073f8-185">Указывайте метки на обоих концах ползунка (за исключением случаев, когда это не требуется при вертикальной ориентации ползунка).</span><span class="sxs-lookup"><span data-stu-id="073f8-185">Label the two ends of the slider range, unless a vertical orientation makes this unnecessary.</span></span>
-   <span data-ttu-id="073f8-186">Для каждой метки используйте только слово, если это возможно.</span><span class="sxs-lookup"><span data-stu-id="073f8-186">Use only word, if possible, for each label.</span></span>
-   <span data-ttu-id="073f8-187">Не используйте знаки препинания в конце метки.</span><span class="sxs-lookup"><span data-stu-id="073f8-187">Don't use ending punctuation.</span></span>
-   <span data-ttu-id="073f8-188">Убедитесь, что метки носят описательный характер и имеют параллельные значения.</span><span class="sxs-lookup"><span data-stu-id="073f8-188">Make sure these labels are descriptive and parallel.</span></span> <span data-ttu-id="073f8-189">Примеры "Максимум/минимум", "Больше/меньше", "Громко/тихо".</span><span class="sxs-lookup"><span data-stu-id="073f8-189">Examples: Maximum/Minimum, More/Less, Low/High, Soft/Loud.</span></span>
-   <span data-ttu-id="073f8-190">Используйте выделение прописных букв, как в предложении.</span><span class="sxs-lookup"><span data-stu-id="073f8-190">Use sentence-style capitalization.</span></span>
-   <span data-ttu-id="073f8-191">Не присваивайте ключи доступа.</span><span class="sxs-lookup"><span data-stu-id="073f8-191">Don't assign access keys.</span></span>

### <a name="value-labels"></a><span data-ttu-id="073f8-192">Метки значений</span><span class="sxs-lookup"><span data-stu-id="073f8-192">Value labels</span></span>

-   <span data-ttu-id="073f8-193">Если требуется использовать метку значения, располагайте ее под ползунком.</span><span class="sxs-lookup"><span data-stu-id="073f8-193">If you need a value label, display it below the slider.</span></span>
-   <span data-ttu-id="073f8-194">Выровняйте текст относительно элемента управления и добавьте единицы измерения (например, пиксели).</span><span class="sxs-lookup"><span data-stu-id="073f8-194">Center the text relative to the control and include the units (such as pixels).</span></span>

    ![<span data-ttu-id="073f8-195">Рисунок метки в центре ползунка</span><span class="sxs-lookup"><span data-stu-id="073f8-195">figure of label centered under the slider</span></span> ](images/ctrl-sliders-image8.png)

    <span data-ttu-id="073f8-196">В этом примере метка значения центрируется под ползунком и включает единицы измерения.</span><span class="sxs-lookup"><span data-stu-id="073f8-196">In this example, the value label is centered under the slider and includes the units.</span></span>

## <a name="documentation"></a><span data-ttu-id="073f8-197">Документация</span><span class="sxs-lookup"><span data-stu-id="073f8-197">Documentation</span></span>

<span data-ttu-id="073f8-198">При ссылке на ползунки:</span><span class="sxs-lookup"><span data-stu-id="073f8-198">When referring to sliders:</span></span>

-   <span data-ttu-id="073f8-199">Используйте точный текст метки, включая его прописную букву, и включите ползунок слова.</span><span class="sxs-lookup"><span data-stu-id="073f8-199">Use the exact label text, including its capitalization, and include the word slider.</span></span> <span data-ttu-id="073f8-200">Не включайте символ подчеркивания или двоеточие.</span><span class="sxs-lookup"><span data-stu-id="073f8-200">Don't include the access key underscore or colon.</span></span>
-   <span data-ttu-id="073f8-201">Чтобы описать взаимодействие с пользователем, используйте Move.</span><span class="sxs-lookup"><span data-stu-id="073f8-201">To describe user interaction, use move.</span></span>
-   <span data-ttu-id="073f8-202">По возможности отформатируйте метку, используя полужирный текст.</span><span class="sxs-lookup"><span data-stu-id="073f8-202">When possible, format the label using bold text.</span></span> <span data-ttu-id="073f8-203">В противном случае заключите метку в кавычки, только если это необходимо для предотвращения путаницы.</span><span class="sxs-lookup"><span data-stu-id="073f8-203">Otherwise, put the label in quotation marks only if required to prevent confusion.</span></span>

<span data-ttu-id="073f8-204">Пример. чтобы увеличить разрешение экрана, переместите ползунок **разрешения экрана** вправо.</span><span class="sxs-lookup"><span data-stu-id="073f8-204">Example: To increase your screen resolution, move the **Screen resolution** slider to the right.</span></span>

## <a name="related-topics"></a><span data-ttu-id="073f8-205">См. также</span><span class="sxs-lookup"><span data-stu-id="073f8-205">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="073f8-206">Словарь терминов</span><span class="sxs-lookup"><span data-stu-id="073f8-206">Glossary</span></span>](glossary.md)
</dt> </dl>

 

 