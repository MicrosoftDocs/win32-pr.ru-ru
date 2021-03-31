---
description: Дополнительные сведения о функции Жетопентабле
title: Функция JetOpenTable
TOCTitle: JetOpenTable Function
ms:assetid: ded6348c-a82a-49bc-8a5d-e40ed5d6315c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294118(v=EXCHG.10)
ms:contentKeyID: 32765732
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenTable
- JetOpenTableW
- JetOpenTableA
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7a3ffe9490b75606910c5867d3e8b59d9a8c520d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808429"
---
# <a name="jetopentable-function"></a><span data-ttu-id="9ae17-103">Функция JetOpenTable</span><span class="sxs-lookup"><span data-stu-id="9ae17-103">JetOpenTable Function</span></span>


<span data-ttu-id="9ae17-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="9ae17-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetopentable-function"></a><span data-ttu-id="9ae17-105">Функция JetOpenTable</span><span class="sxs-lookup"><span data-stu-id="9ae17-105">JetOpenTable Function</span></span>

<span data-ttu-id="9ae17-106">Функция **жетопентабле** открывает курсор в ранее созданной таблице.</span><span class="sxs-lookup"><span data-stu-id="9ae17-106">The **JetOpenTable** function opens a cursor on a previously created table.</span></span>

```cpp
    JET_ERR JET_API JetOpenTable(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          const tchar* szTableName,
      __in_opt      const void* pvParameters,
      __in          unsigned long cbParameters,
      __in          JET_GRBIT grbit,
      __out         JET_TABLEID* ptableid
    );
```

### <a name="parameters"></a><span data-ttu-id="9ae17-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="9ae17-107">Parameters</span></span>

<span data-ttu-id="9ae17-108">*сесид*</span><span class="sxs-lookup"><span data-stu-id="9ae17-108">*sesid*</span></span>

<span data-ttu-id="9ae17-109">Используемый контекст сеанса базы данных.</span><span class="sxs-lookup"><span data-stu-id="9ae17-109">The database session context to use.</span></span>

<span data-ttu-id="9ae17-110">*DBID*</span><span class="sxs-lookup"><span data-stu-id="9ae17-110">*dbid*</span></span>

<span data-ttu-id="9ae17-111">Идентификатор базы данных, используемый для поиска таблицы.</span><span class="sxs-lookup"><span data-stu-id="9ae17-111">The database identifier to use to find the table.</span></span>

<span data-ttu-id="9ae17-112">*сзтабленаме*</span><span class="sxs-lookup"><span data-stu-id="9ae17-112">*szTableName*</span></span>

<span data-ttu-id="9ae17-113">Имя открываемой таблицы.</span><span class="sxs-lookup"><span data-stu-id="9ae17-113">The name of the table to open.</span></span>

<span data-ttu-id="9ae17-114">*пвпараметерс*</span><span class="sxs-lookup"><span data-stu-id="9ae17-114">*pvParameters*</span></span>

<span data-ttu-id="9ae17-115">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="9ae17-115">Deprecated.</span></span> <span data-ttu-id="9ae17-116">Задайте **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="9ae17-116">Set to **NULL**.</span></span>

<span data-ttu-id="9ae17-117">*кбпараметерс*</span><span class="sxs-lookup"><span data-stu-id="9ae17-117">*cbParameters*</span></span>

<span data-ttu-id="9ae17-118">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="9ae17-118">Deprecated.</span></span> <span data-ttu-id="9ae17-119">Задайте значение 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="9ae17-119">Set to 0 (zero).</span></span>

<span data-ttu-id="9ae17-120">*грбит*</span><span class="sxs-lookup"><span data-stu-id="9ae17-120">*grbit*</span></span>

