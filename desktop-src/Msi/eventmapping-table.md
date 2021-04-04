---
description: В таблице таблица eventmapping перечислены элементы управления, которые подписываются на некоторые события элемента управления, а также список изменяемых атрибутов при публикации события другим элементом управления или установщик Windows.
ms.assetid: 63c9ba3e-aa8a-475b-8360-4aec78ed19db
title: Таблица Таблица eventmapping
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6e9a7b5b4283b5d70102123dcb11e3e9e844221
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908856"
---
# <a name="eventmapping-table"></a><span data-ttu-id="dcf48-103">Таблица Таблица eventmapping</span><span class="sxs-lookup"><span data-stu-id="dcf48-103">EventMapping Table</span></span>

<span data-ttu-id="dcf48-104">В таблице таблица eventmapping перечислены элементы управления, которые подписываются на некоторые события элемента управления, а также список изменяемых атрибутов при публикации события другим элементом управления или установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="dcf48-104">The EventMapping Table lists the controls that subscribe to some control events, and lists the attribute to be changed when the event is published by another control or the Windows Installer.</span></span>

<span data-ttu-id="dcf48-105">Таблица Таблица eventmapping содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="dcf48-105">The EventMapping Table has the following columns.</span></span>



| <span data-ttu-id="dcf48-106">Столбец</span><span class="sxs-lookup"><span data-stu-id="dcf48-106">Column</span></span>    | <span data-ttu-id="dcf48-107">Type</span><span class="sxs-lookup"><span data-stu-id="dcf48-107">Type</span></span>                         | <span data-ttu-id="dcf48-108">Ключ</span><span class="sxs-lookup"><span data-stu-id="dcf48-108">Key</span></span> | <span data-ttu-id="dcf48-109">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="dcf48-109">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="dcf48-110">Диалог\_</span><span class="sxs-lookup"><span data-stu-id="dcf48-110">Dialog\_</span></span>  | [<span data-ttu-id="dcf48-111">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="dcf48-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="dcf48-112">Да</span><span class="sxs-lookup"><span data-stu-id="dcf48-112">Y</span></span>   | <span data-ttu-id="dcf48-113">Нет</span><span class="sxs-lookup"><span data-stu-id="dcf48-113">N</span></span>        |
| <span data-ttu-id="dcf48-114">элементом управления\_</span><span class="sxs-lookup"><span data-stu-id="dcf48-114">Control\_</span></span> | [<span data-ttu-id="dcf48-115">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="dcf48-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="dcf48-116">Да</span><span class="sxs-lookup"><span data-stu-id="dcf48-116">Y</span></span>   | <span data-ttu-id="dcf48-117">Нет</span><span class="sxs-lookup"><span data-stu-id="dcf48-117">N</span></span>        |
| <span data-ttu-id="dcf48-118">Событие</span><span class="sxs-lookup"><span data-stu-id="dcf48-118">Event</span></span>     | [<span data-ttu-id="dcf48-119">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="dcf48-119">Identifier</span></span>](identifier.md) | <span data-ttu-id="dcf48-120">Да</span><span class="sxs-lookup"><span data-stu-id="dcf48-120">Y</span></span>   | <span data-ttu-id="dcf48-121">Нет</span><span class="sxs-lookup"><span data-stu-id="dcf48-121">N</span></span>        |
| <span data-ttu-id="dcf48-122">attribute</span><span class="sxs-lookup"><span data-stu-id="dcf48-122">Attribute</span></span> | [<span data-ttu-id="dcf48-123">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="dcf48-123">Identifier</span></span>](identifier.md) | <span data-ttu-id="dcf48-124">Нет</span><span class="sxs-lookup"><span data-stu-id="dcf48-124">N</span></span>   | <span data-ttu-id="dcf48-125">Нет</span><span class="sxs-lookup"><span data-stu-id="dcf48-125">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="dcf48-126">Столбцы</span><span class="sxs-lookup"><span data-stu-id="dcf48-126">Columns</span></span>

<dl> <dt>

<span data-ttu-id="dcf48-127"><span id="Dialog_"></span><span id="dialog_"></span><span id="DIALOG_"></span>Откроется\_</span><span class="sxs-lookup"><span data-stu-id="dcf48-127"><span id="Dialog_"></span><span id="dialog_"></span><span id="DIALOG_"></span>Dialog\_</span></span>
</dt> <dd>

<span data-ttu-id="dcf48-128">Внешний ключ к первому столбцу [диалоговой таблицы](dialog-table.md).</span><span class="sxs-lookup"><span data-stu-id="dcf48-128">An external key to the first column of the [Dialog Table](dialog-table.md).</span></span> <span data-ttu-id="dcf48-129">Это поле и поле элемента управления \_ вместе определяют элемент управления.</span><span class="sxs-lookup"><span data-stu-id="dcf48-129">This field and the Control\_ field together identify a control.</span></span>

</dd> <dt>

<span data-ttu-id="dcf48-130"><span id="Control_"></span><span id="control_"></span><span id="CONTROL_"></span>Элемента\_</span><span class="sxs-lookup"><span data-stu-id="dcf48-130"><span id="Control_"></span><span id="control_"></span><span id="CONTROL_"></span>Control\_</span></span>
</dt> <dd>

<span data-ttu-id="dcf48-131">Внешний ключ ко второму столбцу [управляющей таблицы](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="dcf48-131">An external key to the second column of the [Control Table](control-table.md).</span></span> <span data-ttu-id="dcf48-132">Это поле и поле диалога \_ вместе определяют элемент управления.</span><span class="sxs-lookup"><span data-stu-id="dcf48-132">This field and the Dialog\_ field together identify a control.</span></span>

</dd> <dt>

<span data-ttu-id="dcf48-133"><span id="Event"></span><span id="event"></span><span id="EVENT"></span>Журнале</span><span class="sxs-lookup"><span data-stu-id="dcf48-133"><span id="Event"></span><span id="event"></span><span id="EVENT"></span>Event</span></span>
</dt> <dd>

<span data-ttu-id="dcf48-134">Это поле представляет собой идентификатор, указывающий тип события, на которое подписан элемент управления.</span><span class="sxs-lookup"><span data-stu-id="dcf48-134">This field is an identifier that specifies the type of event that is subscribed to by the control.</span></span> <span data-ttu-id="dcf48-135">Дополнительные сведения см. в разделе [таблице ControlEvent событие Overview](controlevent-overview.md).</span><span class="sxs-lookup"><span data-stu-id="dcf48-135">For more information, see [ControlEvent Overview](controlevent-overview.md).</span></span>

</dd> <dt>

<span data-ttu-id="dcf48-136"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>Версию</span><span class="sxs-lookup"><span data-stu-id="dcf48-136"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>Attribute</span></span>
</dt> <dd>

<span data-ttu-id="dcf48-137">Имя атрибута элемента управления \_ , заданное при получении события в столбце событий.</span><span class="sxs-lookup"><span data-stu-id="dcf48-137">The name of the Control\_ attribute that is set when the event in the Event column is received.</span></span> <span data-ttu-id="dcf48-138">Аргумент события передается в качестве аргумента вызова атрибута для изменения этого атрибута элемента управления.</span><span class="sxs-lookup"><span data-stu-id="dcf48-138">The Argument of the event is passed as the argument of the attribute call to change this attribute of the control.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dcf48-139">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dcf48-139">Remarks</span></span>

<span data-ttu-id="dcf48-140">В [таблице таблице ControlEvent событие](controlevent-table.md) указываются события элемента управления, которые запускаются, когда пользователь взаимодействует с элементом [управления "кнопка](pushbutton-control.md) [", элементом управления CheckBox](checkbox-control.md)или [элементом управления селектионтри](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="dcf48-140">The [ControlEvent Table](controlevent-table.md) specifies the control events that are started when a user interacts with a [PushButton Control](pushbutton-control.md), [CheckBox Control](checkbox-control.md), or [SelectionTree Control](selectiontree-control.md).</span></span> <span data-ttu-id="dcf48-141">Это единственные элементы управления, которые пользователь может использовать для инициации событий элемента управления.</span><span class="sxs-lookup"><span data-stu-id="dcf48-141">These are the only controls that a user can use to initiate control events.</span></span>

<span data-ttu-id="dcf48-142">Несколько элементов управления в диалоговом окне могут подписываться на одно и то же событие.</span><span class="sxs-lookup"><span data-stu-id="dcf48-142">More than one control on a dialog box can subscribe to the same event.</span></span>

<span data-ttu-id="dcf48-143">В следующем списке перечислены типичные варианты использования таблицы таблица eventmapping.</span><span class="sxs-lookup"><span data-stu-id="dcf48-143">The following list identifies the typical uses for the EventMapping Table:</span></span>

-   <span data-ttu-id="dcf48-144">Чтобы подписывать [элемент управления Text](text-control.md) на [актионтекст таблице ControlEvent событие](actiontext-controlevent.md), [актиондата таблице ControlEvent событие](actiondata-controlevent.md), [скриптинпрогресс таблице controlevent событие](scriptinprogress-controlevent.md) или [TimeRemaining таблице ControlEvent событие](timeremaining-controlevent.md) , опубликованных установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="dcf48-144">To subscribe a [Text Control](text-control.md) to an [ActionText ControlEvent](actiontext-controlevent.md), [ActionData ControlEvent](actiondata-controlevent.md), [ScriptInProgress ControlEvent](scriptinprogress-controlevent.md) or [TimeRemaining ControlEvent](timeremaining-controlevent.md) published by the Windows Installer.</span></span>
-   <span data-ttu-id="dcf48-145">Для подписки [элемента управления ProgressBar](progressbar-control.md) или [элемента управления объявлением](billboard-control.md) на [сетпрогресс таблице ControlEvent событие](setprogress-controlevent.md).</span><span class="sxs-lookup"><span data-stu-id="dcf48-145">To subscribe a [ProgressBar Control](progressbar-control.md) or [Billboard Control](billboard-control.md) to a [SetProgress ControlEvent](setprogress-controlevent.md).</span></span>
-   <span data-ttu-id="dcf48-146">Для подписки [элемента управления директорикомбо](directorycombo-control.md) на [игноречанже таблице ControlEvent событие](ignorechange-controlevent.md).</span><span class="sxs-lookup"><span data-stu-id="dcf48-146">To subscribe a [DirectoryCombo Control](directorycombo-control.md) to an [IgnoreChange ControlEvent](ignorechange-controlevent.md).</span></span>
-   <span data-ttu-id="dcf48-147">Для автоматического отключения [элемента управления "кнопка](pushbutton-control.md) ", расположенного в том же диалоговом окне с [элементом управления селектионтри](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="dcf48-147">To automatically disable a [PushButton Control](pushbutton-control.md) located on the same dialog with a [SelectionTree Control](selectiontree-control.md).</span></span> <span data-ttu-id="dcf48-148">Чтобы отключить кнопку "Отправить", если в [элементе управления селектионтри](selectiontree-control.md)не указаны какие-либо функции, используйте таблицу таблица eventmapping для подписки элемента управления "Кнопка" на [селектионноитемс таблице ControlEvent событие](selectionnoitems-controlevent.md).</span><span class="sxs-lookup"><span data-stu-id="dcf48-148">To disable the push button when no features are listed in the [SelectionTree Control](selectiontree-control.md), use the EventMapping Table to subscribe the PushButton control to a [SelectionNoItems ControlEvent](selectionnoitems-controlevent.md).</span></span> <span data-ttu-id="dcf48-149">Введите **включить** в поле атрибуты таблицы таблица eventmapping.</span><span class="sxs-lookup"><span data-stu-id="dcf48-149">Enter **Enable** in the Attributes field of the EventMapping Table.</span></span>
-   <span data-ttu-id="dcf48-150">Для отображения [текстового элемента управления](text-control.md) , отображающего путь к расположению установки компонента, выбранного в [элементе управления селектионтри](selectiontree-control.md) в том же диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="dcf48-150">To display a [Text Control](text-control.md) that shows the path to the installation location for the feature that is selected in a [SelectionTree Control](selectiontree-control.md) on the same dialog.</span></span> <span data-ttu-id="dcf48-151">Используйте таблицу таблица eventmapping для подписки [элемента управления Text](text-control.md) на [Селектионпасон таблице ControlEvent событие](selectionpathon-controlevent.md) и [Селектионпас таблице ControlEvent событие](selectionpath-controlevent.md) , опубликованные [элементом управления селектионтри](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="dcf48-151">Use the EventMapping Table to subscribe the [Text Control](text-control.md) to both a [SelectionPathOn ControlEvent](selectionpathon-controlevent.md) and [SelectionPath ControlEvent](selectionpath-controlevent.md) published by the [SelectionTree Control](selectiontree-control.md).</span></span>
-   <span data-ttu-id="dcf48-152">Чтобы отобразить [элемент управления "текст](text-control.md) ", в котором отображается описание элемента, выделенного в элементе [управления селектионтри](selectiontree-control.md) , расположенном в том же диалоговом окне, используйте таблицу таблица eventmapping для подписки [элемента управления Text](text-control.md) на [Селектиондескриптион таблице ControlEvent событие](selectiondescription-controlevent.md), [селектионсизе таблице ControlEvent событие](selectionsize-controlevent.md) или [селектионактион таблице ControlEvent событие](selectionaction-controlevent.md).</span><span class="sxs-lookup"><span data-stu-id="dcf48-152">To display a [Text Control](text-control.md) that shows a description of the item highlighted in a [SelectionTree Control](selectiontree-control.md) located on the same dialog, use the EventMapping Table to subscribe the [Text Control](text-control.md) to a [SelectionDescription ControlEvent](selectiondescription-controlevent.md), [SelectionSize ControlEvent](selectionsize-controlevent.md) or [SelectionAction ControlEvent](selectionaction-controlevent.md).</span></span> <span data-ttu-id="dcf48-153">Введите **текст** в поле атрибут таблицы таблица eventmapping.</span><span class="sxs-lookup"><span data-stu-id="dcf48-153">Enter **Text** in the Attribute field of the EventMapping Table.</span></span>

## <a name="validation"></a><span data-ttu-id="dcf48-154">Проверка</span><span class="sxs-lookup"><span data-stu-id="dcf48-154">Validation</span></span>

<dl>

[<span data-ttu-id="dcf48-155">ICE03</span><span class="sxs-lookup"><span data-stu-id="dcf48-155">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="dcf48-156">ICE06</span><span class="sxs-lookup"><span data-stu-id="dcf48-156">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="dcf48-157">ICE32</span><span class="sxs-lookup"><span data-stu-id="dcf48-157">ICE32</span></span>](ice32.md)  
</dl>

 

 



