---
description: ICE34 проверяет, что каждый переключатель в каждом элементе управления Радиобуттонграуп имеет свойство в столбце свойств таблицы RadioButton, в котором указана группа переключателей.
ms.assetid: 23a88a5a-89e9-47bc-9c0a-6101ce03123c
title: ICE34
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7723cb530397eae66374b0f218db9ad8505195a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663661"
---
# <a name="ice34"></a><span data-ttu-id="8183d-103">ICE34</span><span class="sxs-lookup"><span data-stu-id="8183d-103">ICE34</span></span>

<span data-ttu-id="8183d-104">ICE34 проверяет, что каждый переключатель в каждом [элементе управления радиобуттонграуп](radiobuttongroup-control.md) имеет свойство в столбце свойств [таблицы RadioButton](radiobutton-table.md) , в котором указана группа переключателей.</span><span class="sxs-lookup"><span data-stu-id="8183d-104">ICE34 validates that each radio button on every [RadioButtonGroup Control](radiobuttongroup-control.md) has a property in the Property column of the [RadioButton table](radiobutton-table.md) that specifies its radio button group.</span></span> <span data-ttu-id="8183d-105">ICE34 проверяет, существует это свойство и имеет значение по умолчанию в [таблице свойств](property-table.md) , равное одному из значений переключателей группы в столбце значение таблицы RadioButton.</span><span class="sxs-lookup"><span data-stu-id="8183d-105">ICE34 validates that this property exists and is set to a default value in the [Property table](property-table.md) which is equal to one of the group's radio button values in the Value column of the RadioButton table.</span></span>

<span data-ttu-id="8183d-106">Группа переключателей должна иметь значение по умолчанию, чтобы пользователи могли выбрать нужный вариант с помощью клавиши TAB.</span><span class="sxs-lookup"><span data-stu-id="8183d-106">A radio button group must have a default for users to be able to select a choice using the TAB key.</span></span> <span data-ttu-id="8183d-107">Это необходимо для правильного доступа пользователей.</span><span class="sxs-lookup"><span data-stu-id="8183d-107">This is required for proper user accessibility.</span></span>

<span data-ttu-id="8183d-108">ICE34 сообщает об отсутствии таблиц.</span><span class="sxs-lookup"><span data-stu-id="8183d-108">ICE34 reports missing tables.</span></span>

## <a name="result"></a><span data-ttu-id="8183d-109">Результат</span><span class="sxs-lookup"><span data-stu-id="8183d-109">Result</span></span>

<span data-ttu-id="8183d-110">ICE34 отправить сообщение об ошибке, если имеется переключатель, указывающий недопустимое свойство.</span><span class="sxs-lookup"><span data-stu-id="8183d-110">ICE34 post an error message if there is a radio button that specifies an invalid property.</span></span>

## <a name="example"></a><span data-ttu-id="8183d-111">Пример</span><span class="sxs-lookup"><span data-stu-id="8183d-111">Example</span></span>

<span data-ttu-id="8183d-112">ICE34 сообщает о следующих ошибках в приведенном примере.</span><span class="sxs-lookup"><span data-stu-id="8183d-112">ICE34 reports the following errors for the example shown.</span></span>