<span data-ttu-id="9ae17-121">Группа битов, задающая ноль или более следующих параметров.</span><span class="sxs-lookup"><span data-stu-id="9ae17-121">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9ae17-122">Значение</span><span class="sxs-lookup"><span data-stu-id="9ae17-122">Value</span></span></p></th>
<th><p><span data-ttu-id="9ae17-123">Значение</span><span class="sxs-lookup"><span data-stu-id="9ae17-123">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9ae17-124">JET_bitTableDenyRead</span><span class="sxs-lookup"><span data-stu-id="9ae17-124">JET_bitTableDenyRead</span></span></p></td>
<td><p><span data-ttu-id="9ae17-125">Невозможно открыть таблицу для доступа на чтение в другом сеансе базы данных.</span><span class="sxs-lookup"><span data-stu-id="9ae17-125">The table cannot be opened for read-access by another database session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ae17-126">JET_bitTableDenyWrite</span><span class="sxs-lookup"><span data-stu-id="9ae17-126">JET_bitTableDenyWrite</span></span></p></td>
<td><p><span data-ttu-id="9ae17-127">Невозможно открыть таблицу для доступа на запись в другом сеансе базы данных.</span><span class="sxs-lookup"><span data-stu-id="9ae17-127">The table cannot be opened for write-access by another database session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ae17-128">JET_bitTableNoCache</span><span class="sxs-lookup"><span data-stu-id="9ae17-128">JET_bitTableNoCache</span></span></p></td>
<td><p><span data-ttu-id="9ae17-129">Не кэшировать страницы для этой таблицы.</span><span class="sxs-lookup"><span data-stu-id="9ae17-129">Do not cache the pages for this table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ae17-130">JET_bitTablePermitDDL</span><span class="sxs-lookup"><span data-stu-id="9ae17-130">JET_bitTablePermitDDL</span></span></p></td>
<td><p><span data-ttu-id="9ae17-131">Разрешает изменение DDL для таблиц, помеченных как Фикседддл.</span><span class="sxs-lookup"><span data-stu-id="9ae17-131">Allows DDL modification on tables flagged as FixedDDL.</span></span> <span data-ttu-id="9ae17-132">Этот параметр следует использовать с параметром JET_bitTableDenyRead.</span><span class="sxs-lookup"><span data-stu-id="9ae17-132">This option must be used with the JET_bitTableDenyRead option.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ae17-133">JET_bitTablePreread</span><span class="sxs-lookup"><span data-stu-id="9ae17-133">JET_bitTablePreread</span></span></p></td>
<td><p><span data-ttu-id="9ae17-134">Предоставляет указание о том, что таблица, вероятно, не находится в буферном кэше, и что предварительное чтение может быть полезно для повышения производительности.</span><span class="sxs-lookup"><span data-stu-id="9ae17-134">Provides a hint that the table is probably not in the buffer cache, and that pre-reading may be beneficial to performance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ae17-135">JET_bitTableReadOnly</span><span class="sxs-lookup"><span data-stu-id="9ae17-135">JET_bitTableReadOnly</span></span></p></td>
<td><p><span data-ttu-id="9ae17-136">Запрашивает доступ только для чтения к таблице.</span><span class="sxs-lookup"><span data-stu-id="9ae17-136">Requests read-only access to the table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ae17-137">JET_bitTableSequential</span><span class="sxs-lookup"><span data-stu-id="9ae17-137">JET_bitTableSequential</span></span></p></td>
<td><p><span data-ttu-id="9ae17-138">Таблица должна быть очень агрессивно выбиралась с диска, так как приложение будет сканировать его последовательно.</span><span class="sxs-lookup"><span data-stu-id="9ae17-138">The table should be very aggressively prefetched from disk because the application will be scanning it sequentially.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ae17-139">JET_bitTableUpdatable</span><span class="sxs-lookup"><span data-stu-id="9ae17-139">JET_bitTableUpdatable</span></span></p></td>
<td><p><span data-ttu-id="9ae17-140">Запрашивает доступ на запись к таблице.</span><span class="sxs-lookup"><span data-stu-id="9ae17-140">Requests write-access to the table.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9ae17-141">*pTableID*</span><span class="sxs-lookup"><span data-stu-id="9ae17-141">*ptableid*</span></span>

<span data-ttu-id="9ae17-142">При успешном выполнении указывает на идентификатор таблицы.</span><span class="sxs-lookup"><span data-stu-id="9ae17-142">On success, points to the identifier of the table.</span></span> <span data-ttu-id="9ae17-143">При сбое содержимое для *pTableID* не определено.</span><span class="sxs-lookup"><span data-stu-id="9ae17-143">On failure, the contents for *ptableid* are undefined.</span></span>

### <a name="return-value"></a><span data-ttu-id="9ae17-144">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9ae17-144">Return Value</span></span>

