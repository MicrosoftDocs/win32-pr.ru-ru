---
description: Дополнительные сведения о функции Жетопентемптабле
title: Функция JetOpenTempTable
TOCTitle: JetOpenTempTable Function
ms:assetid: 29261333-a1bc-4159-9046-c32c36f47410
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269211(v=EXCHG.10)
ms:contentKeyID: 32765514
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenTempTable
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 66c58abc5cff433bb4d944e39c283ba712d7cebf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692123"
---
# <a name="jetopentemptable-function"></a><span data-ttu-id="f2017-103">Функция JetOpenTempTable</span><span class="sxs-lookup"><span data-stu-id="f2017-103">JetOpenTempTable Function</span></span>


<span data-ttu-id="f2017-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="f2017-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetopentemptable-function"></a><span data-ttu-id="f2017-105">Функция JetOpenTempTable</span><span class="sxs-lookup"><span data-stu-id="f2017-105">JetOpenTempTable Function</span></span>

<span data-ttu-id="f2017-106">Функция **жетопентемптабле** создает временную таблицу с одним индексом.</span><span class="sxs-lookup"><span data-stu-id="f2017-106">The **JetOpenTempTable** function creates a temporary table with a single index.</span></span> <span data-ttu-id="f2017-107">Временная таблица хранит и извлекает записи так же, как обычная таблица, созданная с помощью [жеткреатетаблеколумниндекс](./jetcreatetablecolumnindex-function.md).</span><span class="sxs-lookup"><span data-stu-id="f2017-107">A temporary table stores and retrieves records just like an ordinary table created using [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md).</span></span> <span data-ttu-id="f2017-108">Однако временные таблицы выполняются гораздо быстрее, чем обычные таблицы, в связи с их постоянным характером.</span><span class="sxs-lookup"><span data-stu-id="f2017-108">However, temporary tables are much faster than ordinary tables due to their volatile nature.</span></span> <span data-ttu-id="f2017-109">Они также могут использоваться для очень быстрой сортировки и удаления дубликатов наборов записей при обращении к ним только последовательно.</span><span class="sxs-lookup"><span data-stu-id="f2017-109">They can also be used to very quickly sort and perform duplicate removal on record sets when accessed in a purely sequential manner.</span></span>

```cpp
    JET_ERR JET_API JetOpenTempTable(
      __in          JET_SESID sesid,
      __in          const JET_COLUMNDEF* prgcolumndef,
      __in          unsigned long ccolumn,
      __in          JET_GRBIT grbit,
      __out         JET_TABLEID* ptableid,
      __out         JET_COLUMNID* prgcolumnid
    );
```

### <a name="parameters"></a><span data-ttu-id="f2017-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="f2017-110">Parameters</span></span>

<span data-ttu-id="f2017-111">*сесид*</span><span class="sxs-lookup"><span data-stu-id="f2017-111">*sesid*</span></span>

<span data-ttu-id="f2017-112">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="f2017-112">The session to use.</span></span>

<span data-ttu-id="f2017-113">*пргколумндеф*</span><span class="sxs-lookup"><span data-stu-id="f2017-113">*prgcolumndef*</span></span>

<span data-ttu-id="f2017-114">Определения столбцов для столбцов, созданных во временной таблице.</span><span class="sxs-lookup"><span data-stu-id="f2017-114">Column definitions for the columns created in the temporary table.</span></span>

<span data-ttu-id="f2017-115">Для параметров определения столбца, используемых во временной таблице, имеются **важные** ограничения.</span><span class="sxs-lookup"><span data-stu-id="f2017-115">**Important**   limitations exist for the column definition options that are used with a temporary table.</span></span> <span data-ttu-id="f2017-116">Дополнительные сведения см. в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="f2017-116">See the Remarks section for more information.</span></span>

<span data-ttu-id="f2017-117">В дополнение к обычным параметрам определения столбца можно также указать ноль или более следующих параметров, которые важны только в контексте временной таблицы.</span><span class="sxs-lookup"><span data-stu-id="f2017-117">In addition to the usual column definition options, zero or more of the following options can also be specified that are relevant only in the context of a temporary table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f2017-118">Значение</span><span class="sxs-lookup"><span data-stu-id="f2017-118">Value</span></span></p></th>
<th><p><span data-ttu-id="f2017-119">Значение</span><span class="sxs-lookup"><span data-stu-id="f2017-119">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f2017-120">JET_bitColumnTTDescending</span><span class="sxs-lookup"><span data-stu-id="f2017-120">JET_bitColumnTTDescending</span></span></p></td>
<td><p><span data-ttu-id="f2017-121">Порядок сортировки ключевого столбца для временной таблицы должен быть по убыванию, а не по возрастанию.</span><span class="sxs-lookup"><span data-stu-id="f2017-121">The sort order of the key column for the temporary table should be descending rather than ascending.</span></span> <span data-ttu-id="f2017-122">Если этот параметр указан без JET_bitColumnTTKey то этот параметр игнорируется.</span><span class="sxs-lookup"><span data-stu-id="f2017-122">If this option is specified without JET_bitColumnTTKey then this option is ignored.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2017-123">JET_bitColumnTTKey</span><span class="sxs-lookup"><span data-stu-id="f2017-123">JET_bitColumnTTKey</span></span></p></td>
<td><p><span data-ttu-id="f2017-124">Столбец будет ключевым столбцом для временной таблицы.</span><span class="sxs-lookup"><span data-stu-id="f2017-124">The column will be a key column for the temporary table.</span></span></p>
<p><span data-ttu-id="f2017-125">Порядок определений столбцов с этим параметром, указанным во входном массиве, определяет приоритет каждого ключевого столбца для временной таблицы.</span><span class="sxs-lookup"><span data-stu-id="f2017-125">The order of the column definitions with this option specified in the input array will determine the precedence of each key column for the temporary table.</span></span> <span data-ttu-id="f2017-126">Первое определение столбца в массиве, для которого задан этот параметр, будет наиболее значимым ключевым столбцом и т. д.</span><span class="sxs-lookup"><span data-stu-id="f2017-126">The first column definition in the array that has this option set will be the most significant key column and so on.</span></span> <span data-ttu-id="f2017-127">Если запрошено больше ключевых столбцов, чем может поддерживать ядро СУБД, этот параметр игнорируется для неподдерживаемых ключевых столбцов.</span><span class="sxs-lookup"><span data-stu-id="f2017-127">If more key columns are requested than can be supported by the database engine then this option is ignored for the unsupportable key columns.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f2017-128">*кколумн*</span><span class="sxs-lookup"><span data-stu-id="f2017-128">*ccolumn*</span></span>

<span data-ttu-id="f2017-129">См. *пргколумндеф*.</span><span class="sxs-lookup"><span data-stu-id="f2017-129">See *prgcolumndef*.</span></span>

<span data-ttu-id="f2017-130">*грбит*</span><span class="sxs-lookup"><span data-stu-id="f2017-130">*grbit*</span></span>

