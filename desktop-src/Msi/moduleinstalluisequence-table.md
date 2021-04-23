---
description: Средство слияния оценивает таблицу Модулеинсталлуисекуенце, а затем вставляет вычисляемые действия в таблицу Инсталлуисекуенце с правильным порядковым номером.
ms.assetid: a125aecc-57d9-4c8e-873e-d5315eaafa56
title: Таблица Модулеинсталлуисекуенце
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ca6771daa0b95acbc23e2d60eddda5420e417db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105650856"
---
# <a name="moduleinstalluisequence-table"></a><span data-ttu-id="59533-103">Таблица Модулеинсталлуисекуенце</span><span class="sxs-lookup"><span data-stu-id="59533-103">ModuleInstallUISequence Table</span></span>

<span data-ttu-id="59533-104">Средство слияния оценивает таблицу Модулеинсталлуисекуенце, а затем вставляет вычисляемые действия в [таблицу инсталлуисекуенце](installuisequence-table.md) с правильным порядковым номером.</span><span class="sxs-lookup"><span data-stu-id="59533-104">A merge tool evaluates the ModuleInstallUISequence table and then inserts the calculated actions into the [InstallUISequence table](installuisequence-table.md) with a correct sequence number.</span></span>

<span data-ttu-id="59533-105">Таблица Модулеинсталлуисекуенце содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="59533-105">The ModuleInstallUISequence table has the following columns.</span></span>



