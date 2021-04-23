---
description: Средство слияния оценивает таблицу Модулеадминуисекуенце, а затем вставляет вычисляемые действия в таблицу Админуисекуенце с правильным порядковым номером.
ms.assetid: c71477e7-22bc-420a-9902-39bbf98b4ee5
title: Таблица Модулеадминуисекуенце
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e128aebd6481c077827f4d1ba2b487eafe6132d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105651108"
---
# <a name="moduleadminuisequence-table"></a><span data-ttu-id="c0875-103">Таблица Модулеадминуисекуенце</span><span class="sxs-lookup"><span data-stu-id="c0875-103">ModuleAdminUISequence Table</span></span>

<span data-ttu-id="c0875-104">Средство слияния оценивает таблицу Модулеадминуисекуенце, а затем вставляет вычисляемые действия в [таблицу админуисекуенце](adminuisequence-table.md) с правильным порядковым номером.</span><span class="sxs-lookup"><span data-stu-id="c0875-104">A merge tool evaluates the ModuleAdminUISequence table and then inserts the calculated actions into the [AdminUISequence table](adminuisequence-table.md) with a correct sequence number.</span></span>

<span data-ttu-id="c0875-105">Таблица Модулеадминуисекуенце содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="c0875-105">The ModuleAdminUISequence table has the following columns.</span></span>



