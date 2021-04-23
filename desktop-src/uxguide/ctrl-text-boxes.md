---
title: Текстовые поля
description: С помощью текстового поля пользователи могут отображать, вводить или редактировать текстовое или числовое значение.
ms.assetid: fb8ed262-1451-496d-a3f4-a29af39763bb
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 2b5257e9772465f26815abb0f6ecbe0ff357ba4b
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/10/2021
ms.locfileid: "104547271"
---
# <a name="text-boxes"></a><span data-ttu-id="c490f-103">Текстовые поля</span><span class="sxs-lookup"><span data-stu-id="c490f-103">Text Boxes</span></span>

> [!NOTE]
> <span data-ttu-id="c490f-104">Это руководство по проектированию было создано для Windows 7 и не Обновлено для более новых версий Windows.</span><span class="sxs-lookup"><span data-stu-id="c490f-104">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="c490f-105">Многие рекомендации по-прежнему применяются в принципе, но презентация и примеры не соответствуют нашим [текущим руководствам по проектированию](/windows/uwp/design/).</span><span class="sxs-lookup"><span data-stu-id="c490f-105">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="c490f-106">С помощью текстового поля пользователи могут отображать, вводить или редактировать текстовое или числовое значение.</span><span class="sxs-lookup"><span data-stu-id="c490f-106">With a text box, users can display, enter, or edit a text or numeric value.</span></span>

![<span data-ttu-id="c490f-107">снимок экрана обычного текстового поля и метки</span><span class="sxs-lookup"><span data-stu-id="c490f-107">screen shot of a typical text box and label</span></span> ](images/ctrl-text-boxes-image1.png)

<span data-ttu-id="c490f-108">Типичное текстовое поле.</span><span class="sxs-lookup"><span data-stu-id="c490f-108">A typical text box.</span></span>

> [!Note]  
> <span data-ttu-id="c490f-109">Рекомендации, связанные с [макетом](vis-layout.md), [шрифтами](vis-fonts.md)и [выносками](ctrl-balloons.md) , представлены в отдельных статьях.</span><span class="sxs-lookup"><span data-stu-id="c490f-109">Guidelines related to [layout](vis-layout.md), [fonts](vis-fonts.md), and [balloons](ctrl-balloons.md) are presented in separate articles.</span></span>

 

## <a name="is-this-the-right-control"></a><span data-ttu-id="c490f-110">Выбор правильного элемента управления</span><span class="sxs-lookup"><span data-stu-id="c490f-110">Is this the right control?</span></span>

<span data-ttu-id="c490f-111">Чтобы определиться, ответьте на вопросы:</span><span class="sxs-lookup"><span data-stu-id="c490f-111">To decide, consider these questions:</span></span>

-   <span data-ttu-id="c490f-112">**Целесообразно ли эффективно перечислять все допустимые значения?**</span><span class="sxs-lookup"><span data-stu-id="c490f-112">**Is it practical to enumerate all the valid values efficiently?**</span></span> <span data-ttu-id="c490f-113">В этом случае рассмотрим [список с одним выбором](ctrl-list-boxes.md), [представление списка](ctrl-list-views.md), раскрывающийся список, раскрывающийся список или [](/windows/desktop/uxguide/ctrl-drop) [ползунок](ctrl-sliders.md) .</span><span class="sxs-lookup"><span data-stu-id="c490f-113">If so, consider a [single-selection list](ctrl-list-boxes.md), [list view](ctrl-list-views.md), [drop-down list](/windows/desktop/uxguide/ctrl-drop), editable drop-down list, or [slider](ctrl-sliders.md) instead.</span></span>
-   <span data-ttu-id="c490f-114">**Все ли допустимые данные полностью неограниченны? Или является допустимым ограничением данных только по формату (длина ограниченного или символьного типа)?**</span><span class="sxs-lookup"><span data-stu-id="c490f-114">**Is the valid data completely unconstrained? Or is the valid data constrained only by format (constrained length or character types)?**</span></span> <span data-ttu-id="c490f-115">Если это так, используйте текстовое поле.</span><span class="sxs-lookup"><span data-stu-id="c490f-115">If so, use a text box.</span></span>
-   <span data-ttu-id="c490f-116">**Если значение представляет такой тип данных, который имеет особый общий элемент управления,**</span><span class="sxs-lookup"><span data-stu-id="c490f-116">**Does the value represent a data type that has a specialized common control?**</span></span> <span data-ttu-id="c490f-117">К примерам относятся Дата, время, адрес IPv4 или IPv6.</span><span class="sxs-lookup"><span data-stu-id="c490f-117">Examples include date, time, or IPv4 or IPv6 address.</span></span> <span data-ttu-id="c490f-118">Если это так, используйте соответствующий элемент управления, например элемент управления даты, а не текстовое поле.</span><span class="sxs-lookup"><span data-stu-id="c490f-118">If so, use the appropriate control, such as a date control rather than a text box.</span></span>
-   <span data-ttu-id="c490f-119">Если данные являются числовыми:</span><span class="sxs-lookup"><span data-stu-id="c490f-119">If the data is numeric:</span></span>
    -   <span data-ttu-id="c490f-120">**Пользователи воспринимают этот параметр как относительное количество?**</span><span class="sxs-lookup"><span data-stu-id="c490f-120">**Do users perceive the setting as a relative quantity?**</span></span> <span data-ttu-id="c490f-121">Если да, то используйте ползунок.</span><span class="sxs-lookup"><span data-stu-id="c490f-121">If so, use a slider.</span></span>
    -   <span data-ttu-id="c490f-122">**Требуется ли пользователю мгновенная обратная связь при изменении значения параметра?**</span><span class="sxs-lookup"><span data-stu-id="c490f-122">**Would the user benefit from instant feedback on the effect of setting changes?**</span></span> <span data-ttu-id="c490f-123">Если это так, используйте ползунок, возможно, вместе с текстовым полем.</span><span class="sxs-lookup"><span data-stu-id="c490f-123">If so, use a slider, possibly along with a text box.</span></span> <span data-ttu-id="c490f-124">Например, пользователи могут легко выбрать цвет с помощью ползунка, так как они могут сразу увидеть результат изменений в значениях тона, насыщенности или яркости.</span><span class="sxs-lookup"><span data-stu-id="c490f-124">For example, users can easily choose a color using a slider because they can immediately see the effect of changes to hue, saturation, or luminosity values.</span></span>

## <a name="design-concepts"></a><span data-ttu-id="c490f-125">Принципы проектирования</span><span class="sxs-lookup"><span data-stu-id="c490f-125">Design concepts</span></span>

<span data-ttu-id="c490f-126">Хотя текстовые поля обладают очень гибким преимуществом, у них есть недостаток ограничений с минимальными ограничениями.</span><span class="sxs-lookup"><span data-stu-id="c490f-126">While text boxes have the benefit of being very flexible, they have the drawback of having minimal constraints.</span></span> <span data-ttu-id="c490f-127">Единственными ограничениями для изменяемого текстового поля являются:</span><span class="sxs-lookup"><span data-stu-id="c490f-127">The only constraints on an editable text box are:</span></span>

-   <span data-ttu-id="c490f-128">При необходимости можно задать максимальное число символов.</span><span class="sxs-lookup"><span data-stu-id="c490f-128">You can optionally set the maximum number of characters.</span></span>
-   <span data-ttu-id="c490f-129">При необходимости можно ограничить ввод только числовыми символами (0 9).</span><span class="sxs-lookup"><span data-stu-id="c490f-129">You can optionally restrict input to numeric characters (0   9) only.</span></span>
-   <span data-ttu-id="c490f-130">Если используется [элемент управления "Счетчик"](ctrl-spin-controls.md), можно ограничить выбор элементов управления "Счетчик" до допустимых значений.</span><span class="sxs-lookup"><span data-stu-id="c490f-130">If you use a [spin control](ctrl-spin-controls.md), you can limit spin control choices to valid values.</span></span>

<span data-ttu-id="c490f-131">Помимо их длины и дополнительного присутствия элемента управления "Счетчик", текстовые поля не имеют визуальных оповещений, предлагающих допустимые значения или их формат.</span><span class="sxs-lookup"><span data-stu-id="c490f-131">Aside from their length and the optional presence of a spin control, text boxes don't have any visual clues that suggest the valid values or their format.</span></span> <span data-ttu-id="c490f-132">Это означает, что полагается на метки, чтобы передавать эти сведения пользователям.</span><span class="sxs-lookup"><span data-stu-id="c490f-132">This means relying on labels to convey this information to users.</span></span> <span data-ttu-id="c490f-133">Если пользователи вводят недопустимый текст, необходимо решить эту ошибку с помощью сообщения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="c490f-133">If users enter text that's not valid, you must handle the error with an error message.</span></span>

