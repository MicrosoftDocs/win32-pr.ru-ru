---
title: Общие параметры управления
description: Ниже описан общий синтаксис для инструкции Control Resource-Definition.
ms.assetid: e7a49a9f-93b5-4221-8006-3d1864b7a6a1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 261c71163276ed39841d6f6d7e125d4eb5420072
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337180"
---
# <a name="common-control-parameters"></a><span data-ttu-id="4b6ab-103">Общие параметры управления</span><span class="sxs-lookup"><span data-stu-id="4b6ab-103">Common Control Parameters</span></span>

<span data-ttu-id="4b6ab-104">Ниже описан общий синтаксис для инструкции Control Resource-Definition.</span><span class="sxs-lookup"><span data-stu-id="4b6ab-104">The following describes the general syntax for a control resource-definition statement.</span></span> <span data-ttu-id="4b6ab-105">Значение каждого параметра приведено ниже.</span><span class="sxs-lookup"><span data-stu-id="4b6ab-105">The meaning of each parameter is given below.</span></span> <span data-ttu-id="4b6ab-106">Иногда инструкция будет использовать параметр иначе или может игнорировать параметр.</span><span class="sxs-lookup"><span data-stu-id="4b6ab-106">Occasionally, a statement will use a parameter differently, or may ignore a parameter.</span></span> <span data-ttu-id="4b6ab-107">Вариант, зависящий от инструкции, описан в документации для инструкции.</span><span class="sxs-lookup"><span data-stu-id="4b6ab-107">The statement-specific variation is described in the documentation for the statement.</span></span>

``` syntax
control [[text,]] id, x, y, width, height[[, style[[, extended-style]]]][, helpId]
[{ data-element-1 [, data-element-2 [,  . . . ]]}]
```

<dl> <dt>

<span data-ttu-id="4b6ab-108"><span id="text"></span><span id="TEXT"></span>*полнотекстовым*</span><span class="sxs-lookup"><span data-stu-id="4b6ab-108"><span id="text"></span><span id="TEXT"></span>*text*</span></span>
</dt> <dd>

<span data-ttu-id="4b6ab-109">Текст, отображаемый с элементом управления.</span><span class="sxs-lookup"><span data-stu-id="4b6ab-109">Text that is to be displayed with the control.</span></span> <span data-ttu-id="4b6ab-110">Текст располагается внутри элемента управления или рядом с элементом управления.</span><span class="sxs-lookup"><span data-stu-id="4b6ab-110">The text is positioned within the control or adjacent to the control.</span></span>

<span data-ttu-id="4b6ab-111">Этот параметр должен содержать ноль или более символов, заключенных в двойные кавычки (").</span><span class="sxs-lookup"><span data-stu-id="4b6ab-111">This parameter must contain zero or more characters enclosed in double quotation marks (").</span></span> <span data-ttu-id="4b6ab-112">Строки автоматически завершаются нулем и преобразуются в Юникод в результирующем файле ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4b6ab-112">Strings are automatically null-terminated and converted to Unicode in the resulting resource file.</span></span>

<span data-ttu-id="4b6ab-113">По умолчанию символы, перечисленные между двойными кавычками, являются символами ANSI, а escape-последовательности обрабатываются как escape-последовательности байтов.</span><span class="sxs-lookup"><span data-stu-id="4b6ab-113">By default, the characters listed between the double quotation marks are ANSI characters, and escape sequences are interpreted as byte escape sequences.</span></span> <span data-ttu-id="4b6ab-114">Если строка предшествует префиксу "L", строка является строкой расширенных символов и escape-последовательностями интерпретируется как escape-последовательности длиной 2 байта, указывающей символы Юникода.</span><span class="sxs-lookup"><span data-stu-id="4b6ab-114">If the string is preceded by the "L" prefix, the string is a wide-character string and escape sequences are interpreted as 2-byte escape sequences that specify Unicode characters.</span></span> <span data-ttu-id="4b6ab-115">Если в тексте требуется двойная кавычка, необходимо дважды ввести двойную кавычку.</span><span class="sxs-lookup"><span data-stu-id="4b6ab-115">If a double quotation mark is required in the text, you must include the double quotation mark twice.</span></span>