| <span data-ttu-id="8183d-113">ICE34, ошибка</span><span class="sxs-lookup"><span data-stu-id="8183d-113">ICE34 error</span></span>                                                                                                                                                                | <span data-ttu-id="8183d-114">Описание</span><span class="sxs-lookup"><span data-stu-id="8183d-114">Description</span></span>                                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8183d-115">Диалоговое окно управления. Control2 должно иметь свойство, так как оно имеет тип Радиобуттонграуп.</span><span class="sxs-lookup"><span data-stu-id="8183d-115">Control DialogA.Control2 must have a property because it is of type RadioButtonGroup.</span></span>                                                                                      | <span data-ttu-id="8183d-116">Существует [элемент управления радиобуттонграуп](radiobuttongroup-control.md)без [неявного контрольного](indirect-control-attribute.md) бита в столбце Attributes [таблицы Control](control-table.md), у которого нет свойства, указанного в столбце свойств.</span><span class="sxs-lookup"><span data-stu-id="8183d-116">There is a [RadioButtonGroup control](radiobuttongroup-control.md), without the [Indirect control](indirect-control-attribute.md) bit set in the Attributes column of the [Control table](control-table.md), that does not have a property listed in the Property column.</span></span> |
| <span data-ttu-id="8183d-117">Возможно, не является допустимым значением по умолчанию для Радиобуттонграуп с помощью свойства Property3.</span><span class="sxs-lookup"><span data-stu-id="8183d-117">Maybe is not a valid default value for the RadioButtonGroup using property Property3.</span></span> <span data-ttu-id="8183d-118">Значение должно быть указано в виде параметра в таблице Радиобуттонграуп.</span><span class="sxs-lookup"><span data-stu-id="8183d-118">The value must be listed as an option in the RadioButtonGroup table.</span></span>                 | <span data-ttu-id="8183d-119">Значение по умолчанию для свойства, указанного в столбце значение [таблицы свойств](property-table.md) , не является одним из значений для группы переключателей, указанной в столбце значение [таблицы RadioButton](radiobutton-table.md).</span><span class="sxs-lookup"><span data-stu-id="8183d-119">There is a default value for a property specified in the Value column of the [Property table](property-table.md) that is not one of the values for the radio button group specified in the Value column of the [RadioButton table](radiobutton-table.md).</span></span>                  |
| <span data-ttu-id="8183d-120">Свойство Пропертиб должно быть определено, так как оно является косвенным свойством диалогового окна элемента управления Радиобуттонграуп. Control4</span><span class="sxs-lookup"><span data-stu-id="8183d-120">Property PropertyB must be defined because it is an indirect property of a RadioButtonGroup control DialogA.Control4</span></span>                                                       | <span data-ttu-id="8183d-121">Свойство, на которое ссылается эта группа RadioButton, является косвенным свойством, а значение косвенного свойства не является одним из вариантов для группы RadioButton.</span><span class="sxs-lookup"><span data-stu-id="8183d-121">The property referenced by this RadioButton group is an indirect property, and the value of the indirect property is not one of the choices for the RadioButton group.</span></span>                                                                                                       |
| <span data-ttu-id="8183d-122">Возможно, не является допустимым значением по умолчанию для свойства a.</span><span class="sxs-lookup"><span data-stu-id="8183d-122">Maybe is not a valid default value for the property PropertyA.</span></span> <span data-ttu-id="8183d-123">Свойство является косвенным свойством Радиобуттонграуп элемента управления Dialog. Control5 (через свойство Property5).</span><span class="sxs-lookup"><span data-stu-id="8183d-123">The property is an indirect RadioButtonGroup property of control DialogA.Control5 (via property Property5).</span></span> | <span data-ttu-id="8183d-124">Значение косвенного свойства, на которое ссылается элемент управления, не является одним из значений по умолчанию для этого Радиобуттонграуп.</span><span class="sxs-lookup"><span data-stu-id="8183d-124">The value of the indirect property referenced via the control is not one of the default values for that RadioButtonGroup.</span></span>                                                                                                                                                    |



 