<span data-ttu-id="c490f-134">В качестве общего правила **следует использовать наиболее ограниченный элемент управления, который можно**.</span><span class="sxs-lookup"><span data-stu-id="c490f-134">As a general rule, **you should use the most constrained control that you can**.</span></span> <span data-ttu-id="c490f-135">Используйте неограниченные элементы управления, такие как текстовые поля, в качестве последнего средства.</span><span class="sxs-lookup"><span data-stu-id="c490f-135">Use unconstrained controls like text boxes as a last resort.</span></span> <span data-ttu-id="c490f-136">С другой стороны, при рассмотрении ограничений необходимо учитывать потребности глобальных пользователей.</span><span class="sxs-lookup"><span data-stu-id="c490f-136">That said, when you are considering constraints, bear in mind the needs of global users.</span></span> <span data-ttu-id="c490f-137">Например, элемент управления, ограниченный США почтовых ИНДЕКСов, не является глобализованным, но неограниченное текстовое поле, принимающее любой формат почтового индекса, —.</span><span class="sxs-lookup"><span data-stu-id="c490f-137">For example, a control that is constrained to United States ZIP Codes isn't globalized, but an unconstrained text box that accepts any postal code format is.</span></span>

## <a name="usage-patterns"></a><span data-ttu-id="c490f-138">Варианты использования</span><span class="sxs-lookup"><span data-stu-id="c490f-138">Usage patterns</span></span>

<span data-ttu-id="c490f-139">Текстовое поле — это гибкий элемент управления с несколькими возможными применениями.</span><span class="sxs-lookup"><span data-stu-id="c490f-139">A text box is a flexible control with several possible uses.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c490f-140"><strong>Входные данные</strong></span><span class="sxs-lookup"><span data-stu-id="c490f-140"><strong>Data input</strong></span></span><br/> <span data-ttu-id="c490f-141">Однострочное неограниченное текстовое поле, используемое для ввода или редактирования коротких строк.</span><span class="sxs-lookup"><span data-stu-id="c490f-141">A single-line, unconstrained text box used to enter or edit short strings.</span></span><br/></td>
<td><img src="images/ctrl-text-boxes-image2.png" alt="Screen shot of a text box with Display name label " /><br/> <span data-ttu-id="c490f-142">Однострочное неограниченное текстовое поле.</span><span class="sxs-lookup"><span data-stu-id="c490f-142">A single-line, unconstrained text box.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c490f-143"><strong>Ввод форматированных данных</strong></span><span class="sxs-lookup"><span data-stu-id="c490f-143"><strong>Formatted data input</strong></span></span><br/> <span data-ttu-id="c490f-144">Набор коротких однострочных текстовых полей фиксированного размера, используемых для ввода данных в определенном формате.</span><span class="sxs-lookup"><span data-stu-id="c490f-144">A set of short, fixed-sized, single-line text boxes used to enter data with a specific format.</span></span> <br/></td>
<td><img src="images/ctrl-text-boxes-image3.png" alt="Screen shot of a Product key text box " /><br/> <span data-ttu-id="c490f-145">Текстовое поле, используемое для форматированного ввода данных.</span><span class="sxs-lookup"><span data-stu-id="c490f-145">A text box used for formatted data input.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="c490f-146">Функция <a href="glossary.md">автоматического выхода</a> автоматически перемещает фокус ввода с одного текстового поля на другое.</span><span class="sxs-lookup"><span data-stu-id="c490f-146">The <a href="glossary.md">auto-exit</a> feature automatically advances the input focus from one text box to the next.</span></span> <span data-ttu-id="c490f-147">Одним из недостатков этого подхода является то, что данные нельзя копировать или вставлять как единое целое.</span><span class="sxs-lookup"><span data-stu-id="c490f-147">One disadvantage to this approach is that the data can't be copied or pasted as a single unit.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c490f-148"><strong>Ввод данных с выбором</strong></span><span class="sxs-lookup"><span data-stu-id="c490f-148"><strong>Assisted data input</strong></span></span><br/> <span data-ttu-id="c490f-149">Однострочное, неограниченное текстовое поле, используемое для ввода или редактирования строк, в сочетании с кнопкой, позволяющей пользователям выбирать допустимые значения.</span><span class="sxs-lookup"><span data-stu-id="c490f-149">A single-line, unconstrained text box used to enter or edit strings, combined with a command button that helps users select valid values.</span></span><br/></td>
<td><img src="images/ctrl-text-boxes-image4.png" alt="Screen shot of text box with Browse button" /><br/> <span data-ttu-id="c490f-150">В этом примере команда Browse помогает пользователям выбрать допустимые значения.</span><span class="sxs-lookup"><span data-stu-id="c490f-150">In this example, the Browse command helps users select valid values.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c490f-151"><strong>Текстовый ввод</strong></span><span class="sxs-lookup"><span data-stu-id="c490f-151"><strong>Textual input</strong></span></span><br/> <span data-ttu-id="c490f-152">Многострочное, неограниченное текстовое поле, используемое для ввода или редактирования длинных строк.</span><span class="sxs-lookup"><span data-stu-id="c490f-152">A multi-line, unconstrained text box used to enter or edit long strings.</span></span> <br/></td>
<td><img src="images/ctrl-text-boxes-image5.png" alt="Screen shot of an Address text box " /><br/> <span data-ttu-id="c490f-153">Многострочное, неограниченное текстовое поле.</span><span class="sxs-lookup"><span data-stu-id="c490f-153">A multi-line, unconstrained text box.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c490f-154"><strong>Числовой ввод</strong></span><span class="sxs-lookup"><span data-stu-id="c490f-154"><strong>Numeric input</strong></span></span><br/> <span data-ttu-id="c490f-155">Однострочное текстовое поле с числовым значением, используемое для ввода или изменения чисел, с необязательным <a href="ctrl-spin-controls.md">элементом управления "Счетчик"</a> для упрощения ввода на основе мыши.</span><span class="sxs-lookup"><span data-stu-id="c490f-155">A single-line, numeric-only text box used to enter or edit numbers, with an optional <a href="ctrl-spin-controls.md">spin control</a> to facilitate mouse-based input.</span></span> <br/></td>
<td><img src="images/ctrl-text-boxes-image6.png" alt="Screen shot of a text box for entering a wait time " /><br/> <span data-ttu-id="c490f-156">Текстовое поле, используемое для числовых входных данных.</span><span class="sxs-lookup"><span data-stu-id="c490f-156">A text box used for numeric input.</span></span><br/> <span data-ttu-id="c490f-157">Сочетание текстового поля и связанного с ним элемента управления "Счетчик" называется <a href="ctrl-spin-controls.md">регулятором</a>.</span><span class="sxs-lookup"><span data-stu-id="c490f-157">The combination of a text box and its associated spin control is called a <a href="ctrl-spin-controls.md">spin box</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c490f-158"><strong>Ввод пароля и ПИН-кода</strong></span><span class="sxs-lookup"><span data-stu-id="c490f-158"><strong>Password and PIN input</strong></span></span><br/> <span data-ttu-id="c490f-159">Однострочное, неограниченное текстовое поле, используемое для безопасного ввода паролей и ПИН-кодов.</span><span class="sxs-lookup"><span data-stu-id="c490f-159">A single-line, unconstrained text box used to enter passwords and PINs securely.</span></span><br/></td>
<td><img src="images/ctrl-text-boxes-image7.png" alt="Screen shot of a Password text box " /><br/> <span data-ttu-id="c490f-160">Текстовое поле, используемое для ввода паролей.</span><span class="sxs-lookup"><span data-stu-id="c490f-160">A text box used to enter passwords.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c490f-161"><strong>Выходные данные</strong></span><span class="sxs-lookup"><span data-stu-id="c490f-161"><strong>Data output</strong></span></span><br/> <span data-ttu-id="c490f-162">Однострочное текстовое поле только для чтения, которое всегда отображается без границы, используемое для отображения коротких строк.</span><span class="sxs-lookup"><span data-stu-id="c490f-162">A single-line, read-only text box, always displayed without a border, used to display short strings.</span></span> <br/></td>
<td><span data-ttu-id="c490f-163">В отличие от статического текста, данные, отображаемые с помощью текстового поля, можно прокручивать (удобно, если данные шире элемента управления), выбраны и скопированы.</span><span class="sxs-lookup"><span data-stu-id="c490f-163">Unlike static text, data displayed using a text box can be scrolled (useful if the data is wider than the control), selected, and copied.</span></span><br/> <img src="images/ctrl-text-boxes-image8.png" alt="Screen shot of a text box showing path to a folder " /><br/> <span data-ttu-id="c490f-164">Однострочное текстовое поле только для чтения, используемое для вывода данных.</span><span class="sxs-lookup"><span data-stu-id="c490f-164">A single-line, read-only text box used to display data.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c490f-165"><strong>Текстовый вывод</strong></span><span class="sxs-lookup"><span data-stu-id="c490f-165"><strong>Textual output</strong></span></span><br/> <span data-ttu-id="c490f-166">Многострочное текстовое поле только для чтения, используемое для вывода длинных строк.</span><span class="sxs-lookup"><span data-stu-id="c490f-166">A multi-line, read-only text box used to display long strings.</span></span> <br/></td>
<td><img src="images/ctrl-text-boxes-image9.png" alt="Screen shot of a Privacy information text box " /><br/> <span data-ttu-id="c490f-167">Текстовое поле только для чтения, используемое для вывода данных.</span><span class="sxs-lookup"><span data-stu-id="c490f-167">A read-only text box used to display data.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="guidelines"></a><span data-ttu-id="c490f-168">Рекомендации</span><span class="sxs-lookup"><span data-stu-id="c490f-168">Guidelines</span></span>

