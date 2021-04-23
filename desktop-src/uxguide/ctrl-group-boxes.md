---
title: Поля группы
description: Поле группы — это прямоугольная рамка с меткой, которая окружает набор связанных элементов управления. Поле группы позволяет отображать связи визуально. Помимо возможности предоставления ключа доступа для группы элементов управления, она не предоставляет никаких функциональных возможностей.
ms.assetid: 5b5ffb36-3ed1-44cd-af87-5cddf46c56a6
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 67f930383f2d4412d30027971c6cab2bd3edcccd
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/10/2021
ms.locfileid: "104563217"
---
# <a name="group-boxes"></a><span data-ttu-id="f560c-104">Поля группы</span><span class="sxs-lookup"><span data-stu-id="f560c-104">Group Boxes</span></span>

> [!NOTE]
> <span data-ttu-id="f560c-105">Это руководство по проектированию было создано для Windows 7 и не Обновлено для более новых версий Windows.</span><span class="sxs-lookup"><span data-stu-id="f560c-105">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="f560c-106">Многие рекомендации по-прежнему применяются в принципе, но презентация и примеры не соответствуют нашим [текущим руководствам по проектированию](/windows/uwp/design/).</span><span class="sxs-lookup"><span data-stu-id="f560c-106">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="f560c-107">Поле группы — это прямоугольная рамка с меткой, которая окружает набор связанных элементов управления.</span><span class="sxs-lookup"><span data-stu-id="f560c-107">A group box is a labeled rectangular frame that surrounds a set of related controls.</span></span> <span data-ttu-id="f560c-108">Поле группы позволяет отображать связи визуально. Помимо возможности предоставления ключа доступа для группы элементов управления, она не предоставляет никаких функциональных возможностей.</span><span class="sxs-lookup"><span data-stu-id="f560c-108">A group box is a way to show relationships visually; aside from possibly providing an access key for a group of controls, it provides no functionality.</span></span>

![<span data-ttu-id="f560c-109">снимок экрана с окном группы с флажками</span><span class="sxs-lookup"><span data-stu-id="f560c-109">screen shot of group box containing check boxes</span></span> ](images/ctrl-group-boxes-image1.png)

<span data-ttu-id="f560c-110">Типичное поле группы.</span><span class="sxs-lookup"><span data-stu-id="f560c-110">A typical group box.</span></span>

> [!Note]  
> <span data-ttu-id="f560c-111">Рекомендации, связанные с [макетом](vis-layout.md) , представлены в отдельной статье.</span><span class="sxs-lookup"><span data-stu-id="f560c-111">Guidelines related to [layout](vis-layout.md) are presented in a separate article.</span></span>

 

## <a name="is-this-the-right-control"></a><span data-ttu-id="f560c-112">Выбор правильного элемента управления</span><span class="sxs-lookup"><span data-stu-id="f560c-112">Is this the right control?</span></span>

<span data-ttu-id="f560c-113">Хотя поля группы являются строгим визуальным средством для указания связей, их чрезмерное использование приводит к недостаточной визуализации и значительно сокращает пространство, доступное на поверхности.</span><span class="sxs-lookup"><span data-stu-id="f560c-113">While group boxes are a strong visual means of indicating relationships, overusing them adds visual clutter and greatly reduces the space available on a surface.</span></span> <span data-ttu-id="f560c-114">Они визуально трудны и должны использоваться экономно, только если нет лучшего решения.</span><span class="sxs-lookup"><span data-stu-id="f560c-114">They are visually heavy and should be used sparingly—only when there isn't a better solution.</span></span>

<span data-ttu-id="f560c-115">Тенденция к проектированию в Windows представляет собой более простой и понятный внешний вид за счет исключения ненужных строк.</span><span class="sxs-lookup"><span data-stu-id="f560c-115">A design trend in Windows is a simpler, cleaner appearance by eliminating unnecessary lines.</span></span>

<span data-ttu-id="f560c-116">Чтобы решить, является ли поле группы обязательным, учитывайте следующие вопросы.</span><span class="sxs-lookup"><span data-stu-id="f560c-116">To decide whether a group box is necessary, consider these questions:</span></span>

