---
description: Средство слияния оценивает таблицу Модулеинсталлексекутесекуенце, а затем вставляет вычисляемые действия в таблицу Инсталлексекутесекуенце с правильным порядковым номером.
ms.assetid: 6cd04d9a-5489-4fde-951e-aa962e9bd755
title: Таблица Модулеинсталлексекутесекуенце
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d294ddfdf06028bf18d518e1086d37a0719f8c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664545"
---
# <a name="moduleinstallexecutesequence-table"></a><span data-ttu-id="6a05b-103">Таблица Модулеинсталлексекутесекуенце</span><span class="sxs-lookup"><span data-stu-id="6a05b-103">ModuleInstallExecuteSequence Table</span></span>

<span data-ttu-id="6a05b-104">Средство слияния оценивает таблицу Модулеинсталлексекутесекуенце, а затем вставляет вычисляемые действия в [таблицу инсталлексекутесекуенце](installexecutesequence-table.md) с правильным порядковым номером.</span><span class="sxs-lookup"><span data-stu-id="6a05b-104">A merge tool evaluates the ModuleInstallExecuteSequence table and then inserts the calculated actions into the [InstallExecuteSequence table](installexecutesequence-table.md) with a correct sequence number.</span></span>

<span data-ttu-id="6a05b-105">Таблица Модулеинсталлексекутесекуенце содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="6a05b-105">The ModuleInstallExecuteSequence table contains the following columns.</span></span>