### <a name="general"></a><span data-ttu-id="c490f-169">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="c490f-169">General</span></span>

-   <span data-ttu-id="c490f-170">**При отключении текстового поля также отключите все связанные метки, метки инструкций, элементы управления "Счетчик" и кнопки команд.**</span><span class="sxs-lookup"><span data-stu-id="c490f-170">**When disabling a text box, also disable any associated labels, instruction labels, spin controls, and command buttons.**</span></span>
-   <span data-ttu-id="c490f-171">**Используйте автозаполнение, чтобы помочь пользователям вводить данные, которые, скорее всего, будут использоваться повторно**.</span><span class="sxs-lookup"><span data-stu-id="c490f-171">**Use auto-complete to help users enter data that is likely to be used repeatedly**.</span></span> <span data-ttu-id="c490f-172">Примеры включают имена пользователей, адреса и имена файлов.</span><span class="sxs-lookup"><span data-stu-id="c490f-172">Examples include user names, addresses, and file names.</span></span> <span data-ttu-id="c490f-173">Однако не используйте автозаполнение для текстовых полей, которые могут содержать конфиденциальные сведения, такие как пароли, ПИН-коды, номера кредитных карт или медицинские сведения.</span><span class="sxs-lookup"><span data-stu-id="c490f-173">However, don't use auto-complete for text boxes that may contain sensitive information, such as passwords, PINs, credit card numbers, or medical information.</span></span>
-   <span data-ttu-id="c490f-174">**Не делайте так, чтобы пользователи прокручиваться без необходимости.**</span><span class="sxs-lookup"><span data-stu-id="c490f-174">**Don't make users scroll unnecessarily.**</span></span> <span data-ttu-id="c490f-175">Если предполагается, что данные будут больше, чем текстовое поле, и вы можете сделать текстовое поле больше, не создавая вред для макета, измените размер поля, чтобы исключить необходимость прокрутки.</span><span class="sxs-lookup"><span data-stu-id="c490f-175">If you expect data to be larger than the text box and you can readily make the text box larger without harming the layout, size the box to eliminate the need for scrolling.</span></span>

    <span data-ttu-id="c490f-176">**Неправильно**:</span><span class="sxs-lookup"><span data-stu-id="c490f-176">**Incorrect:**</span></span>

    ![<span data-ttu-id="c490f-177">снимок экрана текстового поля "имя компьютера"</span><span class="sxs-lookup"><span data-stu-id="c490f-177">screen shot of a computer name text box</span></span> ](images/ctrl-text-boxes-image10.png)

    <span data-ttu-id="c490f-178">В этом примере текстовое поле должно быть значительно больше, чтобы обрабатывать его данные.</span><span class="sxs-lookup"><span data-stu-id="c490f-178">In this example, the text box should be made much longer to handle its data.</span></span>

-   <span data-ttu-id="c490f-179">Полосы прокрутки:</span><span class="sxs-lookup"><span data-stu-id="c490f-179">Scroll bars:</span></span>
    -   <span data-ttu-id="c490f-180">**Не размещайте горизонтальные полосы прокрутки в многострочных текстовых полях.**</span><span class="sxs-lookup"><span data-stu-id="c490f-180">**Don't put horizontal scroll bars on multi-line text boxes.**</span></span> <span data-ttu-id="c490f-181">Вместо этого используйте вертикальную прокрутку и перенос строки.</span><span class="sxs-lookup"><span data-stu-id="c490f-181">Use vertical scrolling and line wrapping instead.</span></span>
    -   <span data-ttu-id="c490f-182">**Не помещайте полосы прокрутки в однострочные текстовые поля.**</span><span class="sxs-lookup"><span data-stu-id="c490f-182">**Don't put any scroll bars on single-line text boxes.**</span></span>
-   <span data-ttu-id="c490f-183">**Для числового ввода можно использовать элемент управления "Счетчик".**</span><span class="sxs-lookup"><span data-stu-id="c490f-183">**For numeric input, you may use a spin control.**</span></span> <span data-ttu-id="c490f-184">Для текстового ввода используйте раскрывающийся список или раскрывающийся список, который следует редактировать.</span><span class="sxs-lookup"><span data-stu-id="c490f-184">For textual input, use a drop-down list or editable drop-down list instead.</span></span>
-   <span data-ttu-id="c490f-185">**Не используйте функцию автоматического выхода, кроме форматированного ввода данных.**</span><span class="sxs-lookup"><span data-stu-id="c490f-185">**Don't use the auto-exit feature except for formatted data input.**</span></span> <span data-ttu-id="c490f-186">Автоматический сдвиг фокуса может неожиданно повлечь пользователей.</span><span class="sxs-lookup"><span data-stu-id="c490f-186">The automatic shift of focus can surprise users.</span></span>

### <a name="editable-text-boxes"></a><span data-ttu-id="c490f-187">Редактируемые текстовые поля</span><span class="sxs-lookup"><span data-stu-id="c490f-187">Editable text boxes</span></span>

-   <span data-ttu-id="c490f-188">**При возможности ограничьте длину входного текста.**</span><span class="sxs-lookup"><span data-stu-id="c490f-188">**Limit the length of the input text when you can.**</span></span> <span data-ttu-id="c490f-189">Например, если допустимые входные данные имеют число от 0 до 999, используйте текстовое поле, длина которого ограничена тремя символами.</span><span class="sxs-lookup"><span data-stu-id="c490f-189">For example, if the valid input is a number between 0 and 999, use a numeric text box that is limited to three characters.</span></span> <span data-ttu-id="c490f-190">Все части текстовых полей, использующих форматированные входные данные, должны иметь короткую фиксированную длину.</span><span class="sxs-lookup"><span data-stu-id="c490f-190">All parts of text boxes that use formatted data input must have a short, fixed length.</span></span>
-   <span data-ttu-id="c490f-191">**Гибкость при работе с форматами данных.**</span><span class="sxs-lookup"><span data-stu-id="c490f-191">**Be flexible with data formats.**</span></span> <span data-ttu-id="c490f-192">Если пользователи, скорее всего, вводят текст с помощью широкого спектра форматов, попробуйте обработать все наиболее распространенные.</span><span class="sxs-lookup"><span data-stu-id="c490f-192">If users are likely to enter text using a wide variety of formats, try to handle all the most common ones.</span></span> <span data-ttu-id="c490f-193">Например, многие имена, числа и идентификаторы могут быть введены с дополнительными пробелами и знаками препинания, и регистр часто не имеет значения.</span><span class="sxs-lookup"><span data-stu-id="c490f-193">For example, many names, numbers, and identifiers can be entered with optional spaces and punctuation, and the capitalization often doesn't matter.</span></span>
-   <span data-ttu-id="c490f-194">Если вы не можете работать с вероятными форматами, запрашивать конкретный формат, используя форматированные входные данные или указывая допустимые форматы в метке.</span><span class="sxs-lookup"><span data-stu-id="c490f-194">If you can't handle the likely formats, require a specific format by using formatted data input or indicate the valid formats in the label.</span></span>

    <span data-ttu-id="c490f-195">**Хорошо:**</span><span class="sxs-lookup"><span data-stu-id="c490f-195">**Acceptable:**</span></span>

    ![<span data-ttu-id="c490f-196">снимок экрана текстового поля для числовых входных данных</span><span class="sxs-lookup"><span data-stu-id="c490f-196">screen shot of a text box for numeric input</span></span> ](images/ctrl-text-boxes-image11.png)

    <span data-ttu-id="c490f-197">В этом примере для текстового поля требуются входные данные в определенном формате.</span><span class="sxs-lookup"><span data-stu-id="c490f-197">In this example, a text box requires input in a specific format.</span></span>

    <span data-ttu-id="c490f-198">**Лучше:**</span><span class="sxs-lookup"><span data-stu-id="c490f-198">**Better:**</span></span>

    ![<span data-ttu-id="c490f-199">снимок экрана с текстовым полем ввода форматированных данных</span><span class="sxs-lookup"><span data-stu-id="c490f-199">screen shot of formatted data input text box</span></span> ](images/ctrl-text-boxes-image12.png)

    <span data-ttu-id="c490f-200">В этом примере шаблон ввода форматированных данных используется для обязательного использования определенного формата.</span><span class="sxs-lookup"><span data-stu-id="c490f-200">In this example, the formatted data input pattern is used to require a specific format.</span></span>

    <span data-ttu-id="c490f-201">**Самое**</span><span class="sxs-lookup"><span data-stu-id="c490f-201">**Best:**</span></span>

    ![<span data-ttu-id="c490f-202">снимок экрана неограниченного текстового поля</span><span class="sxs-lookup"><span data-stu-id="c490f-202">screen shot of an unconstrained text box</span></span> ](images/ctrl-text-boxes-image13.png)

    <span data-ttu-id="c490f-203">В этом примере текстовое поле обрабатывает все вероятные форматы.</span><span class="sxs-lookup"><span data-stu-id="c490f-203">In this example, a text box handles all likely formats.</span></span>

