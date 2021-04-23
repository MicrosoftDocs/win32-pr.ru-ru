---
title: MENUITEM, инструкция
description: Определяет пункт меню.
ms.assetid: b154211a-5267-4dcf-9e70-ac36671d10d3
keywords:
- Меню инструкций MENUITEM и другие ресурсы
topic_type:
- apiref
api_name:
- MENUITEM
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da2051b326b2f2f37c9e24e03bcb5e5116cf290a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "105661669"
---
# <a name="menuitem-statement"></a><span data-ttu-id="fd6e3-104">MENUITEM, инструкция</span><span class="sxs-lookup"><span data-stu-id="fd6e3-104">MENUITEM statement</span></span>

<span data-ttu-id="fd6e3-105">Определяет пункт меню.</span><span class="sxs-lookup"><span data-stu-id="fd6e3-105">Defines a menu item.</span></span>

``` syntax
MENUITEM text, result, [optionlist]  
MENUITEM SEPARATOR
```

<dl> <dt>

<span data-ttu-id="fd6e3-106"><span id="text"></span><span id="TEXT"></span>*полнотекстовым*</span><span class="sxs-lookup"><span data-stu-id="fd6e3-106"><span id="text"></span><span id="TEXT"></span>*text*</span></span>
</dt> <dd>

<span data-ttu-id="fd6e3-107">Имя элемента меню.</span><span class="sxs-lookup"><span data-stu-id="fd6e3-107">The name of the menu item.</span></span>

<span data-ttu-id="fd6e3-108">Строка может содержать escape **\\ -** символы **\\ t** и.</span><span class="sxs-lookup"><span data-stu-id="fd6e3-108">The string can contain the escape characters **\\t** and **\\a**.</span></span> <span data-ttu-id="fd6e3-109">Символ **\\ t** вставляет знак табуляции в строку и используется для выровняйте текст в столбцах.</span><span class="sxs-lookup"><span data-stu-id="fd6e3-109">The **\\t** character inserts a tab in the string and is used to align text in columns.</span></span> <span data-ttu-id="fd6e3-110">Символы табуляции следует использовать только в меню, а не в строках меню.</span><span class="sxs-lookup"><span data-stu-id="fd6e3-110">Tab characters should be used only in menus, not in menu bars.</span></span> <span data-ttu-id="fd6e3-111">(Дополнительные сведения о меню см. в разделе [**ресурс Popup**](popup-resource.md).) Символ выровнять весь текст, следующий за **ним, вправо \\** , в строку меню или во всплывающее меню.</span><span class="sxs-lookup"><span data-stu-id="fd6e3-111">(For information on menus, see [**POPUP Resource**](popup-resource.md).) The **\\a** character aligns all text that follows it flush right to the menu bar or pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="fd6e3-112"><span id="result"></span><span id="RESULT"></span>*результат*</span><span class="sxs-lookup"><span data-stu-id="fd6e3-112"><span id="result"></span><span id="RESULT"></span>*result*</span></span>
</dt> <dd>

<span data-ttu-id="fd6e3-113">Число, указывающее результат, формируемый при выборе пользователем пункта меню.</span><span class="sxs-lookup"><span data-stu-id="fd6e3-113">A number that specifies the result generated when the user selects the menu item.</span></span> <span data-ttu-id="fd6e3-114">Этот параметр принимает целочисленное значение.</span><span class="sxs-lookup"><span data-stu-id="fd6e3-114">This parameter takes an integer value.</span></span> <span data-ttu-id="fd6e3-115">Результаты элемента меню всегда являются целыми числами; Когда пользователь щелкает имя пункта меню, результат отправляется в окно, которому принадлежит меню.</span><span class="sxs-lookup"><span data-stu-id="fd6e3-115">Menu-item results are always integers; when the user clicks the menu-item name, the result is sent to the window that owns the menu.</span></span>

</dd> <dt>

<span data-ttu-id="fd6e3-116"><span id="optionlist"></span><span id="OPTIONLIST"></span>*оптионлист*</span><span class="sxs-lookup"><span data-stu-id="fd6e3-116"><span id="optionlist"></span><span id="OPTIONLIST"></span>*optionlist*</span></span>
</dt> <dd>

<span data-ttu-id="fd6e3-117">Внешний вид пункта меню.</span><span class="sxs-lookup"><span data-stu-id="fd6e3-117">The appearance of the menu item.</span></span> <span data-ttu-id="fd6e3-118">Этот необязательный параметр принимает одно или несколько из следующих переопределенных параметров меню, разделенных запятыми или пробелами.</span><span class="sxs-lookup"><span data-stu-id="fd6e3-118">This optional parameter takes one or more of the following redefined menu options, separated by commas or spaces.</span></span>