<span data-ttu-id="f2017-131">Группа битов, задающая ноль или более следующих параметров.</span><span class="sxs-lookup"><span data-stu-id="f2017-131">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f2017-132">Значение</span><span class="sxs-lookup"><span data-stu-id="f2017-132">Value</span></span></p></th>
<th><p><span data-ttu-id="f2017-133">Значение</span><span class="sxs-lookup"><span data-stu-id="f2017-133">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f2017-134">JET_bitTTErrorOnDuplicateInsertion</span><span class="sxs-lookup"><span data-stu-id="f2017-134">JET_bitTTErrorOnDuplicateInsertion</span></span></p></td>
<td><p><span data-ttu-id="f2017-135">Любая попытка вставить запись с тем же ключом индекса, что и ранее вставленная запись, сразу же завершится с JET_errKeyDuplicate.</span><span class="sxs-lookup"><span data-stu-id="f2017-135">Any attempt to insert a record with the same index key as a previously inserted record will immediately fail with JET_errKeyDuplicate.</span></span> <span data-ttu-id="f2017-136">Если этот параметр не запрашивается, то дубликат обнаруживается немедленно, завершается ошибкой или автоматически удаляется позже, в зависимости от стратегии, выбранной ядром СУБД для реализации временной таблицы в зависимости от запрошенной функциональности.</span><span class="sxs-lookup"><span data-stu-id="f2017-136">If this option is not requested then a duplicate is detected immediately and fails, or is silently removed later, depending on the strategy chosen by the database engine to implement the temporary table, based on the requested functionality.</span></span></p>
<p><span data-ttu-id="f2017-137">Если эта функция не требуется, то лучше не запрашивать ее.</span><span class="sxs-lookup"><span data-stu-id="f2017-137">If this functionality it not required then it is best to not request it.</span></span> <span data-ttu-id="f2017-138">Если эта функция не запрошена, то диспетчер временных таблиц может выбрать стратегию для управления временной таблицей, что приведет к повышению производительности.</span><span class="sxs-lookup"><span data-stu-id="f2017-138">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2017-139">JET_bitTTForceMaterialization</span><span class="sxs-lookup"><span data-stu-id="f2017-139">JET_bitTTForceMaterialization</span></span></p></td>
<td><p><span data-ttu-id="f2017-140">Заставляет диспетчер временных таблиц отменять поиск лучшей стратегии, используемой для управления временной таблицей, что приведет к повышенной производительности.</span><span class="sxs-lookup"><span data-stu-id="f2017-140">Forces the temporary table manager to abandon the search for the best strategy to use managing the temporary table that will result in enhanced performance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2017-141">JET_bitTTForwardOnly</span><span class="sxs-lookup"><span data-stu-id="f2017-141">JET_bitTTForwardOnly</span></span></p></td>
<td><p><span data-ttu-id="f2017-142">Временная таблица создается только в том случае, если диспетчер временных таблиц может использовать реализацию, оптимизированную для промежуточных результатов запроса.</span><span class="sxs-lookup"><span data-stu-id="f2017-142">The temporary table is only created if the temporary table manager can use the implementation that is optimized for intermediate query results.</span></span> <span data-ttu-id="f2017-143">Если любая характеристика временной таблицы не позволит использовать эту оптимизацию, операция завершится с JET_errCannotMaterializeForwardOnlySort.</span><span class="sxs-lookup"><span data-stu-id="f2017-143">If any characteristic of the temporary table would prevent the use of this optimization then the operation will fail with JET_errCannotMaterializeForwardOnlySort.</span></span></p>
<p><span data-ttu-id="f2017-144">Побочный результат этого параметра — Разрешить временной таблице содержать записи с повторяющимися ключами индекса.</span><span class="sxs-lookup"><span data-stu-id="f2017-144">A side effect of this option is to allow the temporary table to contain records with duplicate index keys.</span></span> <span data-ttu-id="f2017-145">Дополнительные сведения см. в разделе JET_bitTTUnique.</span><span class="sxs-lookup"><span data-stu-id="f2017-145">See JET_bitTTUnique for more information.</span></span></p>
<p><span data-ttu-id="f2017-146">Этот параметр доступен только в выпусках Windows Server 2003 и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="f2017-146">This option is only available on Windows Server 2003 and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2017-147">JET_bitTTIndexed</span><span class="sxs-lookup"><span data-stu-id="f2017-147">JET_bitTTIndexed</span></span></p></td>
<td><p><span data-ttu-id="f2017-148">Этот параметр требует, чтобы временная таблица была достаточно гибкой, чтобы позволить использовать <a href="gg294103(v=exchg.10).md">жетсик</a> для поиска записей по ключу индекса.</span><span class="sxs-lookup"><span data-stu-id="f2017-148">This option requests that the temporary table be flexible enough to permit the use of <a href="gg294103(v=exchg.10).md">JetSeek</a> to look up records by index key.</span></span></p>
<p><span data-ttu-id="f2017-149">Если эта функция не требуется, то лучше не запрашивать ее.</span><span class="sxs-lookup"><span data-stu-id="f2017-149">If this functionality it not required then it is best to not request it.</span></span> <span data-ttu-id="f2017-150">Если эта функция не запрошена, то диспетчер временных таблиц может выбрать стратегию для управления временной таблицей, что приведет к повышению производительности.</span><span class="sxs-lookup"><span data-stu-id="f2017-150">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2017-151">JET_bitTTUnique</span><span class="sxs-lookup"><span data-stu-id="f2017-151">JET_bitTTUnique</span></span></p></td>
<td><p><span data-ttu-id="f2017-152">Запросы, в которых записи с повторяющимися ключами индекса удаляются из окончательного набора записей во временной таблице.</span><span class="sxs-lookup"><span data-stu-id="f2017-152">Requests that records with duplicate index keys be removed from the final set of records in the temporary table.</span></span></p>
<p><span data-ttu-id="f2017-153">До Windows Server 2003 в ядре СУБД всегда предполагается, что этот параметр действует из-за того факта, что все кластеризованные индексы также должны быть первичным ключом и, таким же, должны быть уникальными.</span><span class="sxs-lookup"><span data-stu-id="f2017-153">Prior to Windows Server 2003, the database engine always assumed this option to be in effect due to the fact that all clustered indexes must also be a primary key and thus must be unique.</span></span> <span data-ttu-id="f2017-154">Начиная с Windows Server 2003, теперь можно создать временную таблицу, которая не удаляет дубликаты, если также указан параметр JET_bitTTForwardOnly.</span><span class="sxs-lookup"><span data-stu-id="f2017-154">As of Windows Server 2003, it is now possible to create a temporary table that does not remove duplicates when the JET_bitTTForwardOnly option is also specified.</span></span></p>
<p><span data-ttu-id="f2017-155">Невозможно выяснить, какие дубликаты будут выполнены, и какие дубликаты будут отменены в целом.</span><span class="sxs-lookup"><span data-stu-id="f2017-155">It is not possible to know which duplicate will succeed and which duplicates will be discarded, in general.</span></span> <span data-ttu-id="f2017-156">Однако при запросе параметра JET_bitTTErrorOnDuplicateInsertion первая запись с заданным ключом индекса для вставки во временную таблицу всегда будет выполнена.</span><span class="sxs-lookup"><span data-stu-id="f2017-156">However, when the JET_bitTTErrorOnDuplicateInsertion option is requested then the first record with a given index key to be inserted into the temporary table will always succeed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2017-157">JET_bitTTUpdatable</span><span class="sxs-lookup"><span data-stu-id="f2017-157">JET_bitTTUpdatable</span></span></p></td>
<td><p><span data-ttu-id="f2017-158">Требует, чтобы временная таблица была достаточно гибкой, чтобы разрешить впоследствии изменять ранее вставленные записи.</span><span class="sxs-lookup"><span data-stu-id="f2017-158">Requests that the temporary table be flexible enough to allow records that have previously been inserted to be subsequently changed.</span></span> <span data-ttu-id="f2017-159">Если эта функция не требуется, то лучше не запрашивать ее.</span><span class="sxs-lookup"><span data-stu-id="f2017-159">If this functionality it not required then it is best to not request it.</span></span></p>
<p><span data-ttu-id="f2017-160">Если эта функция не запрошена, то диспетчер временных таблиц может выбрать стратегию для управления временной таблицей, что приведет к повышению производительности.</span><span class="sxs-lookup"><span data-stu-id="f2017-160">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2017-161">JET_bitTTScrollable</span><span class="sxs-lookup"><span data-stu-id="f2017-161">JET_bitTTScrollable</span></span></p></td>
<td><p><span data-ttu-id="f2017-162">Требует, чтобы временная таблица была достаточно гибкой, чтобы можно было просматривать записи в произвольном порядке и в направлении с помощью <a href="gg294117(v=exchg.10).md">жетмове</a>.</span><span class="sxs-lookup"><span data-stu-id="f2017-162">Requests that the temporary table be flexible enough to allow records to be scanned in arbitrary order and direction using <a href="gg294117(v=exchg.10).md">JetMove</a>.</span></span></p>
<p><span data-ttu-id="f2017-163">Если эта функция не является обязательной, лучше не запрашивать ее.</span><span class="sxs-lookup"><span data-stu-id="f2017-163">If this functionality is not required then it is best to not request it.</span></span> <span data-ttu-id="f2017-164">Если эта функция не запрошена, то диспетчер временных таблиц может выбрать стратегию для управления временной таблицей, что приведет к повышению производительности.</span><span class="sxs-lookup"><span data-stu-id="f2017-164">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2017-165">JET_bitTTSortNullsHigh</span><span class="sxs-lookup"><span data-stu-id="f2017-165">JET_bitTTSortNullsHigh</span></span></p></td>
<td><p><span data-ttu-id="f2017-166">Запрашивает, что значения ключевого столбца NULL сортируются ближе к концу индекса, чем значения ключевого столбца, отличного от NULL.</span><span class="sxs-lookup"><span data-stu-id="f2017-166">Requests that NULL key column values sort closer to the end of the index than non-NULL key column values.</span></span></p>
<p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2017-167">JET_bitTTIntrinsicLVsOnly</span><span class="sxs-lookup"><span data-stu-id="f2017-167">JET_bitTTIntrinsicLVsOnly</span></span></p></td>
<td><p><span data-ttu-id="f2017-168">Запросы на разрешение только внутренних значений типа long.</span><span class="sxs-lookup"><span data-stu-id="f2017-168">Requests to permit only intrinsic long values.</span></span></p>
<p><span data-ttu-id="f2017-169"><strong>Windows 7</strong>: <strong>JET_bitTTIntrinsicLVsOnly</strong> введен в Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f2017-169"><strong>Windows 7</strong>: <strong>JET_bitTTIntrinsicLVsOnly</strong> is introduced in Windows 7.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f2017-170">*pTableID*</span><span class="sxs-lookup"><span data-stu-id="f2017-170">*ptableid*</span></span>