| <span data-ttu-id="6a05b-106">Столбец</span><span class="sxs-lookup"><span data-stu-id="6a05b-106">Column</span></span>     | <span data-ttu-id="6a05b-107">Type</span><span class="sxs-lookup"><span data-stu-id="6a05b-107">Type</span></span>                         | <span data-ttu-id="6a05b-108">Ключ</span><span class="sxs-lookup"><span data-stu-id="6a05b-108">Key</span></span> | <span data-ttu-id="6a05b-109">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="6a05b-109">Nullable</span></span> |
|------------|------------------------------|-----|----------|
| <span data-ttu-id="6a05b-110">Действие</span><span class="sxs-lookup"><span data-stu-id="6a05b-110">Action</span></span>     | [<span data-ttu-id="6a05b-111">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="6a05b-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="6a05b-112">Да</span><span class="sxs-lookup"><span data-stu-id="6a05b-112">Y</span></span>   | <span data-ttu-id="6a05b-113">Нет</span><span class="sxs-lookup"><span data-stu-id="6a05b-113">N</span></span>        |
| <span data-ttu-id="6a05b-114">Последовательность</span><span class="sxs-lookup"><span data-stu-id="6a05b-114">Sequence</span></span>   | [<span data-ttu-id="6a05b-115">Integer</span><span class="sxs-lookup"><span data-stu-id="6a05b-115">Integer</span></span>](integer.md)       |     | <span data-ttu-id="6a05b-116">Да</span><span class="sxs-lookup"><span data-stu-id="6a05b-116">Y</span></span>        |
| <span data-ttu-id="6a05b-117">басеактион</span><span class="sxs-lookup"><span data-stu-id="6a05b-117">BaseAction</span></span> | [<span data-ttu-id="6a05b-118">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="6a05b-118">Identifier</span></span>](identifier.md) |     | <span data-ttu-id="6a05b-119">Да</span><span class="sxs-lookup"><span data-stu-id="6a05b-119">Y</span></span>        |
| <span data-ttu-id="6a05b-120">После</span><span class="sxs-lookup"><span data-stu-id="6a05b-120">After</span></span>      | [<span data-ttu-id="6a05b-121">Integer</span><span class="sxs-lookup"><span data-stu-id="6a05b-121">Integer</span></span>](integer.md)       |     | <span data-ttu-id="6a05b-122">Да</span><span class="sxs-lookup"><span data-stu-id="6a05b-122">Y</span></span>        |
| <span data-ttu-id="6a05b-123">Условие</span><span class="sxs-lookup"><span data-stu-id="6a05b-123">Condition</span></span>  | [<span data-ttu-id="6a05b-124">Condition</span><span class="sxs-lookup"><span data-stu-id="6a05b-124">Condition</span></span>](condition.md)   |     | <span data-ttu-id="6a05b-125">Да</span><span class="sxs-lookup"><span data-stu-id="6a05b-125">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="6a05b-126">Столбцы</span><span class="sxs-lookup"><span data-stu-id="6a05b-126">Columns</span></span>

<dl> <dt>

<span data-ttu-id="6a05b-127"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Поддержки</span><span class="sxs-lookup"><span data-stu-id="6a05b-127"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span></span>
</dt> <dd>

<span data-ttu-id="6a05b-128">Действие для вставки в последовательность.</span><span class="sxs-lookup"><span data-stu-id="6a05b-128">Action to insert into sequence.</span></span> <span data-ttu-id="6a05b-129">Ссылается на одно из [стандартных действий](standard-actions.md)установщика или запись в [таблице CustomAction](customaction-table.md)модуля слияния или в [таблице диалоговых окон](dialog-table.md).</span><span class="sxs-lookup"><span data-stu-id="6a05b-129">Refers to one of the installer [standard actions](standard-actions.md), or an entry in the merge module's [CustomAction table](customaction-table.md), or [Dialog table](dialog-table.md).</span></span>

<span data-ttu-id="6a05b-130">Если в столбце Action таблицы последовательности модуля слияния используется [стандартное действие](standard-actions.md) , то столбцы Басеактион и After этой записи должны иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="6a05b-130">If a [standard action](standard-actions.md) is used in the Action column of a merge module sequence table, the BaseAction and After columns of that record must be null.</span></span>

</dd> <dt>

<span data-ttu-id="6a05b-131"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Виртуализирован</span><span class="sxs-lookup"><span data-stu-id="6a05b-131"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequence</span></span>
</dt> <dd>

<span data-ttu-id="6a05b-132">Порядковый номер стандартного действия.</span><span class="sxs-lookup"><span data-stu-id="6a05b-132">The sequence number of a standard action.</span></span> <span data-ttu-id="6a05b-133">Если пользовательское действие или диалоговое окно помещается в столбец Action этой строки, это поле должно иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="6a05b-133">If a custom action or dialog is entered into the Action column of this row, this field must be set to null.</span></span>

<span data-ttu-id="6a05b-134">При использовании [стандартных действий](standard-actions.md) в таблицах последовательности модулей слияния значением в столбце последовательности должен быть рекомендуемый порядковый номер действия.</span><span class="sxs-lookup"><span data-stu-id="6a05b-134">When using [standard actions](standard-actions.md) in merge module sequence tables, the value in the Sequence column should be the recommended action sequence number.</span></span> <span data-ttu-id="6a05b-135">Если порядковый номер в модуле слияния отличается от того же действия в таблице последовательности файлов. msi, то средство слияния использует порядковый номер из MSI файла.</span><span class="sxs-lookup"><span data-stu-id="6a05b-135">If the sequence number in the merge module differs from that for the same action in the .msi file sequence table, the merge tool uses the sequence number from the .msi file.</span></span> <span data-ttu-id="6a05b-136">Рекомендуемые порядковые номера стандартных действий см. в разделе [Использование таблицы последовательностей](using-a-sequence-table.md) в предлагаемых последовательностях.</span><span class="sxs-lookup"><span data-stu-id="6a05b-136">See the suggested sequences in [Using a Sequence Table](using-a-sequence-table.md) for the recommended sequence numbers of standard actions.</span></span>

</dd> <dt>

<span data-ttu-id="6a05b-137"><span id="BaseAction"></span><span id="baseaction"></span><span id="BASEACTION"></span>басеактион</span><span class="sxs-lookup"><span data-stu-id="6a05b-137"><span id="BaseAction"></span><span id="baseaction"></span><span id="BASEACTION"></span>BaseAction</span></span>
</dt> <dd>

<span data-ttu-id="6a05b-138">Столбец Басеактион может содержать стандартное действие, пользовательское действие, указанное в пользовательской таблице действий модуля слияния, или диалоговое окно, указанное в таблице диалогового окна модуля.</span><span class="sxs-lookup"><span data-stu-id="6a05b-138">The BaseAction column may contain a standard action, a custom action specified in the merge module's custom action table, or a dialog specified in the module's dialog table.</span></span> <span data-ttu-id="6a05b-139">Столбец Басеактион является ключом в столбце Action этой таблицы.</span><span class="sxs-lookup"><span data-stu-id="6a05b-139">The BaseAction column is a key into the Action column of this table.</span></span> <span data-ttu-id="6a05b-140">Он не может быть внешним ключом в другой таблице слияния или таблице в файле установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="6a05b-140">It cannot be a foreign key into another merge table or table in the Windows Installer file.</span></span> <span data-ttu-id="6a05b-141">Это означает, что каждое стандартное действие, настраиваемое действие или диалоговое окно, перечисленные в столбце Басеактион, также должны быть перечислены в столбце Action другой записи в этой таблице.</span><span class="sxs-lookup"><span data-stu-id="6a05b-141">This means that every standard action, custom action, or dialog listed in the BaseAction column must also be listed in the Action column of another record in this table.</span></span>

</dd> <dt>

<span data-ttu-id="6a05b-142"><span id="After"></span><span id="after"></span><span id="AFTER"></span>Запуска</span><span class="sxs-lookup"><span data-stu-id="6a05b-142"><span id="After"></span><span id="after"></span><span id="AFTER"></span>After</span></span>
</dt> <dd>

<span data-ttu-id="6a05b-143">Логическое значение, которое указывает, приходится ли действие до или после Басеактион.</span><span class="sxs-lookup"><span data-stu-id="6a05b-143">Boolean for whether Action comes before or after BaseAction.</span></span>



| <span data-ttu-id="6a05b-144">Значение</span><span class="sxs-lookup"><span data-stu-id="6a05b-144">Value</span></span> | <span data-ttu-id="6a05b-145">Значение</span><span class="sxs-lookup"><span data-stu-id="6a05b-145">Meaning</span></span>                          |
|-------|----------------------------------|
| <span data-ttu-id="6a05b-146">0</span><span class="sxs-lookup"><span data-stu-id="6a05b-146">0</span></span>     | <span data-ttu-id="6a05b-147">Действие, которое следует выполнить до Басеактион</span><span class="sxs-lookup"><span data-stu-id="6a05b-147">Action to come before BaseAction</span></span> |
| <span data-ttu-id="6a05b-148">1</span><span class="sxs-lookup"><span data-stu-id="6a05b-148">1</span></span>     | <span data-ttu-id="6a05b-149">Действие, которое будет получено после Басеактион</span><span class="sxs-lookup"><span data-stu-id="6a05b-149">Action to come after BaseAction</span></span>  |



 

</dd> <dt>

<span data-ttu-id="6a05b-150"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Выполняет</span><span class="sxs-lookup"><span data-stu-id="6a05b-150"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condition</span></span>
</dt> <dd>

<span data-ttu-id="6a05b-151">Условный оператор, указывающий, должно ли выполняться действие.</span><span class="sxs-lookup"><span data-stu-id="6a05b-151">A conditional statement that indicates if the action is to be executed.</span></span> <span data-ttu-id="6a05b-152">Значение NULL вычисляется как true.</span><span class="sxs-lookup"><span data-stu-id="6a05b-152">A null value evaluates to true.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6a05b-153">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6a05b-153">Remarks</span></span>

<span data-ttu-id="6a05b-154">Если [Таблица модулеинсталлексекутесекуенце](installexecutesequence-table.md) имеется, [Таблица инсталлексекутесекуенце](installexecutesequence-table.md) также должна присутствовать в модуле слияния.</span><span class="sxs-lookup"><span data-stu-id="6a05b-154">If the [ModuleInstallExecuteSequence table](installexecutesequence-table.md) is present, the [InstallExecuteSequence table](installexecutesequence-table.md) must also be present in the merge module.</span></span>

 

 



