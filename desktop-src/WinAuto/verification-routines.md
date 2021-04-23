---
title: Подпрограммы проверки
description: В этом разделе описываются подпрограммы проверки доступности пользовательского интерфейса, которые можно использовать для тестирования реализации специальных возможностей приложения.
ms.assetid: 0ff38f83-5741-4c0e-a070-a8385f95eba3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78eea821a4c918078c6390e33fa7046de1452f76
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330216"
---
# <a name="verification-routines"></a><span data-ttu-id="da2b5-103">Подпрограммы проверки</span><span class="sxs-lookup"><span data-stu-id="da2b5-103">Verification Routines</span></span>

<span data-ttu-id="da2b5-104">В этом разделе описываются подпрограммы проверки доступности пользовательского интерфейса, которые можно использовать для тестирования реализации специальных возможностей приложения.</span><span class="sxs-lookup"><span data-stu-id="da2b5-104">This section describes the verification routines that UI Accessibility Checker can run to test an application's accessibility implementation.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="da2b5-105">Категория</span><span class="sxs-lookup"><span data-stu-id="da2b5-105">Category</span></span></th>
<th><span data-ttu-id="da2b5-106">Подпрограмма</span><span class="sxs-lookup"><span data-stu-id="da2b5-106">Routine</span></span></th>
<th><span data-ttu-id="da2b5-107">Описание</span><span class="sxs-lookup"><span data-stu-id="da2b5-107">Description</span></span></th>
</tr><span data-ttu-id="da2b5-108">
</thead>
<tbody>
<tr class="odd">
<td rowspan="2"><strong>Согласованность</strong>$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="da2b5-108">
</thead>
<tbody>
<tr class="odd">
<td rowspan="2"><strong>Consistency</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="da2b5-109"><strong>скринреадер</strong></span><span class="sxs-lookup"><span data-stu-id="da2b5-109"><strong>ScreenReader</strong></span></span></td>
<td><span data-ttu-id="da2b5-110">Компилирует все видимые элементы в целевом объекте проверки и отображает их в элементе управления ListView в том порядке, в котором Стандартный средство чтения с экрана сообщает о них пользователю.</span><span class="sxs-lookup"><span data-stu-id="da2b5-110">Compiles all visible elements in the verification target and displays them in a ListView control in the order that a standard screen reader announces them to a user.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="da2b5-111"><strong>уиаскринреадер</strong></span><span class="sxs-lookup"><span data-stu-id="da2b5-111"><strong>UiaScreenReader</strong></span></span></td>
<td><span data-ttu-id="da2b5-112">То же, что и <strong>скринреадер</strong>, но для реализации UIA.</span><span class="sxs-lookup"><span data-stu-id="da2b5-112">Same as <strong>ScreenReader</strong>, but for UIA implementations.</span></span></td>

</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="da2b5-113"><strong>Навигация</strong>$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="da2b5-113"><strong>Navigation</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="da2b5-114"><strong>чекктридепс</strong></span><span class="sxs-lookup"><span data-stu-id="da2b5-114"><strong>CheckTreeDepth</strong></span></span></td>
<td><span data-ttu-id="da2b5-115">Отправляет символы табуляции (или SHIFT + TAB) в качестве входных данных в целевой объект проверки, чтобы убедиться в том, что пользовательский интерфейс целевого объекта не слишком сложен или недоступен с помощью стандартной навигации по клавиатуре.</span><span class="sxs-lookup"><span data-stu-id="da2b5-115">Sends Tab (or Shift+Tab) characters as input to the verification target to confirm that the target's UI isn't overly complex or inaccessible using standard keyboard navigation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="da2b5-116"><strong>чекктаббингуиа</strong></span><span class="sxs-lookup"><span data-stu-id="da2b5-116"><strong>CheckTabbingUia</strong></span></span></td>
<td><span data-ttu-id="da2b5-117">Отправляет символы табуляции (или SHIFT + TAB) в качестве входных данных в целевой объект проверки, чтобы убедиться, что все фокусы в пользовательском интерфейсе доступны в правильном порядке, с помощью стандартной навигации по клавиатуре.</span><span class="sxs-lookup"><span data-stu-id="da2b5-117">Sends Tab (or Shift+Tab) characters as input to the verification target to confirm that all focusable elements in the UI are reachable in an orderly, logical fashion using standard keyboard navigation.</span></span></td>

