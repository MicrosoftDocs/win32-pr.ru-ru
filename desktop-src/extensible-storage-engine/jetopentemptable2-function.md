---
description: Дополнительные сведения о функции JetOpenTempTable2
title: Функция JetOpenTempTable2
TOCTitle: JetOpenTempTable2 Function
ms:assetid: 788ec4f9-b0c3-409b-850c-7567dec47024
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269302(v=EXCHG.10)
ms:contentKeyID: 32765594
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenTempTable2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 324bcde75c0ba9376c8ad9f5e98df585b1d341e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693348"
---
# <a name="jetopentemptable2-function"></a><span data-ttu-id="54f73-103">Функция JetOpenTempTable2</span><span class="sxs-lookup"><span data-stu-id="54f73-103">JetOpenTempTable2 Function</span></span>


<span data-ttu-id="54f73-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="54f73-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetopentemptable2-function"></a><span data-ttu-id="54f73-105">Функция JetOpenTempTable2</span><span class="sxs-lookup"><span data-stu-id="54f73-105">JetOpenTempTable2 Function</span></span>

<span data-ttu-id="54f73-106">Функция **JetOpenTempTable2** создает временную таблицу с одним индексом, который может использоваться для хранения и извлечения записей точно так же, как обычная таблица, созданная с помощью [жеткреатетаблеколумниндекс](./jetcreatetablecolumnindex-function.md).</span><span class="sxs-lookup"><span data-stu-id="54f73-106">The **JetOpenTempTable2** function creates a temporary table with a single index that can be used to store and retrieve records just like an ordinary table created using [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md).</span></span> <span data-ttu-id="54f73-107">Эта функция также имеет код локали, который можно использовать для сравнения данных ключевого столбца Юникода во временной таблице.</span><span class="sxs-lookup"><span data-stu-id="54f73-107">This function also has a Locale ID that can be used to compare Unicode key column data in the temporary table.</span></span> <span data-ttu-id="54f73-108">Однако временные таблицы выполняются гораздо быстрее, чем обычные таблицы, в связи с их постоянным характером.</span><span class="sxs-lookup"><span data-stu-id="54f73-108">However, temporary tables are much faster than ordinary tables due to their volatile nature.</span></span> <span data-ttu-id="54f73-109">Они также могут использоваться для очень быстрой сортировки и удаления дубликатов наборов записей при обращении к ним только последовательно.</span><span class="sxs-lookup"><span data-stu-id="54f73-109">They can also be used to very quickly sort and perform duplicate removal on record sets when accessed in a purely sequential manner.</span></span>

```cpp
    JET_ERR JET_API JetOpenTempTable2(
      __in          JET_SESID sesid,
      __in          const JET_COLUMNDEF* prgcolumndef,
      __in          unsigned long ccolumn,
      __in          unsigned long lcid,
      __in          JET_GRBIT grbit,
      __out         JET_TABLEID* ptableid,
      __out         JET_COLUMNID* prgcolumnid
    );
```

### <a name="parameters"></a><span data-ttu-id="54f73-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="54f73-110">Parameters</span></span>

<span data-ttu-id="54f73-111">*сесид*</span><span class="sxs-lookup"><span data-stu-id="54f73-111">*sesid*</span></span>

<span data-ttu-id="54f73-112">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="54f73-112">The session to use.</span></span>

<span data-ttu-id="54f73-113">*пргколумндеф*</span><span class="sxs-lookup"><span data-stu-id="54f73-113">*prgcolumndef*</span></span>

<span data-ttu-id="54f73-114">Определения столбцов для столбцов, создаваемых во временной таблице.</span><span class="sxs-lookup"><span data-stu-id="54f73-114">The column definitions of the columns to be created in the temporary table.</span></span>

<span data-ttu-id="54f73-115">Для параметров определения столбца, используемых во временной таблице, имеются важные ограничения.</span><span class="sxs-lookup"><span data-stu-id="54f73-115">Important limitations exist for the column definition options that are used with a temporary table.</span></span> <span data-ttu-id="54f73-116">Дополнительные сведения см. в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="54f73-116">See the Remarks section for more information.</span></span>

