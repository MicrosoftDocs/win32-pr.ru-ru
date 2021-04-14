---
title: Поддержка типов элементов управления модели автоматизации пользовательского интерфейса
description: В этом разделе содержатся подробные сведения о древовидной структуре, свойствах, шаблонах элементов управления и событиях, которые должен поддерживать каждый тип элемента управления модели автоматизации пользовательского интерфейса Майкрософт.
ms.assetid: 35232907-6c54-47cd-b82a-0daee279ef17
keywords:
- Модель автоматизации пользовательского интерфейса, о типах элементов управления
- Модель автоматизации пользовательского интерфейса, общие сведения о типах элементов управления
- Поддержка типа элемента управления
- типы элементов управления, поддержка
- типы элементов управления, сведения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26ac6f857da87691428c747cfe5dbff5102218f6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413469"
---
# <a name="supporting-ui-automation-control-types"></a><span data-ttu-id="065b5-108">Поддержка типов элементов управления модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="065b5-108">Supporting UI Automation Control Types</span></span>

<span data-ttu-id="065b5-109">В этом разделе содержатся подробные сведения о древовидной структуре, свойствах, шаблонах элементов управления и событиях, которые должен поддерживать каждый тип элемента управления модели автоматизации пользовательского интерфейса Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="065b5-109">This section contains detailed information about the tree structure, properties, control patterns, and events that each Microsoft UI Automation control type is required to support.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="065b5-110">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="065b5-110">In this section</span></span>