-   <span data-ttu-id="c490f-204">При выборе максимальной длины входных данных рассмотрите возможность гибкого форматирования.</span><span class="sxs-lookup"><span data-stu-id="c490f-204">Consider format flexibility when choosing the maximum input length.</span></span> <span data-ttu-id="c490f-205">Например, допустимый номер кредитной карты может использовать до 19 символов, поэтому ограничение длины до чем-то более короткое может усложнить ввод чисел с использованием более длинных форматов.</span><span class="sxs-lookup"><span data-stu-id="c490f-205">For example, a valid credit card number can use up to 19 characters so limiting the length to anything shorter would make it difficult to enter numbers using the longer formats.</span></span>
-   <span data-ttu-id="c490f-206">**Не используйте шаблон ввода форматированных данных, если пользователи чаще всего вставляют длинные, сложные данные.**</span><span class="sxs-lookup"><span data-stu-id="c490f-206">**Don't use the formatted data input pattern if users are more likely to paste in long, complex data.**</span></span> <span data-ttu-id="c490f-207">Вместо этого следует зарезервировать шаблон ввода форматированных данных в тех ситуациях, когда пользователи, скорее всего, будут вводить данные.</span><span class="sxs-lookup"><span data-stu-id="c490f-207">Rather, reserve the formatted data input pattern for situations where users are more likely to type the data.</span></span>

    ![<span data-ttu-id="c490f-208">снимок экрана текстового поля с меткой: IPv6-адрес</span><span class="sxs-lookup"><span data-stu-id="c490f-208">screen shot of a text box with label: ipv6 address</span></span> ](images/ctrl-text-boxes-image14.png)

    <span data-ttu-id="c490f-209">В этом примере форматированный шаблон ввода данных не используется, чтобы пользователи могли вставлять IPv6-адреса.</span><span class="sxs-lookup"><span data-stu-id="c490f-209">In this example, the formatted data input pattern isn't used, so that users can to paste IPv6 addresses.</span></span>

-   <span data-ttu-id="c490f-210">**Если пользователи, скорее всего, будут повторно вводить все значение, выделите весь текст на фокусе ввода.**</span><span class="sxs-lookup"><span data-stu-id="c490f-210">**If users are more likely going to reenter the entire value, select all the text on input focus.**</span></span> <span data-ttu-id="c490f-211">Если пользователи, скорее всего, будут редактироваться, поместите курсор в конец текста.</span><span class="sxs-lookup"><span data-stu-id="c490f-211">If users are more likely to edit, place the caret at the end of the text.</span></span>

    ![<span data-ttu-id="c490f-212">снимок экрана текстового поля пароля</span><span class="sxs-lookup"><span data-stu-id="c490f-212">screen shot of a password text box</span></span> ](images/ctrl-text-boxes-image15.png)

    <span data-ttu-id="c490f-213">В этом примере пользователи, скорее всего, заменяются, чем Edit, поэтому для фокуса ввода выделяется все значение.</span><span class="sxs-lookup"><span data-stu-id="c490f-213">In this example, users are more likely to replace than edit, so the entire value is selected on input focus.</span></span>

    ![<span data-ttu-id="c490f-214">снимок экрана текстового поля для ввода ключевых слов</span><span class="sxs-lookup"><span data-stu-id="c490f-214">screen shot of a text box for entering keywords</span></span> ](images/ctrl-text-boxes-image16.png)

    <span data-ttu-id="c490f-215">В этом примере пользователи скорее всего добавляют ключевые слова, чем заменяют текст, поэтому курсор помещается в конец текста.</span><span class="sxs-lookup"><span data-stu-id="c490f-215">In this example, users are more likely to add keywords than replace the text, so the caret is placed at the end of the text.</span></span>

-   <span data-ttu-id="c490f-216">**Всегда используйте многострочное текстовое поле, если символы новой строки являются допустимыми входными данными.**</span><span class="sxs-lookup"><span data-stu-id="c490f-216">**Always use a multi-line text box if new-line characters are valid input.**</span></span>
-   <span data-ttu-id="c490f-217">**Если текстовое поле предназначено для файла или пути, всегда следует указать кнопку обзора.**</span><span class="sxs-lookup"><span data-stu-id="c490f-217">**When the text box is for a file or path, always provide a Browse button.**</span></span>

### <a name="numeric-text-boxes"></a><span data-ttu-id="c490f-218">Числовые текстовые поля</span><span class="sxs-lookup"><span data-stu-id="c490f-218">Numeric text boxes</span></span>

-   <span data-ttu-id="c490f-219">**Выберите наиболее удобное устройство и пометка единиц.**</span><span class="sxs-lookup"><span data-stu-id="c490f-219">**Choose the most convenient unit and label the units.**</span></span> <span data-ttu-id="c490f-220">Например, можно использовать миллилитерс вместо литров (или наоборот), проценты вместо прямых значений (или наоборот) и т. д.</span><span class="sxs-lookup"><span data-stu-id="c490f-220">For example, consider using milliliters instead of liters (or vice versa), percentages instead of direct values (or vice versa), and so on.</span></span>

    <span data-ttu-id="c490f-221">**Правильно:**</span><span class="sxs-lookup"><span data-stu-id="c490f-221">**Correct:**</span></span>

    ![<span data-ttu-id="c490f-222">снимок экрана текстового поля с литрами в виде единицы</span><span class="sxs-lookup"><span data-stu-id="c490f-222">screen shot of text box with liters as unit</span></span> ](images/ctrl-text-boxes-image17.png)

    <span data-ttu-id="c490f-223">В этом примере единицей является метка, но она требует, чтобы пользователи вводили десятичные числа.</span><span class="sxs-lookup"><span data-stu-id="c490f-223">In this example, the unit is labeled, but it requires users to enter decimal numbers.</span></span>

    <span data-ttu-id="c490f-224">**Лучше:**</span><span class="sxs-lookup"><span data-stu-id="c490f-224">**Better:**</span></span>

    ![<span data-ttu-id="c490f-225">снимок экрана текстового поля с миллилитерс как единицей</span><span class="sxs-lookup"><span data-stu-id="c490f-225">screen shot of text box with milliliters as unit</span></span> ](images/ctrl-text-boxes-image18.png)

    <span data-ttu-id="c490f-226">В этом примере в текстовом поле используется более удобная единица.</span><span class="sxs-lookup"><span data-stu-id="c490f-226">In this example, the text box uses a more convenient unit.</span></span>

-   <span data-ttu-id="c490f-227">**Используйте элемент управления "Счетчик", когда он полезен.**</span><span class="sxs-lookup"><span data-stu-id="c490f-227">**Use a spin control whenever it is helpful.**</span></span> <span data-ttu-id="c490f-228">Однако иногда элементы управления "Счетчик" не являются практичными, например, когда пользователям нужно вводить большое количество больших чисел.</span><span class="sxs-lookup"><span data-stu-id="c490f-228">However, sometimes spin controls aren't practical, such as when users need to enter many large numbers.</span></span> <span data-ttu-id="c490f-229">Используйте элементы управления "Счетчик", если:</span><span class="sxs-lookup"><span data-stu-id="c490f-229">Use spin controls when:</span></span>
    -   <span data-ttu-id="c490f-230">Входные данные, скорее всего, будут небольшими, обычно под номером 100.</span><span class="sxs-lookup"><span data-stu-id="c490f-230">The input is likely to be a small number, typically under 100.</span></span>
    -   <span data-ttu-id="c490f-231">Пользователи, скорее всего, будут вносить небольшое изменение в существующий номер.</span><span class="sxs-lookup"><span data-stu-id="c490f-231">Users are likely to make a small change to an existing number.</span></span>
    -   <span data-ttu-id="c490f-232">Чаще всего пользователи используют мышь, а не клавиатуру.</span><span class="sxs-lookup"><span data-stu-id="c490f-232">Users are more likely to be using the mouse than the keyboard.</span></span>
