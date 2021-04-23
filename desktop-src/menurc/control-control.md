---
title: Элемент управления
description: Определяет определяемый пользователем элемент управления.
ms.assetid: e5e7b7af-e2b0-41ff-b697-b9ea80e7c61f
keywords:
- Управление меню и другими ресурсами
topic_type:
- apiref
api_name:
- CONTROL
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 703f95778c66522d67e40a51293c8fb8fe956ecb
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103987442"
---
# <a name="control-control"></a><span data-ttu-id="99f56-104">Элемент управления</span><span class="sxs-lookup"><span data-stu-id="99f56-104">CONTROL control</span></span>

<span data-ttu-id="99f56-105">Определяет определяемый пользователем элемент управления.</span><span class="sxs-lookup"><span data-stu-id="99f56-105">Defines a user-defined control.</span></span>

``` syntax
CONTROL text, id, class, style, x, y, width, height [, extended-style]
```

<dl> <dt>

<span data-ttu-id="99f56-106"><span id="class"></span><span id="CLASS"></span>*см*</span><span class="sxs-lookup"><span data-stu-id="99f56-106"><span id="class"></span><span id="CLASS"></span>*class*</span></span>
</dt> <dd>

<span data-ttu-id="99f56-107">Переопределенное имя, символьная строка или 16-битовое целочисленное значение без знака, определяющее класс.</span><span class="sxs-lookup"><span data-stu-id="99f56-107">Redefined name, character string, or a 16-bit unsigned integer value that defines the class.</span></span> <span data-ttu-id="99f56-108">Это может быть любой из классов элементов управления. Список классов элементов управления см. в первом списке, следующем за этим описанием.</span><span class="sxs-lookup"><span data-stu-id="99f56-108">This can be any one of the control classes; for a list of the control classes, see the first list following this description.</span></span> <span data-ttu-id="99f56-109">Если значением является переопределенное имя, предоставленное приложением, оно должно быть строкой, заключенной в двойные кавычки (").</span><span class="sxs-lookup"><span data-stu-id="99f56-109">If the value is a redefined name supplied by the application, it must be a string enclosed in double quotation marks (").</span></span>

</dd> <dt>

<span data-ttu-id="99f56-110"><span id="style"></span><span id="STYLE"></span>*стиль*</span><span class="sxs-lookup"><span data-stu-id="99f56-110"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="99f56-111">Переопределенное имя или целочисленное значение, определяющее стиль данного элемента управления.</span><span class="sxs-lookup"><span data-stu-id="99f56-111">Redefined name or integer value that specifies the style of the given control.</span></span> <span data-ttu-id="99f56-112">Точное значение *стиля* зависит от значения *класса* .</span><span class="sxs-lookup"><span data-stu-id="99f56-112">The exact meaning of *style* depends on the *class* value.</span></span> <span data-ttu-id="99f56-113">В разделах, следующих за этим описанием, показаны классы элементов управления и соответствующие стили.</span><span class="sxs-lookup"><span data-stu-id="99f56-113">The sections following this description show the control classes and corresponding styles.</span></span>

</dd> </dl>

