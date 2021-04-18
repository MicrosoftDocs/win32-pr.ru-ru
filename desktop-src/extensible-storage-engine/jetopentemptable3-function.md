---
description: Дополнительные сведения о функции JetOpenTempTable3
title: Функция JetOpenTempTable3
TOCTitle: JetOpenTempTable3 Function
ms:assetid: 58d6e264-705e-402b-928f-96eefe5e9771
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269255(v=EXCHG.10)
ms:contentKeyID: 32765557
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenTempTable3
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7820f90ef0192c1f700759835bf1572b187cf3be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692122"
---
# <a name="jetopentemptable3-function"></a><span data-ttu-id="a1585-103">Функция JetOpenTempTable3</span><span class="sxs-lookup"><span data-stu-id="a1585-103">JetOpenTempTable3 Function</span></span>


<span data-ttu-id="a1585-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="a1585-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetopentemptable3-function"></a><span data-ttu-id="a1585-105">Функция JetOpenTempTable3</span><span class="sxs-lookup"><span data-stu-id="a1585-105">JetOpenTempTable3 Function</span></span>

<span data-ttu-id="a1585-106">Функция **JetOpenTempTable3** создает временную таблицу с одним индексом, который может использоваться для хранения и извлечения записей точно так же, как обычная таблица, созданная с помощью [жеткреатетаблеколумниндекс](./jetcreatetablecolumnindex-function.md).</span><span class="sxs-lookup"><span data-stu-id="a1585-106">The **JetOpenTempTable3** function creates a temporary table with a single index that can be used to store and retrieve records just like an ordinary table created using [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md).</span></span> <span data-ttu-id="a1585-107">Однако временные таблицы выполняются гораздо быстрее, чем обычные таблицы, в связи с их постоянным характером.</span><span class="sxs-lookup"><span data-stu-id="a1585-107">However, temporary tables are much faster than ordinary tables due to their volatile nature.</span></span> <span data-ttu-id="a1585-108">Они также могут использоваться для очень быстрой сортировки и удаления дубликатов наборов записей при обращении к ним только последовательно.</span><span class="sxs-lookup"><span data-stu-id="a1585-108">They can also be used to very quickly sort and perform duplicate removal on record sets when accessed in a purely sequential manner.</span></span>

```cpp
    JET_ERR JET_API JetOpenTempTable3(
      __in          JET_SESID sesid,
      __in          const JET_COLUMNDEF* prgcolumndef,
      __in          unsigned long ccolumn,
      __in_opt      JET_UNICODEINDEX* pidxunicode,
      __in          JET_GRBIT grbit,
      __out         JET_TABLEID* ptableid,
      __out         JET_COLUMNID* prgcolumnid
    );
```

### <a name="parameters"></a><span data-ttu-id="a1585-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="a1585-109">Parameters</span></span>

<span data-ttu-id="a1585-110">*сесид*</span><span class="sxs-lookup"><span data-stu-id="a1585-110">*sesid*</span></span>

<span data-ttu-id="a1585-111">Сеанс, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="a1585-111">The session to use for this call.</span></span>

<span data-ttu-id="a1585-112">*пргколумндеф*</span><span class="sxs-lookup"><span data-stu-id="a1585-112">*prgcolumndef*</span></span>

<span data-ttu-id="a1585-113">Определяет определения столбцов, которые должны быть созданы во временной таблице.</span><span class="sxs-lookup"><span data-stu-id="a1585-113">Identifies the column definitions of the columns to be created in the temporary table.</span></span>

<span data-ttu-id="a1585-114">Существуют важные ограничения для параметров определения столбца, которые могут использоваться во временной таблице.</span><span class="sxs-lookup"><span data-stu-id="a1585-114">Important limitations exist to the column definition options that may be used with a temporary table.</span></span> <span data-ttu-id="a1585-115">Дополнительные сведения см. в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="a1585-115">See the Remarks section for more information.</span></span>