-   <span data-ttu-id="c490f-233">**Выровняйте числовой текст по правому краю каждый раз:**</span><span class="sxs-lookup"><span data-stu-id="c490f-233">**Right-align numeric text whenever:**</span></span>

    -   <span data-ttu-id="c490f-234">Существует более одного числового текстового поля.</span><span class="sxs-lookup"><span data-stu-id="c490f-234">There is more than one numeric text box.</span></span>
    -   <span data-ttu-id="c490f-235">Текстовые поля выравниваться по вертикали.</span><span class="sxs-lookup"><span data-stu-id="c490f-235">The text boxes are vertically aligned.</span></span>
    -   <span data-ttu-id="c490f-236">Пользователи, скорее всего, будут добавлять или сравнивать значения.</span><span class="sxs-lookup"><span data-stu-id="c490f-236">Users are likely to add or compare the values.</span></span>

    <span data-ttu-id="c490f-237">**Правильно:**</span><span class="sxs-lookup"><span data-stu-id="c490f-237">**Correct:**</span></span>

    ![<span data-ttu-id="c490f-238">снимок экрана: текстовые поля расходов (Гостиницы и т. д.)</span><span class="sxs-lookup"><span data-stu-id="c490f-238">screen shot of expenses text boxes (hotel, etc.)</span></span> ](images/ctrl-text-boxes-image19.png)

    <span data-ttu-id="c490f-239">В этом примере числовой текст выдается по правому краю, чтобы облегчить сравнение значений.</span><span class="sxs-lookup"><span data-stu-id="c490f-239">In this example, the numeric text is right-aligned to make it easy to compare values.</span></span>

    <span data-ttu-id="c490f-240">**Неправильно**:</span><span class="sxs-lookup"><span data-stu-id="c490f-240">**Incorrect:**</span></span>

    ![<span data-ttu-id="c490f-241">снимок экрана с текстовыми полями для значений RGB</span><span class="sxs-lookup"><span data-stu-id="c490f-241">screen shot of text boxes for rgb values</span></span> ](images/ctrl-text-boxes-image20.png)

    <span data-ttu-id="c490f-242">В этом примере числовой текст неправильно соответствует по левому краю.</span><span class="sxs-lookup"><span data-stu-id="c490f-242">In this example, the numeric text is incorrectly left-aligned.</span></span>

-   <span data-ttu-id="c490f-243">**Всегда выровняйте денежные значения по правому краю.**</span><span class="sxs-lookup"><span data-stu-id="c490f-243">**Always right-align monetary values.**</span></span>
-   <span data-ttu-id="c490f-244">**Не следует назначать специальные значения конкретным числовым значениями**, даже если они используются внутри приложения.</span><span class="sxs-lookup"><span data-stu-id="c490f-244">**Don't assign special meanings to specific numeric values**, even if those special meanings are used internally by your application.</span></span> <span data-ttu-id="c490f-245">Вместо этого используйте флажки или переключатели для явного выбора пользователя.</span><span class="sxs-lookup"><span data-stu-id="c490f-245">Instead, use check boxes or radio buttons for an explicit user selection.</span></span>

    <span data-ttu-id="c490f-246">**Неправильно**:</span><span class="sxs-lookup"><span data-stu-id="c490f-246">**Incorrect:**</span></span>

    ![<span data-ttu-id="c490f-247">снимок экрана Метки: используйте значение-1, чтобы отключить кэширование</span><span class="sxs-lookup"><span data-stu-id="c490f-247">screen shot of label: use -1 to disable caching</span></span> ](images/ctrl-text-boxes-image21.png)

    <span data-ttu-id="c490f-248">В этом примере значение-1 имеет специальное значение.</span><span class="sxs-lookup"><span data-stu-id="c490f-248">In this example, the value -1 has a special meaning.</span></span>

    <span data-ttu-id="c490f-249">**Правильно:**</span><span class="sxs-lookup"><span data-stu-id="c490f-249">**Correct:**</span></span>

    ![<span data-ttu-id="c490f-250">снимок экрана с флажком метка: кэширование</span><span class="sxs-lookup"><span data-stu-id="c490f-250">screen shot of check box label: caching</span></span> ](images/ctrl-text-boxes-image22.png)

    <span data-ttu-id="c490f-251">В этом примере флажок делает параметр явным.</span><span class="sxs-lookup"><span data-stu-id="c490f-251">In this example, a check box makes the option explicit.</span></span>

### <a name="password-and-pin-input"></a><span data-ttu-id="c490f-252">Ввод пароля и ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="c490f-252">Password and PIN input</span></span>

-   <span data-ttu-id="c490f-253">**Всегда используйте общий элемент управления пароля вместо создания собственного.**</span><span class="sxs-lookup"><span data-stu-id="c490f-253">**Always use the password common control instead of creating your own.**</span></span> <span data-ttu-id="c490f-254">Для безопасной обработки паролей и ПИН-кодов требуется специальная обработка.</span><span class="sxs-lookup"><span data-stu-id="c490f-254">Passwords and PINs require special treatment to be handled securely.</span></span>

<span data-ttu-id="c490f-255">Дополнительные рекомендации и примеры см. в разделе [выноски](ctrl-balloons.md).</span><span class="sxs-lookup"><span data-stu-id="c490f-255">For more guidelines and examples, see [Balloons](ctrl-balloons.md).</span></span>

### <a name="textual-output"></a><span data-ttu-id="c490f-256">Текстовый вывод</span><span class="sxs-lookup"><span data-stu-id="c490f-256">Textual output</span></span>

-   <span data-ttu-id="c490f-257">**Рассмотрите возможность использования белого фонового цвета системы для большого, многострочного текста, доступного только для чтения.**</span><span class="sxs-lookup"><span data-stu-id="c490f-257">**Consider using the white background system color for large, multi-line read-only text.**</span></span> <span data-ttu-id="c490f-258">Белый фон упрощает чтение текста.</span><span class="sxs-lookup"><span data-stu-id="c490f-258">A white background makes the text easier to read.</span></span> <span data-ttu-id="c490f-259">Большое количество текста на сером фоне не рекомендует читать.</span><span class="sxs-lookup"><span data-stu-id="c490f-259">Lots of text on a gray background discourages reading.</span></span>

<span data-ttu-id="c490f-260">Дополнительные сведения о цветах фона см. в разделе [шрифты](vis-fonts.md).</span><span class="sxs-lookup"><span data-stu-id="c490f-260">For more information on background colors, see [Fonts](vis-fonts.md).</span></span>

### <a name="data-output"></a><span data-ttu-id="c490f-261">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="c490f-261">Data output</span></span>

-   <span data-ttu-id="c490f-262">**Не используйте границы для однострочных текстовых полей, предназначенных только для чтения.**</span><span class="sxs-lookup"><span data-stu-id="c490f-262">**Don't use a border for single-line, read-only text boxes.**</span></span> <span data-ttu-id="c490f-263">Граница — это визуальная подговорит, что текст является редактируемым.</span><span class="sxs-lookup"><span data-stu-id="c490f-263">The border is a visual clue that the text is editable.</span></span>
-   <span data-ttu-id="c490f-264">**Не отключать однострочные текстовые поля только для чтения.**</span><span class="sxs-lookup"><span data-stu-id="c490f-264">**Don't disable single-line, read-only text boxes.**</span></span> <span data-ttu-id="c490f-265">Это запрещает пользователям выбирать и копировать текст в буфер обмена.</span><span class="sxs-lookup"><span data-stu-id="c490f-265">This prevents users from selecting and copying the text to the clipboard.</span></span> <span data-ttu-id="c490f-266">Кроме того, он не позволяет пользователям прокручивать данные, если они выходят за пределы их размеров.</span><span class="sxs-lookup"><span data-stu-id="c490f-266">It also prevents users from scrolling the data if it exceeds the size of its boundaries.</span></span>
-   <span data-ttu-id="c490f-267">**Не устанавливайте позицию табуляции в однострочном текстовом поле только для чтения, если пользователь, скорее всего, не потребует прокрутки или копирования текста.**</span><span class="sxs-lookup"><span data-stu-id="c490f-267">**Don't set a tab stop on single-line, read-only text box unless the user is likely to need to scroll or copy the text.**</span></span>

## <a name="input-validation-and-error-handling"></a><span data-ttu-id="c490f-268">Проверка входных данных и обработка ошибок</span><span class="sxs-lookup"><span data-stu-id="c490f-268">Input validation and error handling</span></span>

<span data-ttu-id="c490f-269">Так как текстовые поля обычно не ограничены приемом только допустимых входных данных, может потребоваться проверка входных данных и их устранение.</span><span class="sxs-lookup"><span data-stu-id="c490f-269">Because text boxes are usually not constrained to accept only valid input, you may need to validate the input and handle any problems.</span></span> <span data-ttu-id="c490f-270">Проверьте различные типы проблем ввода, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="c490f-270">Validate the various types of input problems as follows:</span></span>

-   <span data-ttu-id="c490f-271">Если пользователь вводит недопустимый символ, пропустите этот символ и отобразит [всплывающее сообщение с проблемой ввода](ctrl-balloons.md) , поясняющее допустимые символы.</span><span class="sxs-lookup"><span data-stu-id="c490f-271">If the user enters a character that isn't valid, ignore the character and display an [input problem balloon](ctrl-balloons.md) that explains the valid characters.</span></span>

    ![снимок экрана текстового поля "ключ продукта"](images/ctrl-text-boxes-image23.png)

    <span data-ttu-id="c490f-273">В этом примере всплывающее сообщение сообщает о неправильном вводе символа.</span><span class="sxs-lookup"><span data-stu-id="c490f-273">In this example, a balloon reports an incorrect input character.</span></span>

-   <span data-ttu-id="c490f-274">Если входные данные имеют недопустимое значение или формат, отобразится всплывающее сообщение с проблемой ввода, когда текстовое поле теряет фокус ввода.</span><span class="sxs-lookup"><span data-stu-id="c490f-274">If the input data has a value or format that isn't valid, display an input problem balloon when the text box loses input focus.</span></span>
-   <span data-ttu-id="c490f-275">Если входные данные не согласуются с другими элементами управления в окне, выдайте сообщение об ошибке при завершении всех входных данных, например при нажатии пользователем кнопки ОК для модального диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="c490f-275">If the input data is inconsistent with other controls on the window, give an error message when the entire input is complete, such as when users click OK for a modal dialog box.</span></span>

