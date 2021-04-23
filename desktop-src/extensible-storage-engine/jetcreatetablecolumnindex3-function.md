---
description: Дополнительные сведения о функции JetCreateTableColumnIndex3
title: Функция JetCreateTableColumnIndex3
TOCTitle: JetCreateTableColumnIndex3 Function
ms:assetid: c1a1b091-b4a6-4cdc-a0ea-af21c1462449
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294079(v=EXCHG.10)
ms:contentKeyID: 32765694
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateTableColumnIndex3
- JetCreateTableColumnIndex3W
- JetCreateTableColumnIndex3A
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bf1d6aed3178f5593826097f8c5d6b01bd8c72d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105719732"
---
# <a name="jetcreatetablecolumnindex3-function"></a><span data-ttu-id="d6c49-103">Функция JetCreateTableColumnIndex3</span><span class="sxs-lookup"><span data-stu-id="d6c49-103">JetCreateTableColumnIndex3 Function</span></span>


<span data-ttu-id="d6c49-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="d6c49-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetcreatetablecolumnindex3-function"></a><span data-ttu-id="d6c49-105">Функция JetCreateTableColumnIndex3</span><span class="sxs-lookup"><span data-stu-id="d6c49-105">JetCreateTableColumnIndex3 Function</span></span>