-   <span data-ttu-id="f560c-117">**Есть ли в группе более одного элемента управления?**</span><span class="sxs-lookup"><span data-stu-id="f560c-117">**Is there more than one control in the group?**</span></span> <span data-ttu-id="f560c-118">В противном случае используйте обычную текстовую метку.</span><span class="sxs-lookup"><span data-stu-id="f560c-118">If not, use a plain text label instead.</span></span> <span data-ttu-id="f560c-119">Редким исключением является использование поля группы с одним элементом управления для обеспечения согласованности с другими полями группы на той же поверхности.</span><span class="sxs-lookup"><span data-stu-id="f560c-119">A rare exception is to use a group box with a single control to maintain consistency with other group boxes on the same surface.</span></span>

<span data-ttu-id="f560c-120">**Неправильный:** ![ снимок экрана с окном группы, содержащим одно текстовое поле ](images/ctrl-group-boxes-image2.png)</span><span class="sxs-lookup"><span data-stu-id="f560c-120">**Incorrect:** ![screen shot of group box containing one text box ](images/ctrl-group-boxes-image2.png)</span></span>

<span data-ttu-id="f560c-121">В этом примере поле группы содержит только один элемент управления.</span><span class="sxs-lookup"><span data-stu-id="f560c-121">In this example, the group box has only a single control.</span></span>

-   <span data-ttu-id="f560c-122">**Связаны ли элементы управления? Показывает ли связь Добавление ясности?**</span><span class="sxs-lookup"><span data-stu-id="f560c-122">**Are the controls related? Does showing the relationship add clarity?**</span></span> <span data-ttu-id="f560c-123">Если нет, представления элементов управления отдельно за пределами поля группы.</span><span class="sxs-lookup"><span data-stu-id="f560c-123">If not, present the controls separately outside of a group box.</span></span>
-   <span data-ttu-id="f560c-124">**Все элементы управления внутри группы?**</span><span class="sxs-lookup"><span data-stu-id="f560c-124">**Are all the controls inside the group?**</span></span> <span data-ttu-id="f560c-125">Если это так, укажите связь на более крупной поверхности, например в родительском диалоговом окне или странице.</span><span class="sxs-lookup"><span data-stu-id="f560c-125">If so, indicate the relationship on the larger surface, such as the parent dialog box or page.</span></span>

<span data-ttu-id="f560c-126">**Неправильный:** ![ снимок экрана с окном группы, содержащим все элементы управления ](images/ctrl-group-boxes-image3.png)</span><span class="sxs-lookup"><span data-stu-id="f560c-126">**Incorrect:** ![screen shot of group box containing all controls ](images/ctrl-group-boxes-image3.png)</span></span>

<span data-ttu-id="f560c-127">В этом примере все элементы управления (помимо кнопок фиксации) в диалоговом окне находятся в поле Группа.</span><span class="sxs-lookup"><span data-stu-id="f560c-127">In this example, all the controls (aside from the commit buttons) in the dialog box are within the group box.</span></span>

-   <span data-ttu-id="f560c-128">**Можно ли эффективно обмениваться связями, используя только макет?**</span><span class="sxs-lookup"><span data-stu-id="f560c-128">**Can you effectively communicate the relationships using layout alone?**</span></span> <span data-ttu-id="f560c-129">Если это так, используйте вместо этого [Макет](vis-layout.md) .</span><span class="sxs-lookup"><span data-stu-id="f560c-129">If so, use [layout](vis-layout.md) instead.</span></span> <span data-ttu-id="f560c-130">Связанные элементы управления можно разместить рядом друг с другом и разместить дополнительный интервал между несвязанными элементами управления.</span><span class="sxs-lookup"><span data-stu-id="f560c-130">You can place related controls next to each other and put extra spacing between unrelated controls.</span></span> <span data-ttu-id="f560c-131">Можно также использовать заголовки и отступы для отображения иерархических связей.</span><span class="sxs-lookup"><span data-stu-id="f560c-131">You can also use headings and indenting to show hierarchical relationships.</span></span>

![<span data-ttu-id="f560c-132">Рисунок из четырех значков, демонстрирующих четыре группы задач</span><span class="sxs-lookup"><span data-stu-id="f560c-132">figure of four icons showing four groups of tasks</span></span> ](images/ctrl-group-boxes-image4.png)

<span data-ttu-id="f560c-133">В этом примере для отображения отношений управления используется только макет.</span><span class="sxs-lookup"><span data-stu-id="f560c-133">In this example, layout alone is used to show control relationships.</span></span>