<span data-ttu-id="4b6ab-116">Символ амперсанда (&) в тексте указывает на то, что следующий символ используется в качестве назначенного символа для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="4b6ab-116">An ampersand (&) character in the text indicates that the following character is used as a mnemonic character for the control.</span></span> <span data-ttu-id="4b6ab-117">При отображении элемента управления амперсанд не отображается, но назначенный символ подчеркивается.</span><span class="sxs-lookup"><span data-stu-id="4b6ab-117">When the control is displayed, the ampersand is not shown, but the mnemonic character is underlined.</span></span> <span data-ttu-id="4b6ab-118">Пользователь может выбрать элемент управления, нажав клавишу, соответствующую подчеркнутой символовой клавише.</span><span class="sxs-lookup"><span data-stu-id="4b6ab-118">The user can choose the control by pressing the key corresponding to the underlined mnemonic character.</span></span> <span data-ttu-id="4b6ab-119">Чтобы использовать амперсанд в качестве символа в строке, вставьте два амперсанда (&&).</span><span class="sxs-lookup"><span data-stu-id="4b6ab-119">To use the ampersand as a character in a string, insert two ampersands (&&).</span></span>

</dd> <dt>

<span data-ttu-id="4b6ab-120"><span id="id"></span><span id="ID"></span>*удостоверения*</span><span class="sxs-lookup"><span data-stu-id="4b6ab-120"><span id="id"></span><span id="ID"></span>*id*</span></span>
</dt> <dd>

<span data-ttu-id="4b6ab-121">Идентификатор элемента управления.</span><span class="sxs-lookup"><span data-stu-id="4b6ab-121">Control identifier.</span></span> <span data-ttu-id="4b6ab-122">Это значение должно быть 16-битным беззнаковым целым числом в диапазоне от 0 до 65 535 или простого арифметического выражения, результатом которого является значение в этом диапазоне.</span><span class="sxs-lookup"><span data-stu-id="4b6ab-122">This value must be a 16-bit unsigned integer in the range 0 through 65,535 or a simple arithmetic expression that evaluates to a value in that range.</span></span>

</dd> <dt>

<span data-ttu-id="4b6ab-123"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="4b6ab-123"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="4b6ab-124">Координата по оси X левой стороны элемента управления относительно левой части диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="4b6ab-124">X-coordinate of the left side of the control relative to the left side of the dialog box.</span></span> <span data-ttu-id="4b6ab-125">Это значение должно быть 16-битным беззнаковым целым числом в диапазоне от 0 до 65 535.</span><span class="sxs-lookup"><span data-stu-id="4b6ab-125">This value must be a 16-bit unsigned integer in the range 0 through 65,535.</span></span> <span data-ttu-id="4b6ab-126">Координата указывается в единицах диалогового окна и задается относительно происхождения диалогового окна, окна или элемента управления, содержащего указанный элемент управления.</span><span class="sxs-lookup"><span data-stu-id="4b6ab-126">The coordinate is in dialog units and is relative to the origin of the dialog box, window, or control containing the specified control.</span></span>

</dd> <dt>

<span data-ttu-id="4b6ab-127"><span id="y"></span><span id="Y"></span>*&*</span><span class="sxs-lookup"><span data-stu-id="4b6ab-127"><span id="y"></span><span id="Y"></span>*y*</span></span>
</dt> <dd>