<span data-ttu-id="a1585-116">В дополнение к обычным параметрам определения столбца можно также указать ноль или более следующих параметров, которые важны только в контексте временной таблицы.</span><span class="sxs-lookup"><span data-stu-id="a1585-116">In addition to the usual column definition options, zero or more of the following options may also be specified that are relevant only in the context of a temporary table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a1585-117">Значение</span><span class="sxs-lookup"><span data-stu-id="a1585-117">Value</span></span></p></th>
<th><p><span data-ttu-id="a1585-118">Значение</span><span class="sxs-lookup"><span data-stu-id="a1585-118">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a1585-119">JET_bitColumnTTDescending</span><span class="sxs-lookup"><span data-stu-id="a1585-119">JET_bitColumnTTDescending</span></span></p></td>
<td><p><span data-ttu-id="a1585-120">Этот параметр указывает, что порядок сортировки ключевого столбца для временной таблицы должен быть по убыванию, а не по возрастанию.</span><span class="sxs-lookup"><span data-stu-id="a1585-120">This option indicates that the sort order of the key column for the temporary table should be descending rather than ascending.</span></span> <span data-ttu-id="a1585-121">Если этот параметр указан без JET_bitColumnTTKey то этот параметр игнорируется.</span><span class="sxs-lookup"><span data-stu-id="a1585-121">If this option is specified without JET_bitColumnTTKey then this option is ignored.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1585-122">JET_bitColumnTTKey</span><span class="sxs-lookup"><span data-stu-id="a1585-122">JET_bitColumnTTKey</span></span></p></td>
<td><p><span data-ttu-id="a1585-123">Этот параметр указывает, что столбец будет ключевым столбцом для временной таблицы.</span><span class="sxs-lookup"><span data-stu-id="a1585-123">This option indicates that the column will be a key column for the temporary table.</span></span></p>
<p><span data-ttu-id="a1585-124">Порядок определений столбцов с этим параметром, указанным во входном массиве, определяет приоритет каждого ключевого столбца для временной таблицы.</span><span class="sxs-lookup"><span data-stu-id="a1585-124">The order of the column definitions with this option specified in the input array will determine the precedence of each key column for the temporary table.</span></span> <span data-ttu-id="a1585-125">Первое определение столбца в массиве с этим набором параметров будет наиболее значимым ключевым столбцом и т. д.</span><span class="sxs-lookup"><span data-stu-id="a1585-125">The first column definition in the array with this option set will be the most significant key column and so on.</span></span> <span data-ttu-id="a1585-126">Если запрошено больше ключевых столбцов, чем может поддерживать ядро СУБД, этот параметр игнорируется для неподдерживаемых ключевых столбцов.</span><span class="sxs-lookup"><span data-stu-id="a1585-126">If more key columns are requested than can be supported by the database engine then this option is ignored for the unsupportable key columns.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a1585-127">*кколумн*</span><span class="sxs-lookup"><span data-stu-id="a1585-127">*ccolumn*</span></span>

<span data-ttu-id="a1585-128">См. *пргколумндеф*.</span><span class="sxs-lookup"><span data-stu-id="a1585-128">See *prgcolumndef*.</span></span>

<span data-ttu-id="a1585-129">*пидксуникоде*</span><span class="sxs-lookup"><span data-stu-id="a1585-129">*pidxunicode*</span></span>

<span data-ttu-id="a1585-130">КОД локали и флаги нормализации, которые будут использоваться для сравнения данных любого ключевого столбца Юникода во временной таблице.</span><span class="sxs-lookup"><span data-stu-id="a1585-130">The Locale ID and normalization flags that will be used to compare any Unicode key column data in the temporary table.</span></span>

<span data-ttu-id="a1585-131">Если этот параметр отсутствует, то для сравнения всех ключевых столбцов Юникода во временной таблице будет использоваться код по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a1585-131">When this parameter is not present then the default LCID will be used to compare any Unicode key columns in the temporary table.</span></span> <span data-ttu-id="a1585-132">По умолчанию используется языковой стандарт «Английский (США)».</span><span class="sxs-lookup"><span data-stu-id="a1585-132">The default LCID is the U.S. English locale.</span></span>

<span data-ttu-id="a1585-133">Если этот параметр отсутствует, для сравнения данных любого ключевого столбца Юникода во временной таблице будут использоваться флаги нормализации по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a1585-133">When this parameter is not present then the default normalization flags will be used to compare any Unicode key column data in the temp table.</span></span> <span data-ttu-id="a1585-134">Флаги нормализации по умолчанию: NORM_IGNORECASE, NORM_IGNOREKANATYPE и NORM_IGNOREWIDTH.</span><span class="sxs-lookup"><span data-stu-id="a1585-134">The default normalization flags are: NORM_IGNORECASE, NORM_IGNOREKANATYPE, and NORM_IGNOREWIDTH.</span></span>

<span data-ttu-id="a1585-135">*грбит*</span><span class="sxs-lookup"><span data-stu-id="a1585-135">*grbit*</span></span>