<span data-ttu-id="54f73-117">В дополнение к обычным параметрам определения столбца можно также указать ноль или более следующих параметров, которые важны только в контексте временной таблицы.</span><span class="sxs-lookup"><span data-stu-id="54f73-117">In addition to the usual column definition options, zero or more of the following options can also be specified that are relevant only in the context of a temporary table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="54f73-118">Значение</span><span class="sxs-lookup"><span data-stu-id="54f73-118">Value</span></span></p></th>
<th><p><span data-ttu-id="54f73-119">Значение</span><span class="sxs-lookup"><span data-stu-id="54f73-119">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="54f73-120">JET_bitColumnTTDescending</span><span class="sxs-lookup"><span data-stu-id="54f73-120">JET_bitColumnTTDescending</span></span></p></td>
<td><p><span data-ttu-id="54f73-121">Порядок сортировки ключевого столбца для временной таблицы должен быть по убыванию, а не по возрастанию.</span><span class="sxs-lookup"><span data-stu-id="54f73-121">The sort order of the key column for the temporary table should be descending rather than ascending.</span></span> <span data-ttu-id="54f73-122">Если этот параметр указан без JET_bitColumnTTKey то этот параметр игнорируется.</span><span class="sxs-lookup"><span data-stu-id="54f73-122">If this option is specified without JET_bitColumnTTKey then this option is ignored.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54f73-123">JET_bitColumnTTKey</span><span class="sxs-lookup"><span data-stu-id="54f73-123">JET_bitColumnTTKey</span></span></p></td>
<td><p><span data-ttu-id="54f73-124">Столбец будет ключевым столбцом для временной таблицы.</span><span class="sxs-lookup"><span data-stu-id="54f73-124">The column will be a key column for the temporary table.</span></span></p>
<p><span data-ttu-id="54f73-125">Порядок определений столбцов с этим параметром, указанным во входном массиве, определяет приоритет каждого ключевого столбца для временной таблицы.</span><span class="sxs-lookup"><span data-stu-id="54f73-125">The order of the column definitions with this option specified in the input array will determine the precedence of each key column for the temporary table.</span></span> <span data-ttu-id="54f73-126">Первое определение столбца в массиве с этим набором параметров будет наиболее значимым ключевым столбцом и т. д.</span><span class="sxs-lookup"><span data-stu-id="54f73-126">The first column definition in the array with this option set will be the most significant key column and so on.</span></span> <span data-ttu-id="54f73-127">Если запрошено больше ключевых столбцов, чем может поддерживать ядро СУБД, этот параметр игнорируется для неподдерживаемых ключевых столбцов.</span><span class="sxs-lookup"><span data-stu-id="54f73-127">If more key columns are requested than can be supported by the database engine then this option is ignored for the unsupportable key columns.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="54f73-128">*кколумн*</span><span class="sxs-lookup"><span data-stu-id="54f73-128">*ccolumn*</span></span>

<span data-ttu-id="54f73-129">См. *пргколумндеф*.</span><span class="sxs-lookup"><span data-stu-id="54f73-129">See *prgcolumndef*.</span></span>

<span data-ttu-id="54f73-130">*lcid*</span><span class="sxs-lookup"><span data-stu-id="54f73-130">*lcid*</span></span>

<span data-ttu-id="54f73-131">КОД локали, используемый для сравнения данных любого ключевого столбца Юникода во временной таблице.</span><span class="sxs-lookup"><span data-stu-id="54f73-131">The locale ID to use to compare any Unicode key column data in the temporary table.</span></span>

<span data-ttu-id="54f73-132">Любой языковой стандарт может использоваться при условии, что на компьютере установлен соответствующий языковой пакет.</span><span class="sxs-lookup"><span data-stu-id="54f73-132">Any locale may be used as long as the appropriate language pack has been installed on the machine.</span></span> <span data-ttu-id="54f73-133">Единственное исключение заключается в том, что независимый от языка языковой стандарт (LCID 0) является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="54f73-133">The one exception is that the Language Neutral locale (LCID of zero) is illegal.</span></span>

<span data-ttu-id="54f73-134">В Windows Server 2003 и более поздних версиях, если для этого параметра задан язык, не зависящий от языка, вместо него будет использоваться идентификатор локали по умолчанию (Английский (США)).</span><span class="sxs-lookup"><span data-stu-id="54f73-134">On Windows Server 2003 and later, if the Language Neutral locale is specified for this parameter then the default locale ID (U.S. English) will be used instead.</span></span> <span data-ttu-id="54f73-135">Это позволяет использовать нулевое значение для обозначения значения по умолчанию, а не недопустимого значения.</span><span class="sxs-lookup"><span data-stu-id="54f73-135">This is to allow a value of zero to signify the default rather than an illegal value.</span></span>

<span data-ttu-id="54f73-136">Если этот параметр отсутствует и параметр *пидксуникоде* отсутствует, то для сравнения данных любого ключевого столбца Юникода во временной таблице будет использоваться код по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="54f73-136">When this parameter is not present and when the *pidxunicode* parameter is not present, then the default LCID will be used to compare any Unicode key column data in the temporary table.</span></span> <span data-ttu-id="54f73-137">По умолчанию используется языковой стандарт «Английский (США)».</span><span class="sxs-lookup"><span data-stu-id="54f73-137">The default LCID is the U.S. English locale.</span></span>

<span data-ttu-id="54f73-138">*грбит*</span><span class="sxs-lookup"><span data-stu-id="54f73-138">*grbit*</span></span>

