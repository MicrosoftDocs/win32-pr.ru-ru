---
title: Поддержка автоматизации пользовательского интерфейса для стандартных элементов управления
description: В этом разделе определяются стандартные элементы управления Windows, поддерживаемые Microsoft UI Automation. Полная поддержка предоставляется только для элементов управления версии 6 ComCtrl32.dll (доступных в Windows XP и более поздних версиях).
ms.assetid: 4821684c-8a90-413c-8ddc-699926e3bb09
keywords:
- Клиенты, поддержка модели автоматизации пользовательского интерфейса для стандартных элементов управления
- Клиенты, поддержка стандартных элементов управления
- Клиенты, элементы управления Win32
- Модель автоматизации пользовательского интерфейса, поддержка стандартных элементов управления
- Модель автоматизации пользовательского интерфейса, поддержка стандартных элементов управления
- Модель автоматизации пользовательского интерфейса, элементы управления Win32
- поддержка стандартных элементов управления
- Поддержка стандартных элементов управления
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae6e384b9ee0fd72fd8a41aa3f791a5c996fe6d6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104531919"
---
# <a name="ui-automation-support-for-standard-controls"></a><span data-ttu-id="58b06-112">Поддержка автоматизации пользовательского интерфейса для стандартных элементов управления</span><span class="sxs-lookup"><span data-stu-id="58b06-112">UI Automation Support for Standard Controls</span></span>

<span data-ttu-id="58b06-113">В этом разделе определяются стандартные элементы управления Windows, поддерживаемые Microsoft UI Automation.</span><span class="sxs-lookup"><span data-stu-id="58b06-113">This topic identifies the standard Windows controls that are supported by Microsoft UI Automation.</span></span> <span data-ttu-id="58b06-114">Полная поддержка предоставляется только для элементов управления версии 6 ComCtrl32.dll (доступных в Windows XP и более поздних версиях).</span><span class="sxs-lookup"><span data-stu-id="58b06-114">Full support is provided only for controls from version 6 of ComCtrl32.dll (available with Windows XP and later).</span></span>

> [!Note]  
> <span data-ttu-id="58b06-115">Элемент управления RichEdit поддерживается только для версий, поставляемых с Windows Vista (в RichEd20.dll версии 3,1 и более поздних версий и MsftEdit.dll версии 4,1 и более поздних версий).</span><span class="sxs-lookup"><span data-stu-id="58b06-115">The RichEdit control is supported only for versions shipped with Windows Vista (in RichEd20.dll version 3.1 and later, and MsftEdit.dll version 4.1 and later).</span></span>

 

<span data-ttu-id="58b06-116">В следующей таблице перечислены имена классов поддерживаемых стандартных элементов управления, а также соответствующие типы элементов управления модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="58b06-116">The following table lists the class names of the supported standard controls, along with the corresponding UI Automation control types.</span></span>