<span data-ttu-id="a1585-136">Группа битов, содержащая параметры, которые должны использоваться для этого вызова, включая ноль или более следующих значений.</span><span class="sxs-lookup"><span data-stu-id="a1585-136">A group of bits that contain the options to be used for this call, which include zero or more of the following.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a1585-137">Значение</span><span class="sxs-lookup"><span data-stu-id="a1585-137">Value</span></span></p></th>
<th><p><span data-ttu-id="a1585-138">Значение</span><span class="sxs-lookup"><span data-stu-id="a1585-138">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a1585-139">JET_bitTTErrorOnDuplicateInsertion</span><span class="sxs-lookup"><span data-stu-id="a1585-139">JET_bitTTErrorOnDuplicateInsertion</span></span></p></td>
<td><p><span data-ttu-id="a1585-140">Этот параметр запрашивает неудачную попытку вставки записи с тем же ключом индекса, что и ранее вставленная запись, с JET_errKeyDuplicate.</span><span class="sxs-lookup"><span data-stu-id="a1585-140">This option requests that any attempt to insert a record with the same index key as a previously inserted record will immediately fail with JET_errKeyDuplicate.</span></span> <span data-ttu-id="a1585-141">Если этот параметр не запрошен, то дубликат может быть обнаружен немедленно, с ошибкой или автоматически удален позже в зависимости от стратегии, выбранной ядром СУБД для реализации временной таблицы на основе запрошенной функциональности.</span><span class="sxs-lookup"><span data-stu-id="a1585-141">If this option is not requested then a duplicate may be detected immediately and fail or may be silently removed later depending on the strategy chosen by the database engine to implement the temporary table based on the requested functionality.</span></span></p>
<p><span data-ttu-id="a1585-142">Если эта функция не требуется, то лучше не запрашивать ее.</span><span class="sxs-lookup"><span data-stu-id="a1585-142">If this functionality it not required then it is best to not request it.</span></span> <span data-ttu-id="a1585-143">Если эта функция не запрошена, то диспетчер временных таблиц может выбрать стратегию для управления временной таблицей, что приведет к повышению производительности.</span><span class="sxs-lookup"><span data-stu-id="a1585-143">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1585-144">JET_bitTTForceMaterialization</span><span class="sxs-lookup"><span data-stu-id="a1585-144">JET_bitTTForceMaterialization</span></span></p></td>
<td><p><span data-ttu-id="a1585-145">Этот параметр заставляет диспетчер временных таблиц отказаться от любой попытки выбрать стратегию для управления временной таблицей, что приведет к повышению производительности.</span><span class="sxs-lookup"><span data-stu-id="a1585-145">This option forces the temporary table manager to abandon any attempt to choose a clever strategy for managing the temporary table that will result in enhanced performance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1585-146">JET_bitTTForwardOnly</span><span class="sxs-lookup"><span data-stu-id="a1585-146">JET_bitTTForwardOnly</span></span></p></td>
<td><p><span data-ttu-id="a1585-147">Этот параметр запрашивает создание временной таблицы только в том случае, если диспетчер временных таблиц может использовать реализацию, оптимизированную для промежуточных результатов запроса.</span><span class="sxs-lookup"><span data-stu-id="a1585-147">This option requests that the temporary table only be created if the temporary table manager can use the implementation optimized for intermediate query results.</span></span> <span data-ttu-id="a1585-148">Если любая характеристика временной таблицы не позволит использовать эту оптимизацию, операция завершится с JET_errCannotMaterializeForwardOnlySort.</span><span class="sxs-lookup"><span data-stu-id="a1585-148">If any characteristic of the temporary table would prevent the use of this optimization then the operation will fail with JET_errCannotMaterializeForwardOnlySort.</span></span></p>
<p><span data-ttu-id="a1585-149">Побочный результат этого параметра — Разрешить временной таблице содержать записи с повторяющимися ключами индекса.</span><span class="sxs-lookup"><span data-stu-id="a1585-149">A side effect of this option is to allow the temporary table to contain records with duplicate index keys.</span></span> <span data-ttu-id="a1585-150">Дополнительные сведения см. в разделе JET_bitTTUnique.</span><span class="sxs-lookup"><span data-stu-id="a1585-150">See JET_bitTTUnique for more information.</span></span></p>
<p><span data-ttu-id="a1585-151">Этот параметр доступен только в выпусках Windows Server 2003 и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="a1585-151">This option is only available on Windows Server 2003 and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1585-152">JET_bitTTIndexed</span><span class="sxs-lookup"><span data-stu-id="a1585-152">JET_bitTTIndexed</span></span></p></td>
<td><p><span data-ttu-id="a1585-153">Этот параметр требует, чтобы временная таблица была достаточно гибкой, чтобы позволить использовать <a href="gg294103(v=exchg.10).md">жетсик</a> для поиска записей по ключу индекса.</span><span class="sxs-lookup"><span data-stu-id="a1585-153">This option requests that the temporary table be flexible enough to permit the use of <a href="gg294103(v=exchg.10).md">JetSeek</a> to look up records by index key.</span></span></p>
<p><span data-ttu-id="a1585-154">Если эта функция не требуется, то лучше не запрашивать ее.</span><span class="sxs-lookup"><span data-stu-id="a1585-154">If this functionality it not required then it is best to not request it.</span></span> <span data-ttu-id="a1585-155">Если эта функция не запрошена, то диспетчер временных таблиц может выбрать стратегию для управления временной таблицей, что приведет к повышению производительности.</span><span class="sxs-lookup"><span data-stu-id="a1585-155">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1585-156">JET_bitTTUnique</span><span class="sxs-lookup"><span data-stu-id="a1585-156">JET_bitTTUnique</span></span></p></td>
<td><p><span data-ttu-id="a1585-157">Этот параметр запрашивает удаление записей с повторяющимися ключами индекса из окончательного набора записей во временной таблице.</span><span class="sxs-lookup"><span data-stu-id="a1585-157">This option requests that records with duplicate index keys be removed from the final set of records in the temporary table.</span></span></p>
<p><span data-ttu-id="a1585-158">До Windows Server 2003 в ядре СУБД всегда предполагается, что этот параметр действует из-за того факта, что все кластеризованные индексы также должны быть первичным ключом и, таким же, должны быть уникальными.</span><span class="sxs-lookup"><span data-stu-id="a1585-158">Prior to Windows Server 2003, the database engine always assumed this option to be in effect due to the fact that all clustered indexes must also be a primary key and thus must be unique.</span></span> <span data-ttu-id="a1585-159">Начиная с Windows Server 2003, теперь можно создать временную таблицу, которая не удаляет дубликаты, если также указан параметр JET_bitTTForwardOnly.</span><span class="sxs-lookup"><span data-stu-id="a1585-159">As of Windows Server 2003, it is now possible to create a temporary table that does NOT remove duplicates when the JET_bitTTForwardOnly option is also specified.</span></span></p>
<p><span data-ttu-id="a1585-160">Невозможно понять, какие дубликаты будут выдаваться, и какие дубликаты будут отменены в целом.</span><span class="sxs-lookup"><span data-stu-id="a1585-160">It is not possible to know which duplicate will win and which duplicates will be discarded in general.</span></span> <span data-ttu-id="a1585-161">Однако при запросе параметра JET_bitTTErrorOnDuplicateInsertion первая запись с заданным ключом индекса для вставки во временную таблицу всегда будет выдаваться.</span><span class="sxs-lookup"><span data-stu-id="a1585-161">However, when the JET_bitTTErrorOnDuplicateInsertion option is requested then the first record with a given index key to be inserted into the temporary table will always win.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1585-162">JET_bitTTUpdatable</span><span class="sxs-lookup"><span data-stu-id="a1585-162">JET_bitTTUpdatable</span></span></p></td>
<td><p><span data-ttu-id="a1585-163">Этот параметр требует, чтобы временная таблица была достаточно гибкой, чтобы разрешить впоследствии изменять записи, которые были вставлены.</span><span class="sxs-lookup"><span data-stu-id="a1585-163">This option requests that the temporary table be flexible enough to allow records that have previously been inserted to be subsequently changed.</span></span> <span data-ttu-id="a1585-164">Если эта функция не требуется, то лучше не запрашивать ее.</span><span class="sxs-lookup"><span data-stu-id="a1585-164">If this functionality it not required then it is best to not request it.</span></span></p>
<p><span data-ttu-id="a1585-165">Если эта функция не запрошена, то диспетчер временных таблиц может выбрать стратегию для управления временной таблицей, что приведет к повышению производительности.</span><span class="sxs-lookup"><span data-stu-id="a1585-165">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1585-166">JET_bitTTScrollable</span><span class="sxs-lookup"><span data-stu-id="a1585-166">JET_bitTTScrollable</span></span></p></td>
<td><p><span data-ttu-id="a1585-167">Этот параметр требует, чтобы временная таблица была достаточно гибкой, чтобы разрешить сканирование записей в произвольном порядке и направлении с помощью <a href="gg294117(v=exchg.10).md">жетмове</a>.</span><span class="sxs-lookup"><span data-stu-id="a1585-167">This option requests that the temporary table be flexible enough to allow records to be scanned in arbitrary order and direction using <a href="gg294117(v=exchg.10).md">JetMove</a>.</span></span></p>
<p><span data-ttu-id="a1585-168">Если эта функция не требуется, то лучше не запрашивать ее.</span><span class="sxs-lookup"><span data-stu-id="a1585-168">If this functionality it not required then it is best to not request it.</span></span> <span data-ttu-id="a1585-169">Если эта функция не запрошена, то диспетчер временных таблиц может выбрать стратегию для управления временной таблицей, что приведет к повышению производительности.</span><span class="sxs-lookup"><span data-stu-id="a1585-169">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1585-170">JET_bitTTSortNullsHigh</span><span class="sxs-lookup"><span data-stu-id="a1585-170">JET_bitTTSortNullsHigh</span></span></p></td>
<td><p><span data-ttu-id="a1585-171">При выборе этого варианта значения ключевого столбца NULL сортируются ближе к концу индекса, чем значения ключевого столбца, отличные от NULL.</span><span class="sxs-lookup"><span data-stu-id="a1585-171">This option requests that NULL key column values sort closer to the end of the index than non-NULL key column values.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1585-172">JET_bitTTIntrinsicLVsOnly</span><span class="sxs-lookup"><span data-stu-id="a1585-172">JET_bitTTIntrinsicLVsOnly</span></span></p></td>
<td><p><span data-ttu-id="a1585-173">Запросы на разрешение только внутренних значений типа long.</span><span class="sxs-lookup"><span data-stu-id="a1585-173">Requests to permit only intrinsic long values.</span></span></p>
<p><span data-ttu-id="a1585-174"><strong>Windows 7</strong>: <strong>JET_bitTTIntrinsicLVsOnly</strong> введен в Windows 7.</span><span class="sxs-lookup"><span data-stu-id="a1585-174"><strong>Windows 7</strong>: <strong>JET_bitTTIntrinsicLVsOnly</strong> is introduced in Windows 7.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a1585-175">*pTableID*</span><span class="sxs-lookup"><span data-stu-id="a1585-175">*ptableid*</span></span>