<span data-ttu-id="54f73-139">Группа битов, содержащая параметры, которые должны использоваться для этого вызова, включая ноль или более следующих значений.</span><span class="sxs-lookup"><span data-stu-id="54f73-139">A group of bits that contain the options to be used for this call, which include zero or more of the following.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="54f73-140">Значение</span><span class="sxs-lookup"><span data-stu-id="54f73-140">Value</span></span></p></th>
<th><p><span data-ttu-id="54f73-141">Значение</span><span class="sxs-lookup"><span data-stu-id="54f73-141">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="54f73-142">JET_bitTTErrorOnDuplicateInsertion</span><span class="sxs-lookup"><span data-stu-id="54f73-142">JET_bitTTErrorOnDuplicateInsertion</span></span></p></td>
<td><p><span data-ttu-id="54f73-143">Этот параметр запрашивает неудачную попытку вставки записи с тем же ключом индекса, что и ранее вставленная запись, с JET_errKeyDuplicate.</span><span class="sxs-lookup"><span data-stu-id="54f73-143">This option requests that any attempt to insert a record with the same index key as a previously inserted record will immediately fail with JET_errKeyDuplicate.</span></span> <span data-ttu-id="54f73-144">Если этот параметр не запрошен, то дубликат может быть обнаружен немедленно, с ошибкой или автоматически удален позже в зависимости от стратегии, выбранной ядром СУБД для реализации временной таблицы на основе запрошенной функциональности.</span><span class="sxs-lookup"><span data-stu-id="54f73-144">If this option is not requested then a duplicate may be detected immediately and fail or may be silently removed later depending on the strategy chosen by the database engine to implement the temporary table based on the requested functionality.</span></span></p>
<p><span data-ttu-id="54f73-145">Если эта функция не требуется, то лучше не запрашивать ее.</span><span class="sxs-lookup"><span data-stu-id="54f73-145">If this functionality it not required then it is best to not request it.</span></span> <span data-ttu-id="54f73-146">Если эта функция не запрошена, то диспетчер временных таблиц может выбрать стратегию для управления временной таблицей, что приведет к повышению производительности.</span><span class="sxs-lookup"><span data-stu-id="54f73-146">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54f73-147">JET_bitTTForceMaterialization</span><span class="sxs-lookup"><span data-stu-id="54f73-147">JET_bitTTForceMaterialization</span></span></p></td>
<td><p><span data-ttu-id="54f73-148">Этот параметр заставляет диспетчер временных таблиц отказаться от любой попытки выбрать стратегию для управления временной таблицей, что приведет к повышению производительности.</span><span class="sxs-lookup"><span data-stu-id="54f73-148">This option forces the temporary table manager to abandon any attempt to choose a clever strategy for managing the temporary table that will result in enhanced performance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54f73-149">JET_bitTTForwardOnly</span><span class="sxs-lookup"><span data-stu-id="54f73-149">JET_bitTTForwardOnly</span></span></p></td>
<td><p><span data-ttu-id="54f73-150">Этот параметр запрашивает создание временной таблицы только в том случае, если диспетчер временных таблиц может использовать реализацию, оптимизированную для промежуточных результатов запроса.</span><span class="sxs-lookup"><span data-stu-id="54f73-150">This option requests that the temporary table only be created if the temporary table manager can use the implementation optimized for intermediate query results.</span></span> <span data-ttu-id="54f73-151">Если любая характеристика временной таблицы не позволит использовать эту оптимизацию, операция завершится с JET_errCannotMaterializeForwardOnlySort.</span><span class="sxs-lookup"><span data-stu-id="54f73-151">If any characteristic of the temporary table would prevent the use of this optimization then the operation will fail with JET_errCannotMaterializeForwardOnlySort.</span></span></p>
<p><span data-ttu-id="54f73-152">Побочный результат этого параметра — Разрешить временной таблице содержать записи с повторяющимися ключами индекса.</span><span class="sxs-lookup"><span data-stu-id="54f73-152">A side effect of this option is to allow the temporary table to contain records with duplicate index keys.</span></span> <span data-ttu-id="54f73-153">Дополнительные сведения см. в разделе JET_bitTTUnique.</span><span class="sxs-lookup"><span data-stu-id="54f73-153">See JET_bitTTUnique for more information.</span></span></p>
<p><span data-ttu-id="54f73-154">Этот параметр доступен только в выпусках Windows Server 2003 и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="54f73-154">This option is only available on Windows Server 2003 and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54f73-155">JET_bitTTIndexed</span><span class="sxs-lookup"><span data-stu-id="54f73-155">JET_bitTTIndexed</span></span></p></td>
<td><p><span data-ttu-id="54f73-156">Этот параметр требует, чтобы временная таблица была достаточно гибкой, чтобы позволить использовать <a href="gg294103(v=exchg.10).md">жетсик</a> для поиска записей по ключу индекса.</span><span class="sxs-lookup"><span data-stu-id="54f73-156">This option requests that the temporary table be flexible enough to permit the use of <a href="gg294103(v=exchg.10).md">JetSeek</a> to look up records by index key.</span></span></p>
<p><span data-ttu-id="54f73-157">Если эта функция не требуется, то лучше не запрашивать ее.</span><span class="sxs-lookup"><span data-stu-id="54f73-157">If this functionality it not required then it is best to not request it.</span></span> <span data-ttu-id="54f73-158">Если эта функция не запрошена, то диспетчер временных таблиц может выбрать стратегию для управления временной таблицей, что приведет к повышению производительности.</span><span class="sxs-lookup"><span data-stu-id="54f73-158">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54f73-159">JET_bitTTScrollable</span><span class="sxs-lookup"><span data-stu-id="54f73-159">JET_bitTTScrollable</span></span></p></td>
<td><p><span data-ttu-id="54f73-160">Этот параметр требует, чтобы временная таблица была достаточно гибкой, чтобы разрешить сканирование записей в произвольном порядке и направлении с помощью <a href="gg294117(v=exchg.10).md">жетмове</a>.</span><span class="sxs-lookup"><span data-stu-id="54f73-160">This option requests that the temporary table be flexible enough to allow records to be scanned in arbitrary order and direction using <a href="gg294117(v=exchg.10).md">JetMove</a>.</span></span></p>
<p><span data-ttu-id="54f73-161">Если эта функция не требуется, то лучше не запрашивать ее.</span><span class="sxs-lookup"><span data-stu-id="54f73-161">If this functionality it not required then it is best to not request it.</span></span> <span data-ttu-id="54f73-162">Если эта функция не запрошена, то диспетчер временных таблиц может выбрать стратегию для управления временной таблицей, что приведет к повышению производительности.</span><span class="sxs-lookup"><span data-stu-id="54f73-162">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54f73-163">JET_bitTTSortNullsHigh</span><span class="sxs-lookup"><span data-stu-id="54f73-163">JET_bitTTSortNullsHigh</span></span></p></td>
<td><p><span data-ttu-id="54f73-164">При выборе этого варианта значения ключевого столбца NULL сортируются ближе к концу индекса, чем значения ключевого столбца, отличные от NULL.</span><span class="sxs-lookup"><span data-stu-id="54f73-164">This option requests that NULL key column values sort closer to the end of the index than non-NULL key column values.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54f73-165">JET_bitTTUnique</span><span class="sxs-lookup"><span data-stu-id="54f73-165">JET_bitTTUnique</span></span></p></td>
<td><p><span data-ttu-id="54f73-166">Этот параметр запрашивает удаление записей с повторяющимися ключами индекса из окончательного набора записей во временной таблице.</span><span class="sxs-lookup"><span data-stu-id="54f73-166">This option requests that records with duplicate index keys be removed from the final set of records in the temporary table.</span></span></p>
<p><span data-ttu-id="54f73-167">До Windows Server 2003 в ядре СУБД всегда предполагается, что этот параметр действует из-за того факта, что все кластеризованные индексы также должны быть первичным ключом и, таким же, должны быть уникальными.</span><span class="sxs-lookup"><span data-stu-id="54f73-167">Prior to Windows Server 2003, the database engine always assumed this option to be in effect due to the fact that all clustered indexes must also be a primary key and thus must be unique.</span></span> <span data-ttu-id="54f73-168">Начиная с Windows Server 2003, теперь можно создать временную таблицу, которая не удаляет дубликаты, если также указан параметр JET_bitTTForwardOnly.</span><span class="sxs-lookup"><span data-stu-id="54f73-168">As of Windows Server 2003, it is now possible to create a temporary table that does NOT remove duplicates when the JET_bitTTForwardOnly option is also specified.</span></span></p>
<p><span data-ttu-id="54f73-169">Невозможно понять, какие дубликаты будут выдаваться, и какие дубликаты будут отменены в целом.</span><span class="sxs-lookup"><span data-stu-id="54f73-169">It is not possible to know which duplicate will win and which duplicates will be discarded in general.</span></span> <span data-ttu-id="54f73-170">Однако при запросе параметра JET_bitTTErrorOnDuplicateInsertion первая запись с заданным ключом индекса для вставки во временную таблицу всегда будет выдаваться.</span><span class="sxs-lookup"><span data-stu-id="54f73-170">However, when the JET_bitTTErrorOnDuplicateInsertion option is requested then the first record with a given index key to be inserted into the temporary table will always win.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54f73-171">JET_bitTTUpdatable</span><span class="sxs-lookup"><span data-stu-id="54f73-171">JET_bitTTUpdatable</span></span></p></td>
<td><p><span data-ttu-id="54f73-172">Этот параметр требует, чтобы временная таблица была достаточно гибкой, чтобы разрешить впоследствии изменять записи, которые были вставлены.</span><span class="sxs-lookup"><span data-stu-id="54f73-172">This option requests that the temporary table be flexible enough to allow records that have previously been inserted to be subsequently changed.</span></span> <span data-ttu-id="54f73-173">Если эта функция не требуется, то лучше не запрашивать ее.</span><span class="sxs-lookup"><span data-stu-id="54f73-173">If this functionality it not required then it is best to not request it.</span></span></p>
<p><span data-ttu-id="54f73-174">Если эта функция не запрошена, то диспетчер временных таблиц может выбрать стратегию для управления временной таблицей, что приведет к повышению производительности.</span><span class="sxs-lookup"><span data-stu-id="54f73-174">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54f73-175">JET_bitTTIntrinsicLVsOnly</span><span class="sxs-lookup"><span data-stu-id="54f73-175">JET_bitTTIntrinsicLVsOnly</span></span></p></td>
<td><p><span data-ttu-id="54f73-176">Запросы на разрешение только внутренних значений типа long.</span><span class="sxs-lookup"><span data-stu-id="54f73-176">Requests to permit only intrinsic long values.</span></span></p>
<p><span data-ttu-id="54f73-177"><strong>Windows 7</strong>: <strong>JET_bitTTIntrinsicLVsOnly</strong> введен в Windows 7.</span><span class="sxs-lookup"><span data-stu-id="54f73-177"><strong>Windows 7</strong>: <strong>JET_bitTTIntrinsicLVsOnly</strong> is introduced in Windows 7.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="54f73-178">*pTableID*</span><span class="sxs-lookup"><span data-stu-id="54f73-178">*ptableid*</span></span>