</tr>
<tr class="odd">
<td rowspan="5"><span data-ttu-id="da2b5-118"><strong>Свойства</strong>$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="da2b5-118"><strong>Properties</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="da2b5-119"><strong>чеккроле</strong></span><span class="sxs-lookup"><span data-stu-id="da2b5-119"><strong>CheckRole</strong></span></span></td>
<td><span data-ttu-id="da2b5-120">Подтверждает, что каждый сфокусированный элемент в пользовательском интерфейсе сообщает о допустимой логической роли MSAA и что элемент управления имеет значение, требуемое этой ролью.</span><span class="sxs-lookup"><span data-stu-id="da2b5-120">Confirms that each focusable element in the UI reports a valid, logical MSAA role, and that the control has a value as required by that role.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="da2b5-121"><strong>Свойство CheckState</strong></span><span class="sxs-lookup"><span data-stu-id="da2b5-121"><strong>CheckState</strong></span></span></td>
<td><span data-ttu-id="da2b5-122">Подтверждает, что каждый фокусный элемент в пользовательском интерфейсе сообщает допустимое логическое состояние MSAA.</span><span class="sxs-lookup"><span data-stu-id="da2b5-122">Confirms that each focusable element in the UI reports a valid, logical MSAA state.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="da2b5-123"><strong>CheckName</strong></span><span class="sxs-lookup"><span data-stu-id="da2b5-123"><strong>CheckName</strong></span></span></td>
<td><span data-ttu-id="da2b5-124">Подтверждает, что каждый фокусный элемент в пользовательском интерфейсе сообщает допустимое логическое имя MSAA.</span><span class="sxs-lookup"><span data-stu-id="da2b5-124">Confirms that each focusable element in the UI reports a valid, logical MSAA name.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="da2b5-125"><strong>чеккакцесскэйс</strong></span><span class="sxs-lookup"><span data-stu-id="da2b5-125"><strong>CheckAccessKeys</strong></span></span></td>
<td><span data-ttu-id="da2b5-126">Подтверждает, что ключи доступа, назначенные элементам в целевом объекте проверки, являются уникальными в рамках целевого объекта проверки.</span><span class="sxs-lookup"><span data-stu-id="da2b5-126">Confirms that access keys that are assigned to elements in the verification target are unique within the verification target.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="da2b5-127"><strong>чеккбаундингрект</strong></span><span class="sxs-lookup"><span data-stu-id="da2b5-127"><strong>CheckBoundingRect</strong></span></span></td>
<td><span data-ttu-id="da2b5-128">Подтверждает, что каждый сфокусированный элемент в пользовательском интерфейсе имеет ограничивающий прямоугольник, который можно использовать в качестве целевого объекта для проверки попадания.</span><span class="sxs-lookup"><span data-stu-id="da2b5-128">Confirms that each focusable element in the UI has a bounding rectangle that can be used as a target for hit testing.</span></span></td>

</tr>
<tr class="even">
<td rowspan="2"><span data-ttu-id="da2b5-129"><strong>Дерево</strong>$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="da2b5-129"><strong>Tree</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="da2b5-130"><strong>чеккпарентчилд</strong></span><span class="sxs-lookup"><span data-stu-id="da2b5-130"><strong>CheckParentChild</strong></span></span></td>
<td><span data-ttu-id="da2b5-131">Родительские и дочерние отношения в дереве элементов являются единообразными и прогнозируемыми.</span><span class="sxs-lookup"><span data-stu-id="da2b5-131">Parent and child relationships in the element tree are consistent and predictable.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="da2b5-132"><strong>чеккорфанчилдрен</strong></span><span class="sxs-lookup"><span data-stu-id="da2b5-132"><strong>CheckOrphanChildren</strong></span></span></td>
<td><span data-ttu-id="da2b5-133">Подтверждает, что каждый фокусный элемент в пользовательском интерфейсе сообщает о допустимом родителе MSAA.</span><span class="sxs-lookup"><span data-stu-id="da2b5-133">Confirms that each focusable element in the UI reports a valid MSAA parent.</span></span></td>