<span data-ttu-id="a1585-176">Выходной буфер, который получит новый курсор, Открытый во вновь созданной временной таблице.</span><span class="sxs-lookup"><span data-stu-id="a1585-176">The output buffer that will receive the new cursor opened on the newly created temporary table.</span></span>

<span data-ttu-id="a1585-177">*пргколумнид*</span><span class="sxs-lookup"><span data-stu-id="a1585-177">*prgcolumnid*</span></span>

<span data-ttu-id="a1585-178">Выходной буфер, который будет принимать массив идентификаторов столбцов, сформированных во время создания временной таблицы.</span><span class="sxs-lookup"><span data-stu-id="a1585-178">The output buffer that will receive the array of column IDs generated during the creation of the temporary table.</span></span>

<span data-ttu-id="a1585-179">Идентификаторы столбцов в этом массиве будут точно соответствовать входному массиву определений столбцов.</span><span class="sxs-lookup"><span data-stu-id="a1585-179">The column IDs in this array will exactly correspond to the input array of column definitions.</span></span> <span data-ttu-id="a1585-180">В результате размер этого буфера должен соответствовать размеру входного массива.</span><span class="sxs-lookup"><span data-stu-id="a1585-180">As a result, the size of this buffer must correspond to the size of the input array.</span></span>