<span data-ttu-id="54f73-179">Выходной буфер, который получит новый курсор, Открытый во вновь созданной временной таблице.</span><span class="sxs-lookup"><span data-stu-id="54f73-179">The output buffer that will receive the new cursor opened on the newly created temporary table.</span></span>

<span data-ttu-id="54f73-180">*пргколумнид*</span><span class="sxs-lookup"><span data-stu-id="54f73-180">*prgcolumnid*</span></span>

<span data-ttu-id="54f73-181">Выходной буфер, который будет принимать массив идентификаторов столбцов, сформированных во время создания временной таблицы.</span><span class="sxs-lookup"><span data-stu-id="54f73-181">The output buffer that will receive the array of column IDs generated during the creation of the temporary table.</span></span>

<span data-ttu-id="54f73-182">Идентификаторы столбцов в этом массиве будут точно соответствовать входному массиву определений столбцов.</span><span class="sxs-lookup"><span data-stu-id="54f73-182">The column IDs in this array will exactly correspond to the input array of column definitions.</span></span> <span data-ttu-id="54f73-183">В результате размер этого буфера должен соответствовать размеру входного массива.</span><span class="sxs-lookup"><span data-stu-id="54f73-183">As a result, the size of this buffer must correspond to the size of the input array.</span></span>

