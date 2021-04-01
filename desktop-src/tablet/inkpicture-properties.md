---
description: Этот раздел содержит свойства для элемента управления InkPicture.
ms.assetid: d724c177-af57-4c99-94f2-c70904910b49
title: Свойства InkPicture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0ae8149098b34a70af5e088814e2a5258b0fa0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103817728"
---
# <a name="inkpicture-properties"></a><span data-ttu-id="f69f3-103">Свойства InkPicture</span><span class="sxs-lookup"><span data-stu-id="f69f3-103">InkPicture Properties</span></span>

<span data-ttu-id="f69f3-104">Этот раздел содержит свойства для элемента управления InkPicture.</span><span class="sxs-lookup"><span data-stu-id="f69f3-104">This section contains Properties for the InkPicture Control.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f69f3-105">Свойство</span><span class="sxs-lookup"><span data-stu-id="f69f3-105">Property</span></span></th>
<th><span data-ttu-id="f69f3-106">Описание</span><span class="sxs-lookup"><span data-stu-id="f69f3-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f69f3-107"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_autoredraw"><strong>Ауторедрав, свойство</strong></a></span><span class="sxs-lookup"><span data-stu-id="f69f3-107"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_autoredraw"><strong>AutoRedraw Property</strong></a></span></span></td>
<td><span data-ttu-id="f69f3-108">Возвращает или задает значение, указывающее, перерисовывается ли элемент управления <a href="inkpicture-control-reference.md">InkPicture</a> при недействительности окна (объект <a href="inkdisp-class.md"><strong>инкдисп</strong></a> , который в данный момент связан с элементом управления InkPicture, автоматически перерисовывается, когда окно, связанное с inkpicture, получает сообщение WM_PAINT).</span><span class="sxs-lookup"><span data-stu-id="f69f3-108">Gets or sets a value that specifies whether the <a href="inkpicture-control-reference.md">InkPicture</a> control repaints when the window is invalidated (whether the <a href="inkdisp-class.md"><strong>InkDisp</strong></a> object currently associated with InkPicture control is automatically redrawn when the window associated with the InkPicture receives a WM_PAINT message).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f69f3-109"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_backcolor"><strong>BackColor</strong></a></span><span class="sxs-lookup"><span data-stu-id="f69f3-109"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_backcolor"><strong>BackColor</strong></a></span></span></td>
<td><span data-ttu-id="f69f3-110">Возвращает или задает цвет фона для элемента управления <a href="inkpicture-control-reference.md">InkPicture</a> .</span><span class="sxs-lookup"><span data-stu-id="f69f3-110">Gets or sets the background color for the <a href="inkpicture-control-reference.md">InkPicture</a> control.</span></span> <span data-ttu-id="f69f3-111">Цвет фона по умолчанию — это цвет фона системного окна, который обычно является белым.</span><span class="sxs-lookup"><span data-stu-id="f69f3-111">The default background color is the system window background color, which is typically white.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f69f3-112"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectingink"><strong>Коллектингинк, свойство</strong></a></span><span class="sxs-lookup"><span data-stu-id="f69f3-112"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectingink"><strong>CollectingInk Property</strong></a></span></span></td>
<td><span data-ttu-id="f69f3-113">Возвращает значение, указывающее, собирает ли элемент управления <a href="inkpicture-control-reference.md">InkPicture</a> рукописный ввод (только время выполнения).</span><span class="sxs-lookup"><span data-stu-id="f69f3-113">Gets the value that specifies whether the <a href="inkpicture-control-reference.md">InkPicture</a> control is collecting ink (run time only).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f69f3-114"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectionmode"><strong>Режиме CollectionMode</strong></a></span><span class="sxs-lookup"><span data-stu-id="f69f3-114"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectionmode"><strong>CollectionMode</strong></a></span></span></td>
<td><span data-ttu-id="f69f3-115">Возвращает или задает режим сбора, определяющий, распознаются ли рукописный ввод, жесты или рукописный ввод и жесты при записи пользователем.</span><span class="sxs-lookup"><span data-stu-id="f69f3-115">Gets or sets the collection mode that determines whether ink, gestures, or ink and gestures are recognized as the user writes.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f69f3-116"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_cursors"><strong>Cursor, свойство</strong></a></span><span class="sxs-lookup"><span data-stu-id="f69f3-116"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_cursors"><strong>Cursors Property</strong></a></span></span></td>
<td><span data-ttu-id="f69f3-117">Возвращает коллекцию <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursors"><strong>иинккурсорс</strong></a> , доступную для использования в области рукописного ввода в элементе управления <a href="inkpicture-control-reference.md">InkPicture</a> .</span><span class="sxs-lookup"><span data-stu-id="f69f3-117">Gets the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursors"><strong>IInkCursors</strong></a> collection available for use in the <a href="inkpicture-control-reference.md">InkPicture</a> control's inking region.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f69f3-118"><a href="/previous-versions/windows/desktop/legacy/ms703274(v=vs.85)"><strong>кустомстрокес</strong></a></span><span class="sxs-lookup"><span data-stu-id="f69f3-118"><a href="/previous-versions/windows/desktop/legacy/ms703274(v=vs.85)"><strong>CustomStrokes</strong></a></span></span></td>
<td><span data-ttu-id="f69f3-119">Возвращает коллекцию <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcustomstrokes"><strong>иинккустомстрокес</strong></a> , которая должна быть сохранена с рукописным вводом (только во время разработки).</span><span class="sxs-lookup"><span data-stu-id="f69f3-119">Gets the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcustomstrokes"><strong>IInkCustomStrokes</strong></a> collection to be persisted with the ink (design-time only).</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f69f3-120"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_defaultdrawingattributes"><strong>DefaultDrawingAttributes, свойство</strong></a></span><span class="sxs-lookup"><span data-stu-id="f69f3-120"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_defaultdrawingattributes"><strong>DefaultDrawingAttributes Property</strong></a></span></span></td>
<td><span data-ttu-id="f69f3-121">Возвращает или задает коллекцию <a href="inkdrawingattributes-class.md"><strong>инкдравингаттрибутес</strong></a> по умолчанию, используемую при прорисовке и отображении рукописного ввода (только во время выполнения).</span><span class="sxs-lookup"><span data-stu-id="f69f3-121">Gets or sets the default <a href="inkdrawingattributes-class.md"><strong>InkDrawingAttributes</strong></a> collection to use when drawing and displaying ink (run time only).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f69f3-122"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_desiredpacketdescription"><strong>Десиредпаккетдескриптион, свойство</strong></a></span><span class="sxs-lookup"><span data-stu-id="f69f3-122"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_desiredpacketdescription"><strong>DesiredPacketDescription Property</strong></a></span></span></td>
<td><span data-ttu-id="f69f3-123">Возвращает или задает описание пакета для элемента управления <a href="inkpicture-control-reference.md">InkPicture</a> (только время выполнения).</span><span class="sxs-lookup"><span data-stu-id="f69f3-123">Gets or sets the packet description of the <a href="inkpicture-control-reference.md">InkPicture</a> control (run time only).</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f69f3-124"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_dynamicrendering"><strong>Динамикрендеринг, свойство</strong></a></span><span class="sxs-lookup"><span data-stu-id="f69f3-124"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_dynamicrendering"><strong>DynamicRendering Property</strong></a></span></span></td>
<td><span data-ttu-id="f69f3-125">Возвращает или задает значение, указывающее, будет ли элемент управления <a href="inkpicture-control-reference.md">InkPicture</a> динамически отображать рукописный ввод при его сборе.</span><span class="sxs-lookup"><span data-stu-id="f69f3-125">Gets or sets the value that specifies whether the <a href="inkpicture-control-reference.md">InkPicture</a> control dynamically renders the ink as it is collected.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f69f3-126"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_editingmode"><strong>EditingMode</strong></a></span><span class="sxs-lookup"><span data-stu-id="f69f3-126"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_editingmode"><strong>EditingMode</strong></a></span></span></td>
<td><span data-ttu-id="f69f3-127">Возвращает или задает значение, указывающее, находится ли элемент управления <a href="inkpicture-control-reference.md">InkPicture</a> в режиме рукописного ввода, режиме удаления или режиме правки или выбора.</span><span class="sxs-lookup"><span data-stu-id="f69f3-127">Gets or sets a value that specifies whether the <a href="inkpicture-control-reference.md">InkPicture</a> control is in ink mode, deletion mode, or selecting/editing mode.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f69f3-128"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_enabled"><strong>Активировано</strong></a></span><span class="sxs-lookup"><span data-stu-id="f69f3-128"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_enabled"><strong>Enabled</strong></a></span></span></td>
<td><span data-ttu-id="f69f3-129">Возвращает или задает значение, определяющее, может ли элемент управления <a href="inkpicture-control-reference.md">InkPicture</a> отвечать на создаваемые пользователем события.</span><span class="sxs-lookup"><span data-stu-id="f69f3-129">Gets or sets a value that determines whether the <a href="inkpicture-control-reference.md">InkPicture</a> control can respond to user-generated events.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="f69f3-130">Это свойство эквивалентно свойству <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled"><strong>инкенаблед</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="f69f3-130">This property is equivalent to the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled"><strong>InkEnabled</strong></a> property.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f69f3-131"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_erasermode"><strong>ерасермоде</strong></a></span><span class="sxs-lookup"><span data-stu-id="f69f3-131"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_erasermode"><strong>EraserMode</strong></a></span></span></td>
<td><span data-ttu-id="f69f3-132">Возвращает или задает значение, указывающее, удаляются ли рукописные данные по штрихам или по точкам.</span><span class="sxs-lookup"><span data-stu-id="f69f3-132">Gets or sets the value that specifies whether ink is erased by stroke or by point.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f69f3-133"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_eraserwidth"><strong>ерасервидс</strong></a></span><span class="sxs-lookup"><span data-stu-id="f69f3-133"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_eraserwidth"><strong>EraserWidth</strong></a></span></span></td>
<td><span data-ttu-id="f69f3-134">Возвращает или задает значение, указывающее ширину кончика пера ластика.</span><span class="sxs-lookup"><span data-stu-id="f69f3-134">Gets or sets the value that specifies the width of the eraser pen tip.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f69f3-135"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_hwnd"><strong>hWnd</strong></a></span><span class="sxs-lookup"><span data-stu-id="f69f3-135"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_hwnd"><strong>hWnd</strong></a></span></span></td>
<td><span data-ttu-id="f69f3-136">Возвращает описатель окна, к которому привязан элемент управления <a href="inkpicture-control-reference.md">InkPicture</a> .</span><span class="sxs-lookup"><span data-stu-id="f69f3-136">Gets the window handle to which the <a href="inkpicture-control-reference.md">InkPicture</a> control is bound.</span></span> <span data-ttu-id="f69f3-137">(только время выполнения)</span><span class="sxs-lookup"><span data-stu-id="f69f3-137">(run time only)</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f69f3-138"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink"><strong>Рукописный ввод</strong></a></span><span class="sxs-lookup"><span data-stu-id="f69f3-138"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink"><strong>Ink</strong></a></span></span></td>
<td><span data-ttu-id="f69f3-139">Возвращает или задает объект <a href="inkdisp-class.md"><strong>инкдисп</strong></a> , связанный с элементом управления <a href="inkpicture-control-reference.md">InkPicture</a> (только время выполнения).</span><span class="sxs-lookup"><span data-stu-id="f69f3-139">Gets or sets the <a href="inkdisp-class.md"><strong>InkDisp</strong></a> object that is associated with the <a href="inkpicture-control-reference.md">InkPicture</a> control (run time only).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f69f3-140"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled"><strong>инкенаблед</strong></a></span><span class="sxs-lookup"><span data-stu-id="f69f3-140"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled"><strong>InkEnabled</strong></a></span></span></td>
<td><span data-ttu-id="f69f3-141">Возвращает или задает значение, указывающее, собирает ли элемент управления <a href="inkpicture-control-reference.md">InkPicture</a> входные данные пера (пакеты в сети Air, курсоры в пределах диапазона и т. д.).</span><span class="sxs-lookup"><span data-stu-id="f69f3-141">Gets or sets a value that specifies whether the <a href="inkpicture-control-reference.md">InkPicture</a> control collects pen input (in-air packets, cursor in range events, and so on).</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f69f3-142"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_marginx"><strong>Маргинкс, свойство</strong></a></span><span class="sxs-lookup"><span data-stu-id="f69f3-142"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_marginx"><strong>MarginX Property</strong></a></span></span></td>
<td><span data-ttu-id="f69f3-143">Возвращает или задает поле оси x вокруг прямоугольника окна в экранных координатах.</span><span class="sxs-lookup"><span data-stu-id="f69f3-143">Gets or sets the x-axis margin around the window rectangle in screen coordinates.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f69f3-144"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_marginy"><strong>Свойство Margin</strong></a></span><span class="sxs-lookup"><span data-stu-id="f69f3-144"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_marginy"><strong>MarginY Property</strong></a></span></span></td>
<td><span data-ttu-id="f69f3-145">Возвращает или задает поле оси y вокруг прямоугольника окна в экранных координатах.</span><span class="sxs-lookup"><span data-stu-id="f69f3-145">Gets or sets the y-axis margin around the window rectangle in screen coordinates.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f69f3-146"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_mouseicon"><strong>Маусеикон, свойство</strong></a></span><span class="sxs-lookup"><span data-stu-id="f69f3-146"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_mouseicon"><strong>MouseIcon Property</strong></a></span></span></td>
<td><span data-ttu-id="f69f3-147">Возвращает или задает текущий пользовательский значок мыши.</span><span class="sxs-lookup"><span data-stu-id="f69f3-147">Gets or sets the current custom mouse icon.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f69f3-148"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_mousepointer"><strong>MousePointer, свойство</strong></a></span><span class="sxs-lookup"><span data-stu-id="f69f3-148"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_mousepointer"><strong>MousePointer Property</strong></a></span></span></td>
<td><span data-ttu-id="f69f3-149">Возвращает или задает значение, указывающее тип указателя мыши, который появляется при наведении указателя мыши на определенную часть элемента управления <a href="inkpicture-control-reference.md">InkPicture</a> .</span><span class="sxs-lookup"><span data-stu-id="f69f3-149">Gets or sets a value that indicates the type of mouse pointer that appears when the mouse is over a particular part of the <a href="inkpicture-control-reference.md">InkPicture</a> control.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f69f3-150"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_picture"><strong>Picture</strong></a></span><span class="sxs-lookup"><span data-stu-id="f69f3-150"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_picture"><strong>Picture</strong></a></span></span></td>
<td><span data-ttu-id="f69f3-151">Возвращает графический файл, отображаемый в элементе управления <a href="inkpicture-control-reference.md">InkPicture</a> .</span><span class="sxs-lookup"><span data-stu-id="f69f3-151">Gets the graphics file to appear on the <a href="inkpicture-control-reference.md">InkPicture</a> control.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f69f3-152"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_renderer"><strong>Свойство модуля подготовки отчетов</strong></a></span><span class="sxs-lookup"><span data-stu-id="f69f3-152"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_renderer"><strong>Renderer Property</strong></a></span></span></td>
<td><span data-ttu-id="f69f3-153">Возвращает или задает объект <a href="inkrenderer-class.md"><strong>инкрендерер</strong></a> , используемый для рисования рукописного ввода в элементе управления <a href="inkpicture-control-reference.md">InkPicture</a> (только время выполнения).</span><span class="sxs-lookup"><span data-stu-id="f69f3-153">Gets or sets the <a href="inkrenderer-class.md"><strong>InkRenderer</strong></a> object that is used to draw ink on the <a href="inkpicture-control-reference.md">InkPicture</a> control (run time only).</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f69f3-154"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection"><strong>Выбор</strong></a></span><span class="sxs-lookup"><span data-stu-id="f69f3-154"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection"><strong>Selection</strong></a></span></span></td>
<td><span data-ttu-id="f69f3-155">Возвращает коллекцию <a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">инкстрокес</a> , выбранную в данный момент в элементе управления <a href="inkpicture-control-reference.md">InkPicture</a> (только время выполнения).</span><span class="sxs-lookup"><span data-stu-id="f69f3-155">Gets the <a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collection currently selected inside the <a href="inkpicture-control-reference.md">InkPicture</a> control (run time only).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f69f3-156"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode"><strong>SizeMode</strong></a></span><span class="sxs-lookup"><span data-stu-id="f69f3-156"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode"><strong>SizeMode</strong></a></span></span></td>
<td><span data-ttu-id="f69f3-157">Возвращает или задает способ, которым элемент управления обрабатывает размещение и изменение размера изображения.</span><span class="sxs-lookup"><span data-stu-id="f69f3-157">Gets or sets how the control handles image placement and sizing.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f69f3-158"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_supporthighcontrastink"><strong>Суппорсигхконтрастинк, свойство</strong></a></span><span class="sxs-lookup"><span data-stu-id="f69f3-158"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_supporthighcontrastink"><strong>SupportHighContrastInk Property</strong></a></span></span></td>
<td><span data-ttu-id="f69f3-159">Возвращает значение, указывающее, отображаются ли рукописные данные только в одном цвете, Color = COLOR_WINDOWTEXT (из вызова Жетсистемметрикс), когда система находится в режиме высокая контрастность.</span><span class="sxs-lookup"><span data-stu-id="f69f3-159">Gets a value that specifies whether ink is rendered as just one color, Color = COLOR_WINDOWTEXT (from the GetSystemMetrics call) when the system is in High Contrast mode.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f69f3-160"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_supporthighcontrastselectionui"><strong>суппорсигхконтрастселектионуи</strong></a></span><span class="sxs-lookup"><span data-stu-id="f69f3-160"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_supporthighcontrastselectionui"><strong>SupportHighContrastSelectionUI</strong></a></span></span></td>
<td><span data-ttu-id="f69f3-161">Возвращает или задает значение, указывающее, отображаются ли все пользовательские интерфейсы выделения (ограничивающие прямоугольники выделения и маркеры выделения) с высокой контрастностью, когда система находится в режиме высокая контрастность.</span><span class="sxs-lookup"><span data-stu-id="f69f3-161">Gets or sets a value that specifies whether all selection user interfaces (selection bounding box and selection handles) are drawn in high contrast when the system is in High Contrast mode.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f69f3-162"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_tablet"><strong>Свойство планшета</strong></a></span><span class="sxs-lookup"><span data-stu-id="f69f3-162"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_tablet"><strong>Tablet Property</strong></a></span></span></td>
<td><span data-ttu-id="f69f3-163">Возвращает объект <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet"><strong>иинктаблет</strong></a> , который в настоящее время использует элемент управления <a href="inkpicture-control-reference.md">InkPicture</a> для получения входных данных.</span><span class="sxs-lookup"><span data-stu-id="f69f3-163">Gets the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet"><strong>IInkTablet</strong></a> object that the <a href="inkpicture-control-reference.md">InkPicture</a> control is currently using to collect input.</span></span><br/></td>
</tr>
</tbody>
</table>



 