| <span data-ttu-id="58b06-117">Имя класса</span><span class="sxs-lookup"><span data-stu-id="58b06-117">Class Name</span></span>          | <span data-ttu-id="58b06-118">Тип элемента управления</span><span class="sxs-lookup"><span data-stu-id="58b06-118">Control Type</span></span>        |
|---------------------|---------------------|
| <span data-ttu-id="58b06-119">Button</span><span class="sxs-lookup"><span data-stu-id="58b06-119">Button</span></span>              | <span data-ttu-id="58b06-120">Button</span><span class="sxs-lookup"><span data-stu-id="58b06-120">Button</span></span>              |
| <span data-ttu-id="58b06-121">Button</span><span class="sxs-lookup"><span data-stu-id="58b06-121">Button</span></span>              | <span data-ttu-id="58b06-122">RadioButton</span><span class="sxs-lookup"><span data-stu-id="58b06-122">RadioButton</span></span>         |
| <span data-ttu-id="58b06-123">Кнопка</span><span class="sxs-lookup"><span data-stu-id="58b06-123">Button</span></span>              | <span data-ttu-id="58b06-124">Группа</span><span class="sxs-lookup"><span data-stu-id="58b06-124">Group</span></span>               |
| <span data-ttu-id="58b06-125">Кнопка</span><span class="sxs-lookup"><span data-stu-id="58b06-125">Button</span></span>              | <span data-ttu-id="58b06-126">CheckBox</span><span class="sxs-lookup"><span data-stu-id="58b06-126">CheckBox</span></span>            |
| <span data-ttu-id="58b06-127">Кнопка</span><span class="sxs-lookup"><span data-stu-id="58b06-127">Button</span></span>              | <span data-ttu-id="58b06-128">Гиперссылка</span><span class="sxs-lookup"><span data-stu-id="58b06-128">Hyperlink</span></span>           |
| <span data-ttu-id="58b06-129">Кнопка</span><span class="sxs-lookup"><span data-stu-id="58b06-129">Button</span></span>              | <span data-ttu-id="58b06-130">SplitButton</span><span class="sxs-lookup"><span data-stu-id="58b06-130">SplitButton</span></span>         |
| <span data-ttu-id="58b06-131">Кнопка</span><span class="sxs-lookup"><span data-stu-id="58b06-131">Button</span></span>              | <span data-ttu-id="58b06-132">CheckBox</span><span class="sxs-lookup"><span data-stu-id="58b06-132">CheckBox</span></span>            |
| <span data-ttu-id="58b06-133">ComboBoxEx32</span><span class="sxs-lookup"><span data-stu-id="58b06-133">ComboBoxEx32</span></span>        | <span data-ttu-id="58b06-134">ComboBox</span><span class="sxs-lookup"><span data-stu-id="58b06-134">ComboBox</span></span>            |
| <span data-ttu-id="58b06-135">ComboBox</span><span class="sxs-lookup"><span data-stu-id="58b06-135">ComboBox</span></span>            | <span data-ttu-id="58b06-136">ComboBox</span><span class="sxs-lookup"><span data-stu-id="58b06-136">ComboBox</span></span>            |
| <span data-ttu-id="58b06-137">Изменить</span><span class="sxs-lookup"><span data-stu-id="58b06-137">Edit</span></span>                | <span data-ttu-id="58b06-138">Документ</span><span class="sxs-lookup"><span data-stu-id="58b06-138">Document</span></span>            |
| <span data-ttu-id="58b06-139">Изменить</span><span class="sxs-lookup"><span data-stu-id="58b06-139">Edit</span></span>                | <span data-ttu-id="58b06-140">Изменить</span><span class="sxs-lookup"><span data-stu-id="58b06-140">Edit</span></span>                |
| <span data-ttu-id="58b06-141">SysLink</span><span class="sxs-lookup"><span data-stu-id="58b06-141">SysLink</span></span>             | <span data-ttu-id="58b06-142">Гиперссылка</span><span class="sxs-lookup"><span data-stu-id="58b06-142">Hyperlink</span></span>           |
| <span data-ttu-id="58b06-143">Статические</span><span class="sxs-lookup"><span data-stu-id="58b06-143">Static</span></span>              | <span data-ttu-id="58b06-144">Текст</span><span class="sxs-lookup"><span data-stu-id="58b06-144">Text</span></span>                |
| <span data-ttu-id="58b06-145">Статические</span><span class="sxs-lookup"><span data-stu-id="58b06-145">Static</span></span>              | <span data-ttu-id="58b06-146">Образ</span><span class="sxs-lookup"><span data-stu-id="58b06-146">Image</span></span>               |
| <span data-ttu-id="58b06-147">SysIPAddress32</span><span class="sxs-lookup"><span data-stu-id="58b06-147">SysIPAddress32</span></span>      | <span data-ttu-id="58b06-148">Особые настройки</span><span class="sxs-lookup"><span data-stu-id="58b06-148">Custom</span></span>              |
| <span data-ttu-id="58b06-149">SysHeader32</span><span class="sxs-lookup"><span data-stu-id="58b06-149">SysHeader32</span></span>         | <span data-ttu-id="58b06-150">Header/HeaderItem</span><span class="sxs-lookup"><span data-stu-id="58b06-150">Header/HeaderItem</span></span>   |
| <span data-ttu-id="58b06-151">SysListView32</span><span class="sxs-lookup"><span data-stu-id="58b06-151">SysListView32</span></span>       | <span data-ttu-id="58b06-152">DataGrid</span><span class="sxs-lookup"><span data-stu-id="58b06-152">DataGrid</span></span>            |
| <span data-ttu-id="58b06-153">SysListView32</span><span class="sxs-lookup"><span data-stu-id="58b06-153">SysListView32</span></span>       | <span data-ttu-id="58b06-154">Список</span><span class="sxs-lookup"><span data-stu-id="58b06-154">List</span></span>                |
| <span data-ttu-id="58b06-155">ListBox</span><span class="sxs-lookup"><span data-stu-id="58b06-155">ListBox</span></span>             | <span data-ttu-id="58b06-156">Список</span><span class="sxs-lookup"><span data-stu-id="58b06-156">List</span></span>                |
| <span data-ttu-id="58b06-157">ListBox</span><span class="sxs-lookup"><span data-stu-id="58b06-157">ListBox</span></span>             | <span data-ttu-id="58b06-158">ListItem</span><span class="sxs-lookup"><span data-stu-id="58b06-158">ListItem</span></span>            |
| <span data-ttu-id="58b06-159">\#32768</span><span class="sxs-lookup"><span data-stu-id="58b06-159">\#32768</span></span>             | <span data-ttu-id="58b06-160">Меню</span><span class="sxs-lookup"><span data-stu-id="58b06-160">Menu</span></span>                |
| <span data-ttu-id="58b06-161">\#32768</span><span class="sxs-lookup"><span data-stu-id="58b06-161">\#32768</span></span>             | <span data-ttu-id="58b06-162">MenuItem</span><span class="sxs-lookup"><span data-stu-id="58b06-162">MenuItem</span></span>            |
| <span data-ttu-id="58b06-163">мсктлс \_ progress32</span><span class="sxs-lookup"><span data-stu-id="58b06-163">msctls\_progress32</span></span>  | <span data-ttu-id="58b06-164">ProgressBar</span><span class="sxs-lookup"><span data-stu-id="58b06-164">ProgressBar</span></span>         |
| <span data-ttu-id="58b06-165">RichEdit</span><span class="sxs-lookup"><span data-stu-id="58b06-165">RichEdit</span></span>            | <span data-ttu-id="58b06-166">Документ.</span><span class="sxs-lookup"><span data-stu-id="58b06-166">Document.</span></span> <span data-ttu-id="58b06-167">См. примечание.</span><span class="sxs-lookup"><span data-stu-id="58b06-167">See note.</span></span> |
| <span data-ttu-id="58b06-168">RichEdit20A</span><span class="sxs-lookup"><span data-stu-id="58b06-168">RichEdit20A</span></span>         | <span data-ttu-id="58b06-169">Документ</span><span class="sxs-lookup"><span data-stu-id="58b06-169">Document</span></span>            |
| <span data-ttu-id="58b06-170">RichEdit20W</span><span class="sxs-lookup"><span data-stu-id="58b06-170">RichEdit20W</span></span>         | <span data-ttu-id="58b06-171">Документ</span><span class="sxs-lookup"><span data-stu-id="58b06-171">Document</span></span>            |
| <span data-ttu-id="58b06-172">RichEdit50W</span><span class="sxs-lookup"><span data-stu-id="58b06-172">RichEdit50W</span></span>         | <span data-ttu-id="58b06-173">Документ</span><span class="sxs-lookup"><span data-stu-id="58b06-173">Document</span></span>            |
| <span data-ttu-id="58b06-174">ScrollBar</span><span class="sxs-lookup"><span data-stu-id="58b06-174">ScrollBar</span></span>           | <span data-ttu-id="58b06-175">Ползунок</span><span class="sxs-lookup"><span data-stu-id="58b06-175">Slider</span></span>              |
| <span data-ttu-id="58b06-176">мсктлс \_ trackbar32</span><span class="sxs-lookup"><span data-stu-id="58b06-176">msctls\_trackbar32</span></span>  | <span data-ttu-id="58b06-177">Ползунок</span><span class="sxs-lookup"><span data-stu-id="58b06-177">Slider</span></span>              |
| <span data-ttu-id="58b06-178">мсктлс \_ updown32</span><span class="sxs-lookup"><span data-stu-id="58b06-178">msctls\_updown32</span></span>    | <span data-ttu-id="58b06-179">Spinner</span><span class="sxs-lookup"><span data-stu-id="58b06-179">Spinner</span></span>             |
| <span data-ttu-id="58b06-180">мсктлс \_ statusbar32</span><span class="sxs-lookup"><span data-stu-id="58b06-180">msctls\_statusbar32</span></span> | <span data-ttu-id="58b06-181">StatusBar</span><span class="sxs-lookup"><span data-stu-id="58b06-181">StatusBar</span></span>           |
| <span data-ttu-id="58b06-182">SysTabControl32</span><span class="sxs-lookup"><span data-stu-id="58b06-182">SysTabControl32</span></span>     | <span data-ttu-id="58b06-183">Вкладка</span><span class="sxs-lookup"><span data-stu-id="58b06-183">Tab</span></span>                 |
| <span data-ttu-id="58b06-184">SysTabControl32</span><span class="sxs-lookup"><span data-stu-id="58b06-184">SysTabControl32</span></span>     | <span data-ttu-id="58b06-185">TabItem</span><span class="sxs-lookup"><span data-stu-id="58b06-185">TabItem</span></span>             |
| <span data-ttu-id="58b06-186">ToolbarWindow32</span><span class="sxs-lookup"><span data-stu-id="58b06-186">ToolbarWindow32</span></span>     | <span data-ttu-id="58b06-187">ToolBar</span><span class="sxs-lookup"><span data-stu-id="58b06-187">ToolBar</span></span>             |
| <span data-ttu-id="58b06-188">ToolbarWindow32</span><span class="sxs-lookup"><span data-stu-id="58b06-188">ToolbarWindow32</span></span>     | <span data-ttu-id="58b06-189">MenuItem</span><span class="sxs-lookup"><span data-stu-id="58b06-189">MenuItem</span></span>            |
| <span data-ttu-id="58b06-190">ToolbarWindow32</span><span class="sxs-lookup"><span data-stu-id="58b06-190">ToolbarWindow32</span></span>     | <span data-ttu-id="58b06-191">Кнопка</span><span class="sxs-lookup"><span data-stu-id="58b06-191">Button</span></span>              |
| <span data-ttu-id="58b06-192">ToolbarWindow32</span><span class="sxs-lookup"><span data-stu-id="58b06-192">ToolbarWindow32</span></span>     | <span data-ttu-id="58b06-193">CheckBox</span><span class="sxs-lookup"><span data-stu-id="58b06-193">CheckBox</span></span>            |
| <span data-ttu-id="58b06-194">ToolbarWindow32</span><span class="sxs-lookup"><span data-stu-id="58b06-194">ToolbarWindow32</span></span>     | <span data-ttu-id="58b06-195">RadioButton</span><span class="sxs-lookup"><span data-stu-id="58b06-195">RadioButton</span></span>         |
| <span data-ttu-id="58b06-196">ToolbarWindow32</span><span class="sxs-lookup"><span data-stu-id="58b06-196">ToolbarWindow32</span></span>     | <span data-ttu-id="58b06-197">Separator</span><span class="sxs-lookup"><span data-stu-id="58b06-197">Separator</span></span>           |
| <span data-ttu-id="58b06-198">подсказки \_ class32</span><span class="sxs-lookup"><span data-stu-id="58b06-198">tooltips\_class32</span></span>   | <span data-ttu-id="58b06-199">ToolTip</span><span class="sxs-lookup"><span data-stu-id="58b06-199">ToolTip</span></span>             |
| <span data-ttu-id="58b06-200">\#32774</span><span class="sxs-lookup"><span data-stu-id="58b06-200">\#32774</span></span>             | <span data-ttu-id="58b06-201">ToolTip</span><span class="sxs-lookup"><span data-stu-id="58b06-201">ToolTip</span></span>             |
| <span data-ttu-id="58b06-202">ReBarWindow32</span><span class="sxs-lookup"><span data-stu-id="58b06-202">ReBarWindow32</span></span>       | <span data-ttu-id="58b06-203">Панель инструментов</span><span class="sxs-lookup"><span data-stu-id="58b06-203">Toolbar</span></span>             |
| <span data-ttu-id="58b06-204">SysTreeView32</span><span class="sxs-lookup"><span data-stu-id="58b06-204">SysTreeView32</span></span>       | <span data-ttu-id="58b06-205">Дерево</span><span class="sxs-lookup"><span data-stu-id="58b06-205">Tree</span></span>                |
| <span data-ttu-id="58b06-206">SysTreeView32</span><span class="sxs-lookup"><span data-stu-id="58b06-206">SysTreeView32</span></span>       | <span data-ttu-id="58b06-207">TreeItem</span><span class="sxs-lookup"><span data-stu-id="58b06-207">TreeItem</span></span>            |



 