### <a name="return-value"></a><span data-ttu-id="54f73-184">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="54f73-184">Return Value</span></span>

<span data-ttu-id="54f73-185">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="54f73-185">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="54f73-186">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="54f73-186">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="54f73-187">Код возврата</span><span class="sxs-lookup"><span data-stu-id="54f73-187">Return code</span></span></p></th>
<th><p><span data-ttu-id="54f73-188">Описание</span><span class="sxs-lookup"><span data-stu-id="54f73-188">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="54f73-189">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="54f73-189">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="54f73-190">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="54f73-190">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54f73-191">JET_errCannotMaterializeForwardOnlySort</span><span class="sxs-lookup"><span data-stu-id="54f73-191">JET_errCannotMaterializeForwardOnlySort</span></span></p></td>
<td><p><span data-ttu-id="54f73-192">Произошел сбой <strong>JetOpenTempTable2</strong> , так как указана JET_bitTTForwardOnly, а временная таблица указана не может быть создана с помощью оптимизации "только вперед".</span><span class="sxs-lookup"><span data-stu-id="54f73-192"><strong>JetOpenTempTable2</strong> failed because JET_bitTTForwardOnly was specified and the temporary table as specified could not be created using the forward-only optimization.</span></span> <span data-ttu-id="54f73-193">Эта ошибка будет возвращена только в Windows Server 2003 и более поздних выпусках.</span><span class="sxs-lookup"><span data-stu-id="54f73-193">This error will only be returned by Windows Server 2003 and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54f73-194">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="54f73-194">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="54f73-195">Невозможно выполнить операцию, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</span><span class="sxs-lookup"><span data-stu-id="54f73-195">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54f73-196">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="54f73-196">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="54f73-197">Невозможно выполнить операцию, поскольку экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</span><span class="sxs-lookup"><span data-stu-id="54f73-197">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="54f73-198">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="54f73-198">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54f73-199">JET_errInvalidCodePage</span><span class="sxs-lookup"><span data-stu-id="54f73-199">JET_errInvalidCodePage</span></span></p></td>
<td><p><span data-ttu-id="54f73-200">Поле CP <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> не было задано как допустимая кодовая страница.</span><span class="sxs-lookup"><span data-stu-id="54f73-200">The cp field of the <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> was not set to a valid code page.</span></span> <span data-ttu-id="54f73-201">Единственными допустимыми значениями для текстовых столбцов являются английский (1252) и Unicode (1200).</span><span class="sxs-lookup"><span data-stu-id="54f73-201">The only valid values for text columns are English (1252) and Unicode (1200).</span></span> <span data-ttu-id="54f73-202">Значение 0 означает, что будет использоваться по умолчанию (английский, 1252).</span><span class="sxs-lookup"><span data-stu-id="54f73-202">A value of 0 means the default will be used (English, 1252).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54f73-203">JET_errInvalidColumnType</span><span class="sxs-lookup"><span data-stu-id="54f73-203">JET_errInvalidColumnType</span></span></p></td>
<td><p><span data-ttu-id="54f73-204">Для поля <em>колтип</em> <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> не был задан допустимый тип столбца.</span><span class="sxs-lookup"><span data-stu-id="54f73-204">The <em>coltyp</em> field of the <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> was not set to a valid column type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54f73-205">JET_errIndexInvalidDef</span><span class="sxs-lookup"><span data-stu-id="54f73-205">JET_errIndexInvalidDef</span></span></p></td>
<td><p><span data-ttu-id="54f73-206">Не удалось создать индекс, так как было указано недопустимое определение индекса.</span><span class="sxs-lookup"><span data-stu-id="54f73-206">The index could not be created because an invalid index definition was specified.</span></span></p>
<p><span data-ttu-id="54f73-207"><strong>JetOpenTempTable2</strong> будет возвращать эту ошибку в следующих случаях:</span><span class="sxs-lookup"><span data-stu-id="54f73-207"><strong>JetOpenTempTable2</strong> will return this error when:</span></span></p>
<ul>
<li><p><span data-ttu-id="54f73-208">Указан языковой стандарт, не зависящий от языка.</span><span class="sxs-lookup"><span data-stu-id="54f73-208">The Language Neutral locale is specified.</span></span></p></li>
<li><p><span data-ttu-id="54f73-209">Указан недопустимый набор флагов нормализации.</span><span class="sxs-lookup"><span data-stu-id="54f73-209">An invalid set of normalization flags is specified.</span></span></p></li>
</ul>
<p><span data-ttu-id="54f73-210">Эта ошибка будет возвращена только Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="54f73-210">This error will only be returned by Windows 2000.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54f73-211">JET_errInvalidLanguageId</span><span class="sxs-lookup"><span data-stu-id="54f73-211">JET_errInvalidLanguageId</span></span></p></td>
<td><p><span data-ttu-id="54f73-212">Не удалось создать индекс, поскольку была предпринята попытка использовать недопустимый код локали.</span><span class="sxs-lookup"><span data-stu-id="54f73-212">The index could not be created because an attempt was made to use an invalid locale ID.</span></span> <span data-ttu-id="54f73-213">КОД локали может быть либо полностью недопустимым, либо связанный языковой пакет не может быть установлен.</span><span class="sxs-lookup"><span data-stu-id="54f73-213">The locale ID may either be completely invalid or the associated language pack may not be installed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54f73-214">JET_errInvalidLCMapStringFlags</span><span class="sxs-lookup"><span data-stu-id="54f73-214">JET_errInvalidLCMapStringFlags</span></span></p></td>
<td><p><span data-ttu-id="54f73-215">Не удалось создать индекс, поскольку предпринята попытка использовать недопустимый набор флагов нормализации.</span><span class="sxs-lookup"><span data-stu-id="54f73-215">The index could not be created because an attempt was made to use an invalid set of normalization flags.</span></span> <span data-ttu-id="54f73-216">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="54f73-216">This error will only be returned by Windows XP and later releases.</span></span> <span data-ttu-id="54f73-217">В Windows 2000 недопустимые флаги нормализации приводят к JET_errIndexInvalidDef.</span><span class="sxs-lookup"><span data-stu-id="54f73-217">On Windows 2000, invalid normalization flags will result in JET_errIndexInvalidDef instead.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54f73-218">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="54f73-218">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="54f73-219">Невозможно выполнить операцию, так как экземпляр, связанный с сеансом, еще не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="54f73-219">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54f73-220">JET_errOutOfCursors</span><span class="sxs-lookup"><span data-stu-id="54f73-220">JET_errOutOfCursors</span></span></p></td>
<td><p><span data-ttu-id="54f73-221">Не удалось выполнить операцию, так как подсистема не может выделить ресурсы, необходимые для открытия нового курсора.</span><span class="sxs-lookup"><span data-stu-id="54f73-221">The operation failed because the engine cannot allocate the resources required to open a new cursor.</span></span> <span data-ttu-id="54f73-222">Ресурсы курсора настраиваются с помощью <a href="gg294044(v=exchg.10).md">жетсетсистемпараметер</a> с <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>.</span><span class="sxs-lookup"><span data-stu-id="54f73-222">Cursor resources are configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54f73-223">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="54f73-223">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="54f73-224">Не удалось выполнить операцию из-за нехватки памяти, выделенной для ее завершения.</span><span class="sxs-lookup"><span data-stu-id="54f73-224">The operation failed because not enough memory could be allocated to complete it.</span></span></p>
<p><span data-ttu-id="54f73-225"><strong>JetOpenTempTable2</strong> может возвращать JET_errOutOfMemory, если адресное пространство хост-процесса оказывается слишком фрагментированным.</span><span class="sxs-lookup"><span data-stu-id="54f73-225"><strong>JetOpenTempTable2</strong> can return JET_errOutOfMemory if the address space of the host process becomes too fragmented.</span></span> <span data-ttu-id="54f73-226">Временный диспетчер таблиц всегда выделяет 1 МБ адресного пространства для каждой временной таблицы, созданной независимо от объема сохраняемых данных.</span><span class="sxs-lookup"><span data-stu-id="54f73-226">The temporary table manager will always allocate a 1MB chunk of address space for every temporary table created regardless of the amount of data to be stored.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54f73-227">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="54f73-227">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="54f73-228">Невозможно выполнить операцию, так как в экземпляре, связанном с сеансом, выполняется операция восстановления.</span><span class="sxs-lookup"><span data-stu-id="54f73-228">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54f73-229">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="54f73-229">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="54f73-230">Один и тот же сеанс нельзя использовать одновременно для нескольких потоков.</span><span class="sxs-lookup"><span data-stu-id="54f73-230">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="54f73-231">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="54f73-231">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54f73-232">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="54f73-232">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="54f73-233">Невозможно выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</span><span class="sxs-lookup"><span data-stu-id="54f73-233">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54f73-234">JET_errTooManyColumns</span><span class="sxs-lookup"><span data-stu-id="54f73-234">JET_errTooManyColumns</span></span></p></td>
<td><p><span data-ttu-id="54f73-235">Предпринята попытка добавить в таблицу слишком много столбцов.</span><span class="sxs-lookup"><span data-stu-id="54f73-235">An attempt was made to add too many columns to the table.</span></span> <span data-ttu-id="54f73-236">Таблица может содержать не более JET_ccolFixedMost фиксированных столбцов, не более JET_ccolVarMost столбцов переменной длины и не более JET_ccolTaggedMost столбцов с тегами.</span><span class="sxs-lookup"><span data-stu-id="54f73-236">A table can have no more than JET_ccolFixedMost fixed columns, no more than JET_ccolVarMost variable-length columns, and no more than JET_ccolTaggedMost tagged columns.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54f73-237">JET_errTooManyOpenIndexes</span><span class="sxs-lookup"><span data-stu-id="54f73-237">JET_errTooManyOpenIndexes</span></span></p></td>
<td><p><span data-ttu-id="54f73-238">Не удалось выполнить операцию, так как подсистема не может выделить ресурсы, необходимые для кэширования индексов таблицы.</span><span class="sxs-lookup"><span data-stu-id="54f73-238">The operation failed because the engine cannot allocate the resources required to cache the indexes of the table.</span></span> <span data-ttu-id="54f73-239">Количество индексов, схема которых может быть кэширована, настраивается с помощью <a href="gg294044(v=exchg.10).md">жетсетсистемпараметер</a> с <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</span><span class="sxs-lookup"><span data-stu-id="54f73-239">The number of indexes whose schema can be cached is configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54f73-240">JET_errTooManyOpenTables</span><span class="sxs-lookup"><span data-stu-id="54f73-240">JET_errTooManyOpenTables</span></span></p></td>
<td><p><span data-ttu-id="54f73-241">Не удалось выполнить операцию, так как подсистема не может выделить ресурсы, необходимые для кэширования схемы таблицы.</span><span class="sxs-lookup"><span data-stu-id="54f73-241">The operation failed because the engine cannot allocate the resources required to cache the schema of the table.</span></span> <span data-ttu-id="54f73-242">Количество таблиц, схема которых может быть кэширована, настраивается с помощью <a href="gg294044(v=exchg.10).md">жетсетсистемпараметер</a> с <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</span><span class="sxs-lookup"><span data-stu-id="54f73-242">The number of tables whose schema can be cached is configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54f73-243">JET_errTooManySorts</span><span class="sxs-lookup"><span data-stu-id="54f73-243">JET_errTooManySorts</span></span></p></td>
<td><p><span data-ttu-id="54f73-244">Не удалось выполнить операцию, так как подсистема не может выделить ресурсы, необходимые для создания временной таблицы.</span><span class="sxs-lookup"><span data-stu-id="54f73-244">The operation failed because the engine cannot allocate the resources required to create a temporary table.</span></span> <span data-ttu-id="54f73-245">Временные ресурсы таблицы настраиваются с помощью <a href="gg294044(v=exchg.10).md">жетсетсистемпараметер</a> с <a href="gg294140(v=exchg.10).md">JET_paramMaxTemporaryTables</a>.</span><span class="sxs-lookup"><span data-stu-id="54f73-245">Temporary table resources are configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg294140(v=exchg.10).md">JET_paramMaxTemporaryTables</a>.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="54f73-246">При успешном выполнении будет возвращен курсор, Открытый во вновь созданной временной таблице.</span><span class="sxs-lookup"><span data-stu-id="54f73-246">On success, a cursor opened on the newly created temporary table will be returned.</span></span> <span data-ttu-id="54f73-247">Состояние временной базы данных будет подготовлено для размещения новой временной таблицы.</span><span class="sxs-lookup"><span data-stu-id="54f73-247">The state of the temporary database will be prepared to contain the new temporary table.</span></span> <span data-ttu-id="54f73-248">Состояние всех обычных баз данных, используемых ядром СУБД, останется неизменным.</span><span class="sxs-lookup"><span data-stu-id="54f73-248">The state of any ordinary databases in use by the database engine will remain unchanged.</span></span>