</tr>
<tr class="even">
<td rowspan="6"><span data-ttu-id="da2b5-134"><strong>Свойства UIA</strong>$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="da2b5-134"><strong>UIA Properties</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="da2b5-135"><strong>чеккнамеуиа</strong></span><span class="sxs-lookup"><span data-stu-id="da2b5-135"><strong>CheckNameUIA</strong></span></span></td>
<td><span data-ttu-id="da2b5-136">Подтверждает, что каждый фокусный элемент в пользовательском интерфейсе сообщает допустимое логическое имя UIA.</span><span class="sxs-lookup"><span data-stu-id="da2b5-136">Confirms that each focusable element in the UI reports a valid, logical UIA name.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="da2b5-137"><strong>чекктридепсуиа</strong></span><span class="sxs-lookup"><span data-stu-id="da2b5-137"><strong>CheckTreeDepthUIA</strong></span></span></td>
<td><span data-ttu-id="da2b5-138">Отправляет символы табуляции (или SHIFT + TAB) в качестве входных данных в целевой объект проверки, чтобы убедиться, что элементы UIA в пользовательском интерфейсе не слишком сложны или недоступны с помощью стандартной навигации по клавиатуре.</span><span class="sxs-lookup"><span data-stu-id="da2b5-138">Sends Tab (or Shift+Tab) characters as input to the verification target to confirm that to UIA elements in the target's UI aren't overly complex or inaccessible using standard keyboard navigation.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="da2b5-139"><strong>чеккстатеуиа</strong></span><span class="sxs-lookup"><span data-stu-id="da2b5-139"><strong>CheckStateUIA</strong></span></span></td>
<td><span data-ttu-id="da2b5-140">Подтверждает, что каждый фокусный элемент в пользовательском интерфейсе сообщает допустимое логическое состояние UIA.</span><span class="sxs-lookup"><span data-stu-id="da2b5-140">Confirms that each focusable element in the UI reports a valid, logical UIA state.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="da2b5-141"><strong>чеккакцесскэйсуиа</strong></span><span class="sxs-lookup"><span data-stu-id="da2b5-141"><strong>CheckAccessKeysUIA</strong></span></span></td>
<td><span data-ttu-id="da2b5-142">Подтверждает, что родственные элементы не имеют одинакового доступа и (или) сочетания клавиш.</span><span class="sxs-lookup"><span data-stu-id="da2b5-142">Confirms that sibling elements do not have the same access and/or accelerator key.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="da2b5-143"><strong>чеккбаундингректуиа</strong></span><span class="sxs-lookup"><span data-stu-id="da2b5-143"><strong>CheckBoundingRectUIA</strong></span></span></td>
<td><span data-ttu-id="da2b5-144">Подтверждает, что каждый сфокусированный элемент UIA в пользовательском интерфейсе имеет ограничивающий прямоугольник, который можно использовать в качестве целевого объекта для проверки попадания.</span><span class="sxs-lookup"><span data-stu-id="da2b5-144">Confirms that each focusable UIA element in the UI has a bounding rectangle that can be used as a target for hit testing.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="da2b5-145"><strong>чеккконтролтипеуиа</strong></span><span class="sxs-lookup"><span data-stu-id="da2b5-145"><strong>CheckControlTypeUIA</strong></span></span></td>
<td><span data-ttu-id="da2b5-146">Подтверждает, что каждый фокусный элемент в пользовательском интерфейсе сообщает о допустимом логическом типе элемента управления UIA.</span><span class="sxs-lookup"><span data-stu-id="da2b5-146">Confirms that each focusable element in the UI reports a valid, logical UIA control type.</span></span></td>