<span data-ttu-id="9ae17-145">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="9ae17-145">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="9ae17-146">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="9ae17-146">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9ae17-147">Код возврата</span><span class="sxs-lookup"><span data-stu-id="9ae17-147">Return code</span></span></p></th>
<th><p><span data-ttu-id="9ae17-148">Описание</span><span class="sxs-lookup"><span data-stu-id="9ae17-148">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9ae17-149">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="9ae17-149">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="9ae17-150">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="9ae17-150">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ae17-151">JET_errInvalidDatabaseId</span><span class="sxs-lookup"><span data-stu-id="9ae17-151">JET_errInvalidDatabaseId</span></span></p></td>
<td><p><span data-ttu-id="9ae17-152"><em>DBID</em> не является допустимым идентификатором базы данных.</span><span class="sxs-lookup"><span data-stu-id="9ae17-152"><em>dbid</em> is not a valid database identifier.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ae17-153">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="9ae17-153">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="9ae17-154">Передано неправильное сочетание <em>грбит</em> .</span><span class="sxs-lookup"><span data-stu-id="9ae17-154">A bad combination of <em>grbit</em> was passed in.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ae17-155">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="9ae17-155">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="9ae17-156">Имя, указанное в <em>сзтабленаме</em> , является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="9ae17-156">The name given in <em>szTableName</em> is invalid.</span></span></p>
<p><span data-ttu-id="9ae17-157">Дополнительные сведения о допустимых именах таблиц см. в описании параметра <em>сзтабленаме</em> в <a href="gg269210(v=exchg.10).md">жеткреатетабле</a>.</span><span class="sxs-lookup"><span data-stu-id="9ae17-157">For more information about valid table names, see the <em>szTableName</em> parameter in <a href="gg269210(v=exchg.10).md">JetCreateTable</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ae17-158">JET_errObjectNotFound</span><span class="sxs-lookup"><span data-stu-id="9ae17-158">JET_errObjectNotFound</span></span></p></td>
<td><p><span data-ttu-id="9ae17-159">Была предпринята попытка открыть таблицу, которая не существует в базе данных.</span><span class="sxs-lookup"><span data-stu-id="9ae17-159">An attempt was made to open a table that does not exist in the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ae17-160">JET_errOutOfCursors</span><span class="sxs-lookup"><span data-stu-id="9ae17-160">JET_errOutOfCursors</span></span></p></td>
<td><p><span data-ttu-id="9ae17-161">Не удалось выполнить операцию, так как подсистема не может выделить ресурсы, необходимые для открытия нового курсора.</span><span class="sxs-lookup"><span data-stu-id="9ae17-161">The operation failed because the engine cannot allocate the resources required to open a new cursor.</span></span> <span data-ttu-id="9ae17-162">См. раздел «Примечания».</span><span class="sxs-lookup"><span data-stu-id="9ae17-162">See the Remarks section.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ae17-163">JET_errTableInUse</span><span class="sxs-lookup"><span data-stu-id="9ae17-163">JET_errTableInUse</span></span></p></td>
<td><p><span data-ttu-id="9ae17-164">Таблица используется другой операцией базы данных.</span><span class="sxs-lookup"><span data-stu-id="9ae17-164">The table is being used by another database operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ae17-165">JET_wrnTableInUseBySystem</span><span class="sxs-lookup"><span data-stu-id="9ae17-165">JET_wrnTableInUseBySystem</span></span></p></td>
<td><p><span data-ttu-id="9ae17-166">Некритическое предупреждение, указывающее, что таблица используется системой.</span><span class="sxs-lookup"><span data-stu-id="9ae17-166">A nonfatal warning indicating that the table is being used by the system.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ae17-167">JET_errTableLocked</span><span class="sxs-lookup"><span data-stu-id="9ae17-167">JET_errTableLocked</span></span></p></td>
<td><p><span data-ttu-id="9ae17-168">Таблица заблокирована другой операцией базы данных.</span><span class="sxs-lookup"><span data-stu-id="9ae17-168">The table is locked by another database operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ae17-169">JET_errTooManyOpenTables</span><span class="sxs-lookup"><span data-stu-id="9ae17-169">JET_errTooManyOpenTables</span></span></p></td>
<td><p><span data-ttu-id="9ae17-170">Была предпринята попытка открыть слишком много уникальных таблиц одновременно.</span><span class="sxs-lookup"><span data-stu-id="9ae17-170">An attempt was made to open too many unique tables at once.</span></span> <span data-ttu-id="9ae17-171">См. раздел «Примечания».</span><span class="sxs-lookup"><span data-stu-id="9ae17-171">See the Remarks section.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="9ae17-172">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9ae17-172">Remarks</span></span>