<span data-ttu-id="54f73-249">При сбое временная таблица не будет создана и курсор не будет возвращен.</span><span class="sxs-lookup"><span data-stu-id="54f73-249">On failure, the temporary table will not be created and a cursor will not be returned.</span></span> <span data-ttu-id="54f73-250">Состояние временной базы данных может быть изменено.</span><span class="sxs-lookup"><span data-stu-id="54f73-250">The state of the temporary database may be changed.</span></span> <span data-ttu-id="54f73-251">Состояние всех обычных баз данных, используемых ядром СУБД, останется неизменным.</span><span class="sxs-lookup"><span data-stu-id="54f73-251">The state of any ordinary databases in use by the database engine will remain unchanged.</span></span>

#### <a name="remarks"></a><span data-ttu-id="54f73-252">Комментарии</span><span class="sxs-lookup"><span data-stu-id="54f73-252">Remarks</span></span>

<span data-ttu-id="54f73-253">См. [жетопентемптабле](./jetopentemptable-function.md).</span><span class="sxs-lookup"><span data-stu-id="54f73-253">See [JetOpenTempTable](./jetopentemptable-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="54f73-254">Требования</span><span class="sxs-lookup"><span data-stu-id="54f73-254">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="54f73-255"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="54f73-255"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="54f73-256">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="54f73-256">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54f73-257"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="54f73-257"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="54f73-258">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="54f73-258">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54f73-259"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="54f73-259"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="54f73-260">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="54f73-260">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54f73-261"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="54f73-261"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="54f73-262">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="54f73-262">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54f73-263"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="54f73-263"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="54f73-264">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="54f73-264">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="54f73-265">См. также:</span><span class="sxs-lookup"><span data-stu-id="54f73-265">See Also</span></span>

[<span data-ttu-id="54f73-266">JET_COLUMNDEF</span><span class="sxs-lookup"><span data-stu-id="54f73-266">JET_COLUMNDEF</span></span>](./jet-columndef-structure.md)  
[<span data-ttu-id="54f73-267">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="54f73-267">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="54f73-268">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="54f73-268">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="54f73-269">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="54f73-269">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="54f73-270">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="54f73-270">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="54f73-271">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="54f73-271">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="54f73-272">JET_UNICODEINDEX</span><span class="sxs-lookup"><span data-stu-id="54f73-272">JET_UNICODEINDEX</span></span>](./jet-unicodeindex-structure.md)  
[<span data-ttu-id="54f73-273">жетклосетабле</span><span class="sxs-lookup"><span data-stu-id="54f73-273">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="54f73-274">жеткреатетаблеколумниндекс</span><span class="sxs-lookup"><span data-stu-id="54f73-274">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="54f73-275">жетдупкурсор</span><span class="sxs-lookup"><span data-stu-id="54f73-275">JetDupCursor</span></span>](./jetdupcursor-function.md)  
[<span data-ttu-id="54f73-276">жетмове</span><span class="sxs-lookup"><span data-stu-id="54f73-276">JetMove</span></span>](./jetmove-function.md)  
[<span data-ttu-id="54f73-277">жетроллбакк</span><span class="sxs-lookup"><span data-stu-id="54f73-277">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="54f73-278">жетсик</span><span class="sxs-lookup"><span data-stu-id="54f73-278">JetSeek</span></span>](./jetseek-function.md)  
[<span data-ttu-id="54f73-279">жетсетсистемпараметер</span><span class="sxs-lookup"><span data-stu-id="54f73-279">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="54f73-280">Системные параметры</span><span class="sxs-lookup"><span data-stu-id="54f73-280">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