<span data-ttu-id="c490f-276">**Не снимайте неправильные входные данные, если пользователи не могут легко исправить ошибки.**</span><span class="sxs-lookup"><span data-stu-id="c490f-276">**Don't clear invalid input data unless users aren't able to correct errors easily.**</span></span> <span data-ttu-id="c490f-277">Это позволит пользователям исправлять ошибки без запуска.</span><span class="sxs-lookup"><span data-stu-id="c490f-277">Doing so allows users to correct mistakes without starting over.</span></span> <span data-ttu-id="c490f-278">Например, следует очистить неверные пароли и ПИН-коды, так как пользователи не могут легко исправить их.</span><span class="sxs-lookup"><span data-stu-id="c490f-278">For example, you should clear incorrect passwords and PINs because users can't correct them easily.</span></span>

<span data-ttu-id="c490f-279">Дополнительные рекомендации и примеры см. в разделе [сообщения об ошибках](mess-error.md) и [всплывающие подсказки](ctrl-balloons.md).</span><span class="sxs-lookup"><span data-stu-id="c490f-279">For more guidelines and examples, see [Error Messages](mess-error.md) and [Balloons](ctrl-balloons.md).</span></span>

## <a name="prompts"></a><span data-ttu-id="c490f-280">Запросы</span><span class="sxs-lookup"><span data-stu-id="c490f-280">Prompts</span></span>

<span data-ttu-id="c490f-281">Приглашение — это метка или короткая инструкция, помещенная в текстовое поле в качестве значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c490f-281">A prompt is a label or short instruction placed inside a text box as its default value.</span></span> <span data-ttu-id="c490f-282">В отличие от статического текста, запросы исчезают с экрана, когда пользователь наводит что-либо в текстовое поле или получает фокус ввода.</span><span class="sxs-lookup"><span data-stu-id="c490f-282">Unlike static text, prompts disappear from the screen once users type something into the text box or it gets input focus.</span></span>

![<span data-ttu-id="c490f-283">снимок экрана: текстовое поле "запрос" с меткой "Поиск"</span><span class="sxs-lookup"><span data-stu-id="c490f-283">screen shot of prompt text box with label: search</span></span> ](images/ctrl-text-boxes-image24.png)

<span data-ttu-id="c490f-284">Типичный запрос.</span><span class="sxs-lookup"><span data-stu-id="c490f-284">A typical prompt.</span></span>

<span data-ttu-id="c490f-285">Использовать запрос в следующих случаях:</span><span class="sxs-lookup"><span data-stu-id="c490f-285">Use a prompt when:</span></span>

-   <span data-ttu-id="c490f-286">Пространство на экране — это такое вознаграждение, что использование метки или инструкции нежелательно, например на панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="c490f-286">Screen space is at such a premium that using a label or instruction is undesirable, such as on a toolbar.</span></span>
-   <span data-ttu-id="c490f-287">Запрос в первую очередь определяет назначение текстового поля компактным способом.</span><span class="sxs-lookup"><span data-stu-id="c490f-287">The prompt is primarily for identifying the purpose of the text box in a compact way.</span></span> <span data-ttu-id="c490f-288">Он не должен быть важной информацией, которую пользователь должен видеть при использовании текстового поля.</span><span class="sxs-lookup"><span data-stu-id="c490f-288">It must not be crucial information that the user needs to see while using the text box.</span></span>

<span data-ttu-id="c490f-289">Не используйте запросы, чтобы направлять пользователей для ввода или нажатия кнопок.</span><span class="sxs-lookup"><span data-stu-id="c490f-289">Don't use prompts just to direct users to type something or to click buttons.</span></span> <span data-ttu-id="c490f-290">Например, не записывайте текст запроса с текстом введите имя файла и нажмите кнопку Отправить.</span><span class="sxs-lookup"><span data-stu-id="c490f-290">For example, don't write prompt text that says Enter a filename and then click Send.</span></span>

<span data-ttu-id="c490f-291">При использовании запросов:</span><span class="sxs-lookup"><span data-stu-id="c490f-291">When using prompts:</span></span>

-   <span data-ttu-id="c490f-292">Нарисуйте текст подсказки полужирным серым цветом и фактическим входным текстом в нормальном черном режиме.</span><span class="sxs-lookup"><span data-stu-id="c490f-292">Draw the prompt text in italic gray and the actual input text in normal black.</span></span> <span data-ttu-id="c490f-293">Текст подсказки не следует путать с реальным текстом.</span><span class="sxs-lookup"><span data-stu-id="c490f-293">The prompt text must not be confused with real text.</span></span>
-   <span data-ttu-id="c490f-294">Текст подсказки следует кратко отображать.</span><span class="sxs-lookup"><span data-stu-id="c490f-294">Keep the prompt text concise.</span></span> <span data-ttu-id="c490f-295">Вместо полных предложений можно использовать фрагменты.</span><span class="sxs-lookup"><span data-stu-id="c490f-295">You can use fragments instead of full sentences.</span></span>
-   <span data-ttu-id="c490f-296">Используйте выделение прописных букв, как в предложении.</span><span class="sxs-lookup"><span data-stu-id="c490f-296">Use sentence-style capitalization.</span></span>
-   <span data-ttu-id="c490f-297">Не используйте закрывающие знаки препинания или многоточие.</span><span class="sxs-lookup"><span data-stu-id="c490f-297">Don't use ending punctuation or ellipsis.</span></span>
-   <span data-ttu-id="c490f-298">Текст подсказки не должен быть редактируемым и должен исчезнуть после нажатия пользователем кнопки или клавиши TAB в текстовом поле.</span><span class="sxs-lookup"><span data-stu-id="c490f-298">The prompt text should not be editable and should disappear once users click in or tab into the text box.</span></span>
    -   <span data-ttu-id="c490f-299">**Исключение:** Если текстовое поле имеет фокус ввода по умолчанию, отображается запрос, и он исчезает после начала ввода пользователем.</span><span class="sxs-lookup"><span data-stu-id="c490f-299">**Exception:** If the text box has default input focus, the prompt is displayed, and it disappears once the user starts typing.</span></span>
-   <span data-ttu-id="c490f-300">Текст подсказки восстанавливается, если текстовое поле остается пустым при потере фокуса ввода.</span><span class="sxs-lookup"><span data-stu-id="c490f-300">The prompt text is restored if the text box is still empty when it loses input focus.</span></span>

## <a name="recommended-sizing-and-spacing"></a><span data-ttu-id="c490f-301">Рекомендуемое изменение размера и расстояния</span><span class="sxs-lookup"><span data-stu-id="c490f-301">Recommended sizing and spacing</span></span>

![<span data-ttu-id="c490f-302">Рисунок однострочных и двух текстовых полей</span><span class="sxs-lookup"><span data-stu-id="c490f-302">figure of one-line and two-line text boxes</span></span> ](images/ctrl-text-boxes-image25.png)

<span data-ttu-id="c490f-303">Рекомендуемый размер и пространство для текстовых полей.</span><span class="sxs-lookup"><span data-stu-id="c490f-303">Recommended sizing and spacing for text boxes.</span></span>

<span data-ttu-id="c490f-304">Ширина текстового поля — это визуальная подмножество ожидаемого размера входных данных.</span><span class="sxs-lookup"><span data-stu-id="c490f-304">The width of a text box is a visual clue of the expected input size.</span></span> <span data-ttu-id="c490f-305">При изменении размера текстовых полей:</span><span class="sxs-lookup"><span data-stu-id="c490f-305">When sizing text boxes:</span></span>

-   <span data-ttu-id="c490f-306">**Выберите ширину, соответствующую наиболее длинным допустимым данным.**</span><span class="sxs-lookup"><span data-stu-id="c490f-306">**Choose a width appropriate for the longest valid data.**</span></span> <span data-ttu-id="c490f-307">В большинстве случаев пользователям не нужно прокручивать самую длинную строку, которую они вводят или просматривают.</span><span class="sxs-lookup"><span data-stu-id="c490f-307">In most situations, users shouldn't have to scroll the longest likely string they'll enter or view.</span></span>
-   <span data-ttu-id="c490f-308">**Включите дополнительные 30%** (до 200 процентов для более короткого текста) для любого текста (но не чисел), который будет локализован.</span><span class="sxs-lookup"><span data-stu-id="c490f-308">**Include an additional 30 percent** (up to 200 percent for shorter text) for any text (but not numbers) that will be localized.</span></span>
-   <span data-ttu-id="c490f-309">**Если ожидаемые входные данные не имеют определенного размера, выберите ширину, которая согласуется с другими текстовыми полями или элементами управления в окне.**</span><span class="sxs-lookup"><span data-stu-id="c490f-309">**If the expected input has no particular size, choose a width that is consistent with the other text boxes or controls on the window.**</span></span>
-   <span data-ttu-id="c490f-310">**Размер многострочных текстовых полей для вывода целого числа строк текста.**</span><span class="sxs-lookup"><span data-stu-id="c490f-310">**Size multi-line text boxes to display an integral number of lines of text.**</span></span>