-   [<span data-ttu-id="065b5-111">Тип элемента управления панель приложений</span><span class="sxs-lookup"><span data-stu-id="065b5-111">AppBar Control Type</span></span>](uiauto-supportappbarcontroltype.md)
-   [<span data-ttu-id="065b5-112">Тип элемента управления Button</span><span class="sxs-lookup"><span data-stu-id="065b5-112">Button Control Type</span></span>](uiauto-supportbuttoncontroltype.md)
-   [<span data-ttu-id="065b5-113">Тип элемента управления Calendar</span><span class="sxs-lookup"><span data-stu-id="065b5-113">Calendar Control Type</span></span>](uiauto-supportcalendarcontroltype.md)
-   [<span data-ttu-id="065b5-114">Тип элемента управления CheckBox</span><span class="sxs-lookup"><span data-stu-id="065b5-114">CheckBox Control Type</span></span>](uiauto-supportcheckboxcontroltype.md)
-   [<span data-ttu-id="065b5-115">Тип элемента управления ComboBox</span><span class="sxs-lookup"><span data-stu-id="065b5-115">ComboBox Control Type</span></span>](uiauto-supportcomboboxcontroltype.md)
-   [<span data-ttu-id="065b5-116">Тип элемента управления DataGrid</span><span class="sxs-lookup"><span data-stu-id="065b5-116">DataGrid Control Type</span></span>](uiauto-supportdatagridcontroltype.md)
-   [<span data-ttu-id="065b5-117">Тип элемента управления DataItem</span><span class="sxs-lookup"><span data-stu-id="065b5-117">DataItem Control Type</span></span>](uiauto-supportdataitemcontroltype.md)
-   [<span data-ttu-id="065b5-118">Тип элемента управления документом</span><span class="sxs-lookup"><span data-stu-id="065b5-118">Document Control Type</span></span>](uiauto-supportdocumentcontroltype.md)
-   [<span data-ttu-id="065b5-119">Изменить тип элемента управления</span><span class="sxs-lookup"><span data-stu-id="065b5-119">Edit Control Type</span></span>](uiauto-supporteditcontroltype.md)
-   [<span data-ttu-id="065b5-120">Тип элемента управления Group</span><span class="sxs-lookup"><span data-stu-id="065b5-120">Group Control Type</span></span>](uiauto-supportgroupcontroltype.md)
-   [<span data-ttu-id="065b5-121">Тип элемента управления "заголовок"</span><span class="sxs-lookup"><span data-stu-id="065b5-121">Header Control Type</span></span>](uiauto-supportheadercontroltype.md)
-   [<span data-ttu-id="065b5-122">Тип элемента управления HeaderItem</span><span class="sxs-lookup"><span data-stu-id="065b5-122">HeaderItem Control Type</span></span>](uiauto-supportheaderitemcontroltype.md)
-   [<span data-ttu-id="065b5-123">Тип элемента управления HyperLink</span><span class="sxs-lookup"><span data-stu-id="065b5-123">Hyperlink Control Type</span></span>](uiauto-supporthyperlinkcontroltype.md)
-   [<span data-ttu-id="065b5-124">Тип элемента управления Image</span><span class="sxs-lookup"><span data-stu-id="065b5-124">Image Control Type</span></span>](uiauto-supportimagecontroltype.md)
-   [<span data-ttu-id="065b5-125">Тип элемента управления List</span><span class="sxs-lookup"><span data-stu-id="065b5-125">List Control Type</span></span>](uiauto-supportlistcontroltype.md)
-   [<span data-ttu-id="065b5-126">Тип элемента управления ListItem</span><span class="sxs-lookup"><span data-stu-id="065b5-126">ListItem Control Type</span></span>](uiauto-supportlistitemcontroltype.md)
-   [<span data-ttu-id="065b5-127">Тип элемента управления Menu</span><span class="sxs-lookup"><span data-stu-id="065b5-127">Menu Control Type</span></span>](uiauto-supportmenucontroltype.md)
-   [<span data-ttu-id="065b5-128">Тип элемента управления MenuBar</span><span class="sxs-lookup"><span data-stu-id="065b5-128">MenuBar Control Type</span></span>](uiauto-supportmenubarcontroltype.md)
-   [<span data-ttu-id="065b5-129">Тип элемента управления MenuItem</span><span class="sxs-lookup"><span data-stu-id="065b5-129">MenuItem Control Type</span></span>](uiauto-supportmenuitemcontroltype.md)
-   [<span data-ttu-id="065b5-130">Тип элемента управления панели</span><span class="sxs-lookup"><span data-stu-id="065b5-130">Pane Control Type</span></span>](uiauto-supportpanecontroltype.md)
-   [<span data-ttu-id="065b5-131">Тип элемента управления ProgressBar</span><span class="sxs-lookup"><span data-stu-id="065b5-131">ProgressBar Control Type</span></span>](uiauto-supportprogressbarcontroltype.md)
-   [<span data-ttu-id="065b5-132">Тип элемента управления RadioButton</span><span class="sxs-lookup"><span data-stu-id="065b5-132">RadioButton Control Type</span></span>](uiauto-supportradiobuttoncontroltype.md)
-   [<span data-ttu-id="065b5-133">Тип элемента управления ScrollBar</span><span class="sxs-lookup"><span data-stu-id="065b5-133">ScrollBar Control Type</span></span>](uiauto-supportscrollbarcontroltype.md)
-   [<span data-ttu-id="065b5-134">Тип элемента управления Семантикзум</span><span class="sxs-lookup"><span data-stu-id="065b5-134">SemanticZoom Control Type</span></span>](/windows/desktop/WinAuto/uiauto-supportsemanticzoomcontroltype)
-   [<span data-ttu-id="065b5-135">Тип элемента управления Separator</span><span class="sxs-lookup"><span data-stu-id="065b5-135">Separator Control Type</span></span>](uiauto-supportseparatorcontroltype.md)
-   [<span data-ttu-id="065b5-136">Тип элемента управления Slider</span><span class="sxs-lookup"><span data-stu-id="065b5-136">Slider Control Type</span></span>](uiauto-supportslidercontroltype.md)
-   [<span data-ttu-id="065b5-137">Тип элемента управления "Счетчик"</span><span class="sxs-lookup"><span data-stu-id="065b5-137">Spinner Control Type</span></span>](uiauto-supportspinnercontroltype.md)
-   [<span data-ttu-id="065b5-138">Тип элемента управления SplitButton</span><span class="sxs-lookup"><span data-stu-id="065b5-138">SplitButton Control Type</span></span>](uiauto-supportsplitbuttoncontroltype.md)
-   [<span data-ttu-id="065b5-139">Тип элемента управления StatusBar</span><span class="sxs-lookup"><span data-stu-id="065b5-139">StatusBar Control Type</span></span>](uiauto-supportstatusbarcontroltype.md)
-   [<span data-ttu-id="065b5-140">Тип элемента управления Tab</span><span class="sxs-lookup"><span data-stu-id="065b5-140">Tab Control Type</span></span>](uiauto-supporttabcontroltype.md)
-   [<span data-ttu-id="065b5-141">Тип элемента управления TabItem</span><span class="sxs-lookup"><span data-stu-id="065b5-141">TabItem Control Type</span></span>](uiauto-supporttabitemcontroltype.md)
-   [<span data-ttu-id="065b5-142">Тип элемента управления Table</span><span class="sxs-lookup"><span data-stu-id="065b5-142">Table Control Type</span></span>](uiauto-supporttablecontroltype.md)
-   [<span data-ttu-id="065b5-143">Тип элемента управления "текст"</span><span class="sxs-lookup"><span data-stu-id="065b5-143">Text Control Type</span></span>](uiauto-supporttextcontroltype.md)
-   [<span data-ttu-id="065b5-144">Тип элемента управления Thumb</span><span class="sxs-lookup"><span data-stu-id="065b5-144">Thumb Control Type</span></span>](uiauto-supportthumbcontroltype.md)
-   [<span data-ttu-id="065b5-145">Тип элемента управления "заголовок"</span><span class="sxs-lookup"><span data-stu-id="065b5-145">TitleBar Control Type</span></span>](uiauto-supporttitlebarcontroltype.md)
-   [<span data-ttu-id="065b5-146">Тип элемента управления ToolBar</span><span class="sxs-lookup"><span data-stu-id="065b5-146">ToolBar Control Type</span></span>](uiauto-supporttoolbarcontroltype.md)
-   [<span data-ttu-id="065b5-147">Тип элемента управления ToolTip</span><span class="sxs-lookup"><span data-stu-id="065b5-147">ToolTip Control Type</span></span>](uiauto-supporttooltipcontroltype.md)
-   [<span data-ttu-id="065b5-148">Тип элемента управления "дерево"</span><span class="sxs-lookup"><span data-stu-id="065b5-148">Tree Control Type</span></span>](uiauto-supporttreecontroltype.md)
-   [<span data-ttu-id="065b5-149">Тип элемента управления TreeItem</span><span class="sxs-lookup"><span data-stu-id="065b5-149">TreeItem Control Type</span></span>](uiauto-supporttreeitemcontroltype.md)
-   [<span data-ttu-id="065b5-150">Тип элемента управления окна</span><span class="sxs-lookup"><span data-stu-id="065b5-150">Window Control Type</span></span>](uiauto-supportwindowcontroltype.md)

## <a name="related-topics"></a><span data-ttu-id="065b5-151">См. также</span><span class="sxs-lookup"><span data-stu-id="065b5-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="065b5-152">Рекомендации программиста поставщика модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="065b5-152">UI Automation Provider Programmer's Guide</span></span>](uiauto-providerportal.md)
</dt> </dl>

 

 