| <span data-ttu-id="fd6e3-119">Параметр</span><span class="sxs-lookup"><span data-stu-id="fd6e3-119">Option</span></span>           | <span data-ttu-id="fd6e3-120">Описание</span><span class="sxs-lookup"><span data-stu-id="fd6e3-120">Description</span></span>                                                                                                                                                           |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd6e3-121">**ОТМЕЧЕН**</span><span class="sxs-lookup"><span data-stu-id="fd6e3-121">**CHECKED**</span></span>      | <span data-ttu-id="fd6e3-122">Рядом с пунктом меню стоит галочка.</span><span class="sxs-lookup"><span data-stu-id="fd6e3-122">Menu item has a check mark next to it.</span></span>                                                                                                                                |
| <span data-ttu-id="fd6e3-123">**СЕРЫМ цветом**</span><span class="sxs-lookup"><span data-stu-id="fd6e3-123">**GRAYED**</span></span>       | <span data-ttu-id="fd6e3-124">Элемент меню изначально неактивен и отображается в меню серым или светлым затенением цвета текста меню.</span><span class="sxs-lookup"><span data-stu-id="fd6e3-124">Menu item is initially inactive and appears on the menu in gray or a lightened shade of the menu-text color.</span></span> <span data-ttu-id="fd6e3-125">Этот параметр нельзя использовать с параметром **Inactive** .</span><span class="sxs-lookup"><span data-stu-id="fd6e3-125">This option cannot be used with the **INACTIVE** option.</span></span> |
| <span data-ttu-id="fd6e3-126">**Справка**</span><span class="sxs-lookup"><span data-stu-id="fd6e3-126">**HELP**</span></span>         | <span data-ttu-id="fd6e3-127">Определяет элемент справки.</span><span class="sxs-lookup"><span data-stu-id="fd6e3-127">Identifies a help item.</span></span> <span data-ttu-id="fd6e3-128">Этот параметр не влияет на внешний вид пункта меню.</span><span class="sxs-lookup"><span data-stu-id="fd6e3-128">This option has no effect on the appearance of the menu item.</span></span>                                                                                 |
| <span data-ttu-id="fd6e3-129">**Активный**</span><span class="sxs-lookup"><span data-stu-id="fd6e3-129">**INACTIVE**</span></span>     | <span data-ttu-id="fd6e3-130">Элемент меню отображается, но не может быть выбран.</span><span class="sxs-lookup"><span data-stu-id="fd6e3-130">Menu item is displayed but it cannot be selected.</span></span> <span data-ttu-id="fd6e3-131">Этот параметр нельзя использовать с **серым** параметром.</span><span class="sxs-lookup"><span data-stu-id="fd6e3-131">This option cannot be used with the **GRAYED** option.</span></span>                                                              |
| <span data-ttu-id="fd6e3-132">**менубарбреак**</span><span class="sxs-lookup"><span data-stu-id="fd6e3-132">**MENUBARBREAK**</span></span> | <span data-ttu-id="fd6e3-133">То же, что и **менубреак** , за исключением того, что для всплывающих меню он отделяет новый столбец от старого со вертикальной линией.</span><span class="sxs-lookup"><span data-stu-id="fd6e3-133">Same as **MENUBREAK** except that for pop-up menus, it separates the new column from the old column with a vertical line.</span></span>                                             |
| <span data-ttu-id="fd6e3-134">**менубреак**</span><span class="sxs-lookup"><span data-stu-id="fd6e3-134">**MENUBREAK**</span></span>    | <span data-ttu-id="fd6e3-135">Помещает пункт меню в новую строку для статических элементов строки меню.</span><span class="sxs-lookup"><span data-stu-id="fd6e3-135">Places the menu item on a new line for static menu-bar items.</span></span> <span data-ttu-id="fd6e3-136">Для меню он помещает пункт меню в новый столбец без разделительной линии между столбцами.</span><span class="sxs-lookup"><span data-stu-id="fd6e3-136">For menus, it places the menu item in a new column with no dividing line between the columns.</span></span>           |



 

</dd> <dt>

<span data-ttu-id="fd6e3-137"><span id="MENUITEM_SEPARATOR"></span><span id="menuitem_separator"></span>**РАЗДЕЛИТЕЛЬ ЭЛЕМЕНТОВ МЕНЮ**</span><span class="sxs-lookup"><span data-stu-id="fd6e3-137"><span id="MENUITEM_SEPARATOR"></span><span id="menuitem_separator"></span>**MENUITEM SEPARATOR**</span></span>
</dt> <dd>

<span data-ttu-id="fd6e3-138">Форма **разделителя MenuItem** в операторе **MenuItem** создает неактивный элемент меню, который выступает в качестве разделителя между двумя активными элементами меню в меню.</span><span class="sxs-lookup"><span data-stu-id="fd6e3-138">The **MENUITEM SEPARATOR** form of the **MENUITEM** statement creates an inactive menu item that serves as a dividing bar between two active menu items on a menu.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="fd6e3-139">Примеры</span><span class="sxs-lookup"><span data-stu-id="fd6e3-139">Examples</span></span>

<span data-ttu-id="fd6e3-140">В следующем примере показано использование операторов разделения **MenuItem** и **MenuItem** :</span><span class="sxs-lookup"><span data-stu-id="fd6e3-140">The following example demonstrates the use of the **MENUITEM** and **MENUITEM SEPARATOR** statements:</span></span>

``` syntax
MENUITEM "&Roman", 206, CHECKED, GRAYED
MENUITEM SEPARATOR
MENUITEM "&Blackletter", 301
```

## <a name="see-also"></a><span data-ttu-id="fd6e3-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fd6e3-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd6e3-142">**МЕНЮ**</span><span class="sxs-lookup"><span data-stu-id="fd6e3-142">**MENU**</span></span>](menu-resource.md)
</dt> <dt>

[<span data-ttu-id="fd6e3-143">**ПОДСКАЗКИ**</span><span class="sxs-lookup"><span data-stu-id="fd6e3-143">**POPUP**</span></span>](popup-resource.md)
</dt> </dl>

 

 




