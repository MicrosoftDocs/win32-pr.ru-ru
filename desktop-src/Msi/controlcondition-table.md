---
description: Таблица Таблица controlcondition позволяет автору указать специальные действия, применяемые к элементам управления в зависимости от результата условного оператора. Например, с помощью этой таблицы автор может скрыть элемент управления на основе свойства Версионнт.
ms.assetid: e36d20ec-cd7b-494f-b517-c07b40d2a338
title: Таблица Таблица controlcondition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 671dcdee6e2ed1067c51a04084693c276b8db2d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998917"
---
# <a name="controlcondition-table"></a><span data-ttu-id="0d16e-104">Таблица Таблица controlcondition</span><span class="sxs-lookup"><span data-stu-id="0d16e-104">ControlCondition Table</span></span>

<span data-ttu-id="0d16e-105">Таблица Таблица controlcondition позволяет автору указать специальные действия, применяемые к элементам управления в зависимости от результата условного оператора.</span><span class="sxs-lookup"><span data-stu-id="0d16e-105">The ControlCondition table enables an author to specify special actions to be applied to controls based on the result of a conditional statement.</span></span> <span data-ttu-id="0d16e-106">Например, с помощью этой таблицы автор может скрыть элемент управления на основе свойства [**версионнт**](versionnt.md) .</span><span class="sxs-lookup"><span data-stu-id="0d16e-106">For example, using this table the author could choose to hide a control based on the [**VersionNT**](versionnt.md) property.</span></span>

<span data-ttu-id="0d16e-107">Таблица Таблица controlcondition содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="0d16e-107">The ControlCondition table has the following columns.</span></span>