<span data-ttu-id="4b6ab-128">Координата по оси Y верхней стороны элемента управления относительно верхней части диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="4b6ab-128">Y-coordinate of the top side of the control relative to the top of the dialog box.</span></span> <span data-ttu-id="4b6ab-129">Это значение должно быть 16-битным беззнаковым целым числом в диапазоне от 0 до 65 535.</span><span class="sxs-lookup"><span data-stu-id="4b6ab-129">This value must be a 16-bit unsigned integer in the range 0 through 65,535.</span></span> <span data-ttu-id="4b6ab-130">Координата указывается в единицах диалогового окна относительно источника диалогового окна, окна или элемента управления, содержащего указанный элемент управления.</span><span class="sxs-lookup"><span data-stu-id="4b6ab-130">The coordinate is in dialog units relative to the origin of the dialog box, window, or control containing the specified control.</span></span>

</dd> <dt>

<span data-ttu-id="4b6ab-131"><span id="width"></span><span id="WIDTH"></span>*Ширина*</span><span class="sxs-lookup"><span data-stu-id="4b6ab-131"><span id="width"></span><span id="WIDTH"></span>*width*</span></span>
</dt> <dd>

<span data-ttu-id="4b6ab-132">Ширина элемента управления.</span><span class="sxs-lookup"><span data-stu-id="4b6ab-132">Width of the control.</span></span> <span data-ttu-id="4b6ab-133">Это значение должно быть 16-битным беззнаковым целым числом в диапазоне от 1 до 65 535.</span><span class="sxs-lookup"><span data-stu-id="4b6ab-133">This value must be a 16-bit unsigned integer in the range 1 through 65,535.</span></span> <span data-ttu-id="4b6ab-134">Ширина — 1/4-символьная единица.</span><span class="sxs-lookup"><span data-stu-id="4b6ab-134">The width is in 1/4-character units.</span></span>

</dd> <dt>

<span data-ttu-id="4b6ab-135"><span id="height"></span><span id="HEIGHT"></span>*равно*</span><span class="sxs-lookup"><span data-stu-id="4b6ab-135"><span id="height"></span><span id="HEIGHT"></span>*height*</span></span>
</dt> <dd>

<span data-ttu-id="4b6ab-136">Высота элемента управления.</span><span class="sxs-lookup"><span data-stu-id="4b6ab-136">Height of the control.</span></span> <span data-ttu-id="4b6ab-137">Это значение должно быть 16-битным беззнаковым целым числом в диапазоне от 1 до 65 535.</span><span class="sxs-lookup"><span data-stu-id="4b6ab-137">This value must be a 16-bit unsigned integer in the range 1 through 65,535.</span></span> <span data-ttu-id="4b6ab-138">Высота — 1/8-символьная единица.</span><span class="sxs-lookup"><span data-stu-id="4b6ab-138">The height is in 1/8-character units.</span></span>

</dd> <dt>

<span data-ttu-id="4b6ab-139"><span id="style"></span><span id="STYLE"></span>*стиль*</span><span class="sxs-lookup"><span data-stu-id="4b6ab-139"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="4b6ab-140">Стили элементов управления.</span><span class="sxs-lookup"><span data-stu-id="4b6ab-140">Control styles.</span></span> <span data-ttu-id="4b6ab-141">Используйте оператор побитового или ( \| ) для объединения стилей.</span><span class="sxs-lookup"><span data-stu-id="4b6ab-141">Use the bitwise OR (\|) operator to combine styles.</span></span> <span data-ttu-id="4b6ab-142">Дополнительные сведения см. в разделе [стили окон](../winmsg/window-styles.md).</span><span class="sxs-lookup"><span data-stu-id="4b6ab-142">For more information, see [Window Styles](../winmsg/window-styles.md).</span></span>

</dd> <dt>

<span data-ttu-id="4b6ab-143"><span id="extended-style"></span><span id="EXTENDED-STYLE"></span>*Расширенный стиль*</span><span class="sxs-lookup"><span data-stu-id="4b6ab-143"><span id="extended-style"></span><span id="EXTENDED-STYLE"></span>*extended-style*</span></span>
</dt> <dd>