<span data-ttu-id="d6c49-106">Функция **JetCreateTableColumnIndex3** создает таблицу в базе данных ESE с начальным набором индексов и начальным набором столбцов из массива структур [JET_TABLECREATE3](./jet-tablecreate3-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="d6c49-106">The **JetCreateTableColumnIndex3** function creates a table in an ESE database with an initial set of indexes and an initial set of columns from an array of [JET_TABLECREATE3](./jet-tablecreate3-structure.md) structures.</span></span> <span data-ttu-id="d6c49-107">Структура [JET_TABLECREATE3](./jet-tablecreate3-structure.md) позволяет указать функцию обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="d6c49-107">The [JET_TABLECREATE3](./jet-tablecreate3-structure.md) structure allows a callback function to be specified.</span></span>

<span data-ttu-id="d6c49-108">**Windows 7:** **JetCreateTableColumnIndex3** появился в операционной системе Windows 7.</span><span class="sxs-lookup"><span data-stu-id="d6c49-108">**Windows 7:** **JetCreateTableColumnIndex3** is introduced in the Windows 7 operating system.</span></span>

```cpp
    JET_ERR JET_API JetCreateTableColumnIndex3(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in_out      JET_TABLECREATE3* ptablecreate
    );
```

### <a name="parameters"></a><span data-ttu-id="d6c49-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="d6c49-109">Parameters</span></span>

<span data-ttu-id="d6c49-110">*сесид*</span><span class="sxs-lookup"><span data-stu-id="d6c49-110">*sesid*</span></span>

<span data-ttu-id="d6c49-111">Контекст сеанса базы данных, используемый для вызова API.</span><span class="sxs-lookup"><span data-stu-id="d6c49-111">The database session context to use for the API call.</span></span>

<span data-ttu-id="d6c49-112">*DBID*</span><span class="sxs-lookup"><span data-stu-id="d6c49-112">*dbid*</span></span>

<span data-ttu-id="d6c49-113">Идентификатор базы данных, используемый для вызова API.</span><span class="sxs-lookup"><span data-stu-id="d6c49-113">The database identifier to use for the API call.</span></span>

<span data-ttu-id="d6c49-114">*птаблекреате*</span><span class="sxs-lookup"><span data-stu-id="d6c49-114">*ptablecreate*</span></span>

<span data-ttu-id="d6c49-115">Указатель на структуру [JET_TABLECREATE3](./jet-tablecreate3-structure.md) , определяющую создаваемую таблицу.</span><span class="sxs-lookup"><span data-stu-id="d6c49-115">A pointer to a [JET_TABLECREATE3](./jet-tablecreate3-structure.md) structure that defines the table to be created.</span></span> <span data-ttu-id="d6c49-116">Дополнительные сведения см. в разделе [JET_TABLECREATE3](./jet-tablecreate3-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="d6c49-116">See [JET_TABLECREATE3](./jet-tablecreate3-structure.md) for more details.</span></span>

### <a name="return-value"></a><span data-ttu-id="d6c49-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d6c49-117">Return Value</span></span>

<span data-ttu-id="d6c49-118">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="d6c49-118">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="d6c49-119">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="d6c49-119">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d6c49-120">Код возврата</span><span class="sxs-lookup"><span data-stu-id="d6c49-120">Return code</span></span></p></th>
<th><p><span data-ttu-id="d6c49-121">Описание</span><span class="sxs-lookup"><span data-stu-id="d6c49-121">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d6c49-122">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="d6c49-122">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="d6c49-123">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="d6c49-123">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6c49-124">JET_errCallbackNotResolved</span><span class="sxs-lookup"><span data-stu-id="d6c49-124">JET_errCallbackNotResolved</span></span></p></td>
<td><p><span data-ttu-id="d6c49-125">Не удалось разрешить функцию обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="d6c49-125">The callback function could not be resolved.</span></span> <span data-ttu-id="d6c49-126">Возможно, Библиотека DLL не найдена или не найдена функция в библиотеке DLL.</span><span class="sxs-lookup"><span data-stu-id="d6c49-126">The DLL might not have been found, or the function in the DLL might not have been found.</span></span> <span data-ttu-id="d6c49-127">Если ведение журнала включено, в журнале событий будут представлены дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="d6c49-127">With sufficient logging enabled, the event log will provide more details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d6c49-128">JET_errCannotIndex</span><span class="sxs-lookup"><span data-stu-id="d6c49-128">JET_errCannotIndex</span></span></p></td>
<td><p><span data-ttu-id="d6c49-129">Предпринята попытка индексирования по столбцу с использованием типа "условно-Update" или "SLV" (Обратите внимание, что столбцы SLV устарели).</span><span class="sxs-lookup"><span data-stu-id="d6c49-129">An attempt was made to index over an escrow-update or SLV column (note that SLV columns are deprecated).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6c49-130">JET_errCannotNestDDL</span><span class="sxs-lookup"><span data-stu-id="d6c49-130">JET_errCannotNestDDL</span></span></p></td>
<td><p><span data-ttu-id="d6c49-131">Если птаблекреате- &gt; грбит указывает JET_bitTableCreateTemplateTable, но птаблекреате- &gt; сзтемплатетабленаме имеет значение null.</span><span class="sxs-lookup"><span data-stu-id="d6c49-131">If ptablecreate-&gt;grbit specifies JET_bitTableCreateTemplateTable, but ptablecreate-&gt;szTemplateTableName is set to NULL.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d6c49-132">JET_errColumnDuplicate</span><span class="sxs-lookup"><span data-stu-id="d6c49-132">JET_errColumnDuplicate</span></span></p></td>
<td><p><span data-ttu-id="d6c49-133">Столбец уже существует.</span><span class="sxs-lookup"><span data-stu-id="d6c49-133">A column already exists.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6c49-134">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="d6c49-134">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="d6c49-135">Предпринята попытка индексировать несуществующий столбец.</span><span class="sxs-lookup"><span data-stu-id="d6c49-135">An attempt was made to index over a non-existent column.</span></span> <span data-ttu-id="d6c49-136">Эта ошибка также может возникнуть при попытке условного индексирования по несуществующему столбцу.</span><span class="sxs-lookup"><span data-stu-id="d6c49-136">Attempting to conditionally index over a non-existent column can also produce this error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d6c49-137">JET_errColumnRedundant</span><span class="sxs-lookup"><span data-stu-id="d6c49-137">JET_errColumnRedundant</span></span></p></td>
<td><p><span data-ttu-id="d6c49-138">Была предпринята попытка добавить избыточный столбец.</span><span class="sxs-lookup"><span data-stu-id="d6c49-138">An attempt was made to add a redundant column.</span></span> <span data-ttu-id="d6c49-139">Не должно быть более одного столбца автоинкремента и не более одного столбца версий для каждой таблицы.</span><span class="sxs-lookup"><span data-stu-id="d6c49-139">There should be no more than one autoincrement column, and no more than one version column per table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6c49-140">JET_errDensityInvalid</span><span class="sxs-lookup"><span data-stu-id="d6c49-140">JET_errDensityInvalid</span></span></p></td>
<td><p><span data-ttu-id="d6c49-141">Эта ошибка будет возвращена, если элементу <strong>улденсити</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> присвоено число меньше 20 или больше 100.</span><span class="sxs-lookup"><span data-stu-id="d6c49-141">This error will be returned if the <strong>ulDensity</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is set to a number less than 20 or more than 100.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d6c49-142">JET_errDDLNotInheritable</span><span class="sxs-lookup"><span data-stu-id="d6c49-142">JET_errDDLNotInheritable</span></span></p></td>
<td><p><span data-ttu-id="d6c49-143">Означает, что таблица, указанная в элементе <strong>сзтемплатетабленаме</strong> структуры <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a> , не была помечена как таблица шаблона (т. е. в таблице не задан JET_bitTableCreateTemplateTable).</span><span class="sxs-lookup"><span data-stu-id="d6c49-143">Signifies that the table named in the <strong>szTemplateTableName</strong> member of the <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a> structure was not marked as a template table (that is, that table did not have JET_bitTableCreateTemplateTable set).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6c49-144">JET_errIndexDuplicate</span><span class="sxs-lookup"><span data-stu-id="d6c49-144">JET_errIndexDuplicate</span></span></p></td>
<td><p><span data-ttu-id="d6c49-145">Была выполнена попытка определить два одинаковых индекса.</span><span class="sxs-lookup"><span data-stu-id="d6c49-145">An attempt to define two identical indexes was made.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d6c49-146">JET_errIndexHasPrimary</span><span class="sxs-lookup"><span data-stu-id="d6c49-146">JET_errIndexHasPrimary</span></span></p></td>
<td><p><span data-ttu-id="d6c49-147">Предпринята попытка указать более одного первичного индекса для таблицы.</span><span class="sxs-lookup"><span data-stu-id="d6c49-147">An attempt was made to specify more than one primary index for a table.</span></span> <span data-ttu-id="d6c49-148">У таблицы должен быть ровно один первичный индекс.</span><span class="sxs-lookup"><span data-stu-id="d6c49-148">A table must have exactly one primary index.</span></span> <span data-ttu-id="d6c49-149">Если первичный индекс не указан, ядро СУБД будет прозрачно создавать его.</span><span class="sxs-lookup"><span data-stu-id="d6c49-149">If no primary index is specified, the database engine will transparently create one.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6c49-150">JET_errIndexInvalidDef</span><span class="sxs-lookup"><span data-stu-id="d6c49-150">JET_errIndexInvalidDef</span></span></p></td>
<td><p><span data-ttu-id="d6c49-151">Указано недопустимое определение индекса.</span><span class="sxs-lookup"><span data-stu-id="d6c49-151">An invalid index definition was specified.</span></span> <span data-ttu-id="d6c49-152">Ниже приведены некоторые из возможных причин для получения этой ошибки.</span><span class="sxs-lookup"><span data-stu-id="d6c49-152">The following are some of the possible reasons for receiving this error:</span></span></p>
<ul>
<li><p><span data-ttu-id="d6c49-153">Первичный индекс является условным (т. е. элемент <strong>грбит</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> имеет JET_bitIndexPrimary Set, а член <strong>ккондитионалколумн</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> больше нуля).</span><span class="sxs-lookup"><span data-stu-id="d6c49-153">A primary index is conditional (that is, the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure has JET_bitIndexPrimary set, and <strong>cConditionalColumn</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is greater than zero).</span></span></p></li>
<li><p><span data-ttu-id="d6c49-154">Windows Server 2003 и более поздние версии Windows.</span><span class="sxs-lookup"><span data-stu-id="d6c49-154">Windows Server 2003 and later versions of Windows.</span></span> <span data-ttu-id="d6c49-155">Попытка создать индекс кортежа с ограничениями кортежей, но без передачи элемента <strong>птуплелимитс</strong> в структуре <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> (т. е. элемент <strong>грбит</strong> структуры JET_INDEXCREATE2 имеет JET_bitIndexTupleLimits установлен, но указатель <strong>птуплелимитс</strong> имеет значение null).</span><span class="sxs-lookup"><span data-stu-id="d6c49-155">Attempting to create a tuple index with tuple limits, but without passing the <strong>ptuplelimits</strong> member in the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure (that is, the <strong>grbit</strong> member of the JET_INDEXCREATE2 structure has JET_bitIndexTupleLimits set, but the <strong>ptuplelimits</strong> pointer is NULL).</span></span></p></li>
<li><p><span data-ttu-id="d6c49-156">Передача недопустимого определения ключа в элемент <strong>сзкэй</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> .</span><span class="sxs-lookup"><span data-stu-id="d6c49-156">Passing in an invalid key definition in the <strong>szKey</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure.</span></span> <span data-ttu-id="d6c49-157">Описание допустимых определений см. в разделе <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> .</span><span class="sxs-lookup"><span data-stu-id="d6c49-157">See <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> for a discussion of valid definitions.</span></span></p></li>
<li><p><span data-ttu-id="d6c49-158">Установка для элемента <strong>кбварсегмак</strong> в <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> значение больше JET_cbPrimaryKeyMost (для первичного индекса) или больше JET_cbSecondaryKeyMost (для вторичного индекса).</span><span class="sxs-lookup"><span data-stu-id="d6c49-158">Setting the <strong>cbVarSegMac</strong> member in <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> to be greater than JET_cbPrimaryKeyMost (for a primary index) or greater than JET_cbSecondaryKeyMost (for a secondary index).</span></span></p></li>
<li><p><span data-ttu-id="d6c49-159">Передача недопустимого сочетания для определяемого пользователем индекса в Юникоде (один из которых имеет JET_bitIndexUnicode бит, заданный в элементе <strong>грбит</strong> в <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>).</span><span class="sxs-lookup"><span data-stu-id="d6c49-159">Passing an invalid combination for a user-defined Unicode index (one that has the JET_bitIndexUnicode bit set in the <strong>grbit</strong> member of <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>).</span></span> <span data-ttu-id="d6c49-160">Некоторые распространенные причины: элемент <strong>пидксуникоде</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> имеет значение null, или код LCID, указанный в структуре <strong>пидксуникоде</strong> , является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="d6c49-160">Some common causes include the <strong>pidxunicode</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is NULL, or the LCID specified in the <strong>pidxunicode</strong> structure is invalid.</span></span></p></li>
<li><p><span data-ttu-id="d6c49-161">Указание столбца с несколькими значениями для первичного индекса.</span><span class="sxs-lookup"><span data-stu-id="d6c49-161">Specifying a multi-valued column for a primary index.</span></span></p></li>
<li><p><span data-ttu-id="d6c49-162">Попытка индексировать слишком много условных столбцов.</span><span class="sxs-lookup"><span data-stu-id="d6c49-162">Trying to index too many conditional columns.</span></span> <span data-ttu-id="d6c49-163">Элемент <strong>ккондитионалколумн</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> не должен быть больше JET_ccolKeyMost.</span><span class="sxs-lookup"><span data-stu-id="d6c49-163">The <strong>cConditionalColumn</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure must not be greater than JET_ccolKeyMost.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d6c49-164">JET_errIndexTuplesInvalidLimits</span><span class="sxs-lookup"><span data-stu-id="d6c49-164">JET_errIndexTuplesInvalidLimits</span></span></p></td>
<td><p><span data-ttu-id="d6c49-165">Windows XP и более поздние версии Windows.</span><span class="sxs-lookup"><span data-stu-id="d6c49-165">Windows XP and later versions of Windows.</span></span> <span data-ttu-id="d6c49-166">Указана структура <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> , а ее ограничения не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="d6c49-166">A <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure was specified, and its limits are not supported.</span></span> <span data-ttu-id="d6c49-167">См. раздел "Примечания" структуры <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> .</span><span class="sxs-lookup"><span data-stu-id="d6c49-167">See the remarks section of the <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6c49-168">JET_errIndexTuplesNonUniqueOnly</span><span class="sxs-lookup"><span data-stu-id="d6c49-168">JET_errIndexTuplesNonUniqueOnly</span></span></p></td>
<td><p><span data-ttu-id="d6c49-169">Windows XP и более поздние версии Windows.</span><span class="sxs-lookup"><span data-stu-id="d6c49-169">Windows XP and later versions of Windows.</span></span> <span data-ttu-id="d6c49-170">Индекс кортежа не может быть уникальным (т. е. элемент <em>грбит</em> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> не должен иметь одновременно JET_bitIndexPrimary и JET_bitIndexUnique).</span><span class="sxs-lookup"><span data-stu-id="d6c49-170">A tuple index cannot be unique (that is, the <em>grbit</em> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure must not have both JET_bitIndexPrimary and JET_bitIndexUnique set).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d6c49-171">JET_errIndexTuplesOneColumnOnly</span><span class="sxs-lookup"><span data-stu-id="d6c49-171">JET_errIndexTuplesOneColumnOnly</span></span></p></td>
<td><p><span data-ttu-id="d6c49-172">Windows XP и более поздние версии Windows.</span><span class="sxs-lookup"><span data-stu-id="d6c49-172">Windows XP and later versions of Windows.</span></span> <span data-ttu-id="d6c49-173">Индекс кортежа может находиться только в одном столбце (т. е. Если элемент <strong>грбит</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> JET_bitIndexTuples задан, а элемент <strong>сзкэй</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> указывает более одного столбца).</span><span class="sxs-lookup"><span data-stu-id="d6c49-173">A tuple index can only be over a single column (that is, if the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure has JET_bitIndexTuples set, and the <strong>szKey</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure specifies more than one column).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6c49-174">JET_errIndexTuplesSecondaryIndexOnly</span><span class="sxs-lookup"><span data-stu-id="d6c49-174">JET_errIndexTuplesSecondaryIndexOnly</span></span></p></td>
<td><p><span data-ttu-id="d6c49-175">Windows XP и более поздние версии Windows.</span><span class="sxs-lookup"><span data-stu-id="d6c49-175">Windows XP and later versions of Windows.</span></span> <span data-ttu-id="d6c49-176">Индекс кортежа не может быть первичным индексом (т. е. элемент <strong>грбит</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> не должен иметь одновременно JET_bitIndexPrimary и JET_bitIndexTuples).</span><span class="sxs-lookup"><span data-stu-id="d6c49-176">A tuple index cannot be a primary index (that is, the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure must not have both JET_bitIndexPrimary and JET_bitIndexTuples set).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d6c49-177">JET_errIndexTuplesTextColumnsOnly</span><span class="sxs-lookup"><span data-stu-id="d6c49-177">JET_errIndexTuplesTextColumnsOnly</span></span></p></td>
<td><p><span data-ttu-id="d6c49-178">Windows XP и более поздние версии Windows.</span><span class="sxs-lookup"><span data-stu-id="d6c49-178">Windows XP and later versions of Windows.</span></span> <span data-ttu-id="d6c49-179">Индекс кортежа может находиться только в тексте или столбце Юникода.</span><span class="sxs-lookup"><span data-stu-id="d6c49-179">A tuple index can only be on a text or Unicode column.</span></span> <span data-ttu-id="d6c49-180">Попытка индексировать другие столбцы (например, двоичные столбцы) приведет к JET_errIndexTuplesTextColumnsOnly.</span><span class="sxs-lookup"><span data-stu-id="d6c49-180">An attempt to index other columns (such as binary columns) will result in JET_errIndexTuplesTextColumnsOnly.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6c49-181">JET_errIndexTuplesVarSegMacNotAllowed</span><span class="sxs-lookup"><span data-stu-id="d6c49-181">JET_errIndexTuplesVarSegMacNotAllowed</span></span></p></td>
<td><p><span data-ttu-id="d6c49-182">Windows XP и более поздние версии Windows.</span><span class="sxs-lookup"><span data-stu-id="d6c49-182">Windows XP and later versions of Windows.</span></span> <span data-ttu-id="d6c49-183">Индекс кортежа не позволяет установить элемент <strong>кбварсегмак</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> .</span><span class="sxs-lookup"><span data-stu-id="d6c49-183">A tuple index does not allow the <strong>cbVarSegMac</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure to be set.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d6c49-184">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="d6c49-184">JET_errInTransaction</span></span></p></td>
<td><p><span data-ttu-id="d6c49-185">Предпринята попытка создать индекс без сведений о версии во время транзакции.</span><span class="sxs-lookup"><span data-stu-id="d6c49-185">An attempt was made to create an index without version information while in a transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6c49-186">JET_errInvalidCodePage</span><span class="sxs-lookup"><span data-stu-id="d6c49-186">JET_errInvalidCodePage</span></span></p></td>
<td><p><span data-ttu-id="d6c49-187">Элементу <strong>CP</strong> структуры <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> не задана допустимая кодовая страница.</span><span class="sxs-lookup"><span data-stu-id="d6c49-187">The <strong>cp</strong> member of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structure was not set to a valid code page.</span></span> <span data-ttu-id="d6c49-188">Единственными допустимыми значениями для текстовых столбцов являются английский (1252) и Unicode (1200).</span><span class="sxs-lookup"><span data-stu-id="d6c49-188">The only valid values for text columns are English (1252) and Unicode (1200).</span></span> <span data-ttu-id="d6c49-189">Значение 0 означает, что будет использоваться по умолчанию (английский, 1252).</span><span class="sxs-lookup"><span data-stu-id="d6c49-189">A value of 0 means the default will be used (English, 1252).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d6c49-190">JET_errInvalidColumnType</span><span class="sxs-lookup"><span data-stu-id="d6c49-190">JET_errInvalidColumnType</span></span></p></td>
<td><p><span data-ttu-id="d6c49-191">Элементу <strong>колтип</strong> структуры <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> не был задан допустимый тип столбца.</span><span class="sxs-lookup"><span data-stu-id="d6c49-191">The <strong>coltyp</strong> member of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structure was not set to a valid column type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6c49-192">JET_errInvalidCreateIndex</span><span class="sxs-lookup"><span data-stu-id="d6c49-192">JET_errInvalidCreateIndex</span></span></p></td>
<td><p><span data-ttu-id="d6c49-193">Ниже приведены некоторые причины, по которым может возникнуть Эта ошибка:</span><span class="sxs-lookup"><span data-stu-id="d6c49-193">The following are some reasons why this error may occur:</span></span></p>
<ul>
<li><p><span data-ttu-id="d6c49-194">Элементу <strong>ргиндекскреате</strong> структуры <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> присвоено значение null.</span><span class="sxs-lookup"><span data-stu-id="d6c49-194">The <strong>rgindexcreate</strong> member of the <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure was set to NULL.</span></span></p></li>
<li><p><span data-ttu-id="d6c49-195">Элементу <strong>ргколумнкреате</strong> структуры <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> присвоено значение null.</span><span class="sxs-lookup"><span data-stu-id="d6c49-195">The <strong>rgcolumncreate</strong> member of the <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure was set to NULL.</span></span></p></li>
<li><p><span data-ttu-id="d6c49-196">Элементу <strong>кбструкт</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> не было присвоено допустимое значение.</span><span class="sxs-lookup"><span data-stu-id="d6c49-196">The <strong>cbStruct</strong> member of a <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure was not set to a valid value.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d6c49-197">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="d6c49-197">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="d6c49-198">В <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a>было указано недопустимое сочетание членов <strong>грбит</strong> .</span><span class="sxs-lookup"><span data-stu-id="d6c49-198">An invalid combination of <strong>grbit</strong> members was specified in <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a>.</span></span></p>
<p><span data-ttu-id="d6c49-199">Определение индекса недопустимо, так как элемент <strong>грбит</strong> содержит неправильные значения.</span><span class="sxs-lookup"><span data-stu-id="d6c49-199">The index definition is invalid because the <strong>grbit</strong> member contains inconsistent values.</span></span> <span data-ttu-id="d6c49-200">Ниже приведены некоторые возможные причины.</span><span class="sxs-lookup"><span data-stu-id="d6c49-200">The following are some possible reasons:</span></span></p>
<ul>
<li><p><span data-ttu-id="d6c49-201">Для первичного индекса задан бит игнорирования (то есть JET_bitIndexPrimary передан с JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull или JET_bitIndexIgnoreFirstNull).</span><span class="sxs-lookup"><span data-stu-id="d6c49-201">A primary index had an ignore bit specified (that is, JET_bitIndexPrimary was passed with JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull, or JET_bitIndexIgnoreFirstNull).</span></span></p></li>
<li><p><span data-ttu-id="d6c49-202">Пустой индекс не игнорирует все элементы NULL (т. е. элемент <strong>грбит</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> JET_bitIndexEmpty установлен, но не имеет JET_bitIndexIgnoreAnyNull).</span><span class="sxs-lookup"><span data-stu-id="d6c49-202">An empty index does not ignore any NULL members (that is, the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure has JET_bitIndexEmpty set, but does not have JET_bitIndexIgnoreAnyNull set).</span></span></p></li>
<li><p><span data-ttu-id="d6c49-203">Передача структуры <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> с недопустимым элементом <strong>грбит</strong> .</span><span class="sxs-lookup"><span data-stu-id="d6c49-203">Passing in a <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> structure with an invalid <strong>grbit</strong> member.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6c49-204">JET_errInvalidLanguageId</span><span class="sxs-lookup"><span data-stu-id="d6c49-204">JET_errInvalidLanguageId</span></span></p></td>
<td><p><span data-ttu-id="d6c49-205">Передан недопустимый код локали (LCID) (либо с помощью элемента <strong>LCID</strong> структуры <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> , на который указывает элемент <strong>пидксуникоде</strong> в структуре <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> , либо с помощью поля <strong>LCID</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ).</span><span class="sxs-lookup"><span data-stu-id="d6c49-205">An invalid Locale ID (LCID) was passed in (either through the <strong>lcid</strong> member of the <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> structure which is pointed to by the <strong>pidxunicode</strong> member in the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure, or through the <strong>lcid</strong> field of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d6c49-206">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="d6c49-206">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="d6c49-207">Указан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="d6c49-207">An invalid parameter was given.</span></span> <span data-ttu-id="d6c49-208">Ниже приведены некоторые возможные причины.</span><span class="sxs-lookup"><span data-stu-id="d6c49-208">The following are some possible reasons:</span></span></p>
<ul>
<li><p><span data-ttu-id="d6c49-209">Элемент <strong>ргколумнкреате</strong> структуры <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a> имеет значение null.</span><span class="sxs-lookup"><span data-stu-id="d6c49-209">The <strong>rgcolumncreate</strong> member of the <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a> structure is NULL.</span></span></p></li>
<li><p><span data-ttu-id="d6c49-210">Элемент <strong>кбструкт</strong> одной из структур <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> , указанных в элементе <strong>ргколумнкреате</strong> структуры <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> , не был задан как sizeof (JET_COLUMNCREATE).</span><span class="sxs-lookup"><span data-stu-id="d6c49-210">The <strong>cbStruct</strong> member of one of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structures given in the <strong>rgcolumncreate</strong> member of the <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure was not set to sizeof( JET_COLUMNCREATE ).</span></span></p></li>
<li><p><span data-ttu-id="d6c49-211">Элемент <strong>cbKey</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> имеет значение 0.</span><span class="sxs-lookup"><span data-stu-id="d6c49-211">The <strong>cbKey</strong> member of a <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is set to zero.</span></span></p></li>
<li><p><span data-ttu-id="d6c49-212">Элементу <strong>кбструкт</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> не присвоено значение sizeof (JET_INDEXCREATE2).</span><span class="sxs-lookup"><span data-stu-id="d6c49-212">The <strong>cbStruct</strong> member of a <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is not set to sizeof( JET_INDEXCREATE2 ).</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6c49-213">JET_errRecordTooBig</span><span class="sxs-lookup"><span data-stu-id="d6c49-213">JET_errRecordTooBig</span></span></p></td>
<td><p><span data-ttu-id="d6c49-214">Запись слишком велика.</span><span class="sxs-lookup"><span data-stu-id="d6c49-214">The record is too big.</span></span> <span data-ttu-id="d6c49-215">Сумма элемента <strong>кбмакс</strong> структуры <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> для всех фиксированных столбцов не должна превышать определенное значение.</span><span class="sxs-lookup"><span data-stu-id="d6c49-215">The sum of the <strong>cbMax</strong> member of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structure for all fixed columns must not exceed a certain value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d6c49-216">JET_errTableDuplicate</span><span class="sxs-lookup"><span data-stu-id="d6c49-216">JET_errTableDuplicate</span></span></p></td>
<td><p><span data-ttu-id="d6c49-217">Таблица уже существует.</span><span class="sxs-lookup"><span data-stu-id="d6c49-217">The table already exists.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6c49-218">JET_errTooManyColumns</span><span class="sxs-lookup"><span data-stu-id="d6c49-218">JET_errTooManyColumns</span></span></p></td>
<td><p><span data-ttu-id="d6c49-219">Предпринята попытка добавить в таблицу слишком много столбцов.</span><span class="sxs-lookup"><span data-stu-id="d6c49-219">An attempt was made to add too many columns to the table.</span></span> <span data-ttu-id="d6c49-220">Таблица может содержать не более JET_ccolFixedMost фиксированных столбцов, не более JET_ccolVarMost столбцов переменной длины и не более JET_ccolTaggedMost столбцов с тегами.</span><span class="sxs-lookup"><span data-stu-id="d6c49-220">A table can have no more than JET_ccolFixedMost fixed columns, no more than JET_ccolVarMost variable-length columns, and no more than JET_ccolTaggedMost tagged columns.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d6c49-221">JET_errUnicodeTranslationFail</span><span class="sxs-lookup"><span data-stu-id="d6c49-221">JET_errUnicodeTranslationFail</span></span></p></td>
<td><p><span data-ttu-id="d6c49-222">Произошла ошибка при попытке нормализовать столбец в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="d6c49-222">An error occurred attempting to normalize a Unicode column.</span></span> <span data-ttu-id="d6c49-223">Это может быть вызвано недостатком системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d6c49-223">This can be caused by running out of system resources.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6c49-224">JET_errSpaceHintsInvalid</span><span class="sxs-lookup"><span data-stu-id="d6c49-224">JET_errSpaceHintsInvalid</span></span></p></td>
<td><p><span data-ttu-id="d6c49-225">Неверное или неправильное действие элемента структуры подсказок пространства JET.</span><span class="sxs-lookup"><span data-stu-id="d6c49-225">An element of the JET space hints structure was not correct or actionable.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="d6c49-226">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d6c49-226">Remarks</span></span>

<span data-ttu-id="d6c49-227">Имя **JetCreateTableColumnIndex3** поступает из порядка создания объектов: сначала создается таблица, столбцы и, наконец, индексы.</span><span class="sxs-lookup"><span data-stu-id="d6c49-227">The name **JetCreateTableColumnIndex3** comes from the order of creation of the objects: It first creates a table, columns, and then finally indexes.</span></span> <span data-ttu-id="d6c49-228">**JetCreateTableColumnIndex3** создает таблицу с начальным набором столбцов и индексов.</span><span class="sxs-lookup"><span data-stu-id="d6c49-228">**JetCreateTableColumnIndex3** creates a table with an initial set of columns and indexes.</span></span> <span data-ttu-id="d6c49-229">Дополнительные столбцы и индексы можно добавлять и удалять динамически с помощью [жетаддколумн](./jetaddcolumn-function.md), [жетделетеколумн](./jetdeletecolumn-function.md), [JetDeleteColumn2](./jetdeletecolumn2-function.md), [жеткреатеиндекс](./jetcreateindex-function.md), [JetCreateIndex2](./jetcreateindex2-function.md), [JetCreateIndex3](./jetcreateindex3-function.md)и [жетделетеиндекс](./jetdeleteindex-function.md).</span><span class="sxs-lookup"><span data-stu-id="d6c49-229">Additional columns and indexes can be added and removed dynamically with [JetAddColumn](./jetaddcolumn-function.md), [JetDeleteColumn](./jetdeletecolumn-function.md), [JetDeleteColumn2](./jetdeletecolumn2-function.md), [JetCreateIndex](./jetcreateindex-function.md), [JetCreateIndex2](./jetcreateindex2-function.md), [JetCreateIndex3](./jetcreateindex3-function.md), and [JetDeleteIndex](./jetdeleteindex-function.md).</span></span>

<span data-ttu-id="d6c49-230">Как и [жетопентабле](./jetopentable-function.md), когда приложение выполняется с помощью возвращенного *TableID*, оно обычно должно быть закрыто с помощью [жетклосетабле](./jetclosetable-function.md).</span><span class="sxs-lookup"><span data-stu-id="d6c49-230">Like [JetOpenTable](./jetopentable-function.md), when the application is done using the returned *tableid*, it should usually be closed with [JetCloseTable](./jetclosetable-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="d6c49-231">Требования</span><span class="sxs-lookup"><span data-stu-id="d6c49-231">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d6c49-232"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="d6c49-232"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="d6c49-233">Требуется Windows Vista или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d6c49-233">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6c49-234"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="d6c49-234"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="d6c49-235">Требуется Windows Server 2008 или Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="d6c49-235">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d6c49-236"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="d6c49-236"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="d6c49-237">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="d6c49-237">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6c49-238"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="d6c49-238"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="d6c49-239">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="d6c49-239">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d6c49-240"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="d6c49-240"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="d6c49-241">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="d6c49-241">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6c49-242"><strong>Юникод</strong></span><span class="sxs-lookup"><span data-stu-id="d6c49-242"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="d6c49-243">Реализуется как <strong>JetCreateTableColumnIndex3W</strong> (Юникод) и <strong>JetCreateTableColumnIndex3A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="d6c49-243">Implemented as <strong>JetCreateTableColumnIndex3W</strong> (Unicode) and <strong>JetCreateTableColumnIndex3A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="d6c49-244">См. также:</span><span class="sxs-lookup"><span data-stu-id="d6c49-244">See Also</span></span>

[<span data-ttu-id="d6c49-245">JET_CBTYP</span><span class="sxs-lookup"><span data-stu-id="d6c49-245">JET_CBTYP</span></span>](./jet-cbtyp.md)  
[<span data-ttu-id="d6c49-246">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="d6c49-246">JET_DBID</span></span>](./jet-dbid.md)  
[<span data-ttu-id="d6c49-247">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="d6c49-247">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="d6c49-248">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="d6c49-248">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="d6c49-249">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="d6c49-249">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)  
[<span data-ttu-id="d6c49-250">JET_INDEXCREATE2</span><span class="sxs-lookup"><span data-stu-id="d6c49-250">JET_INDEXCREATE2</span></span>](./jet-indexcreate2-structure.md)  
[<span data-ttu-id="d6c49-251">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="d6c49-251">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="d6c49-252">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="d6c49-252">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="d6c49-253">JET_TABLECREATE2</span><span class="sxs-lookup"><span data-stu-id="d6c49-253">JET_TABLECREATE2</span></span>](./jet-tablecreate2-structure.md)  
[<span data-ttu-id="d6c49-254">JET_TABLECREATE3</span><span class="sxs-lookup"><span data-stu-id="d6c49-254">JET_TABLECREATE3</span></span>](./jet-tablecreate3-structure.md)  
[<span data-ttu-id="d6c49-255">JET_TUPLELIMITS</span><span class="sxs-lookup"><span data-stu-id="d6c49-255">JET_TUPLELIMITS</span></span>](./jet-tuplelimits-structure.md)  
[<span data-ttu-id="d6c49-256">жетаддколумн</span><span class="sxs-lookup"><span data-stu-id="d6c49-256">JetAddColumn</span></span>](./jetaddcolumn-function.md)  
[<span data-ttu-id="d6c49-257">жеткреатеиндекс</span><span class="sxs-lookup"><span data-stu-id="d6c49-257">JetCreateIndex</span></span>](./jetcreateindex-function.md)  
[<span data-ttu-id="d6c49-258">JetCreateIndex2</span><span class="sxs-lookup"><span data-stu-id="d6c49-258">JetCreateIndex2</span></span>](./jetcreateindex2-function.md)  
[<span data-ttu-id="d6c49-259">JetCreateIndex3</span><span class="sxs-lookup"><span data-stu-id="d6c49-259">JetCreateIndex3</span></span>](./jetcreateindex3-function.md)  
[<span data-ttu-id="d6c49-260">жеткреатетабле</span><span class="sxs-lookup"><span data-stu-id="d6c49-260">JetCreateTable</span></span>](./jetcreatetable-function.md)  
[<span data-ttu-id="d6c49-261">жеткреатетаблеколумниндекс</span><span class="sxs-lookup"><span data-stu-id="d6c49-261">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="d6c49-262">жетделетеколумн</span><span class="sxs-lookup"><span data-stu-id="d6c49-262">JetDeleteColumn</span></span>](./jetdeletecolumn-function.md)  
[<span data-ttu-id="d6c49-263">JetDeleteColumn2</span><span class="sxs-lookup"><span data-stu-id="d6c49-263">JetDeleteColumn2</span></span>](./jetdeletecolumn2-function.md)