<span data-ttu-id="9ae17-173">Таблицы, открытые с помощью **жетопентабле** , обычно должны быть закрыты с помощью [жетклосетабле](./jetclosetable-function.md).</span><span class="sxs-lookup"><span data-stu-id="9ae17-173">Tables opened with **JetOpenTable** should usually be closed with [JetCloseTable](./jetclosetable-function.md).</span></span> <span data-ttu-id="9ae17-174">Исключение из этого правила происходит при вызове **жетопентабле** в транзакции и откате транзакции (WITH [жетроллбакк](./jetrollback-function.md)).</span><span class="sxs-lookup"><span data-stu-id="9ae17-174">The exception to this rule happens when **JetOpenTable** is called in a transaction and the transaction is rolled back (with [JetRollback](./jetrollback-function.md)).</span></span> <span data-ttu-id="9ae17-175">При откате транзакции таблица автоматически закрывается.</span><span class="sxs-lookup"><span data-stu-id="9ae17-175">When rolling back a transaction, the table is automatically closed.</span></span> <span data-ttu-id="9ae17-176">В этом случае возникает ошибка при закрытии таблицы с помощью [жетклосетабле](./jetclosetable-function.md).</span><span class="sxs-lookup"><span data-stu-id="9ae17-176">In this case, it is an error to close the table with [JetCloseTable](./jetclosetable-function.md).</span></span>

<span data-ttu-id="9ae17-177">Допустимо открывать системные таблицы с помощью **жетопентабле** (например, Мсисобжектс, мсисуникодефиксуп).</span><span class="sxs-lookup"><span data-stu-id="9ae17-177">It is legal to open system tables with **JetOpenTable** (for example, MSysObjects, MSysUnicodeFixup).</span></span> <span data-ttu-id="9ae17-178">Схема системных таблиц может измениться, поэтому доступ к системным таблицам не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="9ae17-178">The schema of the system tables may change, so accessing system tables is discouraged.</span></span> <span data-ttu-id="9ae17-179">Количество уникальных таблиц, которые могут быть открыты одновременно, повлияет непосредственно на *JET_paramMaxOpenTables*.</span><span class="sxs-lookup"><span data-stu-id="9ae17-179">The number of unique tables that can be opened simultaneously is affected directly by *JET_paramMaxOpenTables*.</span></span> <span data-ttu-id="9ae17-180">Если таблица в данный момент открыта, в таблице будет создан новый курсор.</span><span class="sxs-lookup"><span data-stu-id="9ae17-180">If the table is currently open then a new cursor will be created on the table.</span></span> <span data-ttu-id="9ae17-181">Ресурсы курсора настраиваются с помощью [жетсетсистемпараметер](./jetsetsystemparameter-function.md) с *JET_paramMaxCursors*.</span><span class="sxs-lookup"><span data-stu-id="9ae17-181">Cursor resources are configured using [JetSetSystemParameter](./jetsetsystemparameter-function.md) with *JET_paramMaxCursors*.</span></span> <span data-ttu-id="9ae17-182">См. также [жетдупкурсор](./jetdupcursor-function.md).</span><span class="sxs-lookup"><span data-stu-id="9ae17-182">Also see [JetDupCursor](./jetdupcursor-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="9ae17-183">Требования</span><span class="sxs-lookup"><span data-stu-id="9ae17-183">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9ae17-184"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="9ae17-184"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="9ae17-185">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="9ae17-185">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ae17-186"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="9ae17-186"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="9ae17-187">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="9ae17-187">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ae17-188"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="9ae17-188"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="9ae17-189">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="9ae17-189">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ae17-190"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="9ae17-190"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="9ae17-191">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="9ae17-191">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ae17-192"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="9ae17-192"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="9ae17-193">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="9ae17-193">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ae17-194"><strong>Юникод</strong></span><span class="sxs-lookup"><span data-stu-id="9ae17-194"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="9ae17-195">Реализуется как <strong>жетопентаблев</strong> (Юникод) и <strong>жетопентаблеа</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="9ae17-195">Implemented as <strong>JetOpenTableW</strong> (Unicode) and <strong>JetOpenTableA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="9ae17-196">См. также:</span><span class="sxs-lookup"><span data-stu-id="9ae17-196">See Also</span></span>

[<span data-ttu-id="9ae17-197">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="9ae17-197">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="9ae17-198">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="9ae17-198">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="9ae17-199">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="9ae17-199">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="9ae17-200">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="9ae17-200">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="9ae17-201">жетклосетабле</span><span class="sxs-lookup"><span data-stu-id="9ae17-201">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="9ae17-202">жетдупкурсор</span><span class="sxs-lookup"><span data-stu-id="9ae17-202">JetDupCursor</span></span>](./jetdupcursor-function.md)  
[<span data-ttu-id="9ae17-203">жетроллбакк</span><span class="sxs-lookup"><span data-stu-id="9ae17-203">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="9ae17-204">жетсетсистемпараметер</span><span class="sxs-lookup"><span data-stu-id="9ae17-204">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="9ae17-205">Параметры ресурсов</span><span class="sxs-lookup"><span data-stu-id="9ae17-205">Resource Parameters</span></span>](./resource-parameters.md)