<span data-ttu-id="4b6ab-144">Расширенные стили окна.</span><span class="sxs-lookup"><span data-stu-id="4b6ab-144">Extended window styles.</span></span> <span data-ttu-id="4b6ab-145">Для указания *расширенного стиля* необходимо указать *Style* .</span><span class="sxs-lookup"><span data-stu-id="4b6ab-145">You must specify *style* to specify *extended-style*.</span></span> <span data-ttu-id="4b6ab-146">Дополнительные сведения см. в разделе [**операторе EXSTYLE**](exstyle-statement.md).</span><span class="sxs-lookup"><span data-stu-id="4b6ab-146">For more information, see [**EXSTYLE**](exstyle-statement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4b6ab-147"><span id="helpId"></span><span id="helpid"></span><span id="HELPID"></span>*Идентификатор справки*</span><span class="sxs-lookup"><span data-stu-id="4b6ab-147"><span id="helpId"></span><span id="helpid"></span><span id="HELPID"></span>*helpId*</span></span>
</dt> <dd>

<span data-ttu-id="4b6ab-148">Числовое выражение, указывающее идентификатор, используемый для идентификации элемента управления во время обработки [**\_ справки WM**](../shell/wm-help.md) .</span><span class="sxs-lookup"><span data-stu-id="4b6ab-148">Numeric expression indicating the ID used to identify the control during [**WM\_HELP**](../shell/wm-help.md) processing.</span></span>

</dd> <dt>

<span data-ttu-id="4b6ab-149"><span id="controlData"></span><span id="controldata"></span><span id="CONTROLDATA"></span>*контролдата*</span><span class="sxs-lookup"><span data-stu-id="4b6ab-149"><span id="controlData"></span><span id="controldata"></span><span id="CONTROLDATA"></span>*controlData*</span></span>
</dt> <dd>

<span data-ttu-id="4b6ab-150">Данные, относящиеся к элементу управления.</span><span class="sxs-lookup"><span data-stu-id="4b6ab-150">Control-specific data for the control.</span></span> <span data-ttu-id="4b6ab-151">При создании диалогового окна и элемента управления в этом диалоговом окне, который содержит данные, относящиеся к элементу управления, указатель на эти данные передается в окно процедуры элемента управления посредством свойства *lParam* сообщения [**WM \_ CREATE**](../winmsg/wm-create.md) для этого элемента управления.</span><span class="sxs-lookup"><span data-stu-id="4b6ab-151">When a dialog is created, and a control in that dialog which has control-specific data is created, a pointer to that data is passed into the control's window procedure through the *lParam* of the [**WM\_CREATE**](../winmsg/wm-create.md) message for that control.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4b6ab-152">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4b6ab-152">Remarks</span></span>

<span data-ttu-id="4b6ab-153">Горизонтальные единицы диалогового окна — 1/4 единиц базовой ширины диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="4b6ab-153">Horizontal dialog units are 1/4 of the dialog base width unit.</span></span> <span data-ttu-id="4b6ab-154">Единицы по вертикали — 1/8 единиц базовой высоты диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="4b6ab-154">Vertical units are 1/8 of the dialog base height unit.</span></span> <span data-ttu-id="4b6ab-155">Текущие базовые единицы диалогового окна вычисляются по высоте и ширине текущего системного шрифта.</span><span class="sxs-lookup"><span data-stu-id="4b6ab-155">The current dialog base units are computed from the height and width of the current system font.</span></span> <span data-ttu-id="4b6ab-156">Функция [**жетдиалогбасеунитс**](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits) Возвращает базовые единицы диалогового окна в пикселях.</span><span class="sxs-lookup"><span data-stu-id="4b6ab-156">The [**GetDialogBaseUnits**](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits) function returns the dialog base units in pixels.</span></span> <span data-ttu-id="4b6ab-157">Координаты задаются относительно источника диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="4b6ab-157">The coordinates are relative to the origin of the dialog box.</span></span>

 

 