### <a name="return-value"></a><span data-ttu-id="a1585-181">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a1585-181">Return Value</span></span>

<span data-ttu-id="a1585-182">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="a1585-182">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="a1585-183">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="a1585-183">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a1585-184">Код возврата</span><span class="sxs-lookup"><span data-stu-id="a1585-184">Return code</span></span></p></th>
<th><p><span data-ttu-id="a1585-185">Описание</span><span class="sxs-lookup"><span data-stu-id="a1585-185">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a1585-186">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="a1585-186">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="a1585-187">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="a1585-187">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1585-188">JET_errCannotMaterializeForwardOnlySort</span><span class="sxs-lookup"><span data-stu-id="a1585-188">JET_errCannotMaterializeForwardOnlySort</span></span></p></td>
<td><p><span data-ttu-id="a1585-189">Произошел сбой <strong>JetOpenTempTable3</strong> , так как указана JET_bitTTForwardOnly, а временная таблица указана не может быть создана с помощью оптимизации "только вперед".</span><span class="sxs-lookup"><span data-stu-id="a1585-189"><strong>JetOpenTempTable3</strong> failed because JET_bitTTForwardOnly was specified and the temporary table as specified could not be created using the forward-only optimization.</span></span> <span data-ttu-id="a1585-190">Эта ошибка будет возвращена только в Windows Server 2003 и более поздних выпусках.</span><span class="sxs-lookup"><span data-stu-id="a1585-190">This error will only be returned by Windows Server 2003 and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1585-191">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="a1585-191">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="a1585-192">Невозможно выполнить операцию, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</span><span class="sxs-lookup"><span data-stu-id="a1585-192">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1585-193">JET_errIndexInvalidDef</span><span class="sxs-lookup"><span data-stu-id="a1585-193">JET_errIndexInvalidDef</span></span></p></td>
<td><p><span data-ttu-id="a1585-194">Не удалось создать индекс, так как было указано недопустимое определение индекса.</span><span class="sxs-lookup"><span data-stu-id="a1585-194">The index could not be created because an invalid index definition was specified.</span></span> <span data-ttu-id="a1585-195"><strong>JetOpenTempTable3</strong> будет возвращать эту ошибку в следующих случаях:</span><span class="sxs-lookup"><span data-stu-id="a1585-195"><strong>JetOpenTempTable3</strong> will return this error when:</span></span></p>
<ul>
<li><p><span data-ttu-id="a1585-196">Указан языковой стандарт, не зависящий от языка.</span><span class="sxs-lookup"><span data-stu-id="a1585-196">The Language Neutral locale is specified.</span></span></p></li>
<li><p><span data-ttu-id="a1585-197">Указан недопустимый набор флагов нормализации.</span><span class="sxs-lookup"><span data-stu-id="a1585-197">An invalid set of normalization flags is specified.</span></span></p></li>
</ul>
<p><span data-ttu-id="a1585-198">Эта ошибка будет возвращена только Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="a1585-198">This error will only be returned by Windows 2000.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1585-199">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="a1585-199">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="a1585-200">Невозможно выполнить операцию, поскольку экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</span><span class="sxs-lookup"><span data-stu-id="a1585-200">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="a1585-201">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="a1585-201">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1585-202">JET_errInvalidCodePage</span><span class="sxs-lookup"><span data-stu-id="a1585-202">JET_errInvalidCodePage</span></span></p></td>
<td><p><span data-ttu-id="a1585-203">Элементу <strong>CP</strong> структуры <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> не задана допустимая кодовая страница.</span><span class="sxs-lookup"><span data-stu-id="a1585-203">The <strong>cp</strong> member of the <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> structure was not set to a valid code page.</span></span> <span data-ttu-id="a1585-204">Единственными допустимыми значениями для текстовых столбцов являются английский (1252) и Unicode (1200).</span><span class="sxs-lookup"><span data-stu-id="a1585-204">The only valid values for text columns are English (1252) and Unicode (1200).</span></span> <span data-ttu-id="a1585-205">Значение 0 означает, что будет использоваться по умолчанию (английский, 1252).</span><span class="sxs-lookup"><span data-stu-id="a1585-205">A value of 0 means the default will be used (English, 1252).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1585-206">JET_errInvalidColumnType</span><span class="sxs-lookup"><span data-stu-id="a1585-206">JET_errInvalidColumnType</span></span></p></td>
<td><p><span data-ttu-id="a1585-207">Элементу <strong>колтип</strong> структуры <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> не был задан допустимый тип столбца.</span><span class="sxs-lookup"><span data-stu-id="a1585-207">The <strong>coltyp</strong> member of the <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> structure was not set to a valid column type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1585-208">JET_errInvalidLanguageId</span><span class="sxs-lookup"><span data-stu-id="a1585-208">JET_errInvalidLanguageId</span></span></p></td>
<td><p><span data-ttu-id="a1585-209">Не удалось создать индекс, поскольку была предпринята попытка использовать недопустимый код локали.</span><span class="sxs-lookup"><span data-stu-id="a1585-209">The index could not be created because an attempt was made to use an invalid locale ID.</span></span> <span data-ttu-id="a1585-210">КОД локали может быть либо полностью недопустимым, либо связанный языковой пакет не может быть установлен.</span><span class="sxs-lookup"><span data-stu-id="a1585-210">The locale ID may either be completely invalid or the associated language pack may not be installed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1585-211">JET_errInvalidLCMapStringFlags</span><span class="sxs-lookup"><span data-stu-id="a1585-211">JET_errInvalidLCMapStringFlags</span></span></p></td>
<td><p><span data-ttu-id="a1585-212">Не удалось создать индекс, поскольку предпринята попытка использовать недопустимый набор флагов нормализации.</span><span class="sxs-lookup"><span data-stu-id="a1585-212">The index could not be created because an attempt was made to use an invalid set of normalization flags.</span></span> <span data-ttu-id="a1585-213">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="a1585-213">This error will only be returned by Windows XP and later releases.</span></span> <span data-ttu-id="a1585-214">В Windows 2000 недопустимые флаги нормализации приводят к JET_errIndexInvalidDef.</span><span class="sxs-lookup"><span data-stu-id="a1585-214">On Windows 2000, invalid normalization flags will result in JET_errIndexInvalidDef instead.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1585-215">JET_errInvalidSesid</span><span class="sxs-lookup"><span data-stu-id="a1585-215">JET_errInvalidSesid</span></span></p></td>
<td><p><span data-ttu-id="a1585-216">Недопустимый обработчик сеанса или ссылается на закрытый сеанс.</span><span class="sxs-lookup"><span data-stu-id="a1585-216">The session handle is invalid or refers to a closed session.</span></span> <span data-ttu-id="a1585-217">Эта ошибка не возвращается при всех обстоятельствах.</span><span class="sxs-lookup"><span data-stu-id="a1585-217">This error is not returned under all circumstances.</span></span> <span data-ttu-id="a1585-218">Дескрипторы проверяются только на основе наилучшей силы.</span><span class="sxs-lookup"><span data-stu-id="a1585-218">Handles are validated on a best effort basis only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1585-219">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="a1585-219">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="a1585-220">Невозможно выполнить операцию, так как экземпляр, связанный с сеансом, еще не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="a1585-220">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1585-221">JET_errOutOfCursors</span><span class="sxs-lookup"><span data-stu-id="a1585-221">JET_errOutOfCursors</span></span></p></td>
<td><p><span data-ttu-id="a1585-222">Не удалось выполнить операцию, так как подсистема не может выделить ресурсы, необходимые для открытия нового курсора.</span><span class="sxs-lookup"><span data-stu-id="a1585-222">The operation failed because the engine cannot allocate the resources required to open a new cursor.</span></span> <span data-ttu-id="a1585-223">Ресурсы курсора настраиваются с помощью <a href="gg294044(v=exchg.10).md">жетсетсистемпараметер</a> с <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>.</span><span class="sxs-lookup"><span data-stu-id="a1585-223">Cursor resources are configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1585-224">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="a1585-224">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="a1585-225">Не удалось выполнить операцию из-за нехватки памяти, выделенной для ее завершения.</span><span class="sxs-lookup"><span data-stu-id="a1585-225">The operation failed because not enough memory could be allocated to complete it.</span></span></p>
<p><span data-ttu-id="a1585-226"><strong>JetOpenTempTable3</strong> может возвращать JET_errOutOfMemory, если адресное пространство хост-процесса оказывается слишком фрагментированным.</span><span class="sxs-lookup"><span data-stu-id="a1585-226"><strong>JetOpenTempTable3</strong> can return JET_errOutOfMemory if the address space of the host process becomes too fragmented.</span></span> <span data-ttu-id="a1585-227">Временный диспетчер таблиц всегда выделяет 1 МБ адресного пространства для каждой временной таблицы, созданной независимо от объема сохраняемых данных.</span><span class="sxs-lookup"><span data-stu-id="a1585-227">The temporary table manager will always allocate a 1MB chunk of address space for every temporary table created regardless of the amount of data to be stored.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1585-228">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="a1585-228">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="a1585-229">Невозможно выполнить операцию, так как в экземпляре, связанном с сеансом, выполняется операция восстановления.</span><span class="sxs-lookup"><span data-stu-id="a1585-229">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1585-230">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="a1585-230">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="a1585-231">Один и тот же сеанс нельзя использовать одновременно для нескольких потоков.</span><span class="sxs-lookup"><span data-stu-id="a1585-231">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="a1585-232">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="a1585-232">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1585-233">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="a1585-233">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="a1585-234">Невозможно выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</span><span class="sxs-lookup"><span data-stu-id="a1585-234">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1585-235">JET_errTooManyColumns</span><span class="sxs-lookup"><span data-stu-id="a1585-235">JET_errTooManyColumns</span></span></p></td>
<td><p><span data-ttu-id="a1585-236">Предпринята попытка добавить в таблицу слишком много столбцов.</span><span class="sxs-lookup"><span data-stu-id="a1585-236">An attempt was made to add too many columns to the table.</span></span> <span data-ttu-id="a1585-237">Таблица может содержать не более JET_ccolFixedMost фиксированных столбцов, не более JET_ccolVarMost столбцов переменной длины и не более JET_ccolTaggedMost столбцов с тегами.</span><span class="sxs-lookup"><span data-stu-id="a1585-237">A table can have no more than JET_ccolFixedMost fixed columns, no more than JET_ccolVarMost variable-length columns, and no more than JET_ccolTaggedMost tagged columns.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1585-238">JET_errTooManyOpenIndexes</span><span class="sxs-lookup"><span data-stu-id="a1585-238">JET_errTooManyOpenIndexes</span></span></p></td>
<td><p><span data-ttu-id="a1585-239">Не удалось выполнить операцию, так как подсистема не может выделить ресурсы, необходимые для кэширования индексов таблицы.</span><span class="sxs-lookup"><span data-stu-id="a1585-239">The operation failed because the engine cannot allocate the resources required to cache the indexes of the table.</span></span> <span data-ttu-id="a1585-240">Количество индексов, схема которых может быть кэширована, настраивается с помощью <a href="gg294044(v=exchg.10).md">жетсетсистемпараметер</a> с <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</span><span class="sxs-lookup"><span data-stu-id="a1585-240">The number of indexes whose schema can be cached is configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1585-241">JET_errTooManyOpenTables</span><span class="sxs-lookup"><span data-stu-id="a1585-241">JET_errTooManyOpenTables</span></span></p></td>
<td><p><span data-ttu-id="a1585-242">Не удалось выполнить операцию, так как подсистема не может выделить ресурсы, необходимые для кэширования схемы таблицы.</span><span class="sxs-lookup"><span data-stu-id="a1585-242">The operation failed because the engine cannot allocate the resources required to cache the schema of the table.</span></span> <span data-ttu-id="a1585-243">Количество таблиц, схема которых может быть кэширована, настраивается с помощью <a href="gg294044(v=exchg.10).md">жетсетсистемпараметер</a> с <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</span><span class="sxs-lookup"><span data-stu-id="a1585-243">The number of tables whose schema can be cached is configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1585-244">JET_errTooManySorts</span><span class="sxs-lookup"><span data-stu-id="a1585-244">JET_errTooManySorts</span></span></p></td>
<td><p><span data-ttu-id="a1585-245">Не удалось выполнить операцию, так как подсистема не может выделить ресурсы, необходимые для создания временной таблицы.</span><span class="sxs-lookup"><span data-stu-id="a1585-245">The operation failed because the engine cannot allocate the resources required to create a temporary table.</span></span> <span data-ttu-id="a1585-246">Временные ресурсы таблицы настраиваются с помощью <a href="gg294044(v=exchg.10).md">жетсетсистемпараметер</a> с <a href="gg294140(v=exchg.10).md">JET_paramMaxTemporaryTables</a>.</span><span class="sxs-lookup"><span data-stu-id="a1585-246">Temporary table resources are configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg294140(v=exchg.10).md">JET_paramMaxTemporaryTables</a>.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a1585-247">При успешном выполнении будет возвращен курсор, Открытый во вновь созданной временной таблице.</span><span class="sxs-lookup"><span data-stu-id="a1585-247">On success, a cursor opened on the newly created temporary table will be returned.</span></span> <span data-ttu-id="a1585-248">Состояние временной базы данных будет подготовлено для размещения новой временной таблицы.</span><span class="sxs-lookup"><span data-stu-id="a1585-248">The state of the temporary database will be prepared to contain the new temporary table.</span></span> <span data-ttu-id="a1585-249">Состояние всех обычных баз данных, используемых ядром СУБД, останется неизменным.</span><span class="sxs-lookup"><span data-stu-id="a1585-249">The state of any ordinary databases in use by the database engine will remain unchanged.</span></span>