## <a name="labels"></a><span data-ttu-id="c490f-311">Метки</span><span class="sxs-lookup"><span data-stu-id="c490f-311">Labels</span></span>

### <a name="text-box-labels"></a><span data-ttu-id="c490f-312">Метки текстовых полей</span><span class="sxs-lookup"><span data-stu-id="c490f-312">Text box labels</span></span>

-   <span data-ttu-id="c490f-313">Для всех текстовых полей требуются метки.</span><span class="sxs-lookup"><span data-stu-id="c490f-313">All text boxes need labels.</span></span> <span data-ttu-id="c490f-314">Напишите метку как слово или фразу, не в виде предложения, заканчивая двоеточием и используя [статический текст](glossary.md).</span><span class="sxs-lookup"><span data-stu-id="c490f-314">Write the label as a word or phrase, not as a sentence, ending with a colon, and using [static text](glossary.md).</span></span>

    <span data-ttu-id="c490f-315">**Отличи**</span><span class="sxs-lookup"><span data-stu-id="c490f-315">**Exceptions:**</span></span>

    -   <span data-ttu-id="c490f-316">Текстовые поля с приглашениями, расположенными в том случае, если пространство имеет уровень "Премиум".</span><span class="sxs-lookup"><span data-stu-id="c490f-316">Text boxes with prompts located where space is at a premium.</span></span>
    -   <span data-ttu-id="c490f-317">Для меток группа текстовых полей, используемых для **ввода форматированных данных** , должна рассматриваться как одно текстовое поле.</span><span class="sxs-lookup"><span data-stu-id="c490f-317">For labeling, a group of text boxes used for **formatted data input** should be treated as a single text box.</span></span>
    -   <span data-ttu-id="c490f-318">Если текстовое поле является подчиненным для переключателя или флажка и введено его меткой, завершающейся двоеточием, не следует добавлять дополнительную метку в текстовое поле.</span><span class="sxs-lookup"><span data-stu-id="c490f-318">If a text box is subordinate to a radio button or check box, and is introduced by its label ending with a colon, don't put an additional label on the text box.</span></span>
    -   <span data-ttu-id="c490f-319">**Пропустите метки элементов управления, которые переопределяют основную инструкцию.**</span><span class="sxs-lookup"><span data-stu-id="c490f-319">**Omit control labels that restate the main instruction.**</span></span> <span data-ttu-id="c490f-320">В этом случае Главная инструкция принимает двоеточие (если это не вопрос) и ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="c490f-320">In this case, the main instruction takes the colon (unless it's a question) and access key.</span></span>

        <span data-ttu-id="c490f-321">**Хорошо:**</span><span class="sxs-lookup"><span data-stu-id="c490f-321">**Acceptable:**</span></span>

        ![снимок экрана текстового поля с меткой какой](images/ctrl-text-boxes-image26.png)

        <span data-ttu-id="c490f-323">В этом примере метка текстового поля — это просто пересохранение основной инструкции.</span><span class="sxs-lookup"><span data-stu-id="c490f-323">In this example, the text box label is just a restatement of the main instruction.</span></span>

        <span data-ttu-id="c490f-324">**Лучше:**</span><span class="sxs-lookup"><span data-stu-id="c490f-324">**Better:**</span></span>

        ![<span data-ttu-id="c490f-325">снимок экрана текстового поля с основной инструкцией</span><span class="sxs-lookup"><span data-stu-id="c490f-325">screen shot of text box with main instruction only</span></span> ](images/ctrl-text-boxes-image27.png)

        <span data-ttu-id="c490f-326">В этом примере избыточная метка удаляется, поэтому основная инструкция принимает двоеточие и ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="c490f-326">In this example, the redundant label is removed, so the main instruction takes the colon and access key.</span></span>

-   <span data-ttu-id="c490f-327">Назначьте уникальный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="c490f-327">Assign a unique access key.</span></span> <span data-ttu-id="c490f-328">Рекомендации по назначению ключей доступа см. в разделе [Клавиатура](inter-keyboard.md).</span><span class="sxs-lookup"><span data-stu-id="c490f-328">For access key assignment guidelines, see [Keyboard](inter-keyboard.md).</span></span>
-   <span data-ttu-id="c490f-329">Используйте выделение прописных букв, как в предложении.</span><span class="sxs-lookup"><span data-stu-id="c490f-329">Use sentence-style capitalization.</span></span>
-   <span data-ttu-id="c490f-330">Разместите метку слева от текстового поля или над ней и выровняйте метку по левому краю текстового поля.</span><span class="sxs-lookup"><span data-stu-id="c490f-330">Position the label either to the left of or above the text box, and align the label with the left edge of the text box.</span></span> <span data-ttu-id="c490f-331">Если метка находится слева, вертикально выровняйте текст метки с текстом текстового поля.</span><span class="sxs-lookup"><span data-stu-id="c490f-331">If the label is on the left, vertically align the label text with the text box text.</span></span>

    <span data-ttu-id="c490f-332">**Правильно:**</span><span class="sxs-lookup"><span data-stu-id="c490f-332">**Correct:**</span></span>

    ![<span data-ttu-id="c490f-333">снимок экрана с надписью, выравниваемая по левому краю, над текстовым полем</span><span class="sxs-lookup"><span data-stu-id="c490f-333">screen shot of left-aligned label above text box</span></span> ](images/ctrl-text-boxes-image28.png)

    ![<span data-ttu-id="c490f-334">снимок экрана с текстовой подписью слева от текстового поля</span><span class="sxs-lookup"><span data-stu-id="c490f-334">screen shot of text-aligned label left of text box</span></span> ](images/ctrl-text-boxes-image29.png)

    <span data-ttu-id="c490f-335">В этих примерах надпись сверху соответствует левому краю текстового поля, а метка слева выполнится по тексту в текстовом поле.</span><span class="sxs-lookup"><span data-stu-id="c490f-335">In these examples, the label on top aligns with the left edge of the text box, and the label on the left aligns with the text in the text box.</span></span>

    <span data-ttu-id="c490f-336">**Неправильно**:</span><span class="sxs-lookup"><span data-stu-id="c490f-336">**Incorrect:**</span></span>

    ![<span data-ttu-id="c490f-337">снимок экрана с текстом метки над текстовым полем</span><span class="sxs-lookup"><span data-stu-id="c490f-337">screen shot of text-aligned label above text box</span></span> ](images/ctrl-text-boxes-image30.png)

    ![<span data-ttu-id="c490f-338">снимок экрана с подпиской, выравниваемая вверх по левому краю текстового поля</span><span class="sxs-lookup"><span data-stu-id="c490f-338">screen shot of top-aligned label left of text box</span></span> ](images/ctrl-text-boxes-image31.png)

    <span data-ttu-id="c490f-339">В этих неверных примерах надпись сверху соответствует тексту в текстовом поле, а метка слева выполнится по верхнему краю текстового поля.</span><span class="sxs-lookup"><span data-stu-id="c490f-339">In these incorrect examples, the label on top aligns with the text in the text box, and the label on the left aligns with the top of the text box.</span></span>

-   <span data-ttu-id="c490f-340">Единицы измерения (например, секунды или соединения) можно указать в круглых скобках после метки.</span><span class="sxs-lookup"><span data-stu-id="c490f-340">You may specify units (for example, seconds or connections) in parentheses after the label.</span></span>
-   <span data-ttu-id="c490f-341">Если текстовое поле допускает произвольное максимальное число символов, можно указать максимальное значение в метке.</span><span class="sxs-lookup"><span data-stu-id="c490f-341">If a text box accepts an arbitrarily small maximum number of characters, you can state the maximum input in the label.</span></span> <span data-ttu-id="c490f-342">Ширина текстового поля должна также предлагать максимальный размер.</span><span class="sxs-lookup"><span data-stu-id="c490f-342">The text box width should also suggest the maximum size.</span></span>

    ![<span data-ttu-id="c490f-343">снимок экрана текстового поля "пароль"</span><span class="sxs-lookup"><span data-stu-id="c490f-343">screen shot of password text box</span></span> ](images/ctrl-text-boxes-image32.png)

    <span data-ttu-id="c490f-344">В этом примере метка дает максимальное число символов.</span><span class="sxs-lookup"><span data-stu-id="c490f-344">In this example, the label gives the maximum number of characters.</span></span>

-   <span data-ttu-id="c490f-345">Не делайте содержимое текстового поля (или его метки единиц измерения) частью предложения, поскольку это не локализуется.</span><span class="sxs-lookup"><span data-stu-id="c490f-345">Don't make the content of the text box (or its units label) part of a sentence, because this is not localizable.</span></span>
-   <span data-ttu-id="c490f-346">Если текстовое поле можно использовать для ввода нескольких элементов, убедитесь, как разделять элементы в метке.</span><span class="sxs-lookup"><span data-stu-id="c490f-346">If the text box can be used to enter several items, make it clear how to separate the items in the label.</span></span>

    ![<span data-ttu-id="c490f-347">снимок экрана с меткой для разделения имен с точкой с запятой</span><span class="sxs-lookup"><span data-stu-id="c490f-347">screen shot of label separate names with semicolon</span></span> ](images/ctrl-text-boxes-image33.png)

    <span data-ttu-id="c490f-348">В этом примере разделитель элементов задается в метке.</span><span class="sxs-lookup"><span data-stu-id="c490f-348">In this example, the item separator is given in the label.</span></span>

-   <span data-ttu-id="c490f-349">Рекомендации по указанию необходимых входных данных см. в разделе Обязательные входные данные в [диалоговых окнах](win-dialog-box.md).</span><span class="sxs-lookup"><span data-stu-id="c490f-349">For guidelines on indicating required input, see Required input in [Dialog Boxes](win-dialog-box.md).</span></span>

### <a name="instruction-labels"></a><span data-ttu-id="c490f-350">Метки инструкций</span><span class="sxs-lookup"><span data-stu-id="c490f-350">Instruction labels</span></span>

-   <span data-ttu-id="c490f-351">Если необходимо добавить пояснительный текст к текстовому полю, добавьте его над меткой.</span><span class="sxs-lookup"><span data-stu-id="c490f-351">If you need to add instructional text about a text box, add it above the label.</span></span> <span data-ttu-id="c490f-352">Используйте полные предложения с закрывающими знаками препинания.</span><span class="sxs-lookup"><span data-stu-id="c490f-352">Use complete sentences with ending punctuation.</span></span>
-   <span data-ttu-id="c490f-353">Используйте выделение прописных букв, как в предложении.</span><span class="sxs-lookup"><span data-stu-id="c490f-353">Use sentence-style capitalization.</span></span>
-   <span data-ttu-id="c490f-354">Дополнительные сведения, которые полезны, но не требуются, должны быть короткими.</span><span class="sxs-lookup"><span data-stu-id="c490f-354">Additional information that is helpful but not necessary should be kept short.</span></span> <span data-ttu-id="c490f-355">Поместите эти сведения в круглые скобки между меткой и двоеточием или без круглых скобок под текстовым полем.</span><span class="sxs-lookup"><span data-stu-id="c490f-355">Place this information either in parentheses between the label and colon, or without parentheses below the text box.</span></span>

    ![<span data-ttu-id="c490f-356">снимок экрана со списком добавленных сведений под текстовым полем</span><span class="sxs-lookup"><span data-stu-id="c490f-356">screen shot of added information below text box</span></span> ](images/ctrl-text-boxes-image34.png)

    <span data-ttu-id="c490f-357">В этом примере дополнительные сведения помещаются под текстовым полем.</span><span class="sxs-lookup"><span data-stu-id="c490f-357">In this example, additional information is placed below the text box.</span></span>

### <a name="prompt-labels"></a><span data-ttu-id="c490f-358">Метки приглашений</span><span class="sxs-lookup"><span data-stu-id="c490f-358">Prompt labels</span></span>

-   <span data-ttu-id="c490f-359">Текст подсказки следует кратко отображать.</span><span class="sxs-lookup"><span data-stu-id="c490f-359">Keep the prompt text concise.</span></span> <span data-ttu-id="c490f-360">Вместо полных предложений можно использовать фрагменты.</span><span class="sxs-lookup"><span data-stu-id="c490f-360">You can use fragments instead of full sentences.</span></span>
-   <span data-ttu-id="c490f-361">Используйте выделение прописных букв, как в предложении.</span><span class="sxs-lookup"><span data-stu-id="c490f-361">Use sentence-style capitalization.</span></span>
-   <span data-ttu-id="c490f-362">Не используйте закрывающие знаки препинания или многоточие.</span><span class="sxs-lookup"><span data-stu-id="c490f-362">Don't use ending punctuation or ellipsis.</span></span>
-   <span data-ttu-id="c490f-363">Если запрос направляет пользователям ввод данных, которые будут обрабатываться кнопкой рядом с текстовым полем, просто поместите кнопку рядом с текстовым полем.</span><span class="sxs-lookup"><span data-stu-id="c490f-363">If the prompt directs users to enter information that will be acted upon by a button next to the text box, simply place the button next to the text box.</span></span> <span data-ttu-id="c490f-364">Не используйте запрос для направления пользователей на нажатие кнопки (например, не записывайте текст запроса с текстом, перетащите файл и нажмите кнопку Отправить).</span><span class="sxs-lookup"><span data-stu-id="c490f-364">Don't use the prompt to direct users to click the button (for example, don't write prompt text that says, Drag a file and then click Send).</span></span>