-   <span data-ttu-id="f560c-134">**Можно ли эффективно обмениваться связями с помощью разделителя?**</span><span class="sxs-lookup"><span data-stu-id="f560c-134">**Can you effectively communicate the relationships using a separator?**</span></span> <span data-ttu-id="f560c-135">Если это так, используйте вместо этого разделитель.</span><span class="sxs-lookup"><span data-stu-id="f560c-135">If so, use a separator instead.</span></span> <span data-ttu-id="f560c-136">Разделитель — это горизонтальная линия, которая объединяет элементы управления, расположенные под ним.</span><span class="sxs-lookup"><span data-stu-id="f560c-136">A separator is a horizontal line that unifies the controls below it.</span></span> <span data-ttu-id="f560c-137">Разделители предоставляют более простой и понятный внешний вид.</span><span class="sxs-lookup"><span data-stu-id="f560c-137">Separators provide a simpler, cleaner look.</span></span> <span data-ttu-id="f560c-138">Однако, в отличие от полей группы, они работают лучше, если они охватывают всю ширину поверхности.</span><span class="sxs-lookup"><span data-stu-id="f560c-138">However, unlike group boxes, they work best when they span the full width of the surface.</span></span>
    -   <span data-ttu-id="f560c-139">**Разработчики:** Можно реализовать разделитель с вдавленное прямоугольником с высотой 1.</span><span class="sxs-lookup"><span data-stu-id="f560c-139">**Developers:** You can implement a separator with an etched rectangle with a height of one.</span></span>

![Снимок экрана, на котором показаны элементы управления электронной почты, разделенные перекрашенными разделителями прямоугольника.](images/ctrl-group-boxes-image5.png)

<span data-ttu-id="f560c-141">В этом примере отмеченные разделители используются для отображения отношений управления.</span><span class="sxs-lookup"><span data-stu-id="f560c-141">In this example, labeled separators are used to show control relationships.</span></span>

![<span data-ttu-id="f560c-142">снимок экрана элементов управления, разделенных разделителями</span><span class="sxs-lookup"><span data-stu-id="f560c-142">screen shot of controls set apart by separators</span></span> ](images/ctrl-group-boxes-image6.png)

<span data-ttu-id="f560c-143">В этом примере непомеченные разделители используются для отображения отношений элементов управления.</span><span class="sxs-lookup"><span data-stu-id="f560c-143">In this example, unlabeled separators are used to show control relationships.</span></span>

-   <span data-ttu-id="f560c-144">**Можно ли эффективно обмениваться связями без текста?**</span><span class="sxs-lookup"><span data-stu-id="f560c-144">**Can you effectively communicate the relationships without text?**</span></span> <span data-ttu-id="f560c-145">Если это так, рассмотрите возможность использования графических элементов, например [фона](vis-graphic.md) или агрегатов.</span><span class="sxs-lookup"><span data-stu-id="f560c-145">If so, consider using graphic elements such as [backgrounds](vis-graphic.md) or aggregators.</span></span>

## <a name="guidelines"></a><span data-ttu-id="f560c-146">Рекомендации</span><span class="sxs-lookup"><span data-stu-id="f560c-146">Guidelines</span></span>

-   <span data-ttu-id="f560c-147">**Не вкладывать поля в группы.**</span><span class="sxs-lookup"><span data-stu-id="f560c-147">**Don't nest group boxes.**</span></span> <span data-ttu-id="f560c-148">Используйте макет для отображения связей в поле группы.</span><span class="sxs-lookup"><span data-stu-id="f560c-148">Use layout to show relationships within a group box.</span></span>

<span data-ttu-id="f560c-149">**Неправильный:** ![ снимок экрана поля группы в поле группы ](images/ctrl-group-boxes-image7.png)</span><span class="sxs-lookup"><span data-stu-id="f560c-149">**Incorrect:** ![screen shot of a group box within a group box ](images/ctrl-group-boxes-image7.png)</span></span>

<span data-ttu-id="f560c-150">В этом примере вложенные поля группы приводят к ненужным визуальным помехам.</span><span class="sxs-lookup"><span data-stu-id="f560c-150">In this example, the nested group boxes result in unnecessary visual clutter.</span></span>