<span data-ttu-id="a1585-250">При сбое временная таблица не будет создана и курсор не будет возвращен.</span><span class="sxs-lookup"><span data-stu-id="a1585-250">On failure, the temporary table will not be created and a cursor will not be returned.</span></span> <span data-ttu-id="a1585-251">Состояние временной базы данных может быть изменено.</span><span class="sxs-lookup"><span data-stu-id="a1585-251">The state of the temporary database may be changed.</span></span> <span data-ttu-id="a1585-252">Состояние всех обычных баз данных, используемых ядром СУБД, останется неизменным.</span><span class="sxs-lookup"><span data-stu-id="a1585-252">The state of any ordinary databases in use by the database engine will remain unchanged.</span></span>

#### <a name="requirements"></a><span data-ttu-id="a1585-253">Требования</span><span class="sxs-lookup"><span data-stu-id="a1585-253">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a1585-254"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="a1585-254"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="a1585-255">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="a1585-255">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1585-256"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="a1585-256"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="a1585-257">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="a1585-257">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1585-258"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="a1585-258"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="a1585-259">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="a1585-259">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1585-260"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="a1585-260"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="a1585-261">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="a1585-261">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1585-262"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="a1585-262"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="a1585-263">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="a1585-263">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="a1585-264">См. также:</span><span class="sxs-lookup"><span data-stu-id="a1585-264">See Also</span></span>