</tr>
<tr class="even">
<td rowspan="3"><span data-ttu-id="da2b5-147"><strong>Дерево UIA</strong>$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="da2b5-147"><strong>UIA Tree</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="da2b5-148"><strong>чеккнавигатеуиа</strong></span><span class="sxs-lookup"><span data-stu-id="da2b5-148"><strong>CheckNavigateUia</strong></span></span></td>
<td><span data-ttu-id="da2b5-149">Подтверждает, что UIA Тривалкер может перемещаться по дочерним элементам элемента.</span><span class="sxs-lookup"><span data-stu-id="da2b5-149">Confirms that the UIA TreeWalker can navigate through an element's children.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="da2b5-150"><strong>чеккорфанчилдренуиа</strong></span><span class="sxs-lookup"><span data-stu-id="da2b5-150"><strong>CheckOrphanChildrenUia</strong></span></span></td>
<td><span data-ttu-id="da2b5-151">Подтверждает, что каждый фокусный элемент в пользовательском интерфейсе сообщает о допустимом родителе UIA.</span><span class="sxs-lookup"><span data-stu-id="da2b5-151">Confirms that each focusable element in the UI reports a valid UIA parent.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="da2b5-152"><strong>чекксиблингсуиа</strong></span><span class="sxs-lookup"><span data-stu-id="da2b5-152"><strong>CheckSiblingsUia</strong></span></span></td>
<td><span data-ttu-id="da2b5-153">Подтверждает, что родственные элементы имеют разные пары "имя: ControlType" и "AutomationId".</span><span class="sxs-lookup"><span data-stu-id="da2b5-153">Confirms that sibling elements do not have the same Name:ControlType pairs, nor the same AutomationId's.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="da2b5-154">$ {ROWSPAN9} $<strong>ARIA веб-проверки</strong>$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="da2b5-154">${ROWSPAN9}$<strong>ARIA Web Verifications</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="da2b5-155"><strong>чеккариароле</strong></span><span class="sxs-lookup"><span data-stu-id="da2b5-155"><strong>CheckARIARole</strong></span></span></td>
<td><span data-ttu-id="da2b5-156">Подтверждает, что все элементы имеют допустимую роль ARIA.</span><span class="sxs-lookup"><span data-stu-id="da2b5-156">Confirms that all elements have a valid ARIA role.</span></span> <span data-ttu-id="da2b5-157">Связанный тег HTML и роль ARIA являются информационными элементами с недопустимыми ролями, помеченными как ошибки.</span><span class="sxs-lookup"><span data-stu-id="da2b5-157">The associated HTML tag and ARIA role are information elements with invalid roles flagged as errors.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="da2b5-158"><strong>чекклабел</strong></span><span class="sxs-lookup"><span data-stu-id="da2b5-158"><strong>CheckLabel</strong></span></span></td>
<td><span data-ttu-id="da2b5-159">Подтверждает, что каждый элемент, у которого есть кнопка ввода, кнопка, изображение или роль ориентира, имеет метку.</span><span class="sxs-lookup"><span data-stu-id="da2b5-159">Confirms each element with input, button, image-button, or landmark role has a label.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="da2b5-160"><strong>чеккранжеконтролс</strong></span><span class="sxs-lookup"><span data-stu-id="da2b5-160"><strong>CheckRangeControls</strong></span></span></td>
<td><span data-ttu-id="da2b5-161">Для подтверждения элементов управления диапазоном с помощью ползунка или роли индикатора выполнения определены правильные атрибуты ARIA.</span><span class="sxs-lookup"><span data-stu-id="da2b5-161">Confirms range controls with slider or progress bar role have proper ARIA attributes defined.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="da2b5-162"><strong>чеккконтаинерроле</strong></span><span class="sxs-lookup"><span data-stu-id="da2b5-162"><strong>CheckContainerRole</strong></span></span></td>
<td><span data-ttu-id="da2b5-163">Подтверждает, что элемент или хотя бы один из его дочерних элементов имеет определенную клавишу "KeyDown" или "OnKeyDown".</span><span class="sxs-lookup"><span data-stu-id="da2b5-163">Confirms an element, or at least one of its children, has onkeydown/onkeypress defined.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="da2b5-164"><strong>чекклайауттабле</strong></span><span class="sxs-lookup"><span data-stu-id="da2b5-164"><strong>CheckLayoutTable</strong></span></span></td>
<td><span data-ttu-id="da2b5-165">Подтверждает, что макет таблицы содержит Summary/TH/ARIA-DescribedBy.</span><span class="sxs-lookup"><span data-stu-id="da2b5-165">Confirms a table layout has a summary/th/aria-describedby included.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="da2b5-166"><strong>чеккгридструктуре</strong></span><span class="sxs-lookup"><span data-stu-id="da2b5-166"><strong>CheckGridStructure</strong></span></span></td>
<td><span data-ttu-id="da2b5-167">Подтверждает, что элемент, не являющийся табличным, с ролью сетки имеет структуру>строк>гридцелл со связанными атрибутами.</span><span class="sxs-lookup"><span data-stu-id="da2b5-167">Confirms a non-table element with grid role has a structure of grid>row>gridcell with associated attributes.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="da2b5-168"><strong>чеккдататабле</strong></span><span class="sxs-lookup"><span data-stu-id="da2b5-168"><strong>CheckDataTable</strong></span></span></td>
<td><span data-ttu-id="da2b5-169">Подтверждает свойства таблиц данных.</span><span class="sxs-lookup"><span data-stu-id="da2b5-169">Confirms the properties of data tables.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="da2b5-170"><strong>чеккактиведесцендантс</strong></span><span class="sxs-lookup"><span data-stu-id="da2b5-170"><strong>CheckActiveDescendants</strong></span></span></td>
<td><span data-ttu-id="da2b5-171">Проверяет свойства элементов с определенным активным потомком.</span><span class="sxs-lookup"><span data-stu-id="da2b5-171">Confirms the properties of elements with an active descendant defined.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="da2b5-172"><strong>чеккелементсвискликкхандлер</strong></span><span class="sxs-lookup"><span data-stu-id="da2b5-172"><strong>CheckElementsWithClickHandler</strong></span></span></td>
<td><span data-ttu-id="da2b5-173">Подтверждает индекс вкладки элементов с помощью обработчиков щелчков.</span><span class="sxs-lookup"><span data-stu-id="da2b5-173">Confirms the tab index of elements with click handlers.</span></span></td>