<span data-ttu-id="f560c-151">**Исправить:** ![ снимок экрана одного элемента управления в одном поле группы ](images/ctrl-group-boxes-image8.png)</span><span class="sxs-lookup"><span data-stu-id="f560c-151">**Correct:** ![screen shot of same controls within one group box ](images/ctrl-group-boxes-image8.png)</span></span>

<span data-ttu-id="f560c-152">В этом примере та же связь элемента управления отображается с помощью макета.</span><span class="sxs-lookup"><span data-stu-id="f560c-152">In this example, the same control relationship is shown using layout instead.</span></span>

-   <span data-ttu-id="f560c-153">Не помещайте элементы управления в метки поля группы.</span><span class="sxs-lookup"><span data-stu-id="f560c-153">Don't put controls in group box labels.</span></span>
    -   <span data-ttu-id="f560c-154">**Исключение:** Флажок можно использовать как метку поля группы, если все элементы управления внутри поля включены и отключены флажком.</span><span class="sxs-lookup"><span data-stu-id="f560c-154">**Exception:** You can use a check box as a group box label if all of the controls inside the box are enabled and disabled by the check box.</span></span>

<span data-ttu-id="f560c-155">**Неправильный:** ![ снимок экрана с раскрывающимся списком на метке группы ](images/ctrl-group-boxes-image9.png)</span><span class="sxs-lookup"><span data-stu-id="f560c-155">**Incorrect:** ![screen shot of drop-down list on a group-box label ](images/ctrl-group-boxes-image9.png)</span></span>

