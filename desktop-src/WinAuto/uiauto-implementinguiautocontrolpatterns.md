---
title: Реализация шаблонов элементов управления модели автоматизации пользовательского интерфейса
description: В этом разделе содержатся подробные сведения о реализации интерфейсов поставщиков автоматизации пользовательского интерфейса Майкрософт, поддерживающих шаблоны элементов управления.
ms.assetid: d1baa245-62a1-40b1-a671-e227dd3df60a
keywords:
- Модель автоматизации пользовательского интерфейса, реализация шаблонов элементов управления
- Модель автоматизации пользовательского интерфейса, шаблоны элементов управления
- реализация шаблонов элементов управления модели автоматизации пользовательского интерфейса
- шаблоны элементов управления, реализация автоматизации пользовательского интерфейса
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bfb75b6b275fee9230eb25d9a0b02e1da26ad4d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105700891"
---
# <a name="implementing-ui-automation-control-patterns"></a><span data-ttu-id="2e6a2-107">Реализация шаблонов элементов управления модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="2e6a2-107">Implementing UI Automation Control Patterns</span></span>

<span data-ttu-id="2e6a2-108">В этом разделе содержатся подробные сведения о реализации интерфейсов поставщиков автоматизации пользовательского интерфейса Майкрософт, поддерживающих шаблоны элементов управления.</span><span class="sxs-lookup"><span data-stu-id="2e6a2-108">This section provides detailed information about implementing the Microsoft UI Automation provider interfaces that support control patterns.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="2e6a2-109">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="2e6a2-109">In this section</span></span>