<span data-ttu-id="f2017-171">Выходной буфер, который получает новый курсор, Открытый во вновь созданной временной таблице.</span><span class="sxs-lookup"><span data-stu-id="f2017-171">The output buffer that receives the new cursor opened on the newly created temporary table.</span></span>

<span data-ttu-id="f2017-172">*пргколумнид*</span><span class="sxs-lookup"><span data-stu-id="f2017-172">*prgcolumnid*</span></span>

<span data-ttu-id="f2017-173">Выходной буфер, который получает массив идентификаторов столбцов, созданных во время создания временной таблицы.</span><span class="sxs-lookup"><span data-stu-id="f2017-173">The output buffer that receives the array of column IDs generated during the creation of the temporary table.</span></span>

<span data-ttu-id="f2017-174">Идентификаторы столбцов в этом массиве будут точно соответствовать входному массиву определений столбцов.</span><span class="sxs-lookup"><span data-stu-id="f2017-174">The column IDs in this array will exactly correspond to the input array of column definitions.</span></span> <span data-ttu-id="f2017-175">В результате размер этого буфера должен соответствовать размеру входного массива.</span><span class="sxs-lookup"><span data-stu-id="f2017-175">As a result, the size of this buffer must correspond to the size of the input array.</span></span>

### <a name="return-value"></a><span data-ttu-id="f2017-176">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f2017-176">Return Value</span></span>