<span data-ttu-id="f560c-156">В этом примере раскрывающийся список неправильно помещается в поле группы.</span><span class="sxs-lookup"><span data-stu-id="f560c-156">In this example, a drop-down list is incorrectly placed on a group box.</span></span> <span data-ttu-id="f560c-157">В этом примере вместо этого следует использовать [вкладки](https://msdn.microsoft.com/library/windows/desktop/aa511493.aspx) .</span><span class="sxs-lookup"><span data-stu-id="f560c-157">This example should use [tabs](https://msdn.microsoft.com/library/windows/desktop/aa511493.aspx) instead.</span></span>

-   <span data-ttu-id="f560c-158">**Не отключайте поля группы.**</span><span class="sxs-lookup"><span data-stu-id="f560c-158">**Don't disable group boxes.**</span></span> <span data-ttu-id="f560c-159">Чтобы указать, что группа элементов управления в настоящее время не применяется, отключите все элементы управления в поле группы, но не саму группу.</span><span class="sxs-lookup"><span data-stu-id="f560c-159">To indicate that a group of controls doesn't currently apply, disable all the controls within the group box, but not the group box itself.</span></span> <span data-ttu-id="f560c-160">Этот подход является более доступным и может поддерживаться единообразно всеми платформами пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="f560c-160">This approach is more accessible and can be supported consistently by all UI frameworks.</span></span>

## <a name="labels"></a><span data-ttu-id="f560c-161">Метки</span><span class="sxs-lookup"><span data-stu-id="f560c-161">Labels</span></span>

-   <span data-ttu-id="f560c-162">Пометка всех полей группы.</span><span class="sxs-lookup"><span data-stu-id="f560c-162">Label all group boxes.</span></span>
-   <span data-ttu-id="f560c-163">Не присваивайте метке ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="f560c-163">Don't assign an access key to the label.</span></span> <span data-ttu-id="f560c-164">Это не является обязательным и делает другие клавиши доступа более сложными для назначения.</span><span class="sxs-lookup"><span data-stu-id="f560c-164">Doing so is unnecessary and makes the other access keys harder to assign.</span></span> <span data-ttu-id="f560c-165">Вместо этого назначьте ключи доступа элементам управления в поле группы.</span><span class="sxs-lookup"><span data-stu-id="f560c-165">Instead, assign access keys to the controls within the group box.</span></span>
    -   <span data-ttu-id="f560c-166">**Исключение:** Если у поверхности много элементов управления, доступные ключи доступа могут быть недостаточно.</span><span class="sxs-lookup"><span data-stu-id="f560c-166">**Exception:** If a surface has many controls, there may not be enough access keys available.</span></span> <span data-ttu-id="f560c-167">Если это так, сократите число ключей доступа, назначив их группам, а не элементам управления в полях группы.</span><span class="sxs-lookup"><span data-stu-id="f560c-167">If so, reduce the number of access keys by assigning them to group boxes instead of the controls within the group boxes.</span></span>
-   <span data-ttu-id="f560c-168">Используйте [прописные буквы в стиле предложения](glossary.md).</span><span class="sxs-lookup"><span data-stu-id="f560c-168">Use [sentence-style capitalization](glossary.md).</span></span>
-   <span data-ttu-id="f560c-169">Напишите метку с помощью существительного или существительного, а не предложения и не используйте закрывающие знаки препинания, включая двоеточия.</span><span class="sxs-lookup"><span data-stu-id="f560c-169">Write the label using a noun or a noun phrase, not as a sentence, and use no ending punctuation, including colons.</span></span>
-   <span data-ttu-id="f560c-170">Используйте параллельные выражения для меток Box группы в той же поверхности.</span><span class="sxs-lookup"><span data-stu-id="f560c-170">Use parallel phrasing for group box labels within the same surface.</span></span>
-   <span data-ttu-id="f560c-171">Оставляйте краткие метки полей группы.</span><span class="sxs-lookup"><span data-stu-id="f560c-171">Keep group box labels concise.</span></span> <span data-ttu-id="f560c-172">Не используйте в качестве метки пояснительный текст.</span><span class="sxs-lookup"><span data-stu-id="f560c-172">Don't use instructional text as the label.</span></span> <span data-ttu-id="f560c-173">Однако можно иметь пояснительный текст в поле группы.</span><span class="sxs-lookup"><span data-stu-id="f560c-173">You can have instructional text within the group box, however.</span></span>
-   <span data-ttu-id="f560c-174">Не повторяйте метку группы в надписях элементов управления в поле.</span><span class="sxs-lookup"><span data-stu-id="f560c-174">Don't repeat the group box label in control labels within the box.</span></span> <span data-ttu-id="f560c-175">Например, если поле группы помечено как выравнивание, пометка переключателей слева, справа и т. д., без выравнивания по левому краю или по правому краю.</span><span class="sxs-lookup"><span data-stu-id="f560c-175">For example, if the group box is labeled Alignment, label the option buttons Left, Right, and so on, not Left alignment or Right alignment.</span></span>
-   <span data-ttu-id="f560c-176">Не используйте поля группы в тексте пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="f560c-176">Don't refer to group boxes in user interface text.</span></span>

## <a name="documentation"></a><span data-ttu-id="f560c-177">Документация</span><span class="sxs-lookup"><span data-stu-id="f560c-177">Documentation</span></span>

<span data-ttu-id="f560c-178">При ссылке на поля группы:</span><span class="sxs-lookup"><span data-stu-id="f560c-178">When referring to group boxes:</span></span>

-   <span data-ttu-id="f560c-179">Ознакомьтесь с полями групп только в программистах и других технических документах.</span><span class="sxs-lookup"><span data-stu-id="f560c-179">Refer to group boxes only in programmer and other technical documentation.</span></span> <span data-ttu-id="f560c-180">В поле Группа используйте два слова в нижнем регистре.</span><span class="sxs-lookup"><span data-stu-id="f560c-180">For group box, use two lowercase words.</span></span>
-   <span data-ttu-id="f560c-181">В любом другом случае не нужно включать имя поля группы в процедуру, если только диалоговое окно не содержит более одного параметра с тем же именем.</span><span class="sxs-lookup"><span data-stu-id="f560c-181">Everywhere else, it is unnecessary to include the name of the group box in a procedure unless a dialog box contains more than one option with the same name.</span></span> <span data-ttu-id="f560c-182">В таких случаях используйте в поле с именем группы.</span><span class="sxs-lookup"><span data-stu-id="f560c-182">In such cases, use under with the group box name.</span></span>
-   <span data-ttu-id="f560c-183">По возможности отформатируйте метку, используя полужирный текст.</span><span class="sxs-lookup"><span data-stu-id="f560c-183">When possible, format the label using bold text.</span></span> <span data-ttu-id="f560c-184">В противном случае заключите метку в кавычки, только если это необходимо для предотвращения путаницы.</span><span class="sxs-lookup"><span data-stu-id="f560c-184">Otherwise, put the label in quotation marks only if required to prevent confusion.</span></span>

<span data-ttu-id="f560c-185">Пример. в разделе " **эффекты**" выберите **скрытый**.</span><span class="sxs-lookup"><span data-stu-id="f560c-185">Example: Under **Effects**, select **Hidden**.</span></span>

 

 