| <span data-ttu-id="59533-106">Столбец</span><span class="sxs-lookup"><span data-stu-id="59533-106">Column</span></span>     | <span data-ttu-id="59533-107">Type</span><span class="sxs-lookup"><span data-stu-id="59533-107">Type</span></span>                         | <span data-ttu-id="59533-108">Ключ</span><span class="sxs-lookup"><span data-stu-id="59533-108">Key</span></span> | <span data-ttu-id="59533-109">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="59533-109">Nullable</span></span> |
|------------|------------------------------|-----|----------|
| <span data-ttu-id="59533-110">Действие</span><span class="sxs-lookup"><span data-stu-id="59533-110">Action</span></span>     | [<span data-ttu-id="59533-111">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="59533-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="59533-112">Да</span><span class="sxs-lookup"><span data-stu-id="59533-112">Y</span></span>   | <span data-ttu-id="59533-113">Нет</span><span class="sxs-lookup"><span data-stu-id="59533-113">N</span></span>        |
| <span data-ttu-id="59533-114">Последовательность</span><span class="sxs-lookup"><span data-stu-id="59533-114">Sequence</span></span>   | [<span data-ttu-id="59533-115">Integer</span><span class="sxs-lookup"><span data-stu-id="59533-115">Integer</span></span>](integer.md)       |     | <span data-ttu-id="59533-116">Да</span><span class="sxs-lookup"><span data-stu-id="59533-116">Y</span></span>        |
| <span data-ttu-id="59533-117">басеактион</span><span class="sxs-lookup"><span data-stu-id="59533-117">BaseAction</span></span> | [<span data-ttu-id="59533-118">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="59533-118">Identifier</span></span>](identifier.md) |     | <span data-ttu-id="59533-119">Да</span><span class="sxs-lookup"><span data-stu-id="59533-119">Y</span></span>        |
| <span data-ttu-id="59533-120">После</span><span class="sxs-lookup"><span data-stu-id="59533-120">After</span></span>      | [<span data-ttu-id="59533-121">Integer</span><span class="sxs-lookup"><span data-stu-id="59533-121">Integer</span></span>](integer.md)       |     | <span data-ttu-id="59533-122">Да</span><span class="sxs-lookup"><span data-stu-id="59533-122">Y</span></span>        |
| <span data-ttu-id="59533-123">Условие</span><span class="sxs-lookup"><span data-stu-id="59533-123">Condition</span></span>  | [<span data-ttu-id="59533-124">Condition</span><span class="sxs-lookup"><span data-stu-id="59533-124">Condition</span></span>](condition.md)   |     | <span data-ttu-id="59533-125">Да</span><span class="sxs-lookup"><span data-stu-id="59533-125">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="59533-126">Столбцы</span><span class="sxs-lookup"><span data-stu-id="59533-126">Columns</span></span>

<dl> <dt>

<span data-ttu-id="59533-127"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Поддержки</span><span class="sxs-lookup"><span data-stu-id="59533-127"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span></span>
</dt> <dd>

<span data-ttu-id="59533-128">Действие для вставки в последовательность.</span><span class="sxs-lookup"><span data-stu-id="59533-128">Action to insert into sequence.</span></span> <span data-ttu-id="59533-129">Ссылается на одно из [стандартных действий](standard-actions.md)установщика или запись в [таблице CustomAction](customaction-table.md) модуля слияния или в [таблице диалоговых окон](dialog-table.md).</span><span class="sxs-lookup"><span data-stu-id="59533-129">Refers to one of the installer [standard actions](standard-actions.md), or an entry in the merge module's [CustomAction table](customaction-table.md) or [Dialog table](dialog-table.md).</span></span>

<span data-ttu-id="59533-130">Если в столбце Action таблицы последовательности модуля слияния используется [стандартное действие](standard-actions.md) , то столбцы Басеактион и After этой записи должны иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="59533-130">If a [standard action](standard-actions.md) is used in the Action column of a merge module sequence table, the BaseAction and After columns of that record must be Null.</span></span>

</dd> <dt>

<span data-ttu-id="59533-131"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Виртуализирован</span><span class="sxs-lookup"><span data-stu-id="59533-131"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequence</span></span>
</dt> <dd>

<span data-ttu-id="59533-132">Порядковый номер стандартного действия.</span><span class="sxs-lookup"><span data-stu-id="59533-132">The sequence number of a standard action.</span></span> <span data-ttu-id="59533-133">Если пользовательское действие или диалоговое окно помещается в столбец Action этой строки, это поле должно иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="59533-133">If a custom action or dialog is entered into the Action column of this row, this field must be set to Null.</span></span>

<span data-ttu-id="59533-134">При использовании [стандартных действий](standard-actions.md) в таблицах последовательности модулей слияния значением в столбце последовательности должен быть рекомендуемый порядковый номер действия.</span><span class="sxs-lookup"><span data-stu-id="59533-134">When using [standard actions](standard-actions.md) in merge module sequence tables, the value in the Sequence column should be the recommended action sequence number.</span></span> <span data-ttu-id="59533-135">Если порядковый номер в модуле слияния отличается от того же действия в таблице последовательности файлов. msi, то средство слияния использует порядковый номер из MSI файла.</span><span class="sxs-lookup"><span data-stu-id="59533-135">If the sequence number in the merge module differs from that for the same action in the .msi file sequence table, the merge tool uses the sequence number from the .msi file.</span></span> <span data-ttu-id="59533-136">Рекомендуемые порядковые номера стандартных действий см. в разделе [Использование таблицы последовательностей](using-a-sequence-table.md) в предлагаемых последовательностях.</span><span class="sxs-lookup"><span data-stu-id="59533-136">See the suggested sequences in [Using a Sequence Table](using-a-sequence-table.md) for the recommended sequence numbers of standard actions.</span></span>

</dd> <dt>

<span data-ttu-id="59533-137"><span id="BaseAction"></span><span id="baseaction"></span><span id="BASEACTION"></span>басеактион</span><span class="sxs-lookup"><span data-stu-id="59533-137"><span id="BaseAction"></span><span id="baseaction"></span><span id="BASEACTION"></span>BaseAction</span></span>
</dt> <dd>

<span data-ttu-id="59533-138">Столбец Басеактион может содержать стандартное действие, пользовательское действие, указанное в пользовательской таблице действий модуля слияния, или диалоговое окно, указанное в таблице диалогового окна модуля.</span><span class="sxs-lookup"><span data-stu-id="59533-138">The BaseAction column can contain a standard action, a custom action specified in the merge module's custom action table, or a dialog specified in the module's dialog table.</span></span> <span data-ttu-id="59533-139">Столбец Басеактион является ключом в столбце Action этой таблицы.</span><span class="sxs-lookup"><span data-stu-id="59533-139">The BaseAction column is a key into the Action column of this table.</span></span> <span data-ttu-id="59533-140">Он не может быть внешним ключом в другой таблице слияния или таблице в MSI-файле.</span><span class="sxs-lookup"><span data-stu-id="59533-140">It cannot be a foreign key into another merge table or table in the .msi file.</span></span> <span data-ttu-id="59533-141">Это означает, что каждое стандартное действие, настраиваемое действие или диалоговое окно, перечисленные в столбце Басеактион, также должны быть перечислены в столбце Action другой записи в этой таблице.</span><span class="sxs-lookup"><span data-stu-id="59533-141">This means that every standard action, custom action, or dialog listed in the BaseAction column must also be listed in the Action column of another record in this table.</span></span>

</dd> <dt>

<span data-ttu-id="59533-142"><span id="After"></span><span id="after"></span><span id="AFTER"></span>Запуска</span><span class="sxs-lookup"><span data-stu-id="59533-142"><span id="After"></span><span id="after"></span><span id="AFTER"></span>After</span></span>
</dt> <dd>

<span data-ttu-id="59533-143">Логическое значение, которое указывает, приходится ли действие до или после Басеактион.</span><span class="sxs-lookup"><span data-stu-id="59533-143">Boolean for whether Action comes before or after BaseAction.</span></span>



| <span data-ttu-id="59533-144">Значение</span><span class="sxs-lookup"><span data-stu-id="59533-144">Value</span></span> | <span data-ttu-id="59533-145">Значение</span><span class="sxs-lookup"><span data-stu-id="59533-145">Meaning</span></span>                          |
|-------|----------------------------------|
| <span data-ttu-id="59533-146">0</span><span class="sxs-lookup"><span data-stu-id="59533-146">0</span></span>     | <span data-ttu-id="59533-147">Действие, которое следует выполнить до Басеактион</span><span class="sxs-lookup"><span data-stu-id="59533-147">Action to come before BaseAction</span></span> |
| <span data-ttu-id="59533-148">1</span><span class="sxs-lookup"><span data-stu-id="59533-148">1</span></span>     | <span data-ttu-id="59533-149">Действие, которое будет получено после Басеактион</span><span class="sxs-lookup"><span data-stu-id="59533-149">Action to come after BaseAction</span></span>  |



 

</dd> <dt>

<span data-ttu-id="59533-150"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Выполняет</span><span class="sxs-lookup"><span data-stu-id="59533-150"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condition</span></span>
</dt> <dd>

<span data-ttu-id="59533-151">Условный оператор, указывающий, выполняется ли действие.</span><span class="sxs-lookup"><span data-stu-id="59533-151">A conditional statement that indicates if the action is be executed.</span></span> <span data-ttu-id="59533-152">Значение NULL вычисляется как true.</span><span class="sxs-lookup"><span data-stu-id="59533-152">Null evaluates to true.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="59533-153">Комментарии</span><span class="sxs-lookup"><span data-stu-id="59533-153">Remarks</span></span>

<span data-ttu-id="59533-154">Если эта таблица представлена, [Таблица инсталлуисекуенце](installuisequence-table.md) также должна присутствовать в модуле слияния.</span><span class="sxs-lookup"><span data-stu-id="59533-154">If this table is present the [InstallUISequence table](installuisequence-table.md) must also be present in the merge module.</span></span>

 

 