<span data-ttu-id="f2017-177">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="f2017-177">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="f2017-178">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="f2017-178">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f2017-179">Код возврата</span><span class="sxs-lookup"><span data-stu-id="f2017-179">Return code</span></span></p></th>
<th><p><span data-ttu-id="f2017-180">Описание</span><span class="sxs-lookup"><span data-stu-id="f2017-180">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f2017-181">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="f2017-181">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="f2017-182">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="f2017-182">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2017-183">JET_errCannotMaterializeForwardOnlySort</span><span class="sxs-lookup"><span data-stu-id="f2017-183">JET_errCannotMaterializeForwardOnlySort</span></span></p></td>
<td><p><span data-ttu-id="f2017-184">Произошел сбой <strong>жетопентемптабле</strong> , так как указана JET_bitTTForwardOnly, а временная таблица указана не может быть создана с помощью оптимизации "только вперед".</span><span class="sxs-lookup"><span data-stu-id="f2017-184"><strong>JetOpenTempTable</strong> failed because JET_bitTTForwardOnly was specified and the temporary table as specified could not be created using the forward-only optimization.</span></span> <span data-ttu-id="f2017-185">Эта ошибка будет возвращена только в Windows Server 2003 и более поздних выпусках.</span><span class="sxs-lookup"><span data-stu-id="f2017-185">This error will only be returned by Windows Server 2003 and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2017-186">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="f2017-186">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="f2017-187">Невозможно выполнить операцию, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</span><span class="sxs-lookup"><span data-stu-id="f2017-187">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2017-188">JET_errIndexInvalidDef</span><span class="sxs-lookup"><span data-stu-id="f2017-188">JET_errIndexInvalidDef</span></span></p></td>
<td><p><span data-ttu-id="f2017-189">Не удалось создать индекс, так как было указано недопустимое определение индекса.</span><span class="sxs-lookup"><span data-stu-id="f2017-189">The index could not be created because an invalid index definition was specified.</span></span></p>
<p><span data-ttu-id="f2017-190"><strong>Жетопентемптабле</strong> будет возвращать эту ошибку в следующих случаях:</span><span class="sxs-lookup"><span data-stu-id="f2017-190"><strong>JetOpenTempTable</strong> will return this error when:</span></span></p>
<ul>
<li><p><span data-ttu-id="f2017-191">Указан языковой стандарт, не зависящий от языка.</span><span class="sxs-lookup"><span data-stu-id="f2017-191">The Language Neutral locale is specified.</span></span></p></li>
<li><p><span data-ttu-id="f2017-192">Указан недопустимый набор флагов нормализации.</span><span class="sxs-lookup"><span data-stu-id="f2017-192">An invalid set of normalization flags is specified.</span></span></p></li>
</ul>
<p><span data-ttu-id="f2017-193">Эта ошибка будет возвращена только Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="f2017-193">This error will only be returned by Windows 2000.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2017-194">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="f2017-194">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="f2017-195">Невозможно выполнить операцию, поскольку экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</span><span class="sxs-lookup"><span data-stu-id="f2017-195">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="f2017-196">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="f2017-196">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2017-197">JET_errInvalidCodePage</span><span class="sxs-lookup"><span data-stu-id="f2017-197">JET_errInvalidCodePage</span></span></p></td>
<td><p><span data-ttu-id="f2017-198">Поле CP <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> не было задано как допустимая кодовая страница.</span><span class="sxs-lookup"><span data-stu-id="f2017-198">The cp field of the <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> was not set to a valid code page.</span></span> <span data-ttu-id="f2017-199">Единственными допустимыми значениями для текстовых столбцов являются английский (1252) и Unicode (1200).</span><span class="sxs-lookup"><span data-stu-id="f2017-199">The only valid values for text columns are English (1252) and Unicode (1200).</span></span> <span data-ttu-id="f2017-200">Значение 0 означает, что будет использоваться по умолчанию (английский, 1252).</span><span class="sxs-lookup"><span data-stu-id="f2017-200">A value of 0 means the default will be used (English, 1252).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2017-201">JET_errInvalidColumnType</span><span class="sxs-lookup"><span data-stu-id="f2017-201">JET_errInvalidColumnType</span></span></p></td>
<td><p><span data-ttu-id="f2017-202">Для поля <em>колтип</em> <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> не был задан допустимый тип столбца.</span><span class="sxs-lookup"><span data-stu-id="f2017-202">The <em>coltyp</em> field of the <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> was not set to a valid column type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2017-203">JET_errInvalidLanguageId</span><span class="sxs-lookup"><span data-stu-id="f2017-203">JET_errInvalidLanguageId</span></span></p></td>
<td><p><span data-ttu-id="f2017-204">Не удалось создать индекс, поскольку была предпринята попытка использовать недопустимый код локали.</span><span class="sxs-lookup"><span data-stu-id="f2017-204">The index could not be created because an attempt was made to use an invalid locale ID.</span></span> <span data-ttu-id="f2017-205">КОД локали может быть либо полностью недопустимым, либо связанный языковой пакет не может быть установлен.</span><span class="sxs-lookup"><span data-stu-id="f2017-205">The locale ID may either be completely invalid or the associated language pack may not be installed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2017-206">JET_errInvalidLCMapStringFlags</span><span class="sxs-lookup"><span data-stu-id="f2017-206">JET_errInvalidLCMapStringFlags</span></span></p></td>
<td><p><span data-ttu-id="f2017-207">Не удалось создать индекс, поскольку предпринята попытка использовать недопустимый набор флагов нормализации.</span><span class="sxs-lookup"><span data-stu-id="f2017-207">The index could not be created because an attempt was made to use an invalid set of normalization flags.</span></span> <span data-ttu-id="f2017-208">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="f2017-208">This error will only be returned by Windows XP and later releases.</span></span> <span data-ttu-id="f2017-209">В Windows 2000 недопустимые флаги нормализации приводят к JET_errIndexInvalidDef.</span><span class="sxs-lookup"><span data-stu-id="f2017-209">On Windows 2000, invalid normalization flags will result in JET_errIndexInvalidDef instead.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2017-210">JET_errInvalidSesid</span><span class="sxs-lookup"><span data-stu-id="f2017-210">JET_errInvalidSesid</span></span></p></td>
<td><p><span data-ttu-id="f2017-211">Недопустимый обработчик сеанса или ссылается на закрытый сеанс.</span><span class="sxs-lookup"><span data-stu-id="f2017-211">The session handle is invalid or refers to a closed session.</span></span></p>
<p><span data-ttu-id="f2017-212"><strong>Примечание</strong>  .  Эта ошибка не возвращается при всех обстоятельствах.</span><span class="sxs-lookup"><span data-stu-id="f2017-212"><strong>Note</strong>  This error is not returned under all circumstances.</span></span> <span data-ttu-id="f2017-213">Дескрипторы проверяются только на основе наилучшей силы.</span><span class="sxs-lookup"><span data-stu-id="f2017-213">Handles are validated on a best effort basis only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2017-214">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="f2017-214">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="f2017-215">Невозможно выполнить операцию, так как экземпляр, связанный с сеансом, еще не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="f2017-215">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2017-216">JET_errOutOfCursors</span><span class="sxs-lookup"><span data-stu-id="f2017-216">JET_errOutOfCursors</span></span></p></td>
<td><p><span data-ttu-id="f2017-217">Не удалось выполнить операцию, так как подсистема не может выделить ресурсы, необходимые для открытия нового курсора.</span><span class="sxs-lookup"><span data-stu-id="f2017-217">The operation failed because the engine cannot allocate the resources required to open a new cursor.</span></span> <span data-ttu-id="f2017-218">Ресурсы курсора настраиваются с помощью <a href="gg294044(v=exchg.10).md">жетсетсистемпараметер</a> с <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>.</span><span class="sxs-lookup"><span data-stu-id="f2017-218">Cursor resources are configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2017-219">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="f2017-219">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="f2017-220">Не удалось выполнить операцию из-за нехватки памяти, выделенной для ее завершения.</span><span class="sxs-lookup"><span data-stu-id="f2017-220">The operation failed because not enough memory could be allocated to complete it.</span></span></p>
<p><span data-ttu-id="f2017-221"><strong>Жетопентемптабле</strong> может возвращать JET_errOutOfMemory, если адресное пространство хост-процесса оказывается слишком фрагментированным.</span><span class="sxs-lookup"><span data-stu-id="f2017-221"><strong>JetOpenTempTable</strong> can return JET_errOutOfMemory if the address space of the host process becomes too fragmented.</span></span> <span data-ttu-id="f2017-222">Временный диспетчер таблиц всегда выделяет 1 МБ адресного пространства для каждой временной таблицы, созданной независимо от объема сохраняемых данных.</span><span class="sxs-lookup"><span data-stu-id="f2017-222">The temporary table manager will always allocate a 1MB chunk of address space for every temporary table created regardless of the amount of data to be stored.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2017-223">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="f2017-223">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="f2017-224">Невозможно выполнить операцию, так как в экземпляре, связанном с сеансом, выполняется операция восстановления.</span><span class="sxs-lookup"><span data-stu-id="f2017-224">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2017-225">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="f2017-225">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="f2017-226">Один и тот же сеанс нельзя использовать одновременно для нескольких потоков.</span><span class="sxs-lookup"><span data-stu-id="f2017-226">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="f2017-227">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="f2017-227">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2017-228">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="f2017-228">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="f2017-229">Невозможно выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</span><span class="sxs-lookup"><span data-stu-id="f2017-229">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2017-230">JET_errTooManyColumns</span><span class="sxs-lookup"><span data-stu-id="f2017-230">JET_errTooManyColumns</span></span></p></td>
<td><p><span data-ttu-id="f2017-231">Предпринята попытка добавить в таблицу слишком много столбцов.</span><span class="sxs-lookup"><span data-stu-id="f2017-231">An attempt was made to add too many columns to the table.</span></span> <span data-ttu-id="f2017-232">Таблица может содержать не более JET_ccolFixedMost фиксированных столбцов, не более JET_ccolVarMost столбцов переменной длины и не более JET_ccolTaggedMost столбцов с тегами.</span><span class="sxs-lookup"><span data-stu-id="f2017-232">A table can have no more than JET_ccolFixedMost fixed columns, no more than JET_ccolVarMost variable-length columns, and no more than JET_ccolTaggedMost tagged columns.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2017-233">JET_errTooManyOpenIndexes</span><span class="sxs-lookup"><span data-stu-id="f2017-233">JET_errTooManyOpenIndexes</span></span></p></td>
<td><p><span data-ttu-id="f2017-234">Не удалось выполнить операцию, так как подсистема не может выделить ресурсы, необходимые для кэширования индексов таблицы.</span><span class="sxs-lookup"><span data-stu-id="f2017-234">The operation failed because the engine cannot allocate the resources required to cache the indexes of the table.</span></span> <span data-ttu-id="f2017-235">Количество индексов, схема которых может быть кэширована, настраивается с помощью <a href="gg294044(v=exchg.10).md">жетсетсистемпараметер</a> с <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</span><span class="sxs-lookup"><span data-stu-id="f2017-235">The number of indexes whose schema can be cached is configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2017-236">JET_errTooManyOpenTables</span><span class="sxs-lookup"><span data-stu-id="f2017-236">JET_errTooManyOpenTables</span></span></p></td>
<td><p><span data-ttu-id="f2017-237">Не удалось выполнить операцию, так как подсистема не может выделить ресурсы, необходимые для кэширования схемы таблицы.</span><span class="sxs-lookup"><span data-stu-id="f2017-237">The operation failed because the engine cannot allocate the resources required to cache the schema of the table.</span></span> <span data-ttu-id="f2017-238">Количество таблиц, схема которых может быть кэширована, настраивается с помощью <a href="gg294044(v=exchg.10).md">жетсетсистемпараметер</a> с <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</span><span class="sxs-lookup"><span data-stu-id="f2017-238">The number of tables whose schema can be cached is configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2017-239">JET_errTooManySorts</span><span class="sxs-lookup"><span data-stu-id="f2017-239">JET_errTooManySorts</span></span></p></td>
<td><p><span data-ttu-id="f2017-240">Не удалось выполнить операцию, так как подсистема не может выделить ресурсы, необходимые для создания временной таблицы.</span><span class="sxs-lookup"><span data-stu-id="f2017-240">The operation failed because the engine cannot allocate the resources required to create a temporary table.</span></span> <span data-ttu-id="f2017-241">Временные ресурсы таблицы настраиваются с помощью <a href="gg294044(v=exchg.10).md">жетсетсистемпараметер</a> с <a href="gg294140(v=exchg.10).md">JET_paramMaxTemporaryTables</a>.</span><span class="sxs-lookup"><span data-stu-id="f2017-241">Temporary table resources are configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg294140(v=exchg.10).md">JET_paramMaxTemporaryTables</a>.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f2017-242">При успешном выполнении будет возвращен курсор, Открытый во вновь созданной временной таблице.</span><span class="sxs-lookup"><span data-stu-id="f2017-242">On success, a cursor opened on the newly created temporary table will be returned.</span></span> <span data-ttu-id="f2017-243">Состояние временной базы данных будет подготовлено для размещения новой временной таблицы.</span><span class="sxs-lookup"><span data-stu-id="f2017-243">The state of the temporary database will be prepared to contain the new temporary table.</span></span> <span data-ttu-id="f2017-244">Состояние всех обычных баз данных, используемых ядром СУБД, останется неизменным.</span><span class="sxs-lookup"><span data-stu-id="f2017-244">The state of any ordinary databases in use by the database engine will remain unchanged.</span></span>