<span data-ttu-id="99f56-114">Дополнительные сведения об общем синтаксисе инструкции Control см. в разделе [Общие параметры управления](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="99f56-114">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="99f56-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="99f56-115">Remarks</span></span>

<span data-ttu-id="99f56-116">Шесть возможных классов элементов управления описаны в следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="99f56-116">The six possible control classes are described in the following sections.</span></span>

### <a name="the-button-control-class"></a><span data-ttu-id="99f56-117">Класс элемента управления Button</span><span class="sxs-lookup"><span data-stu-id="99f56-117">The Button Control Class</span></span>

<span data-ttu-id="99f56-118">Элемент управления "Кнопка" — это небольшое прямоугольное дочернее окно, которое пользователь может включить или отключить, щелкнув его мышью.</span><span class="sxs-lookup"><span data-stu-id="99f56-118">A button control is a small rectangular child window that the user can turn on or off by clicking it with the mouse.</span></span> <span data-ttu-id="99f56-119">Элементы управления "Кнопка" могут использоваться отдельно или в группах и могут быть помечены или отображаться без текста.</span><span class="sxs-lookup"><span data-stu-id="99f56-119">Button controls can be used alone or in groups, and can either be labeled or appear without text.</span></span> <span data-ttu-id="99f56-120">Элементы управления "Кнопка" обычно меняют внешний вид, когда пользователь щелкает их.</span><span class="sxs-lookup"><span data-stu-id="99f56-120">Button controls typically change appearance when the user clicks them.</span></span>

<span data-ttu-id="99f56-121">Стили кнопок описаны в следующем разделе: [стили кнопок](../controls/button-styles.md).</span><span class="sxs-lookup"><span data-stu-id="99f56-121">The button styles are described in the following topic: [Button Styles](../controls/button-styles.md).</span></span>

### <a name="the-combo-box-control-class"></a><span data-ttu-id="99f56-122">Класс элемента управления "поле со списком"</span><span class="sxs-lookup"><span data-stu-id="99f56-122">The Combo Box Control Class</span></span>

<span data-ttu-id="99f56-123">Элементы управления "поле со списком" состоят из поля выбора, похожего на элемент управления редактирования и поле со списком.</span><span class="sxs-lookup"><span data-stu-id="99f56-123">Combo box controls consist of a selection field similar to an edit control plus a list box.</span></span> <span data-ttu-id="99f56-124">Список может отображаться в любое время или отбрасываться, когда пользователь выбирает "всплывающее окно" рядом с полем выбора.</span><span class="sxs-lookup"><span data-stu-id="99f56-124">The list box may be displayed at all times or may be dropped down when the user selects a "pop box" next to the selection field.</span></span>

<span data-ttu-id="99f56-125">В зависимости от стиля поля со списком пользователь может или не может изменять содержимое поля выбора.</span><span class="sxs-lookup"><span data-stu-id="99f56-125">Depending on the style of the combo box, the user can or cannot edit the contents of the selection field.</span></span> <span data-ttu-id="99f56-126">Если список является видимым, ввод символов в поле выбора приведет к выделению первой записи, соответствующей введенным символам.</span><span class="sxs-lookup"><span data-stu-id="99f56-126">If the list box is visible, typing characters into the selection box will cause the first entry that matches the characters typed to be highlighted.</span></span> <span data-ttu-id="99f56-127">И наоборот, при выборе элемента в списке выделенный текст отображается в поле выбора.</span><span class="sxs-lookup"><span data-stu-id="99f56-127">Conversely, selecting an item in the list box displays the selected text in the selection field.</span></span>

<span data-ttu-id="99f56-128">Стили элемента управления "поле со списком" описаны в следующем разделе: [стили полей со](../controls/combo-box-styles.md)списками.</span><span class="sxs-lookup"><span data-stu-id="99f56-128">The combo box control styles are described in the following topic: [Combo Box Styles](../controls/combo-box-styles.md).</span></span>

### <a name="the-edit-control-class"></a><span data-ttu-id="99f56-129">Класс элемента управления Edit</span><span class="sxs-lookup"><span data-stu-id="99f56-129">The Edit Control Class</span></span>

<span data-ttu-id="99f56-130">Элемент управления "поле ввода" — это прямоугольное дочернее окно, в котором пользователь может вводить текст с клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="99f56-130">An edit control is a rectangular child window in which the user can enter text from the keyboard.</span></span> <span data-ttu-id="99f56-131">Пользователь выбирает элемент управления и передает ему фокус ввода, нажимая внутри него указатель мыши или нажимая клавишу TAB.</span><span class="sxs-lookup"><span data-stu-id="99f56-131">The user selects the control, and gives it the input focus, by clicking the mouse inside it or pressing the TAB key.</span></span> <span data-ttu-id="99f56-132">Пользователь может ввести текст, когда элемент управления отображает мигающий курсор вставки.</span><span class="sxs-lookup"><span data-stu-id="99f56-132">The user can enter text when the control displays a flashing insertion point.</span></span> <span data-ttu-id="99f56-133">Мышь может использоваться для перемещения курсора и выбора символов для замены или для позиционирования курсора для вставки символов.</span><span class="sxs-lookup"><span data-stu-id="99f56-133">The mouse can be used to move the cursor and select characters to be replaced, or to position the cursor for inserting characters.</span></span> <span data-ttu-id="99f56-134">Для удаления символов можно использовать клавишу BACKSPACE.</span><span class="sxs-lookup"><span data-stu-id="99f56-134">The BACKSPACE key can be used to delete characters.</span></span>

<span data-ttu-id="99f56-135">Элемент управления "поле ввода" использует шрифт фиксированной высоты и отображает символы Юникода.</span><span class="sxs-lookup"><span data-stu-id="99f56-135">Edit controls use the fixed-pitch font and display Unicode characters.</span></span> <span data-ttu-id="99f56-136">Они разворачивают символы табуляции в столько пробелов, сколько требуется для перемещения курсора на следующую позицию табуляции.</span><span class="sxs-lookup"><span data-stu-id="99f56-136">They expand tab characters into as many space characters as are required to move the cursor to the next tab stop.</span></span> <span data-ttu-id="99f56-137">Позиции табуляции считаются на каждые восьмой знак.</span><span class="sxs-lookup"><span data-stu-id="99f56-137">Tab stops are assumed to be at every eighth character position.</span></span>

<span data-ttu-id="99f56-138">Стили элемента управления Edit описаны в следующем разделе: [Edit Control Styles](../controls/edit-control-styles.md).</span><span class="sxs-lookup"><span data-stu-id="99f56-138">The edit control styles are described in the following topic: [Edit Control Styles](../controls/edit-control-styles.md).</span></span>

### <a name="the-list-box-control-class"></a><span data-ttu-id="99f56-139">Класс элемента управления "список"</span><span class="sxs-lookup"><span data-stu-id="99f56-139">The List Box Control Class</span></span>

<span data-ttu-id="99f56-140">Элементы управления "список" состоят из списка символьных строк.</span><span class="sxs-lookup"><span data-stu-id="99f56-140">List box controls consist of a list of character strings.</span></span> <span data-ttu-id="99f56-141">Элемент управления используется каждый раз, когда приложению требуется предоставить список имен, таких как имена файлов, которые пользователь может просматривать и выбирать.</span><span class="sxs-lookup"><span data-stu-id="99f56-141">The control is used whenever an application needs to present a list of names, such as filenames, that the user can view and select.</span></span> <span data-ttu-id="99f56-142">Пользователь может выбрать строку, указав строку с помощью мыши и нажав кнопку мыши.</span><span class="sxs-lookup"><span data-stu-id="99f56-142">The user can select a string by pointing to the string with the mouse and clicking a mouse button.</span></span> <span data-ttu-id="99f56-143">Если строка выбрана, она выделяется и сообщение уведомления передается родительскому окну.</span><span class="sxs-lookup"><span data-stu-id="99f56-143">When a string is selected, it is highlighted and a notification message is passed to the parent window.</span></span> <span data-ttu-id="99f56-144">Полосу прокрутки можно использовать с элементом управления "список" для прокрутки слишком длинных или слишком широких списков для окна управления.</span><span class="sxs-lookup"><span data-stu-id="99f56-144">A scroll bar can be used with a list box control to scroll lists that are too long or too wide for the control window.</span></span>

<span data-ttu-id="99f56-145">Стили элемента управления "список" описаны в следующем разделе: [стили списка](../controls/list-box-styles.md).</span><span class="sxs-lookup"><span data-stu-id="99f56-145">The list box control styles are described in the following topic: [List Box Styles](../controls/list-box-styles.md).</span></span>

### <a name="the-scroll-bar-control-class"></a><span data-ttu-id="99f56-146">Класс элемента управления Scroll-Bar</span><span class="sxs-lookup"><span data-stu-id="99f56-146">The Scroll-Bar Control Class</span></span>

<span data-ttu-id="99f56-147">Элемент управления "полоса прокрутки" — это прямоугольник, который содержит бегунок прокрутки и имеет стрелки направления на обоих концах.</span><span class="sxs-lookup"><span data-stu-id="99f56-147">A scroll-bar control is a rectangle that contains a scroll thumb and has direction arrows at both ends.</span></span> <span data-ttu-id="99f56-148">Полоса прокрутки отправляет сообщение уведомления родительскому элементу всякий раз, когда пользователь щелкает мышью в элементе управления.</span><span class="sxs-lookup"><span data-stu-id="99f56-148">The scroll bar sends a notification message to its parent whenever the user clicks the mouse in the control.</span></span> <span data-ttu-id="99f56-149">Родительский элемент отвечает за обновление расположения бегунка (при необходимости).</span><span class="sxs-lookup"><span data-stu-id="99f56-149">The parent is responsible for updating the thumb position, if necessary.</span></span> <span data-ttu-id="99f56-150">Элементы управления "полоса прокрутки" имеют те же внешний вид и функции, что и полосы прокрутки, используемые в обычных окнах.</span><span class="sxs-lookup"><span data-stu-id="99f56-150">Scroll-bar controls have the same appearance and function as the scroll bars used in ordinary windows.</span></span> <span data-ttu-id="99f56-151">Но в отличие от полос прокрутки, элементы управления "полоса прокрутки" можно располагать в любом месте окна и использовать при необходимости для обеспечения прокрутки окна.</span><span class="sxs-lookup"><span data-stu-id="99f56-151">But unlike scroll bars, scroll-bar controls can be positioned anywhere within a window and used whenever needed to provide scrolling input for a window.</span></span>

<span data-ttu-id="99f56-152">Стили полосы прокрутки описаны в следующем [разделе.](../controls/scroll-bar-control-styles.md)</span><span class="sxs-lookup"><span data-stu-id="99f56-152">The scroll bar styles are described in the following topic: [Scroll Bar Control Styles](../controls/scroll-bar-control-styles.md).</span></span>

### <a name="the-static-control-class"></a><span data-ttu-id="99f56-153">Статический класс элемента управления</span><span class="sxs-lookup"><span data-stu-id="99f56-153">The Static Control Class</span></span>

<span data-ttu-id="99f56-154">Статические элементы управления — это простые текстовые поля, квадраты и прямоугольники, которые можно использовать для обозначения, бокса или разделения других элементов управления.</span><span class="sxs-lookup"><span data-stu-id="99f56-154">Static controls are simple text fields, boxes, and rectangles that can be used to label, box, or separate other controls.</span></span> <span data-ttu-id="99f56-155">Статические элементы управления не принимают входные данные и не предоставляют выходных данных.</span><span class="sxs-lookup"><span data-stu-id="99f56-155">Static controls take no input and provide no output.</span></span>

<span data-ttu-id="99f56-156">Стили статических элементов управления описаны в следующем разделе: [стили статических элементов управления](../controls/static-control-styles.md).</span><span class="sxs-lookup"><span data-stu-id="99f56-156">The static control styles are described in the following topic: [Static Control Styles](../controls/static-control-styles.md).</span></span>

 

 