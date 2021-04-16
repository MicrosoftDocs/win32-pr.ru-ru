---
description: Дополнительные сведения о функции JetCreateTableColumnIndex4W
title: Функция JetCreateTableColumnIndex4W
TOCTitle: JetCreateTableColumnIndex4W Function
ms:assetid: 5a74b397-dfb4-4a1d-807b-284329239bc3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835042(v=EXCHG.10)
ms:contentKeyID: 49894664
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetCreateTableColumnIndex4W
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 26ebdb8cf62123febe2d44b5a638c285c180062c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105713071"
---
# <a name="jetcreatetablecolumnindex4w-function"></a><span data-ttu-id="0e98d-103">Функция JetCreateTableColumnIndex4W</span><span class="sxs-lookup"><span data-stu-id="0e98d-103">JetCreateTableColumnIndex4W Function</span></span>


<span data-ttu-id="0e98d-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="0e98d-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="0e98d-105">Функция **JetCreateTableColumnIndex4W** создает таблицу в расширяемой подсистеме хранилища (ESE (база данных с начальным набором индексов и начальным набором столбцов из массива структур [JET_TABLECREATE3](./jet-tablecreate3-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="0e98d-105">The **JetCreateTableColumnIndex4W** function creates a table in an Extensible Storage Engine (ESE( database with an initial set of indexes and an initial set of columns from an array of [JET_TABLECREATE3](./jet-tablecreate3-structure.md) structures.</span></span> <span data-ttu-id="0e98d-106">Структура [JET_TABLECREATE3](./jet-tablecreate3-structure.md) позволяет указать функцию обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="0e98d-106">The [JET_TABLECREATE3](./jet-tablecreate3-structure.md) structure allows a callback function to be specified.</span></span>

<span data-ttu-id="0e98d-107">Функция **JetCreateTableColumnIndex4W** была введена в операционной системе Windows 8.</span><span class="sxs-lookup"><span data-stu-id="0e98d-107">The **JetCreateTableColumnIndex4W** function was introduced in the Windows 8 operating system.</span></span>

``` c++
JET_ERR JET_API JetCreateTableColumnIndex4W(
  __in          JET_SESID sesid,
  __in          JET_DBID dbid,
  __in_out      JET_TABLECREATE3* ptablecreate
);
```

### <a name="parameters"></a><span data-ttu-id="0e98d-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="0e98d-108">Parameters</span></span>

<span data-ttu-id="0e98d-109">*сесид*</span><span class="sxs-lookup"><span data-stu-id="0e98d-109">*sesid*</span></span>

<span data-ttu-id="0e98d-110">Контекст сеанса базы данных, используемый для вызова API.</span><span class="sxs-lookup"><span data-stu-id="0e98d-110">The database session context to use for the API call.</span></span>

<span data-ttu-id="0e98d-111">*DBID*</span><span class="sxs-lookup"><span data-stu-id="0e98d-111">*dbid*</span></span>

<span data-ttu-id="0e98d-112">Идентификатор базы данных, используемый для вызова API.</span><span class="sxs-lookup"><span data-stu-id="0e98d-112">The database identifier to use for the API call.</span></span>

<span data-ttu-id="0e98d-113">*птаблекреате*</span><span class="sxs-lookup"><span data-stu-id="0e98d-113">*ptablecreate*</span></span>

<span data-ttu-id="0e98d-114">Указатель на структуру [JET_TABLECREATE3](./jet-tablecreate3-structure.md) , определяющую создаваемую таблицу.</span><span class="sxs-lookup"><span data-stu-id="0e98d-114">A pointer to a [JET_TABLECREATE3](./jet-tablecreate3-structure.md) structure that defines the table to be created.</span></span> <span data-ttu-id="0e98d-115">Дополнительные сведения см. в разделе [JET_TABLECREATE3](./jet-tablecreate3-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="0e98d-115">See [JET_TABLECREATE3](./jet-tablecreate3-structure.md) for more details.</span></span>

### <a name="return-value"></a><span data-ttu-id="0e98d-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0e98d-116">Return value</span></span>

<span data-ttu-id="0e98d-117">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из кодов возврата, перечисленных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="0e98d-117">This function returns the [JET_ERR](./jet-err.md) datatype with one of the return codes listed in the following table.</span></span> <span data-ttu-id="0e98d-118">Дополнительные сведения о возможных ошибках расширенного хранилища Енгинже (ESE) см. в разделе [ошибки расширенного подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="0e98d-118">For more information about the possible Extensible Storage Enginge (ESE) errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0e98d-119">Код возврата</span><span class="sxs-lookup"><span data-stu-id="0e98d-119">Return code</span></span></p></th>
<th><p><span data-ttu-id="0e98d-120">Описание</span><span class="sxs-lookup"><span data-stu-id="0e98d-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0e98d-121">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="0e98d-121">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="0e98d-122">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="0e98d-122">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e98d-123">JET_errCallbackNotResolved</span><span class="sxs-lookup"><span data-stu-id="0e98d-123">JET_errCallbackNotResolved</span></span></p></td>
<td><p><span data-ttu-id="0e98d-124">Не удалось разрешить функцию обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="0e98d-124">The callback function could not be resolved.</span></span> <span data-ttu-id="0e98d-125">Возможно, Библиотека DLL не найдена или не найдена функция в библиотеке DLL.</span><span class="sxs-lookup"><span data-stu-id="0e98d-125">The DLL might not have been found, or the function in the DLL might not have been found.</span></span> <span data-ttu-id="0e98d-126">Если ведение журнала включено, в журнале событий будут представлены дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="0e98d-126">With sufficient logging enabled, the event log will provide more details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0e98d-127">JET_errCannotIndex</span><span class="sxs-lookup"><span data-stu-id="0e98d-127">JET_errCannotIndex</span></span></p></td>
<td><p><span data-ttu-id="0e98d-128">Предпринята попытка индексирования по столбцу с использованием типа "условно-Update" или "SLV" (Обратите внимание, что столбцы SLV устарели).</span><span class="sxs-lookup"><span data-stu-id="0e98d-128">An attempt was made to index over an escrow-update or SLV column (note that SLV columns are deprecated).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e98d-129">JET_errCannotNestDDL</span><span class="sxs-lookup"><span data-stu-id="0e98d-129">JET_errCannotNestDDL</span></span></p></td>
<td><p><span data-ttu-id="0e98d-130">Возвращается, если параметр <em>птаблекреате- &gt; грбит</em> задает JET_bitTableCreateTemplateTable значение, но параметр <em>птаблекреате- &gt; сзтемплатетабленаме</em> имеет значение null.</span><span class="sxs-lookup"><span data-stu-id="0e98d-130">Returned if the <em>ptablecreate-&gt;grbit</em> parameter specifies the JET_bitTableCreateTemplateTable value, but the <em>ptablecreate-&gt;szTemplateTableName</em> parameter is set to null.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0e98d-131">JET_errColumnDuplicate</span><span class="sxs-lookup"><span data-stu-id="0e98d-131">JET_errColumnDuplicate</span></span></p></td>
<td><p><span data-ttu-id="0e98d-132">Столбец уже существует.</span><span class="sxs-lookup"><span data-stu-id="0e98d-132">A column already exists.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e98d-133">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="0e98d-133">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="0e98d-134">Предпринята попытка индексировать несуществующий столбец.</span><span class="sxs-lookup"><span data-stu-id="0e98d-134">An attempt was made to index over a nonexistent column.</span></span> <span data-ttu-id="0e98d-135">Эта ошибка также может возникнуть при попытке условного индексирования по несуществующему столбцу.</span><span class="sxs-lookup"><span data-stu-id="0e98d-135">An attempt to conditionally index over a nonexistent column can also produce this error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0e98d-136">JET_errColumnRedundant</span><span class="sxs-lookup"><span data-stu-id="0e98d-136">JET_errColumnRedundant</span></span></p></td>
<td><p><span data-ttu-id="0e98d-137">Была предпринята попытка добавить избыточный столбец.</span><span class="sxs-lookup"><span data-stu-id="0e98d-137">An attempt was made to add a redundant column.</span></span> <span data-ttu-id="0e98d-138">Должно существовать не более одного столбца автоинкремента, и для каждой таблицы должно существовать не более одного столбца версии.</span><span class="sxs-lookup"><span data-stu-id="0e98d-138">No more than one autoincrement column should exist, and no more than one version column should exist per table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e98d-139">JET_errDensityInvalid</span><span class="sxs-lookup"><span data-stu-id="0e98d-139">JET_errDensityInvalid</span></span></p></td>
<td><p><span data-ttu-id="0e98d-140">Эта ошибка будет возвращена, если элементу <strong>улденсити</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> присвоено число меньше 20 или больше 100.</span><span class="sxs-lookup"><span data-stu-id="0e98d-140">This error will be returned if the <strong>ulDensity</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is set to a number less than 20 or more than 100.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0e98d-141">JET_errDDLNotInheritable</span><span class="sxs-lookup"><span data-stu-id="0e98d-141">JET_errDDLNotInheritable</span></span></p></td>
<td><p><span data-ttu-id="0e98d-142">Означает, что таблица, указанная в элементе <strong>сзтемплатетабленаме</strong> структуры <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a> , не была помечена как таблица шаблона (т. е. в таблице не установлено значение параметра JET_bitTableCreateTemplateTable).</span><span class="sxs-lookup"><span data-stu-id="0e98d-142">Signifies that the table named in the <strong>szTemplateTableName</strong> member of the <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a> structure was not marked as a template table (that is, that table did not have the JET_bitTableCreateTemplateTable parameter value set).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e98d-143">JET_errIndexDuplicate</span><span class="sxs-lookup"><span data-stu-id="0e98d-143">JET_errIndexDuplicate</span></span></p></td>
<td><p><span data-ttu-id="0e98d-144">Была выполнена попытка определить два одинаковых индекса.</span><span class="sxs-lookup"><span data-stu-id="0e98d-144">An attempt to define two identical indexes was made.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0e98d-145">JET_errIndexHasPrimary</span><span class="sxs-lookup"><span data-stu-id="0e98d-145">JET_errIndexHasPrimary</span></span></p></td>
<td><p><span data-ttu-id="0e98d-146">Предпринята попытка указать более одного первичного индекса для таблицы.</span><span class="sxs-lookup"><span data-stu-id="0e98d-146">An attempt was made to specify more than one primary index for a table.</span></span> <span data-ttu-id="0e98d-147">У таблицы должен быть ровно один первичный индекс.</span><span class="sxs-lookup"><span data-stu-id="0e98d-147">A table must have exactly one primary index.</span></span> <span data-ttu-id="0e98d-148">Если первичный индекс не указан, ядро СУБД будет прозрачно создавать его.</span><span class="sxs-lookup"><span data-stu-id="0e98d-148">If no primary index is specified, the database engine will transparently create one.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e98d-149">JET_errIndexInvalidDef</span><span class="sxs-lookup"><span data-stu-id="0e98d-149">JET_errIndexInvalidDef</span></span></p></td>
<td><p><span data-ttu-id="0e98d-150">Указано недопустимое определение индекса.</span><span class="sxs-lookup"><span data-stu-id="0e98d-150">An invalid index definition was specified.</span></span> <span data-ttu-id="0e98d-151">Ниже приведены некоторые возможные причины этой ошибки.</span><span class="sxs-lookup"><span data-stu-id="0e98d-151">The following are some of the possible reasons for this error:</span></span></p>
<ul>
<li><p><span data-ttu-id="0e98d-152">Первичный индекс является условным (то есть элемент <strong>грбит</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> имеет набор значений JET_bitIndexPrimary, а элемент <strong>ккондитионалколумн</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> больше нуля).</span><span class="sxs-lookup"><span data-stu-id="0e98d-152">A primary index is conditional (that is, the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure has the JET_bitIndexPrimary value set, and the <strong>cConditionalColumn</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is greater than zero).</span></span></p></li>
<li><p><span data-ttu-id="0e98d-153">Применимо к версиям операционной системы Windows Server, начиная с Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="0e98d-153">Applies to versions of the Windows Server operating system starting with Windows Server 2003.</span></span> <span data-ttu-id="0e98d-154">Попытка создать индекс кортежа с ограничениями кортежей, но без передачи элемента <strong>птуплелимитс</strong> в структуре <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> (то есть элемент <strong>грбит</strong> структуры <strong>JET_INDEXCREATE2</strong> имеет JET_bitIndexTupleLimits набор значений, но указатель <strong>птуплелимитс</strong> имеет значение null).</span><span class="sxs-lookup"><span data-stu-id="0e98d-154">An attempt to create a tuple index with tuple limits, but without passing the <strong>ptuplelimits</strong> member in the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure (that is, the <strong>grbit</strong> member of the <strong>JET_INDEXCREATE2</strong> structure has JET_bitIndexTupleLimits value set, but the <strong>ptuplelimits</strong> pointer is null).</span></span></p></li>
<li><p><span data-ttu-id="0e98d-155">Передача недопустимого определения ключа в элемент <strong>сзкэй</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> .</span><span class="sxs-lookup"><span data-stu-id="0e98d-155">Passing in an invalid key definition in the <strong>szKey</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure.</span></span> <span data-ttu-id="0e98d-156">Сведения о допустимых определениях см. в разделе <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>.</span><span class="sxs-lookup"><span data-stu-id="0e98d-156">For information about valid definitions, see <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>.</span></span></p></li>
<li><p><span data-ttu-id="0e98d-157">Задание для элемента <strong>кбварсегмак</strong> в <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> значение больше значения JET_cbPrimaryKeyMost (для первичного индекса) или больше значения JET_cbSecondaryKeyMost (для вторичного индекса).</span><span class="sxs-lookup"><span data-stu-id="0e98d-157">Setting the <strong>cbVarSegMac</strong> member in <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> to be greater than the JET_cbPrimaryKeyMost value (for a primary index) or greater than the JET_cbSecondaryKeyMost value (for a secondary index).</span></span></p></li>
<li><p><span data-ttu-id="0e98d-158">Передача недопустимого сочетания для определяемого пользователем индекса в Юникоде (один из которых имеет бит JET_bitIndexUnicode значение, установленный в элементе <strong>грбит</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ).</span><span class="sxs-lookup"><span data-stu-id="0e98d-158">Passing an invalid combination for a user-defined Unicode index (one that has the JET_bitIndexUnicode value bit set in the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure).</span></span> <span data-ttu-id="0e98d-159">Некоторые распространенные причины: элемент <strong>пидксуникоде</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> имеет значение null, или код LCID, указанный в структуре <strong>пидксуникоде</strong> , является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="0e98d-159">Some common causes include the <strong>pidxunicode</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is null, or the LCID specified in the <strong>pidxunicode</strong> structure is invalid.</span></span></p></li>
<li><p><span data-ttu-id="0e98d-160">Указание многозначного столбца для первичного индекса.</span><span class="sxs-lookup"><span data-stu-id="0e98d-160">Specifying a multivalued column for a primary index.</span></span></p></li>
<li><p><span data-ttu-id="0e98d-161">Попытка индексировать слишком много условных столбцов.</span><span class="sxs-lookup"><span data-stu-id="0e98d-161">Trying to index too many conditional columns.</span></span> <span data-ttu-id="0e98d-162">Элемент <strong>ккондитионалколумн</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> не должен быть больше <strong>JET_ccolKeyMost</strong>.</span><span class="sxs-lookup"><span data-stu-id="0e98d-162">The <strong>cConditionalColumn</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure must not be greater than <strong>JET_ccolKeyMost</strong>.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0e98d-163">JET_errIndexTuplesInvalidLimits</span><span class="sxs-lookup"><span data-stu-id="0e98d-163">JET_errIndexTuplesInvalidLimits</span></span></p></td>
<td><p><span data-ttu-id="0e98d-164">Применимо к версиям Windows, начиная с Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0e98d-164">Applies to versions of Windows starting with Windows XP.</span></span> <span data-ttu-id="0e98d-165">Указана структура <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> , а ее ограничения не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="0e98d-165">A <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure was specified, and its limits are not supported.</span></span> <span data-ttu-id="0e98d-166">Дополнительные сведения см. в разделе "Примечания" структуры <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> .</span><span class="sxs-lookup"><span data-stu-id="0e98d-166">For more information, see the remarks section of the <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e98d-167">JET_errIndexTuplesNonUniqueOnly</span><span class="sxs-lookup"><span data-stu-id="0e98d-167">JET_errIndexTuplesNonUniqueOnly</span></span></p></td>
<td><p><span data-ttu-id="0e98d-168">Применимо к версиям Windows, начиная с Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0e98d-168">Applies to versions of Windows starting with Windows XP.</span></span> <span data-ttu-id="0e98d-169">Индекс кортежа не может быть уникальным (т. е. элемент <em>грбит</em> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> не должен иметь одновременно JET_bitIndexPrimary и JET_bitIndexUnique значений).</span><span class="sxs-lookup"><span data-stu-id="0e98d-169">A tuple index cannot be unique (that is, the <em>grbit</em> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure must not have both JET_bitIndexPrimary and JET_bitIndexUnique values set).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0e98d-170">JET_errIndexTuplesOneColumnOnly</span><span class="sxs-lookup"><span data-stu-id="0e98d-170">JET_errIndexTuplesOneColumnOnly</span></span></p></td>
<td><p><span data-ttu-id="0e98d-171">Применимо к версиям Windows, начиная с Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0e98d-171">Applies to versions of Windows starting with Windows XP.</span></span> <span data-ttu-id="0e98d-172">Индекс кортежа может находиться только в одном столбце (т. е. Если элемент <strong>грбит</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> имеет JET_bitIndexTuples набор значений, а элемент <strong>сзкэй</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> указывает более одного столбца).</span><span class="sxs-lookup"><span data-stu-id="0e98d-172">A tuple index can only be over a single column (that is, if the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure has JET_bitIndexTuples value set, and the <strong>szKey</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure specifies more than one column).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e98d-173">JET_errIndexTuplesSecondaryIndexOnly</span><span class="sxs-lookup"><span data-stu-id="0e98d-173">JET_errIndexTuplesSecondaryIndexOnly</span></span></p></td>
<td><p><span data-ttu-id="0e98d-174">Применимо к версиям Windows, начиная с Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0e98d-174">Applies to versions of Windows starting with Windows XP.</span></span> <span data-ttu-id="0e98d-175">Индекс кортежа не может быть первичным индексом (т. е. элемент <strong>грбит</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> не должен иметь одновременно JET_bitIndexPrimary и JET_bitIndexTuples).</span><span class="sxs-lookup"><span data-stu-id="0e98d-175">A tuple index cannot be a primary index (that is, the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure must not have both JET_bitIndexPrimary and JET_bitIndexTuples set).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0e98d-176">JET_errIndexTuplesTextColumnsOnly</span><span class="sxs-lookup"><span data-stu-id="0e98d-176">JET_errIndexTuplesTextColumnsOnly</span></span></p></td>
<td><p><span data-ttu-id="0e98d-177">Применимо к версиям Windows, начиная с Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0e98d-177">Applies to versions of Windows starting with Windows XP.</span></span> <span data-ttu-id="0e98d-178">Индекс кортежа может находиться только в тексте или столбце Юникода.</span><span class="sxs-lookup"><span data-stu-id="0e98d-178">A tuple index can only be on a text or Unicode column.</span></span> <span data-ttu-id="0e98d-179">Попытка индексировать другие столбцы (например, двоичные столбцы) приведет к появлению JET_errIndexTuplesTextColumnsOnly кода ответа.</span><span class="sxs-lookup"><span data-stu-id="0e98d-179">An attempt to index other columns (such as binary columns) will result in a JET_errIndexTuplesTextColumnsOnly response code.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e98d-180">JET_errIndexTuplesVarSegMacNotAllowed</span><span class="sxs-lookup"><span data-stu-id="0e98d-180">JET_errIndexTuplesVarSegMacNotAllowed</span></span></p></td>
<td><p><span data-ttu-id="0e98d-181">Применимо к версиям Windows, начиная с Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0e98d-181">Applies to versions of Windows starting with Windows XP.</span></span> <span data-ttu-id="0e98d-182">Индекс кортежа не позволяет установить элемент <strong>кбварсегмак</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> .</span><span class="sxs-lookup"><span data-stu-id="0e98d-182">A tuple index does not allow the <strong>cbVarSegMac</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure to be set.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0e98d-183">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="0e98d-183">JET_errInTransaction</span></span></p></td>
<td><p><span data-ttu-id="0e98d-184">Предпринята попытка создать индекс без сведений о версии во время транзакции.</span><span class="sxs-lookup"><span data-stu-id="0e98d-184">An attempt was made to create an index without version information while in a transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e98d-185">JET_errInvalidCodePage</span><span class="sxs-lookup"><span data-stu-id="0e98d-185">JET_errInvalidCodePage</span></span></p></td>
<td><p><span data-ttu-id="0e98d-186">Элементу <strong>CP</strong> структуры <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> не задана допустимая кодовая страница.</span><span class="sxs-lookup"><span data-stu-id="0e98d-186">The <strong>cp</strong> member of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structure was not set to a valid code page.</span></span> <span data-ttu-id="0e98d-187">Единственными допустимыми значениями для текстовых столбцов являются английский (1252) и Unicode (1200).</span><span class="sxs-lookup"><span data-stu-id="0e98d-187">The only valid values for text columns are English (1252) and Unicode (1200).</span></span> <span data-ttu-id="0e98d-188">Значение 0 означает, что будет использоваться по умолчанию (английский, 1252).</span><span class="sxs-lookup"><span data-stu-id="0e98d-188">A value of 0 means the default will be used (English, 1252).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0e98d-189">JET_errInvalidColumnType</span><span class="sxs-lookup"><span data-stu-id="0e98d-189">JET_errInvalidColumnType</span></span></p></td>
<td><p><span data-ttu-id="0e98d-190">Элементу <strong>колтип</strong> структуры <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> не был задан допустимый тип столбца.</span><span class="sxs-lookup"><span data-stu-id="0e98d-190">The <strong>coltyp</strong> member of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structure was not set to a valid column type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e98d-191">JET_errInvalidCreateIndex</span><span class="sxs-lookup"><span data-stu-id="0e98d-191">JET_errInvalidCreateIndex</span></span></p></td>
<td><p><span data-ttu-id="0e98d-192">Ниже приведены некоторые причины, по которым может возникнуть Эта ошибка:</span><span class="sxs-lookup"><span data-stu-id="0e98d-192">The following are some reasons why this error may occur:</span></span></p>
<ul>
<li><p><span data-ttu-id="0e98d-193">Элементу <strong>ргиндекскреате</strong> структуры <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> присвоено значение null.</span><span class="sxs-lookup"><span data-stu-id="0e98d-193">The <strong>rgindexcreate</strong> member of the <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure was set to null.</span></span></p></li>
<li><p><span data-ttu-id="0e98d-194">Элементу <strong>ргколумнкреате</strong> структуры <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> присвоено значение null.</span><span class="sxs-lookup"><span data-stu-id="0e98d-194">The <strong>rgcolumncreate</strong> member of the <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure was set to null.</span></span></p></li>
<li><p><span data-ttu-id="0e98d-195">Элементу <strong>кбструкт</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> не было присвоено допустимое значение.</span><span class="sxs-lookup"><span data-stu-id="0e98d-195">The <strong>cbStruct</strong> member of a <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure was not set to a valid value.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0e98d-196">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="0e98d-196">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="0e98d-197">В структуре <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a> было указано недопустимое сочетание элементов <strong>грбит</strong> .</span><span class="sxs-lookup"><span data-stu-id="0e98d-197">An invalid combination of <strong>grbit</strong> members was specified in the <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a> structure.</span></span></p>
<p><span data-ttu-id="0e98d-198">Определение индекса недопустимо, так как элемент <strong>грбит</strong> содержит неправильные значения.</span><span class="sxs-lookup"><span data-stu-id="0e98d-198">The index definition is invalid because the <strong>grbit</strong> member contains inconsistent values.</span></span> <span data-ttu-id="0e98d-199">Ниже приведены некоторые возможные причины.</span><span class="sxs-lookup"><span data-stu-id="0e98d-199">The following are some possible reasons:</span></span></p>
<ul>
<li><p><span data-ttu-id="0e98d-200">Для первичного индекса задан бит игнорирования (то есть JET_bitIndexPrimary значение было передано вместе со значениями JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull или JET_bitIndexIgnoreFirstNull).</span><span class="sxs-lookup"><span data-stu-id="0e98d-200">A primary index had an ignore bit specified (that is, JET_bitIndexPrimary value was passed with the JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull, or JET_bitIndexIgnoreFirstNull values).</span></span></p></li>
<li><p><span data-ttu-id="0e98d-201">Пустой индекс не игнорирует все элементы NULL (т. е. элемент <strong>грбит</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> имеет значение JET_bitIndexEmpty, но не имеет набора значений JET_bitIndexIgnoreAnyNull).</span><span class="sxs-lookup"><span data-stu-id="0e98d-201">An empty index does not ignore any null members (that is, the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure has the JET_bitIndexEmpty value set, but does not have JET_bitIndexIgnoreAnyNull value set).</span></span></p></li>
<li><p><span data-ttu-id="0e98d-202">Передача структуры <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> с недопустимым элементом <strong>грбит</strong> .</span><span class="sxs-lookup"><span data-stu-id="0e98d-202">Passing in a <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> structure with an invalid <strong>grbit</strong> member.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e98d-203">JET_errInvalidLanguageId</span><span class="sxs-lookup"><span data-stu-id="0e98d-203">JET_errInvalidLanguageId</span></span></p></td>
<td><p><span data-ttu-id="0e98d-204">Передан недопустимый код локали (LCID) (либо с помощью элемента <strong>LCID</strong> структуры <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> , на который указывает элемент <strong>пидксуникоде</strong> в структуре <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> , либо через поле <strong>LCID</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ).</span><span class="sxs-lookup"><span data-stu-id="0e98d-204">An invalid Locale ID (LCID) was passed in (either through the <strong>lcid</strong> member of the <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> structure that the <strong>pidxunicode</strong> member in the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure points to, or through the <strong>lcid</strong> field of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0e98d-205">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="0e98d-205">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="0e98d-206">Указан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="0e98d-206">An invalid parameter was given.</span></span> <span data-ttu-id="0e98d-207">Ниже приведены некоторые возможные причины.</span><span class="sxs-lookup"><span data-stu-id="0e98d-207">The following are some possible reasons:</span></span></p>
<ul>
<li><p><span data-ttu-id="0e98d-208">Элемент <strong>ргколумнкреате</strong> структуры <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a> имеет значение null.</span><span class="sxs-lookup"><span data-stu-id="0e98d-208">The <strong>rgcolumncreate</strong> member of the <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a> structure is null.</span></span></p></li>
<li><p><span data-ttu-id="0e98d-209">Элемент <strong>кбструкт</strong> одной из структур <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> , указанных в элементе <strong>ргколумнкреате</strong> структуры <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> , не был задан как sizeof (JET_COLUMNCREATE).</span><span class="sxs-lookup"><span data-stu-id="0e98d-209">The <strong>cbStruct</strong> member of one of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structures given in the <strong>rgcolumncreate</strong> member of the <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure was not set to sizeof( JET_COLUMNCREATE ).</span></span></p></li>
<li><p><span data-ttu-id="0e98d-210">Элемент <strong>cbKey</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> имеет значение 0.</span><span class="sxs-lookup"><span data-stu-id="0e98d-210">The <strong>cbKey</strong> member of a <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is set to zero.</span></span></p></li>
<li><p><span data-ttu-id="0e98d-211">Элементу <strong>кбструкт</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> не присвоено значение sizeof (JET_INDEXCREATE2).</span><span class="sxs-lookup"><span data-stu-id="0e98d-211">The <strong>cbStruct</strong> member of a <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is not set to sizeof( JET_INDEXCREATE2 ).</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e98d-212">JET_errRecordTooBig</span><span class="sxs-lookup"><span data-stu-id="0e98d-212">JET_errRecordTooBig</span></span></p></td>
<td><p><span data-ttu-id="0e98d-213">Запись слишком велика.</span><span class="sxs-lookup"><span data-stu-id="0e98d-213">The record is too big.</span></span> <span data-ttu-id="0e98d-214">Сумма элемента <strong>кбмакс</strong> структуры <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> для всех фиксированных столбцов не должна превышать определенное значение.</span><span class="sxs-lookup"><span data-stu-id="0e98d-214">The sum of the <strong>cbMax</strong> member of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structure for all fixed columns must not exceed a certain value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0e98d-215">JET_errTableDuplicate</span><span class="sxs-lookup"><span data-stu-id="0e98d-215">JET_errTableDuplicate</span></span></p></td>
<td><p><span data-ttu-id="0e98d-216">Таблица уже существует.</span><span class="sxs-lookup"><span data-stu-id="0e98d-216">The table already exists.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e98d-217">JET_errTooManyColumns</span><span class="sxs-lookup"><span data-stu-id="0e98d-217">JET_errTooManyColumns</span></span></p></td>
<td><p><span data-ttu-id="0e98d-218">Предпринята попытка добавить в таблицу слишком много столбцов.</span><span class="sxs-lookup"><span data-stu-id="0e98d-218">An attempt was made to add too many columns to the table.</span></span> <span data-ttu-id="0e98d-219">Таблица может содержать не более <strong>JET_ccolFixedMost</strong> фиксированных столбцов, не более <strong>JET_ccolVarMost</strong> столбцов переменной длины и не более <strong>JET_ccolTaggedMost</strong> столбцов с тегами.</span><span class="sxs-lookup"><span data-stu-id="0e98d-219">A table can have no more than <strong>JET_ccolFixedMost</strong> fixed columns, no more than <strong>JET_ccolVarMost</strong> variable-length columns, and no more than <strong>JET_ccolTaggedMost</strong> tagged columns.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0e98d-220">JET_errUnicodeTranslationFail</span><span class="sxs-lookup"><span data-stu-id="0e98d-220">JET_errUnicodeTranslationFail</span></span></p></td>
<td><p><span data-ttu-id="0e98d-221">Произошла ошибка при попытке нормализовать столбец в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="0e98d-221">An error occurred when an attempt was made to normalize a Unicode column.</span></span> <span data-ttu-id="0e98d-222">Это может быть вызвано недостатком системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0e98d-222">This can be caused by running out of system resources.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e98d-223">JET_errSpaceHintsInvalid</span><span class="sxs-lookup"><span data-stu-id="0e98d-223">JET_errSpaceHintsInvalid</span></span></p></td>
<td><p><span data-ttu-id="0e98d-224">Неверное или неправильное действие элемента структуры подсказок пространства JET.</span><span class="sxs-lookup"><span data-stu-id="0e98d-224">An element of the JET space hints structure was not correct or actionable.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="0e98d-225">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0e98d-225">Remarks</span></span>

<span data-ttu-id="0e98d-226">Функция **JetCreateTableColumnIndex4W** создает таблицу с начальным набором столбцов и индексов.</span><span class="sxs-lookup"><span data-stu-id="0e98d-226">The **JetCreateTableColumnIndex4W** function creates a table with an initial set of columns and indexes.</span></span> <span data-ttu-id="0e98d-227">Дополнительные столбцы и индексы можно добавлять и удалять динамически с помощью функций [жетаддколумн](./jetaddcolumn-function.md), [жетделетеколумн](./jetdeletecolumn-function.md), [JetDeleteColumn2](./jetdeletecolumn2-function.md), [жеткреатеиндекс](./jetcreateindex-function.md), [JetCreateIndex2](./jetcreateindex2-function.md), [JetCreateIndex3](./jetcreateindex3-function.md), [JetCreateIndex4W](./jetcreateindex4w-function.md)и [жетделетеиндекс](./jetdeleteindex-function.md) .</span><span class="sxs-lookup"><span data-stu-id="0e98d-227">Additional columns and indexes can be added and removed dynamically by means of the [JetAddColumn](./jetaddcolumn-function.md), [JetDeleteColumn](./jetdeletecolumn-function.md), [JetDeleteColumn2](./jetdeletecolumn2-function.md), [JetCreateIndex](./jetcreateindex-function.md), [JetCreateIndex2](./jetcreateindex2-function.md), [JetCreateIndex3](./jetcreateindex3-function.md), [JetCreateIndex4W](./jetcreateindex4w-function.md), and [JetDeleteIndex](./jetdeleteindex-function.md) functions.</span></span>

<span data-ttu-id="0e98d-228">Как и в случае с функцией [жетопентабле](./jetopentable-function.md) , когда приложение выполняется с использованием возвращенного *TableID*, функция [жетклосетабле](./jetclosetable-function.md) должна закрыть приложение.</span><span class="sxs-lookup"><span data-stu-id="0e98d-228">As with the [JetOpenTable](./jetopentable-function.md) function, when the application is done using the returned *tableid*, the [JetCloseTable](./jetclosetable-function.md) function should close the application.</span></span>

#### <a name="requirements"></a><span data-ttu-id="0e98d-229">Требования</span><span class="sxs-lookup"><span data-stu-id="0e98d-229">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0e98d-230"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="0e98d-230"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="0e98d-231">Требуется Windows 8.</span><span class="sxs-lookup"><span data-stu-id="0e98d-231">Requires Windows 8.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e98d-232"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="0e98d-232"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="0e98d-233">Требуется Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="0e98d-233">Requires Windows Server 2012.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0e98d-234"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="0e98d-234"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="0e98d-235">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="0e98d-235">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e98d-236"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="0e98d-236"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="0e98d-237">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="0e98d-237">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0e98d-238"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="0e98d-238"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="0e98d-239">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="0e98d-239">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="0e98d-240">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0e98d-240">See also</span></span>

[<span data-ttu-id="0e98d-241">JET_CBTYP</span><span class="sxs-lookup"><span data-stu-id="0e98d-241">JET_CBTYP</span></span>](./jet-cbtyp.md)  
[<span data-ttu-id="0e98d-242">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="0e98d-242">JET_DBID</span></span>](./jet-dbid.md)  
[<span data-ttu-id="0e98d-243">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="0e98d-243">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="0e98d-244">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="0e98d-244">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="0e98d-245">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="0e98d-245">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)  
[<span data-ttu-id="0e98d-246">JET_INDEXCREATE2</span><span class="sxs-lookup"><span data-stu-id="0e98d-246">JET_INDEXCREATE2</span></span>](./jet-indexcreate2-structure.md)  
[<span data-ttu-id="0e98d-247">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="0e98d-247">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="0e98d-248">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="0e98d-248">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="0e98d-249">JET_TABLECREATE2</span><span class="sxs-lookup"><span data-stu-id="0e98d-249">JET_TABLECREATE2</span></span>](./jet-tablecreate2-structure.md)  
[<span data-ttu-id="0e98d-250">JET_TABLECREATE3</span><span class="sxs-lookup"><span data-stu-id="0e98d-250">JET_TABLECREATE3</span></span>](./jet-tablecreate3-structure.md)  
[<span data-ttu-id="0e98d-251">JET_TUPLELIMITS</span><span class="sxs-lookup"><span data-stu-id="0e98d-251">JET_TUPLELIMITS</span></span>](./jet-tuplelimits-structure.md)  
[<span data-ttu-id="0e98d-252">жетаддколумн</span><span class="sxs-lookup"><span data-stu-id="0e98d-252">JetAddColumn</span></span>](./jetaddcolumn-function.md)  
[<span data-ttu-id="0e98d-253">жеткреатеиндекс</span><span class="sxs-lookup"><span data-stu-id="0e98d-253">JetCreateIndex</span></span>](./jetcreateindex-function.md)  
[<span data-ttu-id="0e98d-254">JetCreateIndex2</span><span class="sxs-lookup"><span data-stu-id="0e98d-254">JetCreateIndex2</span></span>](./jetcreateindex2-function.md)  
[<span data-ttu-id="0e98d-255">JetCreateIndex3</span><span class="sxs-lookup"><span data-stu-id="0e98d-255">JetCreateIndex3</span></span>](./jetcreateindex3-function.md)  
[<span data-ttu-id="0e98d-256">жеткреатетабле</span><span class="sxs-lookup"><span data-stu-id="0e98d-256">JetCreateTable</span></span>](./jetcreatetable-function.md)  
[<span data-ttu-id="0e98d-257">жеткреатетаблеколумниндекс</span><span class="sxs-lookup"><span data-stu-id="0e98d-257">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="0e98d-258">жетделетеколумн</span><span class="sxs-lookup"><span data-stu-id="0e98d-258">JetDeleteColumn</span></span>](./jetdeletecolumn-function.md)  
[<span data-ttu-id="0e98d-259">JetDeleteColumn2</span><span class="sxs-lookup"><span data-stu-id="0e98d-259">JetDeleteColumn2</span></span>](./jetdeletecolumn2-function.md)