<span data-ttu-id="8183d-125">[Таблица управления](control-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="8183d-125">[Control Table](control-table.md) (partial)</span></span>



| <span data-ttu-id="8183d-126">Диалог</span><span class="sxs-lookup"><span data-stu-id="8183d-126">Dialog</span></span>  | <span data-ttu-id="8183d-127">Control</span><span class="sxs-lookup"><span data-stu-id="8183d-127">Control</span></span>  | <span data-ttu-id="8183d-128">Тип</span><span class="sxs-lookup"><span data-stu-id="8183d-128">Type</span></span>             | <span data-ttu-id="8183d-129">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="8183d-129">Attributes</span></span> | <span data-ttu-id="8183d-130">Свойство</span><span class="sxs-lookup"><span data-stu-id="8183d-130">Property</span></span>  |
|---------|----------|------------------|------------|-----------|
| <span data-ttu-id="8183d-131">Диалоговое окно</span><span class="sxs-lookup"><span data-stu-id="8183d-131">DialogA</span></span> | <span data-ttu-id="8183d-132">Control1</span><span class="sxs-lookup"><span data-stu-id="8183d-132">Control1</span></span> | <span data-ttu-id="8183d-133">радиобуттонграуп</span><span class="sxs-lookup"><span data-stu-id="8183d-133">RadioButtonGroup</span></span> | <span data-ttu-id="8183d-134">0</span><span class="sxs-lookup"><span data-stu-id="8183d-134">0</span></span>          | <span data-ttu-id="8183d-135">Property1</span><span class="sxs-lookup"><span data-stu-id="8183d-135">Property1</span></span> |
| <span data-ttu-id="8183d-136">Диалоговое окно</span><span class="sxs-lookup"><span data-stu-id="8183d-136">DialogA</span></span> | <span data-ttu-id="8183d-137">Control2</span><span class="sxs-lookup"><span data-stu-id="8183d-137">Control2</span></span> | <span data-ttu-id="8183d-138">радиобуттонграуп</span><span class="sxs-lookup"><span data-stu-id="8183d-138">RadioButtonGroup</span></span> | <span data-ttu-id="8183d-139">0</span><span class="sxs-lookup"><span data-stu-id="8183d-139">0</span></span>          |           |
| <span data-ttu-id="8183d-140">Диалоговое окно</span><span class="sxs-lookup"><span data-stu-id="8183d-140">DialogA</span></span> | <span data-ttu-id="8183d-141">Control3</span><span class="sxs-lookup"><span data-stu-id="8183d-141">Control3</span></span> | <span data-ttu-id="8183d-142">радиобуттонграуп</span><span class="sxs-lookup"><span data-stu-id="8183d-142">RadioButtonGroup</span></span> | <span data-ttu-id="8183d-143">0</span><span class="sxs-lookup"><span data-stu-id="8183d-143">0</span></span>          | <span data-ttu-id="8183d-144">Property3</span><span class="sxs-lookup"><span data-stu-id="8183d-144">Property3</span></span> |
| <span data-ttu-id="8183d-145">Диалоговое окно</span><span class="sxs-lookup"><span data-stu-id="8183d-145">DialogA</span></span> | <span data-ttu-id="8183d-146">Control4</span><span class="sxs-lookup"><span data-stu-id="8183d-146">Control4</span></span> | <span data-ttu-id="8183d-147">радиобуттонграуп</span><span class="sxs-lookup"><span data-stu-id="8183d-147">RadioButtonGroup</span></span> | <span data-ttu-id="8183d-148">8</span><span class="sxs-lookup"><span data-stu-id="8183d-148">8</span></span>          | <span data-ttu-id="8183d-149">Property4</span><span class="sxs-lookup"><span data-stu-id="8183d-149">Property4</span></span> |
| <span data-ttu-id="8183d-150">Диалоговое окно</span><span class="sxs-lookup"><span data-stu-id="8183d-150">DialogA</span></span> | <span data-ttu-id="8183d-151">Control5</span><span class="sxs-lookup"><span data-stu-id="8183d-151">Control5</span></span> | <span data-ttu-id="8183d-152">радиобуттонграуп</span><span class="sxs-lookup"><span data-stu-id="8183d-152">RadioButtonGroup</span></span> | <span data-ttu-id="8183d-153">8</span><span class="sxs-lookup"><span data-stu-id="8183d-153">8</span></span>          | <span data-ttu-id="8183d-154">Property5</span><span class="sxs-lookup"><span data-stu-id="8183d-154">Property5</span></span> |



 

<span data-ttu-id="8183d-155">[Таблица свойств](property-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="8183d-155">[Property Table](property-table.md) (partial)</span></span>



| <span data-ttu-id="8183d-156">Свойство</span><span class="sxs-lookup"><span data-stu-id="8183d-156">Property</span></span>  | <span data-ttu-id="8183d-157">Значение</span><span class="sxs-lookup"><span data-stu-id="8183d-157">Value</span></span>     |
|-----------|-----------|
| <span data-ttu-id="8183d-158">Property1</span><span class="sxs-lookup"><span data-stu-id="8183d-158">Property1</span></span> | <span data-ttu-id="8183d-159">Да</span><span class="sxs-lookup"><span data-stu-id="8183d-159">Yes</span></span>       |
| <span data-ttu-id="8183d-160">Property3</span><span class="sxs-lookup"><span data-stu-id="8183d-160">Property3</span></span> | <span data-ttu-id="8183d-161">Возможно</span><span class="sxs-lookup"><span data-stu-id="8183d-161">Maybe</span></span>     |
| <span data-ttu-id="8183d-162">Property4</span><span class="sxs-lookup"><span data-stu-id="8183d-162">Property4</span></span> | <span data-ttu-id="8183d-163">пропертиб</span><span class="sxs-lookup"><span data-stu-id="8183d-163">PropertyB</span></span> |
| <span data-ttu-id="8183d-164">Property5</span><span class="sxs-lookup"><span data-stu-id="8183d-164">Property5</span></span> | <span data-ttu-id="8183d-165">Свойство а</span><span class="sxs-lookup"><span data-stu-id="8183d-165">PropertyA</span></span> |
| <span data-ttu-id="8183d-166">Свойство а</span><span class="sxs-lookup"><span data-stu-id="8183d-166">PropertyA</span></span> | <span data-ttu-id="8183d-167">Возможно</span><span class="sxs-lookup"><span data-stu-id="8183d-167">Maybe</span></span>     |



 

<span data-ttu-id="8183d-168">[Таблица RadioButton](radiobutton-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="8183d-168">[RadioButton Table](radiobutton-table.md) (partial)</span></span>



| <span data-ttu-id="8183d-169">Свойство</span><span class="sxs-lookup"><span data-stu-id="8183d-169">Property</span></span>  | <span data-ttu-id="8183d-170">Заказ</span><span class="sxs-lookup"><span data-stu-id="8183d-170">Order</span></span> | <span data-ttu-id="8183d-171">Значение</span><span class="sxs-lookup"><span data-stu-id="8183d-171">Value</span></span> |
|-----------|-------|-------|
| <span data-ttu-id="8183d-172">Property1</span><span class="sxs-lookup"><span data-stu-id="8183d-172">Property1</span></span> | <span data-ttu-id="8183d-173">1</span><span class="sxs-lookup"><span data-stu-id="8183d-173">1</span></span>     | <span data-ttu-id="8183d-174">Да</span><span class="sxs-lookup"><span data-stu-id="8183d-174">Yes</span></span>   |
| <span data-ttu-id="8183d-175">Property1</span><span class="sxs-lookup"><span data-stu-id="8183d-175">Property1</span></span> | <span data-ttu-id="8183d-176">2</span><span class="sxs-lookup"><span data-stu-id="8183d-176">2</span></span>     | <span data-ttu-id="8183d-177">Сейчас</span><span class="sxs-lookup"><span data-stu-id="8183d-177">Now</span></span>   |
| <span data-ttu-id="8183d-178">Свойство2</span><span class="sxs-lookup"><span data-stu-id="8183d-178">Property2</span></span> | <span data-ttu-id="8183d-179">1</span><span class="sxs-lookup"><span data-stu-id="8183d-179">1</span></span>     | <span data-ttu-id="8183d-180">Да</span><span class="sxs-lookup"><span data-stu-id="8183d-180">Yes</span></span>   |
| <span data-ttu-id="8183d-181">Свойство2</span><span class="sxs-lookup"><span data-stu-id="8183d-181">Property2</span></span> | <span data-ttu-id="8183d-182">2</span><span class="sxs-lookup"><span data-stu-id="8183d-182">2</span></span>     | <span data-ttu-id="8183d-183">Нет</span><span class="sxs-lookup"><span data-stu-id="8183d-183">No</span></span>    |
| <span data-ttu-id="8183d-184">Property3</span><span class="sxs-lookup"><span data-stu-id="8183d-184">Property3</span></span> | <span data-ttu-id="8183d-185">1</span><span class="sxs-lookup"><span data-stu-id="8183d-185">1</span></span>     | <span data-ttu-id="8183d-186">Да</span><span class="sxs-lookup"><span data-stu-id="8183d-186">Yes</span></span>   |
| <span data-ttu-id="8183d-187">Property3</span><span class="sxs-lookup"><span data-stu-id="8183d-187">Property3</span></span> | <span data-ttu-id="8183d-188">2</span><span class="sxs-lookup"><span data-stu-id="8183d-188">2</span></span>     | <span data-ttu-id="8183d-189">Нет</span><span class="sxs-lookup"><span data-stu-id="8183d-189">No</span></span>    |
| <span data-ttu-id="8183d-190">Property4</span><span class="sxs-lookup"><span data-stu-id="8183d-190">Property4</span></span> | <span data-ttu-id="8183d-191">1</span><span class="sxs-lookup"><span data-stu-id="8183d-191">1</span></span>     | <span data-ttu-id="8183d-192">Да</span><span class="sxs-lookup"><span data-stu-id="8183d-192">Yes</span></span>   |
| <span data-ttu-id="8183d-193">Property4</span><span class="sxs-lookup"><span data-stu-id="8183d-193">Property4</span></span> | <span data-ttu-id="8183d-194">2</span><span class="sxs-lookup"><span data-stu-id="8183d-194">2</span></span>     | <span data-ttu-id="8183d-195">Нет</span><span class="sxs-lookup"><span data-stu-id="8183d-195">No</span></span>    |
| <span data-ttu-id="8183d-196">Свойство а</span><span class="sxs-lookup"><span data-stu-id="8183d-196">PropertyA</span></span> | <span data-ttu-id="8183d-197">1</span><span class="sxs-lookup"><span data-stu-id="8183d-197">1</span></span>     | <span data-ttu-id="8183d-198">Да</span><span class="sxs-lookup"><span data-stu-id="8183d-198">Yes</span></span>   |
| <span data-ttu-id="8183d-199">Свойство а</span><span class="sxs-lookup"><span data-stu-id="8183d-199">PropertyA</span></span> | <span data-ttu-id="8183d-200">2</span><span class="sxs-lookup"><span data-stu-id="8183d-200">2</span></span>     | <span data-ttu-id="8183d-201">Нет</span><span class="sxs-lookup"><span data-stu-id="8183d-201">No</span></span>    |
| <span data-ttu-id="8183d-202">пропертиб</span><span class="sxs-lookup"><span data-stu-id="8183d-202">PropertyB</span></span> | <span data-ttu-id="8183d-203">1</span><span class="sxs-lookup"><span data-stu-id="8183d-203">1</span></span>     | <span data-ttu-id="8183d-204">Да</span><span class="sxs-lookup"><span data-stu-id="8183d-204">Yes</span></span>   |
| <span data-ttu-id="8183d-205">пропертиб</span><span class="sxs-lookup"><span data-stu-id="8183d-205">PropertyB</span></span> | <span data-ttu-id="8183d-206">2</span><span class="sxs-lookup"><span data-stu-id="8183d-206">2</span></span>     | <span data-ttu-id="8183d-207">Нет</span><span class="sxs-lookup"><span data-stu-id="8183d-207">No</span></span>    |



 

<span data-ttu-id="8183d-208">Чтобы устранить ошибки, обнаруженные этим ICE, проверьте следующее:</span><span class="sxs-lookup"><span data-stu-id="8183d-208">To fix the errors reported by this ICE, check the following:</span></span>

-   <span data-ttu-id="8183d-209">Каждая запись элемента управления RadioButton без непрямого набора атрибутов имеет свойство, указанное в столбце свойство.</span><span class="sxs-lookup"><span data-stu-id="8183d-209">That every RadioButton control entry without the indirect attribute set has a property listed in the Property column:</span></span>
-   <span data-ttu-id="8183d-210">У каждого такого свойства есть по крайней мере одна соответствующая запись в таблице RadioButton.</span><span class="sxs-lookup"><span data-stu-id="8183d-210">That every such property has at least one corresponding entry in the RadioButton table.</span></span>
-   <span data-ttu-id="8183d-211">Каждое такое свойство определяется в таблице свойств со значением, которое является одним из вариантов из таблицы RadioButton.</span><span class="sxs-lookup"><span data-stu-id="8183d-211">That every such property is defined in the Property table, with a value that is one of the choices from the RadioButton table.</span></span>
-   <span data-ttu-id="8183d-212">Все свойства, упоминаемые в столбце свойств элемента управления RadioButton с непрямым набором атрибутов, определяются в таблице свойств.</span><span class="sxs-lookup"><span data-stu-id="8183d-212">That every property referenced in the Property column of a RadioButton control with the indirect attribute set is defined in the Property table.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8183d-213">См. также</span><span class="sxs-lookup"><span data-stu-id="8183d-213">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8183d-214">Справочник по ICE</span><span class="sxs-lookup"><span data-stu-id="8183d-214">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