</tr>
<tr class="even">
<td rowspan="3"><span data-ttu-id="da2b5-174"><strong>Веб-проверки</strong>$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="da2b5-174"><strong>Web Verifications</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="da2b5-175"><strong>Чеккхтмл (веб)</strong></span><span class="sxs-lookup"><span data-stu-id="da2b5-175"><strong>CheckHtml (Web)</strong></span></span></td>
<td><span data-ttu-id="da2b5-176">Подтверждает различные характеристики HTML, такие как заголовки, имена, фреймы и заголовки.</span><span class="sxs-lookup"><span data-stu-id="da2b5-176">Confirms various HTML characteristics such as headers, name, frames, and titles.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="da2b5-177"><strong>CheckName (веб)</strong></span><span class="sxs-lookup"><span data-stu-id="da2b5-177"><strong>CheckName (Web)</strong></span></span></td>
<td><span data-ttu-id="da2b5-178">Подтверждает такие характеристики имени, как длина, недопустимые символы и включение роли.</span><span class="sxs-lookup"><span data-stu-id="da2b5-178">Confirms name characteristics such as length, invalid characters, and role inclusion.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="da2b5-179"><strong>Чеккроле (веб)</strong></span><span class="sxs-lookup"><span data-stu-id="da2b5-179"><strong>CheckRole (Web)</strong></span></span></td>
<td><span data-ttu-id="da2b5-180">Подтверждает недопустимые роли, роли, которые должны иметь значения, и (или) роли, не реализованные.</span><span class="sxs-lookup"><span data-stu-id="da2b5-180">Confirms invalid roles, roles that should have values, and/or roles not implemented.</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="da2b5-181">См. также</span><span class="sxs-lookup"><span data-stu-id="da2b5-181">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="da2b5-182">Средство UI Accessibility Checker</span><span class="sxs-lookup"><span data-stu-id="da2b5-182">UI Accessibility Checker</span></span>](ui-accessibility-checker.md)
</dt> </dl>

 

 




