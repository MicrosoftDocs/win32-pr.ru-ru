---
description: Таблица таблице ControlEvent событие позволяет автору указать события элемента управления, запущенные при взаимодействии пользователя с элементом управления "Кнопка", элементом управления CheckBox или элементом управления "Селектионтри".
ms.assetid: e34d17e9-cd6b-4a21-9abc-9562ee648c59
title: Таблица таблице ControlEvent событие
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 721dc7ac9a729b8df0623a2958a4d0fe32851307
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913080"
---
# <a name="controlevent-table"></a><span data-ttu-id="574d7-103">Таблица таблице ControlEvent событие</span><span class="sxs-lookup"><span data-stu-id="574d7-103">ControlEvent Table</span></span>

<span data-ttu-id="574d7-104">Таблица таблице ControlEvent событие позволяет автору указать [события элемента управления](control-events.md) , запущенные при взаимодействии пользователя с элементом [управления "кнопка](pushbutton-control.md) [", элементом управления CheckBox](checkbox-control.md)или [элементом управления "селектионтри](selectiontree-control.md)".</span><span class="sxs-lookup"><span data-stu-id="574d7-104">The ControlEvent table allows the author to specify the [Control Events](control-events.md) started when a user interacts with a [PushButton Control](pushbutton-control.md), [CheckBox Control](checkbox-control.md), or [SelectionTree Control](selectiontree-control.md).</span></span> <span data-ttu-id="574d7-105">Это единственные элементы управления, которые пользователи могут использовать для запуска событий элемента управления.</span><span class="sxs-lookup"><span data-stu-id="574d7-105">These are the only controls users can use to initiate control events.</span></span> <span data-ttu-id="574d7-106">Каждый элемент управления может публиковать несколько событий управления.</span><span class="sxs-lookup"><span data-stu-id="574d7-106">Each control can publish multiple control events.</span></span> <span data-ttu-id="574d7-107">Установщик запускает каждое событие в порядке, указанном в столбце упорядочение.</span><span class="sxs-lookup"><span data-stu-id="574d7-107">The installer starts each event in the order specified in the Ordering column.</span></span> <span data-ttu-id="574d7-108">Например, элемент управления "Кнопка отправки" может публиковать события для инициации перехода в другое диалоговое окно, выхода из последовательности диалоговых окон и начала установки файла.</span><span class="sxs-lookup"><span data-stu-id="574d7-108">For example, a push button control can publish events to initiate a transition to another dialog box, exit the dialog box sequence, and begin file installation.</span></span>

<span data-ttu-id="574d7-109">Это исключение следует отметить, чтобы каждый элемент управления мог опубликовать не более одного [невдиалог](newdialog-controlevent.md) или одного [спавндиалог](spawndialog-controlevent.md) события.</span><span class="sxs-lookup"><span data-stu-id="574d7-109">The exception to note is that each control can publish a most one [NewDialog](newdialog-controlevent.md) or one [SpawnDialog](spawndialog-controlevent.md) event.</span></span> <span data-ttu-id="574d7-110">Если необходимо создать несколько событий управления Невдиалог и Спавндиалог в этой таблице, также включите в поля условия условные операторы, которые гарантируют, что публикуется не более одного события.</span><span class="sxs-lookup"><span data-stu-id="574d7-110">If you need to author multiple NewDialog and SpawnDialog control events in this table, also include conditional statements in the Condition fields that ensure at most one event is published.</span></span> <span data-ttu-id="574d7-111">Если для одного и того же элемента управления выбрано несколько событий управления Невдиалог и Спавндиалог, то только событие с самым большим значением в столбце упорядочения публикуется при активации элемента управления.</span><span class="sxs-lookup"><span data-stu-id="574d7-111">If multiple NewDialog and SpawnDialog control events are selected for the same control, only the event with the largest value in the Ordering column gets published when the control is activated.</span></span>

<span data-ttu-id="574d7-112">Таблица таблице ControlEvent событие содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="574d7-112">The ControlEvent table has the following columns.</span></span>



| <span data-ttu-id="574d7-113">Столбец</span><span class="sxs-lookup"><span data-stu-id="574d7-113">Column</span></span>    | <span data-ttu-id="574d7-114">Type</span><span class="sxs-lookup"><span data-stu-id="574d7-114">Type</span></span>                         | <span data-ttu-id="574d7-115">Ключ</span><span class="sxs-lookup"><span data-stu-id="574d7-115">Key</span></span> | <span data-ttu-id="574d7-116">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="574d7-116">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="574d7-117">Диалог\_</span><span class="sxs-lookup"><span data-stu-id="574d7-117">Dialog\_</span></span>  | [<span data-ttu-id="574d7-118">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="574d7-118">Identifier</span></span>](identifier.md) | <span data-ttu-id="574d7-119">Да</span><span class="sxs-lookup"><span data-stu-id="574d7-119">Y</span></span>   | <span data-ttu-id="574d7-120">Нет</span><span class="sxs-lookup"><span data-stu-id="574d7-120">N</span></span>        |
| <span data-ttu-id="574d7-121">элементом управления\_</span><span class="sxs-lookup"><span data-stu-id="574d7-121">Control\_</span></span> | [<span data-ttu-id="574d7-122">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="574d7-122">Identifier</span></span>](identifier.md) | <span data-ttu-id="574d7-123">Да</span><span class="sxs-lookup"><span data-stu-id="574d7-123">Y</span></span>   | <span data-ttu-id="574d7-124">Нет</span><span class="sxs-lookup"><span data-stu-id="574d7-124">N</span></span>        |
| <span data-ttu-id="574d7-125">Событие</span><span class="sxs-lookup"><span data-stu-id="574d7-125">Event</span></span>     | [<span data-ttu-id="574d7-126">Формате</span><span class="sxs-lookup"><span data-stu-id="574d7-126">Formatted</span></span>](formatted.md)   | <span data-ttu-id="574d7-127">Да</span><span class="sxs-lookup"><span data-stu-id="574d7-127">Y</span></span>   | <span data-ttu-id="574d7-128">Нет</span><span class="sxs-lookup"><span data-stu-id="574d7-128">N</span></span>        |
| <span data-ttu-id="574d7-129">Аргумент</span><span class="sxs-lookup"><span data-stu-id="574d7-129">Argument</span></span>  | [<span data-ttu-id="574d7-130">Формате</span><span class="sxs-lookup"><span data-stu-id="574d7-130">Formatted</span></span>](formatted.md)   | <span data-ttu-id="574d7-131">Да</span><span class="sxs-lookup"><span data-stu-id="574d7-131">Y</span></span>   | <span data-ttu-id="574d7-132">Нет</span><span class="sxs-lookup"><span data-stu-id="574d7-132">N</span></span>        |
| <span data-ttu-id="574d7-133">Условие</span><span class="sxs-lookup"><span data-stu-id="574d7-133">Condition</span></span> | [<span data-ttu-id="574d7-134">Condition</span><span class="sxs-lookup"><span data-stu-id="574d7-134">Condition</span></span>](condition.md)   | <span data-ttu-id="574d7-135">Да</span><span class="sxs-lookup"><span data-stu-id="574d7-135">Y</span></span>   | <span data-ttu-id="574d7-136">Да</span><span class="sxs-lookup"><span data-stu-id="574d7-136">Y</span></span>        |
| <span data-ttu-id="574d7-137">Упорядочение</span><span class="sxs-lookup"><span data-stu-id="574d7-137">Ordering</span></span>  | [<span data-ttu-id="574d7-138">Integer</span><span class="sxs-lookup"><span data-stu-id="574d7-138">Integer</span></span>](integer.md)       | <span data-ttu-id="574d7-139">Нет</span><span class="sxs-lookup"><span data-stu-id="574d7-139">N</span></span>   | <span data-ttu-id="574d7-140">Да</span><span class="sxs-lookup"><span data-stu-id="574d7-140">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="574d7-141">Столбцы</span><span class="sxs-lookup"><span data-stu-id="574d7-141">Columns</span></span>

<dl> <dt>

<span data-ttu-id="574d7-142"><span id="Dialog_"></span><span id="dialog_"></span><span id="DIALOG_"></span>Откроется\_</span><span class="sxs-lookup"><span data-stu-id="574d7-142"><span id="Dialog_"></span><span id="dialog_"></span><span id="DIALOG_"></span>Dialog\_</span></span>
</dt> <dd>

<span data-ttu-id="574d7-143">Внешний ключ к первому столбцу [диалоговой таблицы](dialog-table.md).</span><span class="sxs-lookup"><span data-stu-id="574d7-143">An external key to the first column of the [Dialog table](dialog-table.md).</span></span> <span data-ttu-id="574d7-144">Объединение этого поля с полем элемента управления \_ определяет уникальный элемент управления.</span><span class="sxs-lookup"><span data-stu-id="574d7-144">Combining this field with the Control\_ field identifies a unique control.</span></span>

</dd> <dt>

<span data-ttu-id="574d7-145"><span id="Control_"></span><span id="control_"></span><span id="CONTROL_"></span>Элемента\_</span><span class="sxs-lookup"><span data-stu-id="574d7-145"><span id="Control_"></span><span id="control_"></span><span id="CONTROL_"></span>Control\_</span></span>
</dt> <dd>

<span data-ttu-id="574d7-146">Внешний ключ ко второму столбцу [управляющей таблицы](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="574d7-146">An external key to the second column of the [Control table](control-table.md).</span></span> <span data-ttu-id="574d7-147">Объединение этого поля с полем диалогового окна \_ определяет уникальный элемент управления.</span><span class="sxs-lookup"><span data-stu-id="574d7-147">Combining this field with the Dialog\_ field identifies a unique control.</span></span>

</dd> <dt>

<span data-ttu-id="574d7-148"><span id="Event"></span><span id="event"></span><span id="EVENT"></span>Журнале</span><span class="sxs-lookup"><span data-stu-id="574d7-148"><span id="Event"></span><span id="event"></span><span id="EVENT"></span>Event</span></span>
</dt> <dd>

<span data-ttu-id="574d7-149">Идентификатор, указывающий тип события, которое должно происходить, когда пользователь взаимодействует с элементом управления, указанным в диалоговом окне \_ и элементе управления \_ .</span><span class="sxs-lookup"><span data-stu-id="574d7-149">An identifier that specifies the type of event that should take place when the user interacts with the control specified by Dialog\_ and Control\_.</span></span> <span data-ttu-id="574d7-150">Список возможных значений см. в [обзоре таблице ControlEvent событие](controlevent-overview.md).</span><span class="sxs-lookup"><span data-stu-id="574d7-150">For a list of possible values see [ControlEvent Overview](controlevent-overview.md).</span></span>

<span data-ttu-id="574d7-151">Чтобы задать свойство с элементом управления, укажите \[ \_ \] в этом поле Имя свойства и новое значение в поле Argument.</span><span class="sxs-lookup"><span data-stu-id="574d7-151">To set a property with a control, put \[Property\_Name\] in this field and the new value in the argument field.</span></span> <span data-ttu-id="574d7-152">Вставьте {} в поле Argument, чтобы ввести значение null.</span><span class="sxs-lookup"><span data-stu-id="574d7-152">Put { } into the argument field to enter the null value.</span></span>

</dd> <dt>

<span data-ttu-id="574d7-153"><span id="Argument"></span><span id="argument"></span><span id="ARGUMENT"></span>Параметр</span><span class="sxs-lookup"><span data-stu-id="574d7-153"><span id="Argument"></span><span id="argument"></span><span id="ARGUMENT"></span>Argument</span></span>
</dt> <dd>

<span data-ttu-id="574d7-154">Значение, используемое в качестве модификатора при активации определенного события.</span><span class="sxs-lookup"><span data-stu-id="574d7-154">A value used as a modifier when triggering a particular event.</span></span>

<span data-ttu-id="574d7-155">Например, аргументом [Невдиалог таблице ControlEvent событие](newdialog-controlevent.md) или [спавндиалог таблице ControlEvent событие](spawndialog-controlevent.md) является имя диалогового окна, а аргумент [действия установки](install-action.md) — число, определяющее уровень установки.</span><span class="sxs-lookup"><span data-stu-id="574d7-155">For example, the argument of the [NewDialog ControlEvent](newdialog-controlevent.md) or the [SpawnDialog ControlEvent](spawndialog-controlevent.md) is the name of the dialog box and the argument of the [Install action](install-action.md) is a number defining the install level.</span></span>

</dd> <dt>

<span data-ttu-id="574d7-156"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Выполняет</span><span class="sxs-lookup"><span data-stu-id="574d7-156"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condition</span></span>
</dt> <dd>

<span data-ttu-id="574d7-157">Условный оператор, определяющий, активирует ли установщик событие в столбце событий.</span><span class="sxs-lookup"><span data-stu-id="574d7-157">A conditional statement that determines whether the installer activates the event in the Event column.</span></span> <span data-ttu-id="574d7-158">Установщик активирует событие, если условный оператор в поле Condition имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="574d7-158">The installer triggers the event if the conditional statement in the Condition field evaluates to True.</span></span> <span data-ttu-id="574d7-159">Поэтому установите значение 1 в этом столбце, чтобы установщик запустит событие.</span><span class="sxs-lookup"><span data-stu-id="574d7-159">Therefore put a 1 in this column to ensure that the installer triggers the event.</span></span> <span data-ttu-id="574d7-160">Установщик не запускает событие, если поле Condition содержит инструкцию, результатом которой является значение false.</span><span class="sxs-lookup"><span data-stu-id="574d7-160">The installer does not trigger the event if the Condition field contains a statement that evaluates to False.</span></span> <span data-ttu-id="574d7-161">Установщик не запускает событие с пустым в поле условие, если никакие другие события элемента управления не имеют значение true.</span><span class="sxs-lookup"><span data-stu-id="574d7-161">The installer does not trigger an event with a blank in the Condition field unless no other events of the control evaluate to True.</span></span> <span data-ttu-id="574d7-162">Если ни одно из полей условия для элемента управления, названного в \_ поле Control, не имеет значение true, то установщик запускает одно событие с пустым полем условия, а если больше одного поля условия, оно запускает одно событие с самым большим значением в поле упорядочения.</span><span class="sxs-lookup"><span data-stu-id="574d7-162">If none of the Condition fields for the control named in the Control\_ field evaluate to True, the installer triggers the one event having a blank Condition field, and if more than one Condition field is blank it triggers the one event of these with the largest value in the Ordering field.</span></span> <span data-ttu-id="574d7-163">См. раздел [Синтаксис условных инструкций](conditional-statement-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="574d7-163">See [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span>

</dd> <dt>

<span data-ttu-id="574d7-164"><span id="Ordering"></span><span id="ordering"></span><span id="ORDERING"></span>Упорядочение</span><span class="sxs-lookup"><span data-stu-id="574d7-164"><span id="Ordering"></span><span id="ordering"></span><span id="ORDERING"></span>Ordering</span></span>
</dt> <dd>

<span data-ttu-id="574d7-165">Целое число, используемое для упорядочивания нескольких событий, привязанных к одному элементу управления.</span><span class="sxs-lookup"><span data-stu-id="574d7-165">An integer used to order several events tied to the same control.</span></span> <span data-ttu-id="574d7-166">Это значение должно быть неотрицательным числом.</span><span class="sxs-lookup"><span data-stu-id="574d7-166">This must be a non-negative number.</span></span> <span data-ttu-id="574d7-167">Это поле можно оставить пустым.</span><span class="sxs-lookup"><span data-stu-id="574d7-167">This field may be left blank.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="574d7-168">Комментарии</span><span class="sxs-lookup"><span data-stu-id="574d7-168">Remarks</span></span>

<span data-ttu-id="574d7-169">В [таблице таблица eventmapping](eventmapping-table.md) перечислены элементы управления, которые подписываются на какое-либо событие управления и перечислены изменяемые атрибуты, когда это событие публикуется другим элементом управления или установщиком.</span><span class="sxs-lookup"><span data-stu-id="574d7-169">The [EventMapping table](eventmapping-table.md) lists the controls that subscribe to some control event and lists the control attribute to be changed when that event is published by the another control or the installer.</span></span>

<span data-ttu-id="574d7-170">В операционных системах Windows XP и более ранних версий пользователи могут публиковать события элемента управления только путем взаимодействия с [элементом управления CheckBox](checkbox-control.md) или [кнопками](pushbutton-control.md).</span><span class="sxs-lookup"><span data-stu-id="574d7-170">On Windows XP or earlier operating systems, users can publish a control event only by interacting with a [Checkbox Control](checkbox-control.md) or [Pushbutton Control](pushbutton-control.md).</span></span> <span data-ttu-id="574d7-171">В Windows Server 2003 пользователи могут публиковать события элемента управления только путем взаимодействия с [элементом управления CheckBox](checkbox-control.md), [Селектионтри Control](selectiontree-control.md)и [кнопками](pushbutton-control.md).</span><span class="sxs-lookup"><span data-stu-id="574d7-171">With Windows Server 2003, users can publish a control event only by interacting with a [Checkbox Control](checkbox-control.md), [SelectionTree Control](selectiontree-control.md), and [Pushbutton Control](pushbutton-control.md).</span></span> <span data-ttu-id="574d7-172">Перечисление других элементов управления в поле элемента управления \_ не оказывает никакого влияния.</span><span class="sxs-lookup"><span data-stu-id="574d7-172">Listing other controls in the Control\_ field has no effect.</span></span>

## <a name="validation"></a><span data-ttu-id="574d7-173">Проверка</span><span class="sxs-lookup"><span data-stu-id="574d7-173">Validation</span></span>

<dl>

[<span data-ttu-id="574d7-174">ICE03</span><span class="sxs-lookup"><span data-stu-id="574d7-174">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="574d7-175">ICE06</span><span class="sxs-lookup"><span data-stu-id="574d7-175">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="574d7-176">ICE17</span><span class="sxs-lookup"><span data-stu-id="574d7-176">ICE17</span></span>](ice17.md)  
[<span data-ttu-id="574d7-177">ICE20</span><span class="sxs-lookup"><span data-stu-id="574d7-177">ICE20</span></span>](ice20.md)  
[<span data-ttu-id="574d7-178">ICE32</span><span class="sxs-lookup"><span data-stu-id="574d7-178">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="574d7-179">ICE44</span><span class="sxs-lookup"><span data-stu-id="574d7-179">ICE44</span></span>](ice44.md)  
[<span data-ttu-id="574d7-180">ICE46</span><span class="sxs-lookup"><span data-stu-id="574d7-180">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="574d7-181">ICE79</span><span class="sxs-lookup"><span data-stu-id="574d7-181">ICE79</span></span>](ice79.md)  
[<span data-ttu-id="574d7-182">ICE86</span><span class="sxs-lookup"><span data-stu-id="574d7-182">ICE86</span></span>](ice86.md)  
</dl>

 

 