[<span data-ttu-id="a1585-265">Ошибки расширяемого подсистемы хранилища</span><span class="sxs-lookup"><span data-stu-id="a1585-265">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="a1585-266">Параметры обработки ошибок</span><span class="sxs-lookup"><span data-stu-id="a1585-266">Error Handling Parameters</span></span>](./error-handling-parameters.md)  
[<span data-ttu-id="a1585-267">JET_COLUMNDEF</span><span class="sxs-lookup"><span data-stu-id="a1585-267">JET_COLUMNDEF</span></span>](./jet-columndef-structure.md)  
[<span data-ttu-id="a1585-268">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="a1585-268">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="a1585-269">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="a1585-269">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="a1585-270">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="a1585-270">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="a1585-271">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="a1585-271">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="a1585-272">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="a1585-272">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="a1585-273">JET_UNICODEINDEX</span><span class="sxs-lookup"><span data-stu-id="a1585-273">JET_UNICODEINDEX</span></span>](./jet-unicodeindex-structure.md)  
[<span data-ttu-id="a1585-274">жетклосетабле</span><span class="sxs-lookup"><span data-stu-id="a1585-274">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="a1585-275">жеткреатетаблеколумниндекс</span><span class="sxs-lookup"><span data-stu-id="a1585-275">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="a1585-276">жетдупкурсор</span><span class="sxs-lookup"><span data-stu-id="a1585-276">JetDupCursor</span></span>](./jetdupcursor-function.md)  
[<span data-ttu-id="a1585-277">жетмове</span><span class="sxs-lookup"><span data-stu-id="a1585-277">JetMove</span></span>](./jetmove-function.md)  
[<span data-ttu-id="a1585-278">жетопентемптабле</span><span class="sxs-lookup"><span data-stu-id="a1585-278">JetOpenTempTable</span></span>](./jetopentemptable-function.md)  
[<span data-ttu-id="a1585-279">жетроллбакк</span><span class="sxs-lookup"><span data-stu-id="a1585-279">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="a1585-280">жетсик</span><span class="sxs-lookup"><span data-stu-id="a1585-280">JetSeek</span></span>](./jetseek-function.md)  
[<span data-ttu-id="a1585-281">жетсетсистемпараметер</span><span class="sxs-lookup"><span data-stu-id="a1585-281">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="a1585-282">Системные параметры</span><span class="sxs-lookup"><span data-stu-id="a1585-282">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