<span data-ttu-id="f2017-245">При сбое временная таблица не будет создана и курсор не будет возвращен.</span><span class="sxs-lookup"><span data-stu-id="f2017-245">On failure, the temporary table will not be created and a cursor will not be returned.</span></span> <span data-ttu-id="f2017-246">Состояние временной базы данных может быть изменено.</span><span class="sxs-lookup"><span data-stu-id="f2017-246">The state of the temporary database may be changed.</span></span> <span data-ttu-id="f2017-247">Состояние всех обычных баз данных, используемых ядром СУБД, останется неизменным.</span><span class="sxs-lookup"><span data-stu-id="f2017-247">The state of any ordinary databases in use by the database engine will remain unchanged.</span></span>

#### <a name="remarks"></a><span data-ttu-id="f2017-248">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f2017-248">Remarks</span></span>

<span data-ttu-id="f2017-249">Временные таблицы не поддерживают полное дополнение параметров определения столбца, которые обычно поддерживаются ядром СУБД.</span><span class="sxs-lookup"><span data-stu-id="f2017-249">Temporary tables do not support the full complement of column definition options that are ordinarily supported by the database engine.</span></span> <span data-ttu-id="f2017-250">На самом деле поддерживаются только JET_bitColumnFixed и JET_bitColumnTagged.</span><span class="sxs-lookup"><span data-stu-id="f2017-250">In fact, only JET_bitColumnFixed and JET_bitColumnTagged are supported.</span></span> <span data-ttu-id="f2017-251">Это означает, что невозможно создать столбец с автоматическим приращением, версией или многозначным столбцом во временной таблице.</span><span class="sxs-lookup"><span data-stu-id="f2017-251">This means that it is not possible to create an auto-increment, version, or multi-valued column in a temporary table.</span></span> <span data-ttu-id="f2017-252">Наконец, столбцы депонированного обновления не поддерживаются, так как они не полезны во временной таблице, так как они могут использоваться только одним сеансом одновременно.</span><span class="sxs-lookup"><span data-stu-id="f2017-252">Finally, escrow update columns are not supported because they are not useful in a temporary table since they can only be used by one session at a time.</span></span> <span data-ttu-id="f2017-253">При запросе любого из этих параметров они будут проигнорированы.</span><span class="sxs-lookup"><span data-stu-id="f2017-253">If any of these options are requested then they will be ignored.</span></span>

<span data-ttu-id="f2017-254">Временные таблицы не поддерживают значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f2017-254">Temporary tables do not support default values.</span></span> <span data-ttu-id="f2017-255">Если указано определение столбца, содержащее спецификацию значения по умолчанию, то эта спецификация будет пропущена.</span><span class="sxs-lookup"><span data-stu-id="f2017-255">If a column definition is provided that contains a default value specification then that specification will be ignored.</span></span>

<span data-ttu-id="f2017-256">Временные таблицы возвращаются вызывающему объекту в результате многих различных функций ESE.</span><span class="sxs-lookup"><span data-stu-id="f2017-256">Temporary tables are returned to the caller as a result of many different ESE functions.</span></span> <span data-ttu-id="f2017-257">Например, [жетжетиндексинфо](./jetgetindexinfo-function.md) с параметром JET_IdxInfo, установленным в параметре *инфолевел* , возвращает временную таблицу, содержащую список всех ключевых столбцов в заданном индексе.</span><span class="sxs-lookup"><span data-stu-id="f2017-257">For example, [JetGetIndexInfo](./jetgetindexinfo-function.md) with the JET_IdxInfo option set in the *InfoLevel* parameter will return a temporary table containing a list of all the key columns in a given index.</span></span> <span data-ttu-id="f2017-258">Временные таблицы следуют тем же правилам жизненного цикла, что и обычные временные таблицы, как описано здесь.</span><span class="sxs-lookup"><span data-stu-id="f2017-258">The temporary tables follow the same lifecycle rules as ordinary temporary tables as described here.</span></span>

<span data-ttu-id="f2017-259">Временные таблицы также используются внутренне ядром СУБД для многих задач.</span><span class="sxs-lookup"><span data-stu-id="f2017-259">Temporary tables are also used internally by the database engine for many tasks.</span></span> <span data-ttu-id="f2017-260">Наиболее важной из этих задач является создание индекса для существующей таблицы.</span><span class="sxs-lookup"><span data-stu-id="f2017-260">The most important of these tasks is the creation of an index over an existing table.</span></span> <span data-ttu-id="f2017-261">Для сортировки ключей индекса, используемых для построения этого индекса, будет использоваться временная таблица.</span><span class="sxs-lookup"><span data-stu-id="f2017-261">A temporary table will be used to sort the index keys used to construct that index.</span></span>