| <span data-ttu-id="c0875-106">Столбец</span><span class="sxs-lookup"><span data-stu-id="c0875-106">Column</span></span>     | <span data-ttu-id="c0875-107">Type</span><span class="sxs-lookup"><span data-stu-id="c0875-107">Type</span></span>                         | <span data-ttu-id="c0875-108">Ключ</span><span class="sxs-lookup"><span data-stu-id="c0875-108">Key</span></span> | <span data-ttu-id="c0875-109">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="c0875-109">Nullable</span></span> |
|------------|------------------------------|-----|----------|
| <span data-ttu-id="c0875-110">Действие</span><span class="sxs-lookup"><span data-stu-id="c0875-110">Action</span></span>     | [<span data-ttu-id="c0875-111">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="c0875-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="c0875-112">Да</span><span class="sxs-lookup"><span data-stu-id="c0875-112">Y</span></span>   | <span data-ttu-id="c0875-113">Нет</span><span class="sxs-lookup"><span data-stu-id="c0875-113">N</span></span>        |
| <span data-ttu-id="c0875-114">Последовательность</span><span class="sxs-lookup"><span data-stu-id="c0875-114">Sequence</span></span>   | [<span data-ttu-id="c0875-115">Integer</span><span class="sxs-lookup"><span data-stu-id="c0875-115">Integer</span></span>](integer.md)       |     | <span data-ttu-id="c0875-116">Да</span><span class="sxs-lookup"><span data-stu-id="c0875-116">Y</span></span>        |
| <span data-ttu-id="c0875-117">басеактион</span><span class="sxs-lookup"><span data-stu-id="c0875-117">BaseAction</span></span> | [<span data-ttu-id="c0875-118">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="c0875-118">Identifier</span></span>](identifier.md) |     | <span data-ttu-id="c0875-119">Да</span><span class="sxs-lookup"><span data-stu-id="c0875-119">Y</span></span>        |
| <span data-ttu-id="c0875-120">После</span><span class="sxs-lookup"><span data-stu-id="c0875-120">After</span></span>      | [<span data-ttu-id="c0875-121">Integer</span><span class="sxs-lookup"><span data-stu-id="c0875-121">Integer</span></span>](integer.md)       |     | <span data-ttu-id="c0875-122">Да</span><span class="sxs-lookup"><span data-stu-id="c0875-122">Y</span></span>        |
| <span data-ttu-id="c0875-123">Условие</span><span class="sxs-lookup"><span data-stu-id="c0875-123">Condition</span></span>  | [<span data-ttu-id="c0875-124">Condition</span><span class="sxs-lookup"><span data-stu-id="c0875-124">Condition</span></span>](condition.md)   |     | <span data-ttu-id="c0875-125">Да</span><span class="sxs-lookup"><span data-stu-id="c0875-125">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="c0875-126">Столбцы</span><span class="sxs-lookup"><span data-stu-id="c0875-126">Columns</span></span>

<dl> <dt>

<span data-ttu-id="c0875-127"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Поддержки</span><span class="sxs-lookup"><span data-stu-id="c0875-127"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span></span>
</dt> <dd>

<span data-ttu-id="c0875-128">Действие для вставки в последовательность.</span><span class="sxs-lookup"><span data-stu-id="c0875-128">Action to insert into sequence.</span></span> <span data-ttu-id="c0875-129">Ссылается на одно из [стандартных действий](standard-actions.md)установщика или запись в [таблице CustomAction](customaction-table.md) модуля слияния или в [таблице диалоговых окон](dialog-table.md).</span><span class="sxs-lookup"><span data-stu-id="c0875-129">Refers to one of the installer [standard actions](standard-actions.md), or an entry in the merge module's [CustomAction table](customaction-table.md) or [Dialog table](dialog-table.md).</span></span>

<span data-ttu-id="c0875-130">Если в столбце Action таблицы последовательности модуля слияния используется [стандартное действие](standard-actions.md) , то столбцы Басеактион и After этой записи должны иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="c0875-130">If a [standard action](standard-actions.md) is used in the Action column of a merge module sequence table, the BaseAction and After columns of that record must be Null.</span></span>

</dd> <dt>

<span data-ttu-id="c0875-131"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Виртуализирован</span><span class="sxs-lookup"><span data-stu-id="c0875-131"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequence</span></span>
</dt> <dd>

<span data-ttu-id="c0875-132">Порядковый номер стандартного действия.</span><span class="sxs-lookup"><span data-stu-id="c0875-132">The sequence number of a standard action.</span></span> <span data-ttu-id="c0875-133">Если пользовательское действие или диалоговое окно помещается в столбец Action этой строки, это поле должно иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="c0875-133">If a custom action or dialog is entered into the Action column of this row, this field must be set to Null.</span></span>

<span data-ttu-id="c0875-134">При использовании [стандартных действий](standard-actions.md) в таблицах последовательности модулей слияния значением в столбце последовательности должен быть рекомендуемый порядковый номер действия.</span><span class="sxs-lookup"><span data-stu-id="c0875-134">When using [standard actions](standard-actions.md) in merge module sequence tables, the value in the Sequence column should be the recommended action sequence number.</span></span> <span data-ttu-id="c0875-135">Если порядковый номер в модуле слияния отличается от того же действия в таблице последовательности файлов. msi, то средство слияния использует порядковый номер из MSI файла.</span><span class="sxs-lookup"><span data-stu-id="c0875-135">If the sequence number in the merge module differs from that for the same action in the .msi file sequence table, the merge tool uses the sequence number from the .msi file.</span></span> <span data-ttu-id="c0875-136">Рекомендуемые порядковые номера стандартных действий см. в разделе [Использование таблицы последовательностей](using-a-sequence-table.md) в предлагаемых последовательностях.</span><span class="sxs-lookup"><span data-stu-id="c0875-136">See the suggested sequences in [Using a Sequence Table](using-a-sequence-table.md) for the recommended sequence numbers of standard actions.</span></span>

</dd> <dt>

<span data-ttu-id="c0875-137"><span id="BaseAction"></span><span id="baseaction"></span><span id="BASEACTION"></span>басеактион</span><span class="sxs-lookup"><span data-stu-id="c0875-137"><span id="BaseAction"></span><span id="baseaction"></span><span id="BASEACTION"></span>BaseAction</span></span>
</dt> <dd>

<span data-ttu-id="c0875-138">Столбец Басеактион может содержать стандартное действие, пользовательское действие, указанное в пользовательской таблице действий модуля слияния, или диалоговое окно, указанное в таблице диалогового окна модуля.</span><span class="sxs-lookup"><span data-stu-id="c0875-138">The BaseAction column can contain a standard action, a custom action specified in the merge module's custom action table, or a dialog specified in the module's dialog table.</span></span> <span data-ttu-id="c0875-139">Столбец Басеактион является ключом в столбце Action этой таблицы.</span><span class="sxs-lookup"><span data-stu-id="c0875-139">The BaseAction column is a key into the Action column of this table.</span></span> <span data-ttu-id="c0875-140">Он не может быть внешним ключом в другой таблице слияния или таблице в MSI-файле.</span><span class="sxs-lookup"><span data-stu-id="c0875-140">It cannot be a foreign key into another merge table or table in the .msi file.</span></span> <span data-ttu-id="c0875-141">Это означает, что каждое стандартное действие, настраиваемое действие или диалоговое окно, перечисленные в столбце Басеактион, также должны быть перечислены в столбце Action другой записи в этой таблице.</span><span class="sxs-lookup"><span data-stu-id="c0875-141">This means that every standard action, custom action, or dialog listed in the BaseAction column must also be listed in the Action column of another record in this table.</span></span>

</dd> <dt>

<span data-ttu-id="c0875-142"><span id="After"></span><span id="after"></span><span id="AFTER"></span>Запуска</span><span class="sxs-lookup"><span data-stu-id="c0875-142"><span id="After"></span><span id="after"></span><span id="AFTER"></span>After</span></span>
</dt> <dd>

<span data-ttu-id="c0875-143">Логическое значение, которое указывает, приходится ли действие до или после Басеактион.</span><span class="sxs-lookup"><span data-stu-id="c0875-143">Boolean for whether Action comes before or after BaseAction.</span></span>



| <span data-ttu-id="c0875-144">Значение</span><span class="sxs-lookup"><span data-stu-id="c0875-144">Value</span></span> | <span data-ttu-id="c0875-145">Значение</span><span class="sxs-lookup"><span data-stu-id="c0875-145">Meaning</span></span>                          |
|-------|----------------------------------|
| <span data-ttu-id="c0875-146">0</span><span class="sxs-lookup"><span data-stu-id="c0875-146">0</span></span>     | <span data-ttu-id="c0875-147">Действие, которое следует выполнить до Басеактион</span><span class="sxs-lookup"><span data-stu-id="c0875-147">Action to come before BaseAction</span></span> |
| <span data-ttu-id="c0875-148">1</span><span class="sxs-lookup"><span data-stu-id="c0875-148">1</span></span>     | <span data-ttu-id="c0875-149">Действие, которое будет получено после Басеактион</span><span class="sxs-lookup"><span data-stu-id="c0875-149">Action to come after BaseAction</span></span>  |



 

</dd> <dt>

<span data-ttu-id="c0875-150"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Выполняет</span><span class="sxs-lookup"><span data-stu-id="c0875-150"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condition</span></span>
</dt> <dd>

<span data-ttu-id="c0875-151">Условный оператор, указывающий, выполняется ли действие.</span><span class="sxs-lookup"><span data-stu-id="c0875-151">A conditional statement that indicates if the action is be executed.</span></span> <span data-ttu-id="c0875-152">Значение NULL вычисляется как true.</span><span class="sxs-lookup"><span data-stu-id="c0875-152">Null evaluates to true.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c0875-153">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c0875-153">Remarks</span></span>

<dl> <dt>

<span data-ttu-id="c0875-154"><span id="If_this_table_is_present_the__AdminUISequence_Table_must_also_be_present_in_the_merge_module."></span><span id="if_this_table_is_present_the__adminuisequence_table_must_also_be_present_in_the_merge_module."></span><span id="IF_THIS_TABLE_IS_PRESENT_THE__ADMINUISEQUENCE_TABLE_MUST_ALSO_BE_PRESENT_IN_THE_MERGE_MODULE."></span>Если эта таблица представлена, [Таблица админуисекуенце](adminuisequence-table.md) также должна присутствовать в модуле слияния.</span><span class="sxs-lookup"><span data-stu-id="c0875-154"><span id="If_this_table_is_present_the__AdminUISequence_Table_must_also_be_present_in_the_merge_module."></span><span id="if_this_table_is_present_the__adminuisequence_table_must_also_be_present_in_the_merge_module."></span><span id="IF_THIS_TABLE_IS_PRESENT_THE__ADMINUISEQUENCE_TABLE_MUST_ALSO_BE_PRESENT_IN_THE_MERGE_MODULE."></span>If this table is present the [AdminUISequence Table](adminuisequence-table.md) must also be present in the merge module.</span></span>
<span data-ttu-id="c0875-155"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="c0875-155"></dt> <dd></dd> </dl></span></span>

 

 



