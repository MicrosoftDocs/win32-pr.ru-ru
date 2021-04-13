---
title: Элементы управления "Счетчик"
description: С помощью элемента управления "Счетчик" пользователи могут нажать кнопки со стрелками, чтобы изменить постепенное значение в связанном текстовом поле.
ms.assetid: 5f791fb9-1354-41b9-a9de-ddab35302d50
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 54ce622983e52d65fa58ef05aca783ff67ebce66
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/10/2021
ms.locfileid: "104351102"
---
# <a name="spin-controls"></a><span data-ttu-id="cdc84-103">Элементы управления "Счетчик"</span><span class="sxs-lookup"><span data-stu-id="cdc84-103">Spin Controls</span></span>

> [!NOTE]
> <span data-ttu-id="cdc84-104">Это руководство по проектированию было создано для Windows 7 и не Обновлено для более новых версий Windows.</span><span class="sxs-lookup"><span data-stu-id="cdc84-104">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="cdc84-105">Многие рекомендации по-прежнему применяются в принципе, но презентация и примеры не соответствуют нашим [текущим руководствам по проектированию](/windows/uwp/design/).</span><span class="sxs-lookup"><span data-stu-id="cdc84-105">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="cdc84-106">С помощью элемента управления "Счетчик" пользователи могут нажать кнопки со стрелками, чтобы изменить постепенное значение в связанном [текстовом поле](ctrl-text-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="cdc84-106">With a spin control, users can click arrow buttons to change incrementally the value within its associated [numeric text box](ctrl-text-boxes.md).</span></span> <span data-ttu-id="cdc84-107">Поле «Счетчик терминов» относится к сочетанию текстового поля и связанного с ним элемента управления «счетчик».</span><span class="sxs-lookup"><span data-stu-id="cdc84-107">The term spin box refers to the combination of a text box and its associated spin control.</span></span>

![<span data-ttu-id="cdc84-108">снимок экрана элемента управления "Счетчик" и текстового поля</span><span class="sxs-lookup"><span data-stu-id="cdc84-108">screen shot of spin control and text box</span></span> ](images/ctrl-spin-controls-image1.png)

<span data-ttu-id="cdc84-109">Типичный регулятор.</span><span class="sxs-lookup"><span data-stu-id="cdc84-109">A typical spin box.</span></span>

<span data-ttu-id="cdc84-110">Пользователи часто предпочитают элементы управления "Счетчик", так как они могут вносить изменения, не перемещая их руки от мыши.</span><span class="sxs-lookup"><span data-stu-id="cdc84-110">Users often prefer spin controls because they can make changes without moving their hands from the mouse.</span></span> <span data-ttu-id="cdc84-111">Если элемент управления "Счетчик" связан с текстовым полем, пользователи могут вводить или вставлять данные непосредственно в текстовое поле, поэтому использование элемента управления "Счетчик" является необязательным.</span><span class="sxs-lookup"><span data-stu-id="cdc84-111">When the spin control is paired with a text box, users can type or paste input directly in the text box, so use of the spin control is optional.</span></span>

<span data-ttu-id="cdc84-112">Хотя элементы управления "Счетчик" используются для числовых входных данных, входные данные не должны быть целым числом.</span><span class="sxs-lookup"><span data-stu-id="cdc84-112">While spin controls are used for numeric input, the input doesn't have to be a pure whole number.</span></span> <span data-ttu-id="cdc84-113">Входные данные могут быть десятичными числами и могут иметь отрицательные знаки, разделители (например, двоеточия или дефисы) и модификаторы единиц.</span><span class="sxs-lookup"><span data-stu-id="cdc84-113">The input can be decimal numbers and it can have negative signs, delimiters (such as colons or hyphens), and unit modifiers.</span></span>

> [!Note]  
> <span data-ttu-id="cdc84-114">Рекомендации, связанные с [текстовыми полями](ctrl-text-boxes.md) и [макетом](vis-layout.md) , представлены в отдельных статьях.</span><span class="sxs-lookup"><span data-stu-id="cdc84-114">Guidelines related to [text boxes](ctrl-text-boxes.md) and [layout](vis-layout.md) are presented in separate articles.</span></span>

 

## <a name="is-this-the-right-control"></a><span data-ttu-id="cdc84-115">Выбор правильного элемента управления</span><span class="sxs-lookup"><span data-stu-id="cdc84-115">Is this the right control?</span></span>

<span data-ttu-id="cdc84-116">Чтобы определиться, ответьте на вопросы:</span><span class="sxs-lookup"><span data-stu-id="cdc84-116">To decide, consider these questions:</span></span>

-   <span data-ttu-id="cdc84-117">**Используется ли элемент управления для числовых входных данных?**</span><span class="sxs-lookup"><span data-stu-id="cdc84-117">**Is the control used for numeric input?**</span></span> <span data-ttu-id="cdc84-118">Если нет, используйте другой элемент управления, например [раскрывающийся список](/windows/desktop/uxguide/ctrl-drop) или [ползунок](ctrl-sliders.md), для выбора из фиксированного набора значений.</span><span class="sxs-lookup"><span data-stu-id="cdc84-118">If not, use another control, such as a [drop-down list](/windows/desktop/uxguide/ctrl-drop) or [slider](ctrl-sliders.md), to select from a fixed set of values.</span></span> <span data-ttu-id="cdc84-119">Используйте полосы прокрутки для прокрутки.</span><span class="sxs-lookup"><span data-stu-id="cdc84-119">Use scroll bars for scrolling.</span></span>
-   <span data-ttu-id="cdc84-120">**Пользователи считают значение относительным количеством, а не числовым значением?**</span><span class="sxs-lookup"><span data-stu-id="cdc84-120">**Do users think of the value as a relative quantity, not a numeric value?**</span></span> <span data-ttu-id="cdc84-121">Если да, используйте вместо него ползунок.</span><span class="sxs-lookup"><span data-stu-id="cdc84-121">If so, use a slider instead.</span></span> <span data-ttu-id="cdc84-122">Используйте поля счетчика только для точных и известных числовых значений.</span><span class="sxs-lookup"><span data-stu-id="cdc84-122">Use spin boxes only for exact, known numeric values.</span></span> <span data-ttu-id="cdc84-123">Например: как правило, пользователи хотят уменьшить громкость до минимума или наполовину, а не задать значение 2 или 5.</span><span class="sxs-lookup"><span data-stu-id="cdc84-123">For example, users think about setting their audio volume to low or medium—not about setting the value to 2 or 5.</span></span>
-   <span data-ttu-id="cdc84-124">**Связан ли элемент управления с текстовым полем?**</span><span class="sxs-lookup"><span data-stu-id="cdc84-124">**Is the control paired with a text box?**</span></span> <span data-ttu-id="cdc84-125">Если нет, не используйте.</span><span class="sxs-lookup"><span data-stu-id="cdc84-125">If not, don't use.</span></span> <span data-ttu-id="cdc84-126">Элементы управления "Счетчик" не должны использоваться отдельно или с другими типами элементов управления, кроме текстового поля.</span><span class="sxs-lookup"><span data-stu-id="cdc84-126">Spin controls shouldn't be used alone or with other types of controls besides a text box.</span></span>

    <span data-ttu-id="cdc84-127">**Неправильно**:</span><span class="sxs-lookup"><span data-stu-id="cdc84-127">**Incorrect:**</span></span>

    ![<span data-ttu-id="cdc84-128">снимок экрана: элемент управления "Счетчик", графика, текстовое поле</span><span class="sxs-lookup"><span data-stu-id="cdc84-128">screen shot of spin control, graphic, no text box</span></span> ](images/ctrl-spin-controls-image2.png)

    <span data-ttu-id="cdc84-129">В этом примере для управления динамическим графиком используется элемент управления "Счетчик".</span><span class="sxs-lookup"><span data-stu-id="cdc84-129">In this example, a spin control is used to control a dynamic graphic.</span></span>

-   <span data-ttu-id="cdc84-130">**Допустимы ли непрерывные диапазоны значений?**</span><span class="sxs-lookup"><span data-stu-id="cdc84-130">**Are contiguous value ranges valid?**</span></span> <span data-ttu-id="cdc84-131">В противном случае используйте раскрывающийся список допустимых значений.</span><span class="sxs-lookup"><span data-stu-id="cdc84-131">If not, use a drop-down list of valid values instead.</span></span>

    ![<span data-ttu-id="cdc84-132">снимок экрана с раскрывающимся списком</span><span class="sxs-lookup"><span data-stu-id="cdc84-132">screen shot of drop-down list</span></span> ](images/ctrl-spin-controls-image3.png)

    <span data-ttu-id="cdc84-133">В этом примере не все номера дисков являются допустимыми, поэтому раскрывающийся список лучше всего подходит для выбора.</span><span class="sxs-lookup"><span data-stu-id="cdc84-133">In this example, not all disk drive numbers are valid, so a drop-down list is a better choice.</span></span>

-   <span data-ttu-id="cdc84-134">**Использует ли элемент управления "Счетчик" практически?**</span><span class="sxs-lookup"><span data-stu-id="cdc84-134">**Is using the spin control practical?**</span></span> <span data-ttu-id="cdc84-135">Использование элемента управления "Счетчик" целесообразно для следующих целей:</span><span class="sxs-lookup"><span data-stu-id="cdc84-135">Using a spin control is practical for:</span></span>

    -   <span data-ttu-id="cdc84-136">Ввод небольшого числа (обычно под номером 100).</span><span class="sxs-lookup"><span data-stu-id="cdc84-136">Entering a small number, typically under 100.</span></span>
    -   <span data-ttu-id="cdc84-137">Внесение небольших изменений в существующее значение или по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="cdc84-137">Making small changes to an existing or default value.</span></span>

    <span data-ttu-id="cdc84-138">Хотя элементы управления "Счетчик" могут использоваться для любого числового ввода, они не являются эффективными в ситуациях, отличных от этих.</span><span class="sxs-lookup"><span data-stu-id="cdc84-138">While spin controls can be used for any numeric input, they are inefficient in situations other than these.</span></span>

-   <span data-ttu-id="cdc84-139">**Полезен ли элемент управления "Счетчик"?**</span><span class="sxs-lookup"><span data-stu-id="cdc84-139">**Is the spin control helpful?**</span></span> <span data-ttu-id="cdc84-140">Используется ли элемент управления в контексте, где пользователи, скорее всего, будут использовать мышь?</span><span class="sxs-lookup"><span data-stu-id="cdc84-140">Is the control used in a context where users are likely to be using their mouse?</span></span> <span data-ttu-id="cdc84-141">В противном случае рассмотрим элемент управления "Счетчик" необязательно.</span><span class="sxs-lookup"><span data-stu-id="cdc84-141">If not, consider a spin control optional.</span></span>
-   <span data-ttu-id="cdc84-142">**Являются ли раскрывающиеся списки элементов управления уровнями?**</span><span class="sxs-lookup"><span data-stu-id="cdc84-142">**Are the sibling controls drop-down lists?**</span></span> <span data-ttu-id="cdc84-143">Если имеются другие раскрывающиеся списки, рассмотрите возможность использования раскрывающегося списка для обеспечения согласованности.</span><span class="sxs-lookup"><span data-stu-id="cdc84-143">If there are other drop-down lists, consider using a drop-down list for consistency.</span></span>

    ![<span data-ttu-id="cdc84-144">снимок экрана с диалоговым окном с раскрывающимися списками</span><span class="sxs-lookup"><span data-stu-id="cdc84-144">screen shot of dialog box with drop-down lists</span></span> ](images/ctrl-spin-controls-image4.png)

    <span data-ttu-id="cdc84-145">В этом примере можно использовать регулятор, но для обеспечения согласованности используется раскрывающийся список.</span><span class="sxs-lookup"><span data-stu-id="cdc84-145">In this example, a spin box could be used, but a drop-down list is used for consistency.</span></span>

-   <span data-ttu-id="cdc84-146">**Являются ли пользователи сенсорного ввода или пера первичной целью?**</span><span class="sxs-lookup"><span data-stu-id="cdc84-146">**Are touch or pen users a primary target?**</span></span> <span data-ttu-id="cdc84-147">Если да, рассмотрите возможность использования раскрывающегося списка.</span><span class="sxs-lookup"><span data-stu-id="cdc84-147">If so, consider using a drop-down list instead.</span></span> <span data-ttu-id="cdc84-148">Кнопки со стрелками в элементе управления "Счетчик" слишком малы для эффективного использования касанием или пером.</span><span class="sxs-lookup"><span data-stu-id="cdc84-148">The arrow buttons in a spin control are too small to be used efficiently with touch or a pen.</span></span>

<span data-ttu-id="cdc84-149">Если возможно использование ползунка или регулятора, используйте регулятор, если:</span><span class="sxs-lookup"><span data-stu-id="cdc84-149">If a slider or a spin box is possible, use a spin box if:</span></span>

-   <span data-ttu-id="cdc84-150">На экране недостаточно свободного места.</span><span class="sxs-lookup"><span data-stu-id="cdc84-150">Screen space is tight.</span></span>
-   <span data-ttu-id="cdc84-151">Пользователь, скорее всего, предпочитает использовать клавиатуру.</span><span class="sxs-lookup"><span data-stu-id="cdc84-151">A user is likely to prefer using the keyboard.</span></span>

<span data-ttu-id="cdc84-152">Используйте ползунок, если:</span><span class="sxs-lookup"><span data-stu-id="cdc84-152">Use a slider if:</span></span>

-   <span data-ttu-id="cdc84-153">Пользователям требуется мгновенный эффект при изменении значения параметра.</span><span class="sxs-lookup"><span data-stu-id="cdc84-153">Users will benefit from instant feedback.</span></span>

## <a name="guidelines"></a><span data-ttu-id="cdc84-154">Рекомендации</span><span class="sxs-lookup"><span data-stu-id="cdc84-154">Guidelines</span></span>

### <a name="general"></a><span data-ttu-id="cdc84-155">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="cdc84-155">General</span></span>

-   <span data-ttu-id="cdc84-156">**Используйте элементы управления "Счетчик", когда они практичны и полезны.**</span><span class="sxs-lookup"><span data-stu-id="cdc84-156">**Use spin controls whenever they are practical and helpful.**</span></span> <span data-ttu-id="cdc84-157">Видите [ли это нужный элемент управления?](#is-this-the-right-control)</span><span class="sxs-lookup"><span data-stu-id="cdc84-157">See [Is this the right control?](#is-this-the-right-control)</span></span>

    -   <span data-ttu-id="cdc84-158">**Исключение:** Чтобы обеспечить соответствие с другими текстовыми полями в одном пользовательском интерфейсе, используйте элементы управления "Счетчик", даже если они не всегда практичны.</span><span class="sxs-lookup"><span data-stu-id="cdc84-158">**Exception:** To be consistent with other text boxes on the same user interface (UI), use spin controls even if they aren't always practical.</span></span>

    <span data-ttu-id="cdc84-159">**Правильно:**</span><span class="sxs-lookup"><span data-stu-id="cdc84-159">**Correct:**</span></span>

    ![<span data-ttu-id="cdc84-160">снимок экрана: элементы управления "месяц", "день", "год"</span><span class="sxs-lookup"><span data-stu-id="cdc84-160">screen shot of month, day, year spin controls</span></span> ](images/ctrl-spin-controls-image5.png)

    <span data-ttu-id="cdc84-161">В этом примере элемент управления "Счетчик" используется с элементом управления "год" для обеспечения согласованности, хотя это не всегда целесообразно.</span><span class="sxs-lookup"><span data-stu-id="cdc84-161">In this example, a spin control is used with the year control for consistency, even though it isn't always practical.</span></span>

    <span data-ttu-id="cdc84-162">**Неправильно**:</span><span class="sxs-lookup"><span data-stu-id="cdc84-162">**Incorrect:**</span></span>

    ![<span data-ttu-id="cdc84-163">снимок экрана с элементом управления "Счетчик IP-адресов"</span><span class="sxs-lookup"><span data-stu-id="cdc84-163">screen shot of ip address spin control</span></span> ](images/ctrl-spin-controls-image6.png)

    <span data-ttu-id="cdc84-164">В этом примере элемент управления "Счетчик" непригоден для использования.</span><span class="sxs-lookup"><span data-stu-id="cdc84-164">In this example, the spin control is unusable.</span></span>

-   <span data-ttu-id="cdc84-165">**Всегда делайте счетчик "приятель" текстового поля.**</span><span class="sxs-lookup"><span data-stu-id="cdc84-165">**Always make a spin control the "buddy" of the text box.**</span></span> <span data-ttu-id="cdc84-166">При этом элемент управления "Счетчик" помещается в текстовое поле.</span><span class="sxs-lookup"><span data-stu-id="cdc84-166">Doing so places the spin control inside the text box.</span></span>

    <span data-ttu-id="cdc84-167">**Правильно:**</span><span class="sxs-lookup"><span data-stu-id="cdc84-167">**Correct:**</span></span>

    ![<span data-ttu-id="cdc84-168">снимок экрана элемента управления "Счетчик", помещенного внутрь текстового поля</span><span class="sxs-lookup"><span data-stu-id="cdc84-168">screen shot of spin control placed inside text box</span></span> ](images/ctrl-spin-controls-image7.png)

    <span data-ttu-id="cdc84-169">**Неправильно**:</span><span class="sxs-lookup"><span data-stu-id="cdc84-169">**Incorrect:**</span></span>

    ![<span data-ttu-id="cdc84-170">снимок экрана элемента управления "Счетчик", помещенного за пределы текстового поля</span><span class="sxs-lookup"><span data-stu-id="cdc84-170">screen shot of spin control placed outside text box</span></span> ](images/ctrl-spin-controls-image8.png)

    <span data-ttu-id="cdc84-171">В правильном примере элемент управления "Счетчик" помещается внутрь связанного текстового поля.</span><span class="sxs-lookup"><span data-stu-id="cdc84-171">In the correct example, the spin control is placed inside its associated text box.</span></span>

-   <span data-ttu-id="cdc84-172">**Отключить элемент управления "Счетчик", если его связанное текстовое поле отключено.**</span><span class="sxs-lookup"><span data-stu-id="cdc84-172">**Disable a spin control when its associated text box is disabled.**</span></span> <span data-ttu-id="cdc84-173">Элемент управления "Счетчик" — это дополнительный метод ввода — никогда не единственный метод ввода.</span><span class="sxs-lookup"><span data-stu-id="cdc84-173">The spin control is a supplemental input method—never the only input method.</span></span>

### <a name="values"></a><span data-ttu-id="cdc84-174">Значения</span><span class="sxs-lookup"><span data-stu-id="cdc84-174">Values</span></span>

-   <span data-ttu-id="cdc84-175">**Задайте верхнюю кнопку, чтобы увеличить значение на одну единицу, а нижнюю кнопку для уменьшения на единицу.**</span><span class="sxs-lookup"><span data-stu-id="cdc84-175">**Define the top button to increase the value by one unit and the bottom button to decrease by one unit.**</span></span> <span data-ttu-id="cdc84-176">Как правило, это единица измерения, но это должно быть наименьшее общее изменение в значении.</span><span class="sxs-lookup"><span data-stu-id="cdc84-176">Typically, the unit is one, but it should be the smallest common change in value.</span></span> <span data-ttu-id="cdc84-177">В идеале элемент управления "Счетчик" должен охватывать все допустимые значения, и он должен быть более удобным, чем ввод текста.</span><span class="sxs-lookup"><span data-stu-id="cdc84-177">Ideally, the spin control should cover all valid values, and it should be more convenient than typing in the text.</span></span>

    ![<span data-ttu-id="cdc84-178">снимок экрана элемента управления "поля"</span><span class="sxs-lookup"><span data-stu-id="cdc84-178">screen shot of 'margins' spin control</span></span> ](images/ctrl-spin-controls-image9.png)

    <span data-ttu-id="cdc84-179">В этом примере при щелчке элемента управления "Счетчик" значения изменяются на 0,1, что является наименьшим общим изменением значения.</span><span class="sxs-lookup"><span data-stu-id="cdc84-179">In this example, clicking a spin control changes the values by .1, which is the smallest common change in value.</span></span> <span data-ttu-id="cdc84-180">Использование меньшей единицы охватывает диапазон допустимых значений, но делает элементы управления "Счетчик" непригодными для использования.</span><span class="sxs-lookup"><span data-stu-id="cdc84-180">Using a smaller unit would cover the range of valid values but make the spin controls unusable.</span></span>

-   <span data-ttu-id="cdc84-181">**Используйте элемент управления "Счетчик", чтобы ограничить входные значения допустимыми значениями.**</span><span class="sxs-lookup"><span data-stu-id="cdc84-181">**Use the spin control to limit input to valid values.**</span></span> <span data-ttu-id="cdc84-182">Использование элемента управления "Счетчик" не должно приводить к неправильному значению.</span><span class="sxs-lookup"><span data-stu-id="cdc84-182">Using a spin control should never result in an incorrect value.</span></span>
-   <span data-ttu-id="cdc84-183">**В конце диапазона допустимых значений перезапустите диапазон.**</span><span class="sxs-lookup"><span data-stu-id="cdc84-183">**At the end of a range of valid values, restart the range.**</span></span> <span data-ttu-id="cdc84-184">Метафора контрольного цикла заключается в том, что пользователь вращает колесико значений, поэтому такое поведение подобно колесу.</span><span class="sxs-lookup"><span data-stu-id="cdc84-184">The spin control metaphor is that the user is spinning a wheel of values, hence this wheel-like behavior.</span></span>
    -   <span data-ttu-id="cdc84-185">**Исключение:** Не перезапускайте диапазон, если результирующее значение определено как неверное.</span><span class="sxs-lookup"><span data-stu-id="cdc84-185">**Exception:** Don't restart the range if the resulting value is certain to be incorrect.</span></span>

        ![<span data-ttu-id="cdc84-186">снимок экрана с элементом управления "число копий"</span><span class="sxs-lookup"><span data-stu-id="cdc84-186">screen shot of 'number of copies' spin control</span></span> ](images/ctrl-spin-controls-image10.png)

        <span data-ttu-id="cdc84-187">В этом примере при нажатии кнопки со стрелкой вниз диапазон не перезапускается (путем перехода к максимальному значению), так как это значение является неправильным.</span><span class="sxs-lookup"><span data-stu-id="cdc84-187">In this example, clicking the down arrow button doesn't restart the range (by going to the maximum value) because that value is certain to be incorrect.</span></span>

-   <span data-ttu-id="cdc84-188">**Используйте текст вместо специальных числовых значений.**</span><span class="sxs-lookup"><span data-stu-id="cdc84-188">**Use text instead of special numeric values.**</span></span> <span data-ttu-id="cdc84-189">Разрешить пользователям пропускать эти специальные значения, не зная их и не вводя их.</span><span class="sxs-lookup"><span data-stu-id="cdc84-189">Allow users to spin to these special values instead of having to know them and type them in.</span></span>

    ![<span data-ttu-id="cdc84-190">снимок экрана: элемент управления "спящий режим после (никогда)"</span><span class="sxs-lookup"><span data-stu-id="cdc84-190">screen shot of 'sleep after (never)' spin control</span></span> ](images/ctrl-spin-controls-image11.png)

    <span data-ttu-id="cdc84-191">В этом примере никогда не является специальным значением, но пользователи могут превращение в него.</span><span class="sxs-lookup"><span data-stu-id="cdc84-191">In this example, Never is a special value but users can spin to it.</span></span>

-   <span data-ttu-id="cdc84-192">**Если значение имеет разделители, то связанное текстовое поле должно иметь несколько входных точек фокуса.**</span><span class="sxs-lookup"><span data-stu-id="cdc84-192">**If the value has delimiters, the associated text box should have multiple input focus points.**</span></span> <span data-ttu-id="cdc84-193">Это позволяет управлять числовыми сегментами по отдельности.</span><span class="sxs-lookup"><span data-stu-id="cdc84-193">Doing so allows the numeric segments to be manipulated individually.</span></span>

    ![<span data-ttu-id="cdc84-194">снимок экрана: элемент управления "Счетчик времени", выбранные минуты</span><span class="sxs-lookup"><span data-stu-id="cdc84-194">screen shot of time spin control, minutes selected</span></span> ](images/ctrl-spin-controls-image12.png)

    <span data-ttu-id="cdc84-195">В этом примере элемент управления "Счетчик" влияет на значения часов, минут, секунд и/P.M., в зависимости от того, какое действие имеет фокус.</span><span class="sxs-lookup"><span data-stu-id="cdc84-195">In this example, the spin control affects the values for hours, minutes, seconds, and A.M./P.M.—whichever has the focus.</span></span>

-   <span data-ttu-id="cdc84-196">**Если значение равно единицам, используйте элемент управления "Счетчик", чтобы изменить эти единицы.**</span><span class="sxs-lookup"><span data-stu-id="cdc84-196">**If the value has units, use the spin control to change those units as well.**</span></span>

    ![<span data-ttu-id="cdc84-197">снимок экрана: элемент управления "Счетчик времени", "a.m."</span><span class="sxs-lookup"><span data-stu-id="cdc84-197">screen shot of time spin control, 'a.m.'</span></span> <span data-ttu-id="cdc84-198">Установлен</span><span class="sxs-lookup"><span data-stu-id="cdc84-198">selected</span></span> ](images/ctrl-spin-controls-image13.png)

    <span data-ttu-id="cdc84-199">В этом примере элемент управления "Счетчик" можно использовать для изменения единиц.</span><span class="sxs-lookup"><span data-stu-id="cdc84-199">In this example, the spin control can be used to change units.</span></span>

## <a name="labels"></a><span data-ttu-id="cdc84-200">Метки</span><span class="sxs-lookup"><span data-stu-id="cdc84-200">Labels</span></span>

-   <span data-ttu-id="cdc84-201">Примените рекомендации по [маркировке текстового поля](ctrl-text-boxes.md) , чтобы пометить соответствующее текстовое поле.</span><span class="sxs-lookup"><span data-stu-id="cdc84-201">Apply the [text box labeling](ctrl-text-boxes.md) guidelines to label the associated text box.</span></span> <span data-ttu-id="cdc84-202">Элементы управления "Счетчик" никогда не помечаются напрямую.</span><span class="sxs-lookup"><span data-stu-id="cdc84-202">Spin controls are never labeled directly.</span></span>

## <a name="documentation"></a><span data-ttu-id="cdc84-203">Документация</span><span class="sxs-lookup"><span data-stu-id="cdc84-203">Documentation</span></span>

<span data-ttu-id="cdc84-204">При ссылке на элементы управления "Счетчик":</span><span class="sxs-lookup"><span data-stu-id="cdc84-204">When referring to spin controls:</span></span>

-   <span data-ttu-id="cdc84-205">Не используйте элементы управления "Счетчик" в пользовательской документации.</span><span class="sxs-lookup"><span data-stu-id="cdc84-205">Don't refer to spin controls in user documentation.</span></span> <span data-ttu-id="cdc84-206">Вместо этого обратитесь к метке связанного текстового поля.</span><span class="sxs-lookup"><span data-stu-id="cdc84-206">Instead, refer to the label of the associated text box.</span></span>
-   <span data-ttu-id="cdc84-207">Используйте элементы управления "Счетчик" и "регуляторы" только в программировании и другой технической документации.</span><span class="sxs-lookup"><span data-stu-id="cdc84-207">Refer to spin controls and spin boxes only in programming and other technical documentation.</span></span>

<span data-ttu-id="cdc84-208">Пример. в поле **Дата** введите или выберите часть даты, которую требуется изменить.</span><span class="sxs-lookup"><span data-stu-id="cdc84-208">Example: In the **Date** box, type or select the part of the date you want to change.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cdc84-209">См. также</span><span class="sxs-lookup"><span data-stu-id="cdc84-209">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cdc84-210">Словарь терминов</span><span class="sxs-lookup"><span data-stu-id="cdc84-210">Glossary</span></span>](glossary.md)
</dt> </dl>

 

 