| <span data-ttu-id="0d16e-108">Столбец</span><span class="sxs-lookup"><span data-stu-id="0d16e-108">Column</span></span>    | <span data-ttu-id="0d16e-109">Type</span><span class="sxs-lookup"><span data-stu-id="0d16e-109">Type</span></span>                         | <span data-ttu-id="0d16e-110">Ключ</span><span class="sxs-lookup"><span data-stu-id="0d16e-110">Key</span></span> | <span data-ttu-id="0d16e-111">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="0d16e-111">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="0d16e-112">Диалог\_</span><span class="sxs-lookup"><span data-stu-id="0d16e-112">Dialog\_</span></span>  | [<span data-ttu-id="0d16e-113">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="0d16e-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="0d16e-114">Да</span><span class="sxs-lookup"><span data-stu-id="0d16e-114">Y</span></span>   | <span data-ttu-id="0d16e-115">Нет</span><span class="sxs-lookup"><span data-stu-id="0d16e-115">N</span></span>        |
| <span data-ttu-id="0d16e-116">элементом управления\_</span><span class="sxs-lookup"><span data-stu-id="0d16e-116">Control\_</span></span> | [<span data-ttu-id="0d16e-117">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="0d16e-117">Identifier</span></span>](identifier.md) | <span data-ttu-id="0d16e-118">Да</span><span class="sxs-lookup"><span data-stu-id="0d16e-118">Y</span></span>   | <span data-ttu-id="0d16e-119">Нет</span><span class="sxs-lookup"><span data-stu-id="0d16e-119">N</span></span>        |
| <span data-ttu-id="0d16e-120">Действие</span><span class="sxs-lookup"><span data-stu-id="0d16e-120">Action</span></span>    | [<span data-ttu-id="0d16e-121">Text</span><span class="sxs-lookup"><span data-stu-id="0d16e-121">Text</span></span>](text.md)             | <span data-ttu-id="0d16e-122">Да</span><span class="sxs-lookup"><span data-stu-id="0d16e-122">Y</span></span>   | <span data-ttu-id="0d16e-123">Нет</span><span class="sxs-lookup"><span data-stu-id="0d16e-123">N</span></span>        |
| <span data-ttu-id="0d16e-124">Условие</span><span class="sxs-lookup"><span data-stu-id="0d16e-124">Condition</span></span> | [<span data-ttu-id="0d16e-125">Condition</span><span class="sxs-lookup"><span data-stu-id="0d16e-125">Condition</span></span>](condition.md)   | <span data-ttu-id="0d16e-126">Да</span><span class="sxs-lookup"><span data-stu-id="0d16e-126">Y</span></span>   | <span data-ttu-id="0d16e-127">Нет</span><span class="sxs-lookup"><span data-stu-id="0d16e-127">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="0d16e-128">Столбцы</span><span class="sxs-lookup"><span data-stu-id="0d16e-128">Columns</span></span>

<dl> <dt>

<span data-ttu-id="0d16e-129"><span id="Dialog_"></span><span id="dialog_"></span><span id="DIALOG_"></span>Откроется\_</span><span class="sxs-lookup"><span data-stu-id="0d16e-129"><span id="Dialog_"></span><span id="dialog_"></span><span id="DIALOG_"></span>Dialog\_</span></span>
</dt> <dd>

<span data-ttu-id="0d16e-130">Внешний ключ к первому столбцу [диалоговой таблицы](dialog-table.md).</span><span class="sxs-lookup"><span data-stu-id="0d16e-130">An external key to the first column of the [Dialog table](dialog-table.md).</span></span> <span data-ttu-id="0d16e-131">Объединение этого поля с полем элемента управления \_ определяет уникальный элемент управления.</span><span class="sxs-lookup"><span data-stu-id="0d16e-131">Combining this field with the Control\_ field identifies a unique control.</span></span>

</dd> <dt>

<span data-ttu-id="0d16e-132"><span id="Control_"></span><span id="control_"></span><span id="CONTROL_"></span>Элемента\_</span><span class="sxs-lookup"><span data-stu-id="0d16e-132"><span id="Control_"></span><span id="control_"></span><span id="CONTROL_"></span>Control\_</span></span>
</dt> <dd>

<span data-ttu-id="0d16e-133">Внешний ключ ко второму столбцу [управляющей таблицы](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="0d16e-133">An external key to the second column of the [Control table](control-table.md).</span></span> <span data-ttu-id="0d16e-134">При объединении этого поля поле диалогового окна \_ определяет уникальный элемент управления.</span><span class="sxs-lookup"><span data-stu-id="0d16e-134">Combining this field the Dialog\_ field identifies a unique control.</span></span>

</dd> <dt>

<span data-ttu-id="0d16e-135"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Поддержки</span><span class="sxs-lookup"><span data-stu-id="0d16e-135"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span></span>
</dt> <dd>

<span data-ttu-id="0d16e-136">Действие, выполняемое над элементом управления.</span><span class="sxs-lookup"><span data-stu-id="0d16e-136">The action that is to be taken on the control.</span></span> <span data-ttu-id="0d16e-137">Возможные действия показаны в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="0d16e-137">The possible actions are shown in the following table.</span></span>



| <span data-ttu-id="0d16e-138">Значение</span><span class="sxs-lookup"><span data-stu-id="0d16e-138">Value</span></span>   | <span data-ttu-id="0d16e-139">Значение</span><span class="sxs-lookup"><span data-stu-id="0d16e-139">Meaning</span></span>                     |
|---------|-----------------------------|
| <span data-ttu-id="0d16e-140">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="0d16e-140">Default</span></span> | <span data-ttu-id="0d16e-141">Установите для элемента управления значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0d16e-141">Set control as the default.</span></span> |
| <span data-ttu-id="0d16e-142">Отключить</span><span class="sxs-lookup"><span data-stu-id="0d16e-142">Disable</span></span> | <span data-ttu-id="0d16e-143">Отключить элемент управления.</span><span class="sxs-lookup"><span data-stu-id="0d16e-143">Disable the control.</span></span>        |
| <span data-ttu-id="0d16e-144">Включить</span><span class="sxs-lookup"><span data-stu-id="0d16e-144">Enable</span></span>  | <span data-ttu-id="0d16e-145">Включение элемента управления.</span><span class="sxs-lookup"><span data-stu-id="0d16e-145">Enable the control.</span></span>         |
| <span data-ttu-id="0d16e-146">Скрыть</span><span class="sxs-lookup"><span data-stu-id="0d16e-146">Hide</span></span>    | <span data-ttu-id="0d16e-147">Скрыть элемент управления.</span><span class="sxs-lookup"><span data-stu-id="0d16e-147">Hide the control.</span></span>           |
| <span data-ttu-id="0d16e-148">Показать</span><span class="sxs-lookup"><span data-stu-id="0d16e-148">Show</span></span>    | <span data-ttu-id="0d16e-149">Отображение элемента управления.</span><span class="sxs-lookup"><span data-stu-id="0d16e-149">Display the control.</span></span>        |



 

</dd> <dt>

<span data-ttu-id="0d16e-150"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Выполняет</span><span class="sxs-lookup"><span data-stu-id="0d16e-150"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condition</span></span>
</dt> <dd>

<span data-ttu-id="0d16e-151">Условный оператор, указывающий, при каких условиях должно запускаться действие.</span><span class="sxs-lookup"><span data-stu-id="0d16e-151">A conditional statement that specifies under which conditions the action should be triggered.</span></span> <span data-ttu-id="0d16e-152">Этот столбец нельзя оставлять пустым.</span><span class="sxs-lookup"><span data-stu-id="0d16e-152">This column may not be left blank.</span></span> <span data-ttu-id="0d16e-153">Если эта инструкция не возвращает значение TRUE, действие не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0d16e-153">If this statement does not evaluate to TRUE, the action does not take place.</span></span> <span data-ttu-id="0d16e-154">Если задано значение 1, действие применяется всегда.</span><span class="sxs-lookup"><span data-stu-id="0d16e-154">If it is set to 1, the action is always applied.</span></span> <span data-ttu-id="0d16e-155">Дополнительные сведения о синтаксисе условных операторов см. в разделе [Синтаксис условных](conditional-statement-syntax.md)инструкций.</span><span class="sxs-lookup"><span data-stu-id="0d16e-155">For information on the syntax of conditional statements, see [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0d16e-156">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0d16e-156">Remarks</span></span>

<span data-ttu-id="0d16e-157">Если требуется скрыть и отключить [элемент управления "кнопка](pushbutton-control.md) " или ["флажок"](checkbox-control.md) на основе условного оператора в поле Условие таблицы таблица controlcondition, следует использовать четыре записи для каждого элемента управления, чтобы отключить его, а также скрыть элемент управления.</span><span class="sxs-lookup"><span data-stu-id="0d16e-157">If you want to hide and disable a [PushButton control](pushbutton-control.md) or [CheckBox control](checkbox-control.md) based on a conditional statement in the Condition field of the ControlCondition table, you should use four records for each control to disable as well as hide the control.</span></span> <span data-ttu-id="0d16e-158">Элементы управления "Кнопка" или "флажок", которые были скрыты, по-прежнему могут быть доступны с помощью сочетаний клавиш.</span><span class="sxs-lookup"><span data-stu-id="0d16e-158">PushButton or CheckBox controls that have only been hidden can still be accessed by shortcut keys.</span></span>

<span data-ttu-id="0d16e-159">Например, следующие записи скрывают и отключают элемент управления в диалоговом окне а при установке продукта.</span><span class="sxs-lookup"><span data-stu-id="0d16e-159">For example, the following records hide and disable ControlA on DialogA when the product is installed.</span></span> <span data-ttu-id="0d16e-160">Элемент управления будет видимым и включенным, если продукт не установлен.</span><span class="sxs-lookup"><span data-stu-id="0d16e-160">The control will be visible and enabled when the product is not installed.</span></span>



| <span data-ttu-id="0d16e-161">Диалог</span><span class="sxs-lookup"><span data-stu-id="0d16e-161">Dialog</span></span>  | <span data-ttu-id="0d16e-162">Control</span><span class="sxs-lookup"><span data-stu-id="0d16e-162">Control</span></span>  | <span data-ttu-id="0d16e-163">Действие</span><span class="sxs-lookup"><span data-stu-id="0d16e-163">Action</span></span>  | <span data-ttu-id="0d16e-164">Условие</span><span class="sxs-lookup"><span data-stu-id="0d16e-164">Condition</span></span>                      |
|---------|----------|---------|--------------------------------|
| <span data-ttu-id="0d16e-165">Диалоговое окно</span><span class="sxs-lookup"><span data-stu-id="0d16e-165">DialogA</span></span> | <span data-ttu-id="0d16e-166">Элемент управления</span><span class="sxs-lookup"><span data-stu-id="0d16e-166">ControlA</span></span> | <span data-ttu-id="0d16e-167">Скрыть</span><span class="sxs-lookup"><span data-stu-id="0d16e-167">Hide</span></span>    | [<span data-ttu-id="0d16e-168">**Установлено**</span><span class="sxs-lookup"><span data-stu-id="0d16e-168">**Installed**</span></span>](installed.md) |
| <span data-ttu-id="0d16e-169">Диалоговое окно</span><span class="sxs-lookup"><span data-stu-id="0d16e-169">DialogA</span></span> | <span data-ttu-id="0d16e-170">Элемент управления</span><span class="sxs-lookup"><span data-stu-id="0d16e-170">ControlA</span></span> | <span data-ttu-id="0d16e-171">Отключить</span><span class="sxs-lookup"><span data-stu-id="0d16e-171">Disable</span></span> | <span data-ttu-id="0d16e-172">Установлено</span><span class="sxs-lookup"><span data-stu-id="0d16e-172">Installed</span></span>                      |
| <span data-ttu-id="0d16e-173">Диалоговое окно</span><span class="sxs-lookup"><span data-stu-id="0d16e-173">DialogA</span></span> | <span data-ttu-id="0d16e-174">Элемент управления</span><span class="sxs-lookup"><span data-stu-id="0d16e-174">ControlA</span></span> | <span data-ttu-id="0d16e-175">Показать</span><span class="sxs-lookup"><span data-stu-id="0d16e-175">Show</span></span>    | <span data-ttu-id="0d16e-176">НЕ установлено</span><span class="sxs-lookup"><span data-stu-id="0d16e-176">NOT Installed</span></span>                  |
| <span data-ttu-id="0d16e-177">Диалоговое окно</span><span class="sxs-lookup"><span data-stu-id="0d16e-177">DialogA</span></span> | <span data-ttu-id="0d16e-178">Элемент управления</span><span class="sxs-lookup"><span data-stu-id="0d16e-178">ControlA</span></span> | <span data-ttu-id="0d16e-179">Включить</span><span class="sxs-lookup"><span data-stu-id="0d16e-179">Enable</span></span>  | <span data-ttu-id="0d16e-180">НЕ установлено</span><span class="sxs-lookup"><span data-stu-id="0d16e-180">NOT Installed</span></span>                  |



 

## <a name="validation"></a><span data-ttu-id="0d16e-181">Проверка</span><span class="sxs-lookup"><span data-stu-id="0d16e-181">Validation</span></span>

<dl>

[<span data-ttu-id="0d16e-182">ICE03</span><span class="sxs-lookup"><span data-stu-id="0d16e-182">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="0d16e-183">ICE06</span><span class="sxs-lookup"><span data-stu-id="0d16e-183">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="0d16e-184">ICE17</span><span class="sxs-lookup"><span data-stu-id="0d16e-184">ICE17</span></span>](ice17.md)  
[<span data-ttu-id="0d16e-185">ICE32</span><span class="sxs-lookup"><span data-stu-id="0d16e-185">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="0d16e-186">ICE46</span><span class="sxs-lookup"><span data-stu-id="0d16e-186">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="0d16e-187">ICE79</span><span class="sxs-lookup"><span data-stu-id="0d16e-187">ICE79</span></span>](ice79.md)  
[<span data-ttu-id="0d16e-188">ICE86</span><span class="sxs-lookup"><span data-stu-id="0d16e-188">ICE86</span></span>](ice86.md)  
</dl>

 

 