<span data-ttu-id="f2017-262">Все временные таблицы хранятся во временной базе данных.</span><span class="sxs-lookup"><span data-stu-id="f2017-262">All temporary tables are stored in the temporary database.</span></span> <span data-ttu-id="f2017-263">Временная база данных — это специальный файл базы данных, который сохраняется в течение времени существования экземпляра ESE и удаляется при завершении работы или перезапуске этого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="f2017-263">The temporary database is a special database file that is maintained during the lifetime of an ESE instance and is deleted when that instance is shut down or restarted.</span></span> <span data-ttu-id="f2017-264">Расположение временной базы данных можно настроить с помощью [жетсетсистемпараметер](./jetsetsystemparameter-function.md) с [JET_paramTempPath](./temporary-database-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="f2017-264">The location of the temporary database can be configured using [JetSetSystemParameter](./jetsetsystemparameter-function.md) with [JET_paramTempPath](./temporary-database-parameters.md).</span></span> <span data-ttu-id="f2017-265">Размещение временной базы данных на диске относительно файлов журнала транзакций и файлов базы данных может быть важным, если приложение активно использует временные таблицы или часто создает индексы.</span><span class="sxs-lookup"><span data-stu-id="f2017-265">Placement of the temporary database on disk relative to your transaction log files and database files may be important if your application makes heavy use of temporary tables or creates indexes frequently.</span></span>

<span data-ttu-id="f2017-266">Жизненный цикл временной таблицы привязан к курсорам, ссылающимся на нее.</span><span class="sxs-lookup"><span data-stu-id="f2017-266">The lifecycle of a temporary table is tied to the cursors that reference it.</span></span> <span data-ttu-id="f2017-267">Если все курсоры, ссылающиеся на временную таблицу, закрыты, либо неявно, либо явно, то временная таблица будет удалена.</span><span class="sxs-lookup"><span data-stu-id="f2017-267">If all the cursors that reference a temporary table are closed, either implicitly or explicitly, then the temporary table will be deleted.</span></span> <span data-ttu-id="f2017-268">Если во время транзакции создается временная таблица и эта транзакция затем откатывается назад, то временная таблица будет удалена, так как все курсоры, на которые она ссылается, будут неявно закрыты.</span><span class="sxs-lookup"><span data-stu-id="f2017-268">If a temporary table is created inside a transaction and that transaction is subsequently rolled back then the temporary table will be deleted because any cursors that referenced it at this time will be implicitly closed.</span></span> <span data-ttu-id="f2017-269">Новые курсоры могут ссылаться на временную таблицу только с помощью [жетдупкурсор](./jetdupcursor-function.md).</span><span class="sxs-lookup"><span data-stu-id="f2017-269">New cursors may reference a temporary table only through the use of [JetDupCursor](./jetdupcursor-function.md).</span></span> <span data-ttu-id="f2017-270">В этом случае новые курсоры будут размещены на первой записи индекса временной таблицы.</span><span class="sxs-lookup"><span data-stu-id="f2017-270">In this case, the new cursors will be positioned on the first index entry of the temporary table.</span></span> <span data-ttu-id="f2017-271">[Жетдупкурсор](./jetdupcursor-function.md) будет работать только на определенных этапах использования временной таблицы.</span><span class="sxs-lookup"><span data-stu-id="f2017-271">[JetDupCursor](./jetdupcursor-function.md) will only work during certain phases of use for the temporary table.</span></span> <span data-ttu-id="f2017-272">Дополнительные сведения см. в разделе Примечания о возможностях курсора временной таблицы.</span><span class="sxs-lookup"><span data-stu-id="f2017-272">See the remarks concerning temporary table cursor capabilities for more information.</span></span> <span data-ttu-id="f2017-273">Нельзя ссылаться на временную таблицу более чем за один сеанс за раз.</span><span class="sxs-lookup"><span data-stu-id="f2017-273">It is not possible to reference a temporary table from more than one session at a time.</span></span>

<span data-ttu-id="f2017-274">В [жетдупкурсор](./jetdupcursor-function.md) есть важная проблема, влияющая на временные таблицы.</span><span class="sxs-lookup"><span data-stu-id="f2017-274">There is an important problem in [JetDupCursor](./jetdupcursor-function.md) that affects temporary tables.</span></span> <span data-ttu-id="f2017-275">При попытке скопировать временную таблицу, которая находится в однонаправленном режиме, полученный курсор не будет правильно создан и будет работать неправильно.</span><span class="sxs-lookup"><span data-stu-id="f2017-275">If an attempt is made to duplicate a temporary table that is in forward-only mode then the resulting cursor will not be created properly and will malfunction.</span></span> <span data-ttu-id="f2017-276">По-прежнему можно дублировать курсор по материализованным временным таблицам.</span><span class="sxs-lookup"><span data-stu-id="f2017-276">It is still safe to duplicate a cursor over a materialized temporary table.</span></span>

<span data-ttu-id="f2017-277">Временный диспетчер таблиц может выбрать реализацию временной таблицы тремя способами.</span><span class="sxs-lookup"><span data-stu-id="f2017-277">The temporary table manager may choose to implement a temporary table in three ways.</span></span> <span data-ttu-id="f2017-278">Первый способ — сохранить таблицу в памяти.</span><span class="sxs-lookup"><span data-stu-id="f2017-278">The first method is to maintain an in-memory table.</span></span> <span data-ttu-id="f2017-279">Эта стратегия является самой быстрой, но может использоваться только для небольших и простых временных таблиц.</span><span class="sxs-lookup"><span data-stu-id="f2017-279">This strategy is the fastest but can only be used for small, simple temporary tables.</span></span> <span data-ttu-id="f2017-280">Второй способ — создать дисковую сортировку, которую можно использовать с помощью однонаправленного итератора.</span><span class="sxs-lookup"><span data-stu-id="f2017-280">The second method is to create a disk-based sort that can be driven using a forward-only iterator.</span></span> <span data-ttu-id="f2017-281">Эта стратегия может использоваться только в определенных обстоятельствах и является самым быстрым способом сортировки и удаления дубликатов из очень большого набора данных.</span><span class="sxs-lookup"><span data-stu-id="f2017-281">This strategy can only be used under certain circumstances and is the fastest way to sort and remove duplicates from a very large data set.</span></span> <span data-ttu-id="f2017-282">Третий способ — создать дерево B + во временной базе данных для хранения временной таблицы.</span><span class="sxs-lookup"><span data-stu-id="f2017-282">The third method is to create a B+ Tree in the temporary database to hold the temporary table.</span></span> <span data-ttu-id="f2017-283">Эта стратегия является самой медленной, но наиболее универсальной и называется материализованным временным таблицей.</span><span class="sxs-lookup"><span data-stu-id="f2017-283">This strategy is the slowest, but the most versatile, and is referred to as a materialized temporary table.</span></span> <span data-ttu-id="f2017-284">Эти стратегии можно использовать в сочетании с целью обеспечения функциональности, запрошенной во временной таблице.</span><span class="sxs-lookup"><span data-stu-id="f2017-284">These strategies may be used in combination to ultimately achieve the functionality requested of the temporary table.</span></span>

<span data-ttu-id="f2017-285">Если временная таблица не соматериализованны, она используется в первую очередь на двух основных этапах.</span><span class="sxs-lookup"><span data-stu-id="f2017-285">When the temporary table is not materialized then it is used in primarily two major phases.</span></span> <span data-ttu-id="f2017-286">Первый этап — это фаза вставки, в которой таблица заполняется начальным набором данных.</span><span class="sxs-lookup"><span data-stu-id="f2017-286">The first phase is the insertion phase where the table is populated with its initial data set.</span></span> <span data-ttu-id="f2017-287">На этом этапе допускается только вставка данных.</span><span class="sxs-lookup"><span data-stu-id="f2017-287">During this phase, only data insertion is allowed.</span></span> <span data-ttu-id="f2017-288">Этот этап завершается, когда выполняется попытка переместить курсор с помощью [жетмове](./jetmove-function.md) или [жетсик](./jetseek-function.md).</span><span class="sxs-lookup"><span data-stu-id="f2017-288">This phase ends when an attempt is made to move the cursor using [JetMove](./jetmove-function.md) or [JetSeek](./jetseek-function.md).</span></span> <span data-ttu-id="f2017-289">Второй этап — этап извлечения данных.</span><span class="sxs-lookup"><span data-stu-id="f2017-289">The second phase is the data extraction phase.</span></span> <span data-ttu-id="f2017-290">На этом этапе данные, хранящиеся во временной таблице, могут быть извлечены в соответствии с возможностями, запрошенными при создании временной таблицы.</span><span class="sxs-lookup"><span data-stu-id="f2017-290">During this phase, the data stored in the temporary table may be extracted according to the capabilities requested when the temporary table was created.</span></span>

<span data-ttu-id="f2017-291">**Возможности курсора временной таблицы**</span><span class="sxs-lookup"><span data-stu-id="f2017-291">**Temporary Table Cursor Capabilities**</span></span>

<span data-ttu-id="f2017-292">При материализации временной таблицы курсор имеет следующие возможности, но может быть дополнительно ограничен запрошенными параметрами:</span><span class="sxs-lookup"><span data-stu-id="f2017-292">When the temporary table is materialized, the cursor has the following capabilities but may be further limited by the options requested:</span></span>

  - [<span data-ttu-id="f2017-293">жетклосетабле</span><span class="sxs-lookup"><span data-stu-id="f2017-293">JetCloseTable</span></span>](./jetclosetable-function.md)

  - [<span data-ttu-id="f2017-294">жетделете</span><span class="sxs-lookup"><span data-stu-id="f2017-294">JetDelete</span></span>](./jetdelete-function.md)

  - [<span data-ttu-id="f2017-295">жетдупкурсор</span><span class="sxs-lookup"><span data-stu-id="f2017-295">JetDupCursor</span></span>](./jetdupcursor-function.md)

  - [<span data-ttu-id="f2017-296">жетенумератеколумнс</span><span class="sxs-lookup"><span data-stu-id="f2017-296">JetEnumerateColumns</span></span>](./jetenumeratecolumns-function.md)

  - [<span data-ttu-id="f2017-297">жетескровупдате</span><span class="sxs-lookup"><span data-stu-id="f2017-297">JetEscrowUpdate</span></span>](./jetescrowupdate-function.md)

  - [<span data-ttu-id="f2017-298">жетжетбукмарк</span><span class="sxs-lookup"><span data-stu-id="f2017-298">JetGetBookmark</span></span>](./jetgetbookmark-function.md)

  - [<span data-ttu-id="f2017-299">жетжеткурсоринфо</span><span class="sxs-lookup"><span data-stu-id="f2017-299">JetGetCursorInfo</span></span>](./jetgetcursorinfo-function.md)

  - [<span data-ttu-id="f2017-300">жетжетлс</span><span class="sxs-lookup"><span data-stu-id="f2017-300">JetGetLS</span></span>](./jetgetls-function.md)

  - [<span data-ttu-id="f2017-301">жетжетрекордсизе</span><span class="sxs-lookup"><span data-stu-id="f2017-301">JetGetRecordSize</span></span>](./jetgetrecordsize-function.md)

  - [<span data-ttu-id="f2017-302">жетжеттаблеинфо</span><span class="sxs-lookup"><span data-stu-id="f2017-302">JetGetTableInfo</span></span>](./jetgettableinfo-function.md)

  - [<span data-ttu-id="f2017-303">жетготобукмарк</span><span class="sxs-lookup"><span data-stu-id="f2017-303">JetGotoBookmark</span></span>](./jetgotobookmark-function.md)

  - [<span data-ttu-id="f2017-304">жетмакекэй</span><span class="sxs-lookup"><span data-stu-id="f2017-304">JetMakeKey</span></span>](./jetmakekey-function.md)

  - [<span data-ttu-id="f2017-305">жетмове</span><span class="sxs-lookup"><span data-stu-id="f2017-305">JetMove</span></span>](./jetmove-function.md)

  - [<span data-ttu-id="f2017-306">жетпрепареупдате</span><span class="sxs-lookup"><span data-stu-id="f2017-306">JetPrepareUpdate</span></span>](./jetprepareupdate-function.md)

  - [<span data-ttu-id="f2017-307">жетретриевеколумн</span><span class="sxs-lookup"><span data-stu-id="f2017-307">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)

  - [<span data-ttu-id="f2017-308">жетретриевеколумнс</span><span class="sxs-lookup"><span data-stu-id="f2017-308">JetRetrieveColumns</span></span>](./jetretrievecolumns-function.md)

  - [<span data-ttu-id="f2017-309">жетретриевекэй</span><span class="sxs-lookup"><span data-stu-id="f2017-309">JetRetrieveKey</span></span>](./jetretrievekey-function.md)

  - [<span data-ttu-id="f2017-310">жетсик</span><span class="sxs-lookup"><span data-stu-id="f2017-310">JetSeek</span></span>](./jetseek-function.md)

  - [<span data-ttu-id="f2017-311">жетсетколумн</span><span class="sxs-lookup"><span data-stu-id="f2017-311">JetSetColumn</span></span>](./jetsetcolumn-function.md)

  - [<span data-ttu-id="f2017-312">жетсетколумнс</span><span class="sxs-lookup"><span data-stu-id="f2017-312">JetSetColumns</span></span>](./jetsetcolumns-function.md)

  - [<span data-ttu-id="f2017-313">жетсетиндексранже</span><span class="sxs-lookup"><span data-stu-id="f2017-313">JetSetIndexRange</span></span>](./jetsetindexrange-function.md)

  - [<span data-ttu-id="f2017-314">жетсетлс</span><span class="sxs-lookup"><span data-stu-id="f2017-314">JetSetLS</span></span>](./jetsetls-function.md)

  - [<span data-ttu-id="f2017-315">жетупдате</span><span class="sxs-lookup"><span data-stu-id="f2017-315">JetUpdate</span></span>](./jetupdate-function.md)

<span data-ttu-id="f2017-316">Если временная таблица не соблюдается и находится на стадии вставки, курсор имеет следующие возможности, но может быть дополнительно ограничен запрошенными параметрами:</span><span class="sxs-lookup"><span data-stu-id="f2017-316">When the temporary table is not materialized and is in the insert phase, the cursor has the following capabilities but may be further limited by the options requested:</span></span>

  - [<span data-ttu-id="f2017-317">жетклосетабле</span><span class="sxs-lookup"><span data-stu-id="f2017-317">JetCloseTable</span></span>](./jetclosetable-function.md)

  - [<span data-ttu-id="f2017-318">жетескровупдате</span><span class="sxs-lookup"><span data-stu-id="f2017-318">JetEscrowUpdate</span></span>](./jetescrowupdate-function.md)

  - [<span data-ttu-id="f2017-319">жетмакекэй</span><span class="sxs-lookup"><span data-stu-id="f2017-319">JetMakeKey</span></span>](./jetmakekey-function.md)

  - [<span data-ttu-id="f2017-320">жетмове</span><span class="sxs-lookup"><span data-stu-id="f2017-320">JetMove</span></span>](./jetmove-function.md)
    
    <span data-ttu-id="f2017-321">**Примечание**  .  Вызывает переход на фазу извлечения.</span><span class="sxs-lookup"><span data-stu-id="f2017-321">**Note**  Causes transition to the extract phase.</span></span>

  - [<span data-ttu-id="f2017-322">жетпрепареупдате</span><span class="sxs-lookup"><span data-stu-id="f2017-322">JetPrepareUpdate</span></span>](./jetprepareupdate-function.md)

  - [<span data-ttu-id="f2017-323">жетретриевекэй</span><span class="sxs-lookup"><span data-stu-id="f2017-323">JetRetrieveKey</span></span>](./jetretrievekey-function.md)

  - [<span data-ttu-id="f2017-324">жетсик</span><span class="sxs-lookup"><span data-stu-id="f2017-324">JetSeek</span></span>](./jetseek-function.md)
    
    <span data-ttu-id="f2017-325">**Примечание**  .  Вызывает переход на фазу извлечения.</span><span class="sxs-lookup"><span data-stu-id="f2017-325">**Note**  Causes transition to the extract phase.</span></span>

  - [<span data-ttu-id="f2017-326">жетсетколумн</span><span class="sxs-lookup"><span data-stu-id="f2017-326">JetSetColumn</span></span>](./jetsetcolumn-function.md)

  - [<span data-ttu-id="f2017-327">жетсетколумнс</span><span class="sxs-lookup"><span data-stu-id="f2017-327">JetSetColumns</span></span>](./jetsetcolumns-function.md)

  - [<span data-ttu-id="f2017-328">жетупдате</span><span class="sxs-lookup"><span data-stu-id="f2017-328">JetUpdate</span></span>](./jetupdate-function.md)

<span data-ttu-id="f2017-329">Если временная таблица не материализованный и находится на этапе извлечения, то курсор имеет следующие возможности, но может быть дополнительно ограничен запрошенными параметрами:</span><span class="sxs-lookup"><span data-stu-id="f2017-329">When the temporary table is not materialized and is in the extract phase, the cursor has the following capabilities but may be further limited by the options requested:</span></span>

  - [<span data-ttu-id="f2017-330">жетклосетабле</span><span class="sxs-lookup"><span data-stu-id="f2017-330">JetCloseTable</span></span>](./jetclosetable-function.md)

  - [<span data-ttu-id="f2017-331">жетдупкурсор</span><span class="sxs-lookup"><span data-stu-id="f2017-331">JetDupCursor</span></span>](./jetdupcursor-function.md)
    
    <span data-ttu-id="f2017-332">**Примечание**  .  При попытке скопировать временную таблицу, которая находится в однонаправленном режиме, полученный курсор не будет правильно создан и будет работать неправильно.</span><span class="sxs-lookup"><span data-stu-id="f2017-332">**Note**  If an attempt is made to duplicate a temporary table that is in forward-only mode then the resulting cursor will not be created properly and will malfunction.</span></span> <span data-ttu-id="f2017-333">По-прежнему можно дублировать курсор по материализованным временным таблицам.</span><span class="sxs-lookup"><span data-stu-id="f2017-333">It is still safe to duplicate a cursor over a materialized temporary table.</span></span>

  - [<span data-ttu-id="f2017-334">жетенумератеколумнс</span><span class="sxs-lookup"><span data-stu-id="f2017-334">JetEnumerateColumns</span></span>](./jetenumeratecolumns-function.md)

  - [<span data-ttu-id="f2017-335">жетжетбукмарк</span><span class="sxs-lookup"><span data-stu-id="f2017-335">JetGetBookmark</span></span>](./jetgetbookmark-function.md)

  - [<span data-ttu-id="f2017-336">жетжетлс</span><span class="sxs-lookup"><span data-stu-id="f2017-336">JetGetLS</span></span>](./jetgetls-function.md)

  - [<span data-ttu-id="f2017-337">жетжетрекордсизе</span><span class="sxs-lookup"><span data-stu-id="f2017-337">JetGetRecordSize</span></span>](./jetgetrecordsize-function.md)

  - [<span data-ttu-id="f2017-338">жетжеттаблеинфо</span><span class="sxs-lookup"><span data-stu-id="f2017-338">JetGetTableInfo</span></span>](./jetgettableinfo-function.md)

  - [<span data-ttu-id="f2017-339">жетготобукмарк</span><span class="sxs-lookup"><span data-stu-id="f2017-339">JetGotoBookmark</span></span>](./jetgotobookmark-function.md)

  - [<span data-ttu-id="f2017-340">жетмакекэй</span><span class="sxs-lookup"><span data-stu-id="f2017-340">JetMakeKey</span></span>](./jetmakekey-function.md)

  - [<span data-ttu-id="f2017-341">жетмове</span><span class="sxs-lookup"><span data-stu-id="f2017-341">JetMove</span></span>](./jetmove-function.md)

  - [<span data-ttu-id="f2017-342">жетретриевеколумн</span><span class="sxs-lookup"><span data-stu-id="f2017-342">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)

  - [<span data-ttu-id="f2017-343">жетретриевеколумнс</span><span class="sxs-lookup"><span data-stu-id="f2017-343">JetRetrieveColumns</span></span>](./jetretrievecolumns-function.md)

  - [<span data-ttu-id="f2017-344">жетретриевекэй</span><span class="sxs-lookup"><span data-stu-id="f2017-344">JetRetrieveKey</span></span>](./jetretrievekey-function.md)

  - [<span data-ttu-id="f2017-345">жетсик</span><span class="sxs-lookup"><span data-stu-id="f2017-345">JetSeek</span></span>](./jetseek-function.md)

  - [<span data-ttu-id="f2017-346">жетсетиндексранже</span><span class="sxs-lookup"><span data-stu-id="f2017-346">JetSetIndexRange</span></span>](./jetsetindexrange-function.md)

  - [<span data-ttu-id="f2017-347">жетсетлс</span><span class="sxs-lookup"><span data-stu-id="f2017-347">JetSetLS</span></span>](./jetsetls-function.md)

#### <a name="requirements"></a><span data-ttu-id="f2017-348">Требования</span><span class="sxs-lookup"><span data-stu-id="f2017-348">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f2017-349"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="f2017-349"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="f2017-350">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="f2017-350">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2017-351"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="f2017-351"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="f2017-352">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="f2017-352">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2017-353"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="f2017-353"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="f2017-354">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="f2017-354">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2017-355"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="f2017-355"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="f2017-356">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="f2017-356">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2017-357"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="f2017-357"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="f2017-358">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="f2017-358">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="f2017-359">См. также:</span><span class="sxs-lookup"><span data-stu-id="f2017-359">See Also</span></span>

[<span data-ttu-id="f2017-360">JET_COLUMNDEF</span><span class="sxs-lookup"><span data-stu-id="f2017-360">JET_COLUMNDEF</span></span>](./jet-columndef-structure.md)  
[<span data-ttu-id="f2017-361">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="f2017-361">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="f2017-362">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="f2017-362">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="f2017-363">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="f2017-363">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="f2017-364">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="f2017-364">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="f2017-365">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="f2017-365">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="f2017-366">JET_UNICODEINDEX</span><span class="sxs-lookup"><span data-stu-id="f2017-366">JET_UNICODEINDEX</span></span>](./jet-unicodeindex-structure.md)  
[<span data-ttu-id="f2017-367">жетклосетабле</span><span class="sxs-lookup"><span data-stu-id="f2017-367">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="f2017-368">жеткреатетаблеколумниндекс</span><span class="sxs-lookup"><span data-stu-id="f2017-368">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="f2017-369">жетдупкурсор</span><span class="sxs-lookup"><span data-stu-id="f2017-369">JetDupCursor</span></span>](./jetdupcursor-function.md)  
[<span data-ttu-id="f2017-370">жетмове</span><span class="sxs-lookup"><span data-stu-id="f2017-370">JetMove</span></span>](./jetmove-function.md)  
[<span data-ttu-id="f2017-371">жетроллбакк</span><span class="sxs-lookup"><span data-stu-id="f2017-371">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="f2017-372">жетсик</span><span class="sxs-lookup"><span data-stu-id="f2017-372">JetSeek</span></span>](./jetseek-function.md)  
[<span data-ttu-id="f2017-373">жетсетсистемпараметер</span><span class="sxs-lookup"><span data-stu-id="f2017-373">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="f2017-374">Параметры временной базы данных</span><span class="sxs-lookup"><span data-stu-id="f2017-374">Temporary Database Parameters</span></span>](./temporary-database-parameters.md)