-   [<span data-ttu-id="2e6a2-110">Шаблон элемента Annotation</span><span class="sxs-lookup"><span data-stu-id="2e6a2-110">Annotation Control Pattern</span></span>](uiauto-implementingannotation.md)
-   [<span data-ttu-id="2e6a2-111">Шаблон элемента управления Кустомнавигатион</span><span class="sxs-lookup"><span data-stu-id="2e6a2-111">CustomNavigation Control Pattern</span></span>](uiauto-implementingcustomnavigation.md)
-   [<span data-ttu-id="2e6a2-112">Шаблон элемента управления Dock</span><span class="sxs-lookup"><span data-stu-id="2e6a2-112">Dock Control Pattern</span></span>](uiauto-implementingdock.md)
-   [<span data-ttu-id="2e6a2-113">Перетащите шаблон элемента управления</span><span class="sxs-lookup"><span data-stu-id="2e6a2-113">Drag Control Pattern</span></span>](/windows/desktop/WinAuto/uiauto-implementingdrag)
-   [<span data-ttu-id="2e6a2-114">Шаблон элемента управления Дроптаржет</span><span class="sxs-lookup"><span data-stu-id="2e6a2-114">DropTarget Control Pattern</span></span>](/windows/desktop/WinAuto/uiauto-implementingdroptarget)
-   [<span data-ttu-id="2e6a2-115">Шаблон элемента управления ExpandCollapse</span><span class="sxs-lookup"><span data-stu-id="2e6a2-115">ExpandCollapse Control Pattern</span></span>](uiauto-implementingexpandcollapse.md)
-   [<span data-ttu-id="2e6a2-116">Шаблон элемента управления Grid</span><span class="sxs-lookup"><span data-stu-id="2e6a2-116">Grid Control Pattern</span></span>](uiauto-implementinggrid.md)
-   [<span data-ttu-id="2e6a2-117">Шаблон элемента управления GridItem</span><span class="sxs-lookup"><span data-stu-id="2e6a2-117">GridItem Control Pattern</span></span>](uiauto-implementinggriditem.md)
-   [<span data-ttu-id="2e6a2-118">Вызвать шаблон элемента управления</span><span class="sxs-lookup"><span data-stu-id="2e6a2-118">Invoke Control Pattern</span></span>](uiauto-implementinginvoke.md)
-   [<span data-ttu-id="2e6a2-119">Шаблон элемента управления ItemContainer</span><span class="sxs-lookup"><span data-stu-id="2e6a2-119">ItemContainer Control Pattern</span></span>](uiauto-implementingitemcontainer.md)
-   [<span data-ttu-id="2e6a2-120">Шаблон элемента управления Легацииакцессибле</span><span class="sxs-lookup"><span data-stu-id="2e6a2-120">LegacyIAccessible Control Pattern</span></span>](uiauto-implementinglegacyiaccessible.md)
-   [<span data-ttu-id="2e6a2-121">Шаблон элемента управления Мултиплевиев</span><span class="sxs-lookup"><span data-stu-id="2e6a2-121">MultipleView Control Pattern</span></span>](uiauto-implementingmultipleview.md)
-   [<span data-ttu-id="2e6a2-122">Шаблон элемента управления ObjectModel</span><span class="sxs-lookup"><span data-stu-id="2e6a2-122">ObjectModel Control Pattern</span></span>](uiauto-implementingobjectmodel.md)
-   [<span data-ttu-id="2e6a2-123">Шаблон элемента управления RangeValue</span><span class="sxs-lookup"><span data-stu-id="2e6a2-123">RangeValue Control Pattern</span></span>](uiauto-implementingrangevalue.md)
-   [<span data-ttu-id="2e6a2-124">Шаблон элемента управления Scroll</span><span class="sxs-lookup"><span data-stu-id="2e6a2-124">Scroll Control Pattern</span></span>](uiauto-implementingscroll.md)
-   [<span data-ttu-id="2e6a2-125">Шаблон элемента управления Скроллитем</span><span class="sxs-lookup"><span data-stu-id="2e6a2-125">ScrollItem Control Pattern</span></span>](uiauto-implementingscrollitem.md)
-   [<span data-ttu-id="2e6a2-126">Шаблон элемента управления Selection</span><span class="sxs-lookup"><span data-stu-id="2e6a2-126">Selection Control Pattern</span></span>](uiauto-implementingselection.md)
-   [<span data-ttu-id="2e6a2-127">Шаблон элемента управления SelectionItem</span><span class="sxs-lookup"><span data-stu-id="2e6a2-127">SelectionItem Control Pattern</span></span>](uiauto-implementingselectionitem.md)
-   [<span data-ttu-id="2e6a2-128">Шаблон элемента управления электронной таблицей</span><span class="sxs-lookup"><span data-stu-id="2e6a2-128">Spreadsheet Control Pattern</span></span>](uiauto-implementingspreadsheet.md)
-   [<span data-ttu-id="2e6a2-129">Шаблон элемента управления Спреадшититем</span><span class="sxs-lookup"><span data-stu-id="2e6a2-129">SpreadsheetItem Control Pattern</span></span>](uiauto-implementingspreadsheetitem.md)
-   [<span data-ttu-id="2e6a2-130">Шаблон элемента управления Styles</span><span class="sxs-lookup"><span data-stu-id="2e6a2-130">Styles Control Pattern</span></span>](/windows/desktop/WinAuto/uiauto-implementingstyles)
-   [<span data-ttu-id="2e6a2-131">Шаблон элемента управления Синчронизединпут</span><span class="sxs-lookup"><span data-stu-id="2e6a2-131">SynchronizedInput Control Pattern</span></span>](uiauto-implementingsynchronizedinput.md)
-   [<span data-ttu-id="2e6a2-132">Шаблон элемента управления Table</span><span class="sxs-lookup"><span data-stu-id="2e6a2-132">Table Control Pattern</span></span>](uiauto-implementingtable.md)
-   [<span data-ttu-id="2e6a2-133">Шаблон элемента управления TableItem</span><span class="sxs-lookup"><span data-stu-id="2e6a2-133">TableItem Control Pattern</span></span>](uiauto-implementingtableitem.md)
-   [<span data-ttu-id="2e6a2-134">Шаблоны элементов управления Text и TextRange</span><span class="sxs-lookup"><span data-stu-id="2e6a2-134">Text and TextRange Control Patterns</span></span>](uiauto-implementingtextandtextrange.md)
-   [<span data-ttu-id="2e6a2-135">Шаблон элемента управления Текстчилд</span><span class="sxs-lookup"><span data-stu-id="2e6a2-135">TextChild Control Pattern</span></span>](textchild-control-pattern.md)
-   [<span data-ttu-id="2e6a2-136">Шаблон элемента управления также TextEdit</span><span class="sxs-lookup"><span data-stu-id="2e6a2-136">TextEdit Control Pattern</span></span>](textedit-control-pattern.md)
-   [<span data-ttu-id="2e6a2-137">Переключить шаблон элемента управления</span><span class="sxs-lookup"><span data-stu-id="2e6a2-137">Toggle Control Pattern</span></span>](uiauto-implementingtoggle.md)
-   [<span data-ttu-id="2e6a2-138">Преобразование шаблона элемента управления</span><span class="sxs-lookup"><span data-stu-id="2e6a2-138">Transform Control Pattern</span></span>](uiauto-implementingtransform.md)
-   [<span data-ttu-id="2e6a2-139">Шаблон элемента управления Value</span><span class="sxs-lookup"><span data-stu-id="2e6a2-139">Value Control Pattern</span></span>](uiauto-implementingvalue.md)
-   [<span data-ttu-id="2e6a2-140">Шаблон элемента управления Виртуализедитем</span><span class="sxs-lookup"><span data-stu-id="2e6a2-140">VirtualizedItem Control Pattern</span></span>](uiauto-implementingvirtualizeditem.md)
-   [<span data-ttu-id="2e6a2-141">Шаблон элемента управления Window</span><span class="sxs-lookup"><span data-stu-id="2e6a2-141">Window Control Pattern</span></span>](uiauto-implementingwindow.md)

## <a name="related-topics"></a><span data-ttu-id="2e6a2-142">См. также</span><span class="sxs-lookup"><span data-stu-id="2e6a2-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2e6a2-143">Рекомендации программиста поставщика модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="2e6a2-143">UI Automation Provider Programmer's Guide</span></span>](uiauto-providerportal.md)
</dt> <dt>

[<span data-ttu-id="2e6a2-144">Общие сведения о шаблонах элементов управления модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="2e6a2-144">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="2e6a2-145">Поддержка типов элементов управления модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="2e6a2-145">Supporting UI Automation Control Types</span></span>](uiauto-supportinguiautocontroltypes.md)
</dt> </dl>

 

 