## <a name="documentation"></a><span data-ttu-id="c490f-365">Документация</span><span class="sxs-lookup"><span data-stu-id="c490f-365">Documentation</span></span>

<span data-ttu-id="c490f-366">При ссылке на текстовые поля:</span><span class="sxs-lookup"><span data-stu-id="c490f-366">When referring to text boxes:</span></span>

-   <span data-ttu-id="c490f-367">Используйте тип, чтобы ссылаться на взаимодействия пользователей, требующие ввода или записи. в противном случае используйте клавишу ВВОД, если пользователи могут размещать информацию в текстовом поле с помощью других средств, таких как выбор значения из списка или с помощью кнопки обзора.</span><span class="sxs-lookup"><span data-stu-id="c490f-367">Use type to refer to user interactions that require typing or pasting; otherwise use enter if users can put information into the text box using other means, such as selecting the value from a list or using a Browse button.</span></span>
-   <span data-ttu-id="c490f-368">Используйте Select для ссылки на запись в текстовом поле только для чтения.</span><span class="sxs-lookup"><span data-stu-id="c490f-368">Use select to refer to an entry in a read-only text box.</span></span>
-   <span data-ttu-id="c490f-369">Используйте точный текст метки, включая прописную букву, и включите поле Word.</span><span class="sxs-lookup"><span data-stu-id="c490f-369">Use the exact label text, including its capitalization, and include the word box.</span></span> <span data-ttu-id="c490f-370">Не включайте символ подчеркивания или двоеточие.</span><span class="sxs-lookup"><span data-stu-id="c490f-370">Don't include the access key underscore or colon.</span></span> <span data-ttu-id="c490f-371">Не используйте текстовое поле в качестве текстового поля или поля.</span><span class="sxs-lookup"><span data-stu-id="c490f-371">Don't refer to a text box as a text box or a field.</span></span>
-   <span data-ttu-id="c490f-372">По возможности отформатируйте метку, используя полужирный текст.</span><span class="sxs-lookup"><span data-stu-id="c490f-372">When possible, format the label using bold text.</span></span> <span data-ttu-id="c490f-373">В противном случае заключите метку в кавычки, только если это необходимо для предотвращения путаницы.</span><span class="sxs-lookup"><span data-stu-id="c490f-373">Otherwise, put the label in quotation marks only if required to prevent confusion.</span></span>

    <span data-ttu-id="c490f-374">Пример. Введите пароль в поле **пароль** и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="c490f-374">Example: Type your password into the **Password** box, and then click **OK**.</span></span>

-   <span data-ttu-id="c490f-375">Если текстовому полю требуется конкретный формат, задокументируйте только наиболее распространенный допустимый формат.</span><span class="sxs-lookup"><span data-stu-id="c490f-375">If the text box requires a specific format, document only the most commonly used acceptable format.</span></span> <span data-ttu-id="c490f-376">Позвольте пользователям обнаруживать любые другие форматы самостоятельно.</span><span class="sxs-lookup"><span data-stu-id="c490f-376">Let users discover any other formats on their own.</span></span> <span data-ttu-id="c490f-377">Требуется гибкость при работе с форматами данных, но это не должно приводить к созданию сложной документации.</span><span class="sxs-lookup"><span data-stu-id="c490f-377">You want to be flexible with data formats, but doing so should not result in complex documentation.</span></span>

    <span data-ttu-id="c490f-378">**Правильно:**</span><span class="sxs-lookup"><span data-stu-id="c490f-378">**Correct:**</span></span>

    <span data-ttu-id="c490f-379">Введите серийный номер части, используя формат 1234-56-7890.</span><span class="sxs-lookup"><span data-stu-id="c490f-379">Enter the part's serial number using the 1234-56-7890 format.</span></span>

    <span data-ttu-id="c490f-380">**Неправильно**:</span><span class="sxs-lookup"><span data-stu-id="c490f-380">**Incorrect:**</span></span>

    <span data-ttu-id="c490f-381">Введите серийный номер части, используя любой из следующих форматов:</span><span class="sxs-lookup"><span data-stu-id="c490f-381">Enter the part's serial number using any of the following formats:</span></span>

    <span data-ttu-id="c490f-382">1234567890</span><span class="sxs-lookup"><span data-stu-id="c490f-382">1234567890</span></span>

    <span data-ttu-id="c490f-383">1234-56-7890</span><span class="sxs-lookup"><span data-stu-id="c490f-383">1234-56-7890</span></span>

    <span data-ttu-id="c490f-384">1234 56 7890</span><span class="sxs-lookup"><span data-stu-id="c490f-384">1234 56 7890</span></span>

