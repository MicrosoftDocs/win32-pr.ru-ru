---
description: Дополнительные сведения о функции Жеткреатетаблеколумниндекс
title: Функция Жеткреатетаблеколумниндекс
TOCTitle: JetCreateTableColumnIndex Function
ms:assetid: 9192614b-20a6-40fb-906a-51fc057e7483
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269343(v=EXCHG.10)
ms:contentKeyID: 32765632
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateTableColumnIndexA
- JetCreateTableColumnIndexW
- JetCreateTableColumnIndex
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: aea9f79617c35c5a956f0cd5f621c7faadffe668
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105719614"
---
# <a name="jetcreatetablecolumnindex-function"></a><span data-ttu-id="ef74e-103">Функция Жеткреатетаблеколумниндекс</span><span class="sxs-lookup"><span data-stu-id="ef74e-103">JetCreateTableColumnIndex Function</span></span>


<span data-ttu-id="ef74e-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="ef74e-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetcreatetablecolumnindex-function"></a><span data-ttu-id="ef74e-105">Функция Жеткреатетаблеколумниндекс</span><span class="sxs-lookup"><span data-stu-id="ef74e-105">JetCreateTableColumnIndex Function</span></span>

<span data-ttu-id="ef74e-106">Функция **жеткреатетаблеколумниндекс** создает таблицу в базе данных ESE с начальным набором индексов и начальным набором столбцов из массива структур [JET_TABLECREATE](./jet-tablecreate-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="ef74e-106">The **JetCreateTableColumnIndex** function creates a table in an ESE database with an initial set of indexes and an initial set of columns from an array of [JET_TABLECREATE](./jet-tablecreate-structure.md) structures.</span></span> <span data-ttu-id="ef74e-107">Имя **жеткреатетаблеколумниндекс** поступает из порядка создания объектов.</span><span class="sxs-lookup"><span data-stu-id="ef74e-107">The name **JetCreateTableColumnIndex** comes from the order of creation of the objects.</span></span> <span data-ttu-id="ef74e-108">Сначала он создает таблицу, столбцы и, наконец, индексы.</span><span class="sxs-lookup"><span data-stu-id="ef74e-108">It first creates a table, columns, and then finally indexes.</span></span>

```cpp
    JET_ERR JET_API JetCreateTableColumnIndex(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in_out      JET_TABLECREATE* ptablecreate
    );
```

### <a name="parameters"></a><span data-ttu-id="ef74e-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="ef74e-109">Parameters</span></span>

<span data-ttu-id="ef74e-110">*сесид*</span><span class="sxs-lookup"><span data-stu-id="ef74e-110">*sesid*</span></span>

<span data-ttu-id="ef74e-111">Контекст сеанса базы данных, используемый для вызова API.</span><span class="sxs-lookup"><span data-stu-id="ef74e-111">The database session context to use for the API call.</span></span>

<span data-ttu-id="ef74e-112">*DBID*</span><span class="sxs-lookup"><span data-stu-id="ef74e-112">*dbid*</span></span>

<span data-ttu-id="ef74e-113">Идентификатор базы данных, используемый для вызова API.</span><span class="sxs-lookup"><span data-stu-id="ef74e-113">The database identifier to use for the API call.</span></span>

<span data-ttu-id="ef74e-114">*птаблекреате*</span><span class="sxs-lookup"><span data-stu-id="ef74e-114">*ptablecreate*</span></span>

<span data-ttu-id="ef74e-115">Указатель на структуру [JET_TABLECREATE](./jet-tablecreate-structure.md) , которая определяет создаваемую таблицу.</span><span class="sxs-lookup"><span data-stu-id="ef74e-115">A pointer to a [JET_TABLECREATE](./jet-tablecreate-structure.md) structure which defines the table to be created.</span></span> <span data-ttu-id="ef74e-116">Дополнительные сведения см. в разделе [JET_TABLECREATE](./jet-tablecreate-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="ef74e-116">See [JET_TABLECREATE](./jet-tablecreate-structure.md) for more details.</span></span>

### <a name="return-value"></a><span data-ttu-id="ef74e-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ef74e-117">Return Value</span></span>

<span data-ttu-id="ef74e-118">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="ef74e-118">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="ef74e-119">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="ef74e-119">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ef74e-120">Код возврата</span><span class="sxs-lookup"><span data-stu-id="ef74e-120">Return code</span></span></p></th>
<th><p><span data-ttu-id="ef74e-121">Описание</span><span class="sxs-lookup"><span data-stu-id="ef74e-121">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ef74e-122">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="ef74e-122">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="ef74e-123">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="ef74e-123">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef74e-124">JET_errCallbackNotResolved</span><span class="sxs-lookup"><span data-stu-id="ef74e-124">JET_errCallbackNotResolved</span></span></p></td>
<td><p><span data-ttu-id="ef74e-125">Не удалось разрешить функцию обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="ef74e-125">The callback function could not be resolved.</span></span> <span data-ttu-id="ef74e-126">Возможно, Библиотека DLL не найдена или не найдена функция в библиотеке DLL.</span><span class="sxs-lookup"><span data-stu-id="ef74e-126">The DLL might not have been found, or the function in the DLL might not have been found.</span></span> <span data-ttu-id="ef74e-127">Если ведение журнала включено, в журнале событий будут представлены дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="ef74e-127">With sufficient logging enabled, the event log will provide more details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef74e-128">JET_errCannotIndex</span><span class="sxs-lookup"><span data-stu-id="ef74e-128">JET_errCannotIndex</span></span></p></td>
<td><p><span data-ttu-id="ef74e-129">Предпринята попытка индексирования по столбцу с использованием типа "условно-Update" или "SLV" (Обратите внимание, что столбцы SLV устарели).</span><span class="sxs-lookup"><span data-stu-id="ef74e-129">An attempt was made to index over an escrow-update or SLV column (note that SLV columns are deprecated).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef74e-130">JET_errCannotNestDDL</span><span class="sxs-lookup"><span data-stu-id="ef74e-130">JET_errCannotNestDDL</span></span></p></td>
<td><p><span data-ttu-id="ef74e-131">Если птаблекреате- &gt; грбит указывает JET_bitTableCreateTemplateTable, но птаблекреате- &gt; сзтемплатетабленаме имеет значение null.</span><span class="sxs-lookup"><span data-stu-id="ef74e-131">If ptablecreate-&gt;grbit specifies JET_bitTableCreateTemplateTable, but ptablecreate-&gt;szTemplateTableName is set to NULL.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef74e-132">JET_errColumnDuplicate</span><span class="sxs-lookup"><span data-stu-id="ef74e-132">JET_errColumnDuplicate</span></span></p></td>
<td><p><span data-ttu-id="ef74e-133">Столбец уже существует.</span><span class="sxs-lookup"><span data-stu-id="ef74e-133">A column already exists.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef74e-134">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="ef74e-134">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="ef74e-135">Предпринята попытка индексировать несуществующий столбец.</span><span class="sxs-lookup"><span data-stu-id="ef74e-135">An attempt was made to index over a non-existent column.</span></span> <span data-ttu-id="ef74e-136">Эта ошибка также может возникнуть при попытке условного индексирования по несуществующему столбцу.</span><span class="sxs-lookup"><span data-stu-id="ef74e-136">Attempting to conditionally index over a non-existent column can also produce this error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef74e-137">JET_errColumnRedundant</span><span class="sxs-lookup"><span data-stu-id="ef74e-137">JET_errColumnRedundant</span></span></p></td>
<td><p><span data-ttu-id="ef74e-138">Была предпринята попытка добавить избыточный столбец.</span><span class="sxs-lookup"><span data-stu-id="ef74e-138">An attempt was made to add a redundant column.</span></span> <span data-ttu-id="ef74e-139">Не должно быть более одного столбца автоинкремента и не более одного столбца версий для каждой таблицы.</span><span class="sxs-lookup"><span data-stu-id="ef74e-139">There should be no more than one autoincrement column, and no more than one version column per table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef74e-140">JET_errDensityInvalid</span><span class="sxs-lookup"><span data-stu-id="ef74e-140">JET_errDensityInvalid</span></span></p></td>
<td><p><span data-ttu-id="ef74e-141">Эта ошибка будет возвращена, если элементу <strong>улденсити</strong> структуры <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> присвоено число меньше 20 или больше 100.</span><span class="sxs-lookup"><span data-stu-id="ef74e-141">This error will be returned if the <strong>ulDensity</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure is set to a number less than 20 or more than 100.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef74e-142">JET_errDDLNotInheritable</span><span class="sxs-lookup"><span data-stu-id="ef74e-142">JET_errDDLNotInheritable</span></span></p></td>
<td><p><span data-ttu-id="ef74e-143">Означает, что таблица, указанная в элементе <strong>сзтемплатетабленаме</strong> структуры <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> , не была помечена как таблица шаблона (т. е. в таблице не задан JET_bitTableCreateTemplateTable).</span><span class="sxs-lookup"><span data-stu-id="ef74e-143">Signifies that the table named in the <strong>szTemplateTableName</strong> member of the <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> structure was not marked as a template table (that is, that table did not have JET_bitTableCreateTemplateTable set).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef74e-144">JET_errIndexDuplicate</span><span class="sxs-lookup"><span data-stu-id="ef74e-144">JET_errIndexDuplicate</span></span></p></td>
<td><p><span data-ttu-id="ef74e-145">Была выполнена попытка определить два одинаковых индекса.</span><span class="sxs-lookup"><span data-stu-id="ef74e-145">An attempt to define two identical indexes was made.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef74e-146">JET_errIndexHasPrimary</span><span class="sxs-lookup"><span data-stu-id="ef74e-146">JET_errIndexHasPrimary</span></span></p></td>
<td><p><span data-ttu-id="ef74e-147">Предпринята попытка указать более одного первичного индекса для таблицы.</span><span class="sxs-lookup"><span data-stu-id="ef74e-147">An attempt was made to specify more than one primary index for a table.</span></span> <span data-ttu-id="ef74e-148">У таблицы должен быть ровно один первичный индекс.</span><span class="sxs-lookup"><span data-stu-id="ef74e-148">A table must have exactly one primary index.</span></span> <span data-ttu-id="ef74e-149">Если первичный индекс не указан, ядро СУБД будет прозрачно создавать его.</span><span class="sxs-lookup"><span data-stu-id="ef74e-149">If no primary index is specified, the database engine will transparently create one.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef74e-150">JET_errIndexInvalidDef</span><span class="sxs-lookup"><span data-stu-id="ef74e-150">JET_errIndexInvalidDef</span></span></p></td>
<td><p><span data-ttu-id="ef74e-151">Указано недопустимое определение индекса.</span><span class="sxs-lookup"><span data-stu-id="ef74e-151">An invalid index definition was specified.</span></span> <span data-ttu-id="ef74e-152">Ниже приведены некоторые возможные причины получения этой ошибки:</span><span class="sxs-lookup"><span data-stu-id="ef74e-152">Some of the possible reasons for receiving this error are:</span></span></p>
<ul>
<li><p><span data-ttu-id="ef74e-153">Первичный индекс является условным (т. е. элемент <strong>грбит</strong> структуры <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> имеет JET_bitIndexPrimary Set, а член <strong>ккондитионалколумн</strong> структуры <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> больше нуля).</span><span class="sxs-lookup"><span data-stu-id="ef74e-153">A primary index is conditional (that is, the <strong>grbit</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure has JET_bitIndexPrimary set, and <strong>cConditionalColumn</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure is greater than zero).</span></span></p></li>
<li><p><span data-ttu-id="ef74e-154">Windows Server 2003 и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="ef74e-154">Windows Server 2003 and later.</span></span> <span data-ttu-id="ef74e-155">Попытка создать индекс кортежа с ограничениями кортежей, но без передачи элемента <strong>птуплелимитс</strong> в структуре <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> (т. е. элемент <strong>грбит</strong> структуры <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> имеет JET_bitIndexTupleLimits установлен, но указатель <strong>птуплелимитс</strong> имеет значение null).</span><span class="sxs-lookup"><span data-stu-id="ef74e-155">Attempting to create a tuple index with tuple limits, but without passing the <strong>ptuplelimits</strong> member in the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure (that is, the <strong>grbit</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure has JET_bitIndexTupleLimits set, but the <strong>ptuplelimits</strong> pointer is NULL).</span></span></p></li>
<li><p><span data-ttu-id="ef74e-156">Передача недопустимого определения ключа в элемент <strong>сзкэй</strong> структуры <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</span><span class="sxs-lookup"><span data-stu-id="ef74e-156">Passing in an invalid key definition in the <strong>szKey</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure.</span></span> <span data-ttu-id="ef74e-157">Описание допустимых определений см. в разделе <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</span><span class="sxs-lookup"><span data-stu-id="ef74e-157">See <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> for a discussion of valid definitions.</span></span></p></li>
<li><p><span data-ttu-id="ef74e-158">Установка для элемента <strong>кбварсегмак</strong> в <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> значение больше JET_cbPrimaryKeyMost (для первичного индекса) или больше JET_cbSecondaryKeyMost (для вторичного индекса).</span><span class="sxs-lookup"><span data-stu-id="ef74e-158">Setting the <strong>cbVarSegMac</strong> member in <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> to be greater than JET_cbPrimaryKeyMost (for a primary index) or greater than JET_cbSecondaryKeyMost (for a secondary index).</span></span></p></li>
<li><p><span data-ttu-id="ef74e-159">Передача недопустимого сочетания для определяемого пользователем индекса в Юникоде (одна из которых имеет бит JET_bitIndexUnicode, заданный в элементе <strong>грбит</strong> в <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>).</span><span class="sxs-lookup"><span data-stu-id="ef74e-159">Passing an invalid combination for a user-defined Unicode index (one which has the JET_bitIndexUnicode bit set in the <strong>grbit</strong> member of <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>).</span></span> <span data-ttu-id="ef74e-160">Некоторые распространенные причины: элемент <strong>пидксуникоде</strong> структуры <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> имеет значение null, или код LCID, указанный в структуре <strong>пидксуникоде</strong> , является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="ef74e-160">Some common causes include the <strong>pidxunicode</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure is NULL, or the LCID specified in the <strong>pidxunicode</strong> structure is invalid.</span></span></p></li>
<li><p><span data-ttu-id="ef74e-161">Указание столбца с несколькими значениями для первичного индекса.</span><span class="sxs-lookup"><span data-stu-id="ef74e-161">Specifying a multi-valued column for a primary index.</span></span></p></li>
<li><p><span data-ttu-id="ef74e-162">Попытка индексировать слишком много условных столбцов.</span><span class="sxs-lookup"><span data-stu-id="ef74e-162">Trying to index too many conditional columns.</span></span> <span data-ttu-id="ef74e-163">Элемент <strong>ккондитионалколумн</strong> структуры <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> не должен быть больше JET_ccolKeyMost.</span><span class="sxs-lookup"><span data-stu-id="ef74e-163">The <strong>cConditionalColumn</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure must not be greater than JET_ccolKeyMost.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef74e-164">JET_errIndexTuplesInvalidLimits</span><span class="sxs-lookup"><span data-stu-id="ef74e-164">JET_errIndexTuplesInvalidLimits</span></span></p></td>
<td><p><span data-ttu-id="ef74e-165">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="ef74e-165">Windows XP and later.</span></span> <span data-ttu-id="ef74e-166">Указана структура <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> , а ее ограничения не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="ef74e-166">A <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure was specified, and its limits are not supported.</span></span> <span data-ttu-id="ef74e-167">См. раздел "Примечания" структуры <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> .</span><span class="sxs-lookup"><span data-stu-id="ef74e-167">See the remarks section of the <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef74e-168">JET_errIndexTuplesNonUniqueOnly</span><span class="sxs-lookup"><span data-stu-id="ef74e-168">JET_errIndexTuplesNonUniqueOnly</span></span></p></td>
<td><p><span data-ttu-id="ef74e-169">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="ef74e-169">Windows XP and later.</span></span> <span data-ttu-id="ef74e-170">Индекс кортежа не может быть уникальным (т. е. элемент <em>грбит</em> структуры <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> не должен иметь одновременно JET_bitIndexPrimary и JET_bitIndexUnique).</span><span class="sxs-lookup"><span data-stu-id="ef74e-170">A tuple index cannot be unique (that is, the <em>grbit</em> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure must not have both JET_bitIndexPrimary and JET_bitIndexUnique set).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef74e-171">JET_errIndexTuplesOneColumnOnly</span><span class="sxs-lookup"><span data-stu-id="ef74e-171">JET_errIndexTuplesOneColumnOnly</span></span></p></td>
<td><p><span data-ttu-id="ef74e-172">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="ef74e-172">Windows XP and later.</span></span> <span data-ttu-id="ef74e-173">Индекс кортежа может находиться только в одном столбце (т. е. Если элемент <strong>грбит</strong> структуры <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> JET_bitIndexTuples задан, а элемент <strong>сзкэй</strong> структуры <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> указывает более одного столбца).</span><span class="sxs-lookup"><span data-stu-id="ef74e-173">A tuple index can only be over a single column (that is, if the <strong>grbit</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure has JET_bitIndexTuples set, and the <strong>szKey</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure specifies more than one column).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef74e-174">JET_errIndexTuplesSecondaryIndexOnly</span><span class="sxs-lookup"><span data-stu-id="ef74e-174">JET_errIndexTuplesSecondaryIndexOnly</span></span></p></td>
<td><p><span data-ttu-id="ef74e-175">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="ef74e-175">Windows XP and later.</span></span> <span data-ttu-id="ef74e-176">Индекс кортежа не может быть первичным индексом (т. е. элемент <strong>грбит</strong> структуры <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> не должен иметь одновременно JET_bitIndexPrimary и JET_bitIndexTuples).</span><span class="sxs-lookup"><span data-stu-id="ef74e-176">A tuple index cannot be a primary index (that is, the <strong>grbit</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure must not have both JET_bitIndexPrimary and JET_bitIndexTuples set).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef74e-177">JET_errIndexTuplesTextColumnsOnly</span><span class="sxs-lookup"><span data-stu-id="ef74e-177">JET_errIndexTuplesTextColumnsOnly</span></span></p></td>
<td><p><span data-ttu-id="ef74e-178">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="ef74e-178">Windows XP and later.</span></span> <span data-ttu-id="ef74e-179">Индекс кортежа может находиться только в тексте или столбце Юникода.</span><span class="sxs-lookup"><span data-stu-id="ef74e-179">A tuple index can only be on a text or Unicode column.</span></span> <span data-ttu-id="ef74e-180">Попытка индексировать другие столбцы (например, двоичные столбцы) приведет к JET_errIndexTuplesTextColumnsOnly.</span><span class="sxs-lookup"><span data-stu-id="ef74e-180">An attempt to index other columns (such as binary columns) will result in JET_errIndexTuplesTextColumnsOnly.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef74e-181">JET_errIndexTuplesVarSegMacNotAllowed</span><span class="sxs-lookup"><span data-stu-id="ef74e-181">JET_errIndexTuplesVarSegMacNotAllowed</span></span></p></td>
<td><p><span data-ttu-id="ef74e-182">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="ef74e-182">Windows XP and later.</span></span> <span data-ttu-id="ef74e-183">Индекс кортежа не позволяет установить элемент <strong>кбварсегмак</strong> структуры <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</span><span class="sxs-lookup"><span data-stu-id="ef74e-183">A tuple index does not allow the <strong>cbVarSegMac</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure to be set.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef74e-184">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="ef74e-184">JET_errInTransaction</span></span></p></td>
<td><p><span data-ttu-id="ef74e-185">Предпринята попытка создать индекс без сведений о версии во время транзакции.</span><span class="sxs-lookup"><span data-stu-id="ef74e-185">An attempt was made to create an index without version information while in a transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef74e-186">JET_errInvalidCodePage</span><span class="sxs-lookup"><span data-stu-id="ef74e-186">JET_errInvalidCodePage</span></span></p></td>
<td><p><span data-ttu-id="ef74e-187">Элементу <strong>CP</strong> структуры <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> не задана допустимая кодовая страница.</span><span class="sxs-lookup"><span data-stu-id="ef74e-187">The <strong>cp</strong> member of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structure was not set to a valid code page.</span></span> <span data-ttu-id="ef74e-188">Единственными допустимыми значениями для текстовых столбцов являются английский (1252) и Unicode (1200).</span><span class="sxs-lookup"><span data-stu-id="ef74e-188">The only valid values for text columns are English (1252) and Unicode (1200).</span></span> <span data-ttu-id="ef74e-189">Значение 0 означает, что будет использоваться по умолчанию (английский, 1252).</span><span class="sxs-lookup"><span data-stu-id="ef74e-189">A value of 0 means the default will be used (English, 1252).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef74e-190">JET_errInvalidColumnType</span><span class="sxs-lookup"><span data-stu-id="ef74e-190">JET_errInvalidColumnType</span></span></p></td>
<td><p><span data-ttu-id="ef74e-191">Элементу <strong>колтип</strong> структуры <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> не был задан допустимый тип столбца.</span><span class="sxs-lookup"><span data-stu-id="ef74e-191">The <strong>coltyp</strong> member of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structure was not set to a valid column type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef74e-192">JET_errInvalidCreateIndex</span><span class="sxs-lookup"><span data-stu-id="ef74e-192">JET_errInvalidCreateIndex</span></span></p></td>
<td><p><span data-ttu-id="ef74e-193">Некоторые причины этой ошибки могут возникнуть:</span><span class="sxs-lookup"><span data-stu-id="ef74e-193">Some of the reasons this error may occur:</span></span></p>
<ul>
<li><p><span data-ttu-id="ef74e-194">Элементу <strong>ргиндекскреате</strong> структуры <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> присвоено значение null.</span><span class="sxs-lookup"><span data-stu-id="ef74e-194">The <strong>rgindexcreate</strong> member of the <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure was set to NULL.</span></span></p></li>
<li><p><span data-ttu-id="ef74e-195">Элементу <strong>ргколумнкреате</strong> структуры <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> присвоено значение null.</span><span class="sxs-lookup"><span data-stu-id="ef74e-195">The <strong>rgcolumncreate</strong> member of the <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure was set to NULL.</span></span></p></li>
<li><p><span data-ttu-id="ef74e-196">Элементу <strong>кбструкт</strong> структуры <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> не было присвоено допустимое значение.</span><span class="sxs-lookup"><span data-stu-id="ef74e-196">The <strong>cbStruct</strong> member of a <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure was not set to a valid value.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef74e-197">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="ef74e-197">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="ef74e-198">В <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> или <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a>указано недопустимое сочетание элементов <strong>грбит</strong> .</span><span class="sxs-lookup"><span data-stu-id="ef74e-198">An invalid combination of <strong>grbit</strong> members was specified in <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> or <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a>.</span></span></p>
<p><span data-ttu-id="ef74e-199">Определение индекса недопустимо, так как элемент <strong>грбит</strong> содержит неправильные значения.</span><span class="sxs-lookup"><span data-stu-id="ef74e-199">The index definition is invalid because the <strong>grbit</strong> member contains inconsistent values.</span></span> <span data-ttu-id="ef74e-200">Возможные причины:</span><span class="sxs-lookup"><span data-stu-id="ef74e-200">Some possible reasons are:</span></span></p>
<ul>
<li><p><span data-ttu-id="ef74e-201">Для первичного индекса задан бит игнорирования (то есть JET_bitIndexPrimary передан с JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull или JET_bitIndexIgnoreFirstNull).</span><span class="sxs-lookup"><span data-stu-id="ef74e-201">A primary index had an ignore bit specified (that is, JET_bitIndexPrimary was passed with JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull, or JET_bitIndexIgnoreFirstNull).</span></span></p></li>
<li><p><span data-ttu-id="ef74e-202">Пустой индекс не игнорирует все элементы NULL (т. е. элемент <strong>грбит</strong> структуры <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> JET_bitIndexEmpty установлен, но не имеет JET_bitIndexIgnoreAnyNull).</span><span class="sxs-lookup"><span data-stu-id="ef74e-202">An empty index does not ignore any NULL members (that is, the <strong>grbit</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure has JET_bitIndexEmpty set, but does not have JET_bitIndexIgnoreAnyNull set).</span></span></p></li>
<li><p><span data-ttu-id="ef74e-203">Передача структуры <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> с недопустимым элементом <strong>грбит</strong> .</span><span class="sxs-lookup"><span data-stu-id="ef74e-203">Passing in a <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> structure with an invalid <strong>grbit</strong> member.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef74e-204">JET_errInvalidLanguageId</span><span class="sxs-lookup"><span data-stu-id="ef74e-204">JET_errInvalidLanguageId</span></span></p></td>
<td><p><span data-ttu-id="ef74e-205">Передан недопустимый код локали (LCID) (либо с помощью элемента <strong>LCID</strong> структуры <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> , на который указывает элемент <strong>пидксуникоде</strong> в структуре <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> , либо с помощью поля <strong>LCID</strong> структуры <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> ).</span><span class="sxs-lookup"><span data-stu-id="ef74e-205">An invalid Locale ID (LCID) was passed in (either through the <strong>lcid</strong> member of the <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> structure which is pointed to by the <strong>pidxunicode</strong> member in the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure, or through the <strong>lcid</strong> field of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef74e-206">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="ef74e-206">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="ef74e-207">Указан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="ef74e-207">An invalid parameter was given.</span></span> <span data-ttu-id="ef74e-208">Возможные причины:</span><span class="sxs-lookup"><span data-stu-id="ef74e-208">Some possible reasons are:</span></span></p>
<ul>
<li><p><span data-ttu-id="ef74e-209">Элемент <strong>ргколумнкреате</strong> структуры <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> имеет значение null.</span><span class="sxs-lookup"><span data-stu-id="ef74e-209">The <strong>rgcolumncreate</strong> member of the <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure is NULL.</span></span></p></li>
<li><p><span data-ttu-id="ef74e-210">Элемент <strong>кбструкт</strong> одной из структур <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> , указанных в элементе <strong>ргколумнкреате</strong> структуры <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> , не был задан как sizeof (JET_COLUMNCREATE).</span><span class="sxs-lookup"><span data-stu-id="ef74e-210">The <strong>cbStruct</strong> member of one of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structures given in the <strong>rgcolumncreate</strong> member of the <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure was not set to sizeof( JET_COLUMNCREATE).</span></span></p></li>
<li><p><span data-ttu-id="ef74e-211">Элемент <strong>cbKey</strong> структуры <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> имеет значение 0.</span><span class="sxs-lookup"><span data-stu-id="ef74e-211">The <strong>cbKey</strong> member of a <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure is set to zero.</span></span></p></li>
<li><p><span data-ttu-id="ef74e-212">Элементу <strong>кбструкт</strong> структуры <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> не присвоено значение sizeof (JET_INDEXCREATE).</span><span class="sxs-lookup"><span data-stu-id="ef74e-212">The <strong>cbStruct</strong> member of a <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure is not set to sizeof( JET_INDEXCREATE).</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef74e-213">JET_errRecordTooBig</span><span class="sxs-lookup"><span data-stu-id="ef74e-213">JET_errRecordTooBig</span></span></p></td>
<td><p><span data-ttu-id="ef74e-214">Запись слишком велика.</span><span class="sxs-lookup"><span data-stu-id="ef74e-214">The record is too big.</span></span> <span data-ttu-id="ef74e-215">Сумма элемента <strong>кбмакс</strong> структуры <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> для всех фиксированных столбцов не должна превышать определенное значение.</span><span class="sxs-lookup"><span data-stu-id="ef74e-215">The sum of the <strong>cbMax</strong> member of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structure for all fixed columns must not exceed a certain value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef74e-216">JET_errTableDuplicate</span><span class="sxs-lookup"><span data-stu-id="ef74e-216">JET_errTableDuplicate</span></span></p></td>
<td><p><span data-ttu-id="ef74e-217">Таблица уже существует.</span><span class="sxs-lookup"><span data-stu-id="ef74e-217">The table already exists.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef74e-218">JET_errTooManyColumns</span><span class="sxs-lookup"><span data-stu-id="ef74e-218">JET_errTooManyColumns</span></span></p></td>
<td><p><span data-ttu-id="ef74e-219">Предпринята попытка добавить в таблицу слишком много столбцов.</span><span class="sxs-lookup"><span data-stu-id="ef74e-219">An attempt was made to add too many columns to the table.</span></span> <span data-ttu-id="ef74e-220">Таблица может содержать не более JET_ccolFixedMost фиксированных столбцов, не более JET_ccolVarMost столбцов переменной длины и не более JET_ccolTaggedMost столбцов с тегами.</span><span class="sxs-lookup"><span data-stu-id="ef74e-220">A table can have no more than JET_ccolFixedMost fixed columns, no more than JET_ccolVarMost variable-length columns, and no more than JET_ccolTaggedMost tagged columns.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef74e-221">JET_errUnicodeTranslationFail</span><span class="sxs-lookup"><span data-stu-id="ef74e-221">JET_errUnicodeTranslationFail</span></span></p></td>
<td><p><span data-ttu-id="ef74e-222">Произошла ошибка при попытке нормализовать столбец в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="ef74e-222">An error occurred attempting to normalize a Unicode column.</span></span> <span data-ttu-id="ef74e-223">Это может быть вызвано недостатком системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ef74e-223">This can be caused by running out of system resources.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="ef74e-224">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ef74e-224">Remarks</span></span>

<span data-ttu-id="ef74e-225">Вызов **жеткреатетаблеколумниндекс** идентичен вызову [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md), при этом каждое поле в структуре [JET_TABLECREATE2](./jet-tablecreate2-structure.md) содержит значение соответствующего поля [JET_TABLECREATE](./jet-tablecreate-structure.md)со следующими исключениями:</span><span class="sxs-lookup"><span data-stu-id="ef74e-225">Calling **JetCreateTableColumnIndex** is identical to calling [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md), with each field in the [JET_TABLECREATE2](./jet-tablecreate2-structure.md) structure containing the value of the corresponding field of [JET_TABLECREATE](./jet-tablecreate-structure.md), with the following exceptions:</span></span>

  - <span data-ttu-id="ef74e-226">JET_TABLECREATE2. Кбструкт задано значение sizeof (JET_TABLECREATE2)</span><span class="sxs-lookup"><span data-stu-id="ef74e-226">JET_TABLECREATE2.cbStruct set to sizeof( JET_TABLECREATE2)</span></span>

  - <span data-ttu-id="ef74e-227">JET_TABLECREATE2. Сзкаллбакк имеет значение NULL</span><span class="sxs-lookup"><span data-stu-id="ef74e-227">JET_TABLECREATE2.szCallback set to NULL</span></span>

  - <span data-ttu-id="ef74e-228">JET_TABLECREATE2. кбтип имеет значение 0</span><span class="sxs-lookup"><span data-stu-id="ef74e-228">JET_TABLECREATE2.cbtyp set to 0</span></span>

<span data-ttu-id="ef74e-229">Дополнительные сведения см. в разделе [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md) .</span><span class="sxs-lookup"><span data-stu-id="ef74e-229">See [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md) for more details.</span></span>

<span data-ttu-id="ef74e-230">Как и [жетопентабле](./jetopentable-function.md), когда приложение выполняется с помощью возвращенного *TableID*, оно обычно должно быть закрыто с помощью [жетклосетабле](./jetclosetable-function.md).</span><span class="sxs-lookup"><span data-stu-id="ef74e-230">Like [JetOpenTable](./jetopentable-function.md), when the application is done using the returned *tableid*, it should usually be closed with [JetCloseTable](./jetclosetable-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="ef74e-231">Требования</span><span class="sxs-lookup"><span data-stu-id="ef74e-231">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ef74e-232"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="ef74e-232"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="ef74e-233">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="ef74e-233">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef74e-234"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="ef74e-234"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="ef74e-235">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="ef74e-235">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef74e-236"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="ef74e-236"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="ef74e-237">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="ef74e-237">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef74e-238"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="ef74e-238"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="ef74e-239">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="ef74e-239">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef74e-240"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="ef74e-240"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="ef74e-241">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="ef74e-241">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef74e-242"><strong>Юникод</strong></span><span class="sxs-lookup"><span data-stu-id="ef74e-242"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="ef74e-243">Реализуется как <strong>жеткреатетаблеколумниндексв</strong> (Юникод) и <strong>жеткреатетаблеколумниндекса</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="ef74e-243">Implemented as <strong>JetCreateTableColumnIndexW</strong> (Unicode) and <strong>JetCreateTableColumnIndexA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="ef74e-244">См. также:</span><span class="sxs-lookup"><span data-stu-id="ef74e-244">See Also</span></span>

[<span data-ttu-id="ef74e-245">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="ef74e-245">JET_DBID</span></span>](./jet-dbid.md)  
[<span data-ttu-id="ef74e-246">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="ef74e-246">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="ef74e-247">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="ef74e-247">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="ef74e-248">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="ef74e-248">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="ef74e-249">JET_TABLECREATE</span><span class="sxs-lookup"><span data-stu-id="ef74e-249">JET_TABLECREATE</span></span>](./jet-tablecreate-structure.md)  
[<span data-ttu-id="ef74e-250">JET_TABLECREATE2</span><span class="sxs-lookup"><span data-stu-id="ef74e-250">JET_TABLECREATE2</span></span>](./jet-tablecreate2-structure.md)  
[<span data-ttu-id="ef74e-251">жетаддколумн</span><span class="sxs-lookup"><span data-stu-id="ef74e-251">JetAddColumn</span></span>](./jetaddcolumn-function.md)  
[<span data-ttu-id="ef74e-252">жеткреатетаблеколумниндекс</span><span class="sxs-lookup"><span data-stu-id="ef74e-252">JetCreateTableColumnIndex</span></span>]()  
[<span data-ttu-id="ef74e-253">JetCreateTableColumnIndex2</span><span class="sxs-lookup"><span data-stu-id="ef74e-253">JetCreateTableColumnIndex2</span></span>](./jetcreatetablecolumnindex2-function.md)