<span data-ttu-id="58b06-208">Элементы управления, перечисленные в следующей таблице, не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="58b06-208">The controls listed in the following table are not supported.</span></span>



| <span data-ttu-id="58b06-209">Имя класса</span><span class="sxs-lookup"><span data-stu-id="58b06-209">Class Name</span></span>                                    | <span data-ttu-id="58b06-210">Тип элемента управления</span><span class="sxs-lookup"><span data-stu-id="58b06-210">Control Type</span></span> |
|-----------------------------------------------|--------------|
| <span data-ttu-id="58b06-211">SysAnimate32</span><span class="sxs-lookup"><span data-stu-id="58b06-211">SysAnimate32</span></span>                                  | <span data-ttu-id="58b06-212">Образ</span><span class="sxs-lookup"><span data-stu-id="58b06-212">Image</span></span>        |
| <span data-ttu-id="58b06-213">SysPager</span><span class="sxs-lookup"><span data-stu-id="58b06-213">SysPager</span></span>                                      | <span data-ttu-id="58b06-214">Spinner</span><span class="sxs-lookup"><span data-stu-id="58b06-214">Spinner</span></span>      |
| <span data-ttu-id="58b06-215">SysDateTimePick32</span><span class="sxs-lookup"><span data-stu-id="58b06-215">SysDateTimePick32</span></span>                             | <span data-ttu-id="58b06-216">Особые настройки</span><span class="sxs-lookup"><span data-stu-id="58b06-216">Custom</span></span>       |
| <span data-ttu-id="58b06-217">SysMonthCal32</span><span class="sxs-lookup"><span data-stu-id="58b06-217">SysMonthCal32</span></span>                                 | <span data-ttu-id="58b06-218">Календарь</span><span class="sxs-lookup"><span data-stu-id="58b06-218">Calendar</span></span>     |
| <span data-ttu-id="58b06-219">MS \_ винноте</span><span class="sxs-lookup"><span data-stu-id="58b06-219">MS\_WINNOTE</span></span>                                   | <span data-ttu-id="58b06-220">Всплывающая подсказка</span><span class="sxs-lookup"><span data-stu-id="58b06-220">Tooltip</span></span>      |
| <span data-ttu-id="58b06-221">VBBubble</span><span class="sxs-lookup"><span data-stu-id="58b06-221">VBBubble</span></span>                                      | <span data-ttu-id="58b06-222">Всплывающая подсказка</span><span class="sxs-lookup"><span data-stu-id="58b06-222">Tooltip</span></span>      |
| <span data-ttu-id="58b06-223">ScrollBar (при использовании в качестве отдельного элемента управления)</span><span class="sxs-lookup"><span data-stu-id="58b06-223">ScrollBar (when used as a standalone control)</span></span> | <span data-ttu-id="58b06-224">Ползунок</span><span class="sxs-lookup"><span data-stu-id="58b06-224">Slider</span></span>       |
| <span data-ttu-id="58b06-225">SuperGrid</span><span class="sxs-lookup"><span data-stu-id="58b06-225">SuperGrid</span></span>                                     | <span data-ttu-id="58b06-226">Особые настройки</span><span class="sxs-lookup"><span data-stu-id="58b06-226">Custom</span></span>       |



 

## <a name="related-topics"></a><span data-ttu-id="58b06-227">См. также</span><span class="sxs-lookup"><span data-stu-id="58b06-227">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="58b06-228">Общие сведения о типах элементов управления автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="58b06-228">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> </dl>

 

 




