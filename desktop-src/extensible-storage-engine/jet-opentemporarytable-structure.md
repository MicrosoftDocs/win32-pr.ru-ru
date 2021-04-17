---
description: 'Дополнительные сведения: структура JET_OPENTEMPORARYTABLE'
title: Структура JET_OPENTEMPORARYTABLE
TOCTitle: JET_OPENTEMPORARYTABLE Structure
ms:assetid: 23f4fb0f-ca60-498b-9b8e-14de6188eb87
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269206(v=EXCHG.10)
ms:contentKeyID: 32765509
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 51ae9026098e82538940bde2ef182ba0a7a11c80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104345855"
---
# <a name="jet_opentemporarytable-structure"></a><span data-ttu-id="e0fc0-103">Структура JET_OPENTEMPORARYTABLE</span><span class="sxs-lookup"><span data-stu-id="e0fc0-103">JET_OPENTEMPORARYTABLE Structure</span></span>


<span data-ttu-id="e0fc0-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="e0fc0-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_opentemporarytable-structure"></a><span data-ttu-id="e0fc0-105">Структура JET_OPENTEMPORARYTABLE</span><span class="sxs-lookup"><span data-stu-id="e0fc0-105">JET_OPENTEMPORARYTABLE Structure</span></span>

<span data-ttu-id="e0fc0-106">Структура **JET_OPENTEMPORARYTABLE** содержит легко расширяемую коллекцию параметров для функции **JET_OPENTEMPORARYTABLE** .</span><span class="sxs-lookup"><span data-stu-id="e0fc0-106">The **JET_OPENTEMPORARYTABLE** structure contains an easily extensible collection of parameters for the **JET_OPENTEMPORARYTABLE** function.</span></span> <span data-ttu-id="e0fc0-107">Эта структура является временной таблицей, эквивалентной структуре [JET_TABLECREATE](./jet-tablecreate-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="e0fc0-107">This structure is the temporary table equivalent of the [JET_TABLECREATE](./jet-tablecreate-structure.md) structure.</span></span>

<span data-ttu-id="e0fc0-108">**Windows Vista:** Структура **JET_OPENTEMPORARYTABLE** появилась в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e0fc0-108">**Windows Vista:** The **JET_OPENTEMPORARYTABLE** structure is introduced in Windows Vista.</span></span>

```cpp
    typedef struct tagJET_OPENTEMPORARYTABLE {
      unsigned long cbStruct;
      const JET_COLUMNDEF* prgcolumndef;
      unsigned long ccolumn;
      JET_UNICODEINDEX* pidxunicode;
      JET_GRBIT grbit;
      JET_COLUMNID* prgcolumnid;
      unsigned long cbKeyMost;
      unsigned long cbVarSegMac;
      JET_TABLEID tableid;
    } JET_OPENTEMPORARYTABLE;
```

### <a name="members"></a><span data-ttu-id="e0fc0-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="e0fc0-109">Members</span></span>

<span data-ttu-id="e0fc0-110">**кбструкт**</span><span class="sxs-lookup"><span data-stu-id="e0fc0-110">**cbStruct**</span></span>

<span data-ttu-id="e0fc0-111">Размер этой структуры в байтах (для будущего расширения).</span><span class="sxs-lookup"><span data-stu-id="e0fc0-111">The size of this structure in bytes (for future expansion).</span></span> <span data-ttu-id="e0fc0-112">Он должен иметь значение sizeof (JET_TABLECREATE) в байтах.</span><span class="sxs-lookup"><span data-stu-id="e0fc0-112">It must be set to sizeof( JET_TABLECREATE ) in bytes.</span></span>

<span data-ttu-id="e0fc0-113">**пргколумндеф**</span><span class="sxs-lookup"><span data-stu-id="e0fc0-113">**prgcolumndef**</span></span>

<span data-ttu-id="e0fc0-114">Определения столбцов для столбцов, созданных во временной таблице.</span><span class="sxs-lookup"><span data-stu-id="e0fc0-114">Column definitions for the columns created in the temporary table.</span></span>

<span data-ttu-id="e0fc0-115">Для параметров определения столбца, используемых во временной таблице, имеются **важные** ограничения.</span><span class="sxs-lookup"><span data-stu-id="e0fc0-115">**Important** limitations exist for the column definition options that are used with a temporary table.</span></span> <span data-ttu-id="e0fc0-116">Дополнительные сведения см. в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="e0fc0-116">See the Remarks section for more information.</span></span>

<span data-ttu-id="e0fc0-117">В дополнение к обычным параметрам определения столбца можно также указать ноль или более следующих параметров, которые важны только в контексте временной таблицы.</span><span class="sxs-lookup"><span data-stu-id="e0fc0-117">In addition to the usual column definition options, zero or more of the following options can also be specified that are relevant only in the context of a temporary table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e0fc0-118">Значение</span><span class="sxs-lookup"><span data-stu-id="e0fc0-118">Value</span></span></p></th>
<th><p><span data-ttu-id="e0fc0-119">Значение</span><span class="sxs-lookup"><span data-stu-id="e0fc0-119">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e0fc0-120">JET_bitColumnTTDescending</span><span class="sxs-lookup"><span data-stu-id="e0fc0-120">JET_bitColumnTTDescending</span></span></p></td>
<td><p><span data-ttu-id="e0fc0-121">Порядок сортировки ключевого столбца для временной таблицы должен быть по убыванию, а не по возрастанию.</span><span class="sxs-lookup"><span data-stu-id="e0fc0-121">The sort order of the key column for the temporary table should be descending rather than ascending.</span></span> <span data-ttu-id="e0fc0-122">Если этот параметр указан без JET_bitColumnTTKey то этот параметр игнорируется.</span><span class="sxs-lookup"><span data-stu-id="e0fc0-122">If this option is specified without JET_bitColumnTTKey then this option is ignored.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0fc0-123">JET_bitColumnTTKey</span><span class="sxs-lookup"><span data-stu-id="e0fc0-123">JET_bitColumnTTKey</span></span></p></td>
<td><p><span data-ttu-id="e0fc0-124">Столбец будет ключевым столбцом для временной таблицы.</span><span class="sxs-lookup"><span data-stu-id="e0fc0-124">The column will be a key column for the temporary table.</span></span></p>
<p><span data-ttu-id="e0fc0-125">Порядок определений столбцов с этим параметром, указанным во входном массиве, определяет приоритет каждого ключевого столбца для временной таблицы.</span><span class="sxs-lookup"><span data-stu-id="e0fc0-125">The order of the column definitions with this option specified in the input array will determine the precedence of each key column for the temporary table.</span></span> <span data-ttu-id="e0fc0-126">Первое определение столбца в массиве, для которого задан этот параметр, будет наиболее значимым ключевым столбцом и т. д.</span><span class="sxs-lookup"><span data-stu-id="e0fc0-126">The first column definition in the array that has this option set will be the most significant key column and so on.</span></span> <span data-ttu-id="e0fc0-127">Если запрошено больше ключевых столбцов, чем может поддерживать ядро СУБД, этот параметр игнорируется для неподдерживаемых ключевых столбцов.</span><span class="sxs-lookup"><span data-stu-id="e0fc0-127">If more key columns are requested than can be supported by the database engine then this option is ignored for the unsupportable key columns.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e0fc0-128">**кколумн**</span><span class="sxs-lookup"><span data-stu-id="e0fc0-128">**ccolumn**</span></span>

<span data-ttu-id="e0fc0-129">См. *пргколумндеф*.</span><span class="sxs-lookup"><span data-stu-id="e0fc0-129">See *prgcolumndef*.</span></span>

<span data-ttu-id="e0fc0-130">**пидксуникоде**</span><span class="sxs-lookup"><span data-stu-id="e0fc0-130">**pidxunicode**</span></span>

<span data-ttu-id="e0fc0-131">КОД локали и флаги нормализации, используемые для сравнения данных любого ключевого столбца Юникода во временной таблице.</span><span class="sxs-lookup"><span data-stu-id="e0fc0-131">The locale ID and normalization flags to use to compare any Unicode key column data in the temporary table.</span></span>

<span data-ttu-id="e0fc0-132">Если этот параметр отсутствует, а параметр *LCID* отсутствует, то для сравнения всех ключевых столбцов Юникода во временной таблице будет использоваться код по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e0fc0-132">When this parameter is not present and when the *lcid* parameter is not present, then the default LCID will be used to compare any Unicode key columns in the temporary table.</span></span> <span data-ttu-id="e0fc0-133">По умолчанию используется языковой стандарт «Английский (США)».</span><span class="sxs-lookup"><span data-stu-id="e0fc0-133">The default LCID is the U.S. English locale.</span></span>

<span data-ttu-id="e0fc0-134">Если этот параметр отсутствует, то для сравнения данных любого ключевого столбца Юникода во временной таблице будут использоваться флаги нормализации по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e0fc0-134">When this parameter is not present, then the default normalization flags will be used to compare any Unicode key column data in the temp table.</span></span> <span data-ttu-id="e0fc0-135">Флаги нормализации по умолчанию: NORM_IGNORECASE, NORM_IGNOREKANATYPE и NORM_IGNOREWIDTH.</span><span class="sxs-lookup"><span data-stu-id="e0fc0-135">The default normalization flags are: NORM_IGNORECASE, NORM_IGNOREKANATYPE, and NORM_IGNOREWIDTH.</span></span>

<span data-ttu-id="e0fc0-136">**грбит**</span><span class="sxs-lookup"><span data-stu-id="e0fc0-136">**grbit**</span></span>

<span data-ttu-id="e0fc0-137">Группа битов, задающая ноль или более следующих параметров.</span><span class="sxs-lookup"><span data-stu-id="e0fc0-137">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e0fc0-138">Значение</span><span class="sxs-lookup"><span data-stu-id="e0fc0-138">Value</span></span></p></th>
<th><p><span data-ttu-id="e0fc0-139">Значение</span><span class="sxs-lookup"><span data-stu-id="e0fc0-139">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e0fc0-140">JET_bitTTIndexed</span><span class="sxs-lookup"><span data-stu-id="e0fc0-140">JET_bitTTIndexed</span></span></p></td>
<td><p><span data-ttu-id="e0fc0-141">Этот параметр требует, чтобы временная таблица была достаточно гибкой, чтобы позволить использовать <a href="gg294103(v=exchg.10).md">жетсик</a> для поиска записей по ключу индекса.</span><span class="sxs-lookup"><span data-stu-id="e0fc0-141">This option requests that the temporary table be flexible enough to permit the use of <a href="gg294103(v=exchg.10).md">JetSeek</a> to look up records by index key.</span></span></p>
<p><span data-ttu-id="e0fc0-142">Если эта функция не требуется, то лучше не запрашивать ее.</span><span class="sxs-lookup"><span data-stu-id="e0fc0-142">If this functionality it not required then it is best to not request it.</span></span> <span data-ttu-id="e0fc0-143">Если эта функция не запрошена, то диспетчер временных таблиц может выбрать стратегию для управления временной таблицей, что приведет к повышению производительности.</span><span class="sxs-lookup"><span data-stu-id="e0fc0-143">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0fc0-144">JET_bitTTUnique</span><span class="sxs-lookup"><span data-stu-id="e0fc0-144">JET_bitTTUnique</span></span></p></td>
<td><p><span data-ttu-id="e0fc0-145">Запросы, в которых записи с повторяющимися ключами индекса удаляются из окончательного набора записей во временной таблице.</span><span class="sxs-lookup"><span data-stu-id="e0fc0-145">Requests that records with duplicate index keys be removed from the final set of records in the temporary table.</span></span></p>
<p><span data-ttu-id="e0fc0-146">До Windows Server 2003 в ядре СУБД всегда предполагается, что этот параметр действует из-за того факта, что все кластеризованные индексы также должны быть первичным ключом и, таким же, должны быть уникальными.</span><span class="sxs-lookup"><span data-stu-id="e0fc0-146">Prior to Windows Server 2003, the database engine always assumed this option to be in effect due to the fact that all clustered indexes must also be a primary key and thus must be unique.</span></span> <span data-ttu-id="e0fc0-147">Начиная с Windows Server 2003, теперь можно создать временную таблицу, которая не удаляет дубликаты, если также указан параметр JET_bitTTForwardOnly.</span><span class="sxs-lookup"><span data-stu-id="e0fc0-147">As of Windows Server 2003, it is now possible to create a temporary table that does not remove duplicates when the JET_bitTTForwardOnly option is also specified.</span></span></p>
<p><span data-ttu-id="e0fc0-148">Невозможно выяснить, какие дубликаты будут выполнены, и какие дубликаты будут отменены в целом.</span><span class="sxs-lookup"><span data-stu-id="e0fc0-148">It is not possible to know which duplicate will succeed and which duplicates will be discarded, in general.</span></span> <span data-ttu-id="e0fc0-149">Однако при запросе параметра JET_bitTTErrorOnDuplicateInsertion первая запись с заданным ключом индекса для вставки во временную таблицу всегда будет выполнена.</span><span class="sxs-lookup"><span data-stu-id="e0fc0-149">However, when the JET_bitTTErrorOnDuplicateInsertion option is requested then the first record with a given index key to be inserted into the temporary table will always succeed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0fc0-150">JET_bitTTUpdatable</span><span class="sxs-lookup"><span data-stu-id="e0fc0-150">JET_bitTTUpdatable</span></span></p></td>
<td><p><span data-ttu-id="e0fc0-151">Требует, чтобы временная таблица была достаточно гибкой, чтобы разрешить впоследствии изменять ранее вставленные записи.</span><span class="sxs-lookup"><span data-stu-id="e0fc0-151">Requests that the temporary table be flexible enough to allow records that have previously been inserted to be subsequently changed.</span></span> <span data-ttu-id="e0fc0-152">Если эта функция не требуется, то лучше не запрашивать ее.</span><span class="sxs-lookup"><span data-stu-id="e0fc0-152">If this functionality it not required then it is best to not request it.</span></span></p>
<p><span data-ttu-id="e0fc0-153">Если эта функция не запрошена, то диспетчер временных таблиц может выбрать стратегию для управления временной таблицей, что приведет к повышению производительности.</span><span class="sxs-lookup"><span data-stu-id="e0fc0-153">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0fc0-154">JET_bitTTScrollable</span><span class="sxs-lookup"><span data-stu-id="e0fc0-154">JET_bitTTScrollable</span></span></p></td>
<td><p><span data-ttu-id="e0fc0-155">Требует, чтобы временная таблица была достаточно гибкой, чтобы можно было просматривать записи в произвольном порядке и в направлении с помощью <a href="gg294117(v=exchg.10).md">жетмове</a>.</span><span class="sxs-lookup"><span data-stu-id="e0fc0-155">Requests that the temporary table be flexible enough to allow records to be scanned in arbitrary order and direction using <a href="gg294117(v=exchg.10).md">JetMove</a>.</span></span></p>
<p><span data-ttu-id="e0fc0-156">Если эта функция не является обязательной, лучше не запрашивать ее.</span><span class="sxs-lookup"><span data-stu-id="e0fc0-156">If this functionality is not required then it is best to not request it.</span></span> <span data-ttu-id="e0fc0-157">Если эта функция не запрошена, то диспетчер временных таблиц может выбрать стратегию для управления временной таблицей, что приведет к повышению производительности.</span><span class="sxs-lookup"><span data-stu-id="e0fc0-157">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0fc0-158">JET_bitTTSortNullsHigh</span><span class="sxs-lookup"><span data-stu-id="e0fc0-158">JET_bitTTSortNullsHigh</span></span></p></td>
<td><p><span data-ttu-id="e0fc0-159">Запрашивает, что значения ключевого столбца <strong>null</strong> сортируются ближе к концу индекса, чем значения ключевого столбца, отличного от NULL.</span><span class="sxs-lookup"><span data-stu-id="e0fc0-159">Requests that <strong>NULL</strong> key column values sort closer to the end of the index than non-NULL key column values.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0fc0-160">JET_bitTTForceMaterialization</span><span class="sxs-lookup"><span data-stu-id="e0fc0-160">JET_bitTTForceMaterialization</span></span></p></td>
<td><p><span data-ttu-id="e0fc0-161">Заставляет диспетчер временных таблиц отменять поиск лучшей стратегии, используемой для управления временной таблицей, что приведет к повышенной производительности.</span><span class="sxs-lookup"><span data-stu-id="e0fc0-161">Forces the temporary table manager to abandon the search for the best strategy to use managing the temporary table that will result in enhanced performance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0fc0-162">JET_bitTTErrorOnDuplicateInsertion</span><span class="sxs-lookup"><span data-stu-id="e0fc0-162">JET_bitTTErrorOnDuplicateInsertion</span></span></p></td>
<td><p><span data-ttu-id="e0fc0-163">Любая попытка вставить запись с тем же ключом индекса, что и ранее вставленная запись, сразу же завершится с JET_errKeyDuplicate.</span><span class="sxs-lookup"><span data-stu-id="e0fc0-163">Any attempt to insert a record with the same index key as a previously inserted record will immediately fail with JET_errKeyDuplicate.</span></span> <span data-ttu-id="e0fc0-164">Если этот параметр не запрашивается, то дубликат обнаруживается немедленно, завершается ошибкой или автоматически удаляется позже, в зависимости от стратегии, выбранной ядром СУБД для реализации временной таблицы в зависимости от запрошенной функциональности.</span><span class="sxs-lookup"><span data-stu-id="e0fc0-164">If this option is not requested then a duplicate is detected immediately and fails, or is silently removed later, depending on the strategy chosen by the database engine to implement the temporary table, based on the requested functionality.</span></span></p>
<p><span data-ttu-id="e0fc0-165">Если эта функция не требуется, то лучше не запрашивать ее.</span><span class="sxs-lookup"><span data-stu-id="e0fc0-165">If this functionality it not required then it is best to not request it.</span></span> <span data-ttu-id="e0fc0-166">Если эта функция не запрошена, то диспетчер временных таблиц может выбрать стратегию для управления временной таблицей, что приведет к повышению производительности.</span><span class="sxs-lookup"><span data-stu-id="e0fc0-166">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0fc0-167">JET_bitTTForwardOnly</span><span class="sxs-lookup"><span data-stu-id="e0fc0-167">JET_bitTTForwardOnly</span></span></p></td>
<td><p><span data-ttu-id="e0fc0-168">Временная таблица создается только в том случае, если диспетчер временных таблиц может использовать реализацию, оптимизированную для промежуточных результатов запроса.</span><span class="sxs-lookup"><span data-stu-id="e0fc0-168">The temporary table is only created if the temporary table manager can use the implementation that is optimized for intermediate query results.</span></span> <span data-ttu-id="e0fc0-169">Если любая характеристика временной таблицы не позволит использовать эту оптимизацию, операция завершится с JET_errCannotMaterializeForwardOnlySort.</span><span class="sxs-lookup"><span data-stu-id="e0fc0-169">If any characteristic of the temporary table would prevent the use of this optimization then the operation will fail with JET_errCannotMaterializeForwardOnlySort.</span></span></p>
<p><span data-ttu-id="e0fc0-170">Побочный результат этого параметра — Разрешить временной таблице содержать записи с повторяющимися ключами индекса.</span><span class="sxs-lookup"><span data-stu-id="e0fc0-170">A side effect of this option is to allow the temporary table to contain records with duplicate index keys.</span></span> <span data-ttu-id="e0fc0-171">Дополнительные сведения см. в разделе JET_bitTTUnique.</span><span class="sxs-lookup"><span data-stu-id="e0fc0-171">See JET_bitTTUnique for more information.</span></span></p>
<p><span data-ttu-id="e0fc0-172"><strong>Windows Server 2003:  </strong> Этот параметр доступен только в выпусках Windows Server 2003 и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="e0fc0-172"><strong>Windows Server 2003:  </strong>This option is only available on Windows Server 2003 and later releases.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e0fc0-173">**пргколумнид**</span><span class="sxs-lookup"><span data-stu-id="e0fc0-173">**prgcolumnid**</span></span>

<span data-ttu-id="e0fc0-174">Выходной буфер, который получает массив идентификаторов столбцов, созданных во время создания временной таблицы.</span><span class="sxs-lookup"><span data-stu-id="e0fc0-174">The output buffer that receives the array of column IDs generated during the creation of the temporary table.</span></span>

<span data-ttu-id="e0fc0-175">Идентификаторы столбцов в этом массиве будут точно соответствовать входному массиву определений столбцов.</span><span class="sxs-lookup"><span data-stu-id="e0fc0-175">The column IDs in this array will exactly correspond to the input array of column definitions.</span></span> <span data-ttu-id="e0fc0-176">В результате размер этого буфера должен соответствовать размеру входного массива.</span><span class="sxs-lookup"><span data-stu-id="e0fc0-176">As a result, the size of this buffer must correspond to the size of the input array.</span></span>

<span data-ttu-id="e0fc0-177">**кбкэймост**</span><span class="sxs-lookup"><span data-stu-id="e0fc0-177">**cbKeyMost**</span></span>

<span data-ttu-id="e0fc0-178">Максимальный размер ключа, представляющего заданную строку.</span><span class="sxs-lookup"><span data-stu-id="e0fc0-178">The maximum size for a key representing a given row.</span></span>

<span data-ttu-id="e0fc0-179">Для управления способом усечения ключей можно задать максимальный размер ключа.</span><span class="sxs-lookup"><span data-stu-id="e0fc0-179">The maximum key size may be set to control how keys are truncated.</span></span> <span data-ttu-id="e0fc0-180">Усечение ключа важно, так как это может повлиять на то, что строки считаются разными.</span><span class="sxs-lookup"><span data-stu-id="e0fc0-180">Key truncation is important because it can affect when rows are considered to be distinct.</span></span>

<span data-ttu-id="e0fc0-181">Если этот параметр имеет значение 0 или JET_cbKeyMostMin (255), то максимальный размер ключа и его семантика остаются идентичными максимальному размеру ключа, поддерживаемому Windows Server 2003 и предыдущими выпусками.</span><span class="sxs-lookup"><span data-stu-id="e0fc0-181">If this parameter is set to 0 or JET_cbKeyMostMin (255) then the maximum key size and its semantics will remain identical to the maximum key size supported by Windows Server 2003 and previous releases.</span></span> <span data-ttu-id="e0fc0-182">Для этого параметра также можно задать большее значение в качестве функции размера страницы базы данных для экземпляра (JET_paramDatabasePageSize).</span><span class="sxs-lookup"><span data-stu-id="e0fc0-182">This parameter may also be set to a larger value as a function of the database page size for the instance (JET_paramDatabasePageSize).</span></span> <span data-ttu-id="e0fc0-183">Дополнительные сведения см. в разделе JET_paramKeyMost.</span><span class="sxs-lookup"><span data-stu-id="e0fc0-183">See JET_paramKeyMost for more information.</span></span>

<span data-ttu-id="e0fc0-184">**кбварсегмак**</span><span class="sxs-lookup"><span data-stu-id="e0fc0-184">**cbVarSegMac**</span></span>

<span data-ttu-id="e0fc0-185">Максимальный объем данных, который будет использоваться из любого столбца переменной длины для создания ключа для данной строки.</span><span class="sxs-lookup"><span data-stu-id="e0fc0-185">The maximum amount of data that will be used from any variable length column to construct a key for a given row.</span></span>

<span data-ttu-id="e0fc0-186">Этот параметр может использоваться для управления объемом ключевого пространства, используемого любым ключевым столбцом.</span><span class="sxs-lookup"><span data-stu-id="e0fc0-186">This parameter may be used to control the amount of key space consumed by any given key column.</span></span> <span data-ttu-id="e0fc0-187">Это ограничение указано в байтах.</span><span class="sxs-lookup"><span data-stu-id="e0fc0-187">This limit is in bytes.</span></span> <span data-ttu-id="e0fc0-188">Если этот параметр равен нулю или совпадает с параметром *кбкэймост* , ограничение не действует.</span><span class="sxs-lookup"><span data-stu-id="e0fc0-188">If this parameter is zero or is the same as the *cbKeyMost* parameter then no limit is in effect.</span></span>

<span data-ttu-id="e0fc0-189">**TableID**</span><span class="sxs-lookup"><span data-stu-id="e0fc0-189">**tableid**</span></span>

<span data-ttu-id="e0fc0-190">Табличный маркер для временной таблицы, созданный в результате успешного вызова [жетопентемпораритабле](./jetopentemporarytable-function.md).</span><span class="sxs-lookup"><span data-stu-id="e0fc0-190">The table handle for the temporary table created as a result of a successful call to [JetOpenTemporaryTable](./jetopentemporarytable-function.md).</span></span>

### <a name="requirements"></a><span data-ttu-id="e0fc0-191">Требования</span><span class="sxs-lookup"><span data-stu-id="e0fc0-191">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e0fc0-192"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="e0fc0-192"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="e0fc0-193">Требуется Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e0fc0-193">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0fc0-194"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="e0fc0-194"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="e0fc0-195">Требуется Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="e0fc0-195">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0fc0-196"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="e0fc0-196"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="e0fc0-197">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="e0fc0-197">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="e0fc0-198">См. также:</span><span class="sxs-lookup"><span data-stu-id="e0fc0-198">See Also</span></span>

[<span data-ttu-id="e0fc0-199">JET_TABLECREATE</span><span class="sxs-lookup"><span data-stu-id="e0fc0-199">JET_TABLECREATE</span></span>](./jet-tablecreate-structure.md)  
[<span data-ttu-id="e0fc0-200">JET_COLUMNDEF</span><span class="sxs-lookup"><span data-stu-id="e0fc0-200">JET_COLUMNDEF</span></span>](./jet-columndef-structure.md)  
[<span data-ttu-id="e0fc0-201">JET_UNICODEINDEX</span><span class="sxs-lookup"><span data-stu-id="e0fc0-201">JET_UNICODEINDEX</span></span>](./jet-unicodeindex-structure.md)  
[<span data-ttu-id="e0fc0-202">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="e0fc0-202">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="e0fc0-203">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="e0fc0-203">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="e0fc0-204">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="e0fc0-204">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="e0fc0-205">жетопентемпораритабле</span><span class="sxs-lookup"><span data-stu-id="e0fc0-205">JetOpenTemporaryTable</span></span>](./jetopentemporarytable-function.md)  
[<span data-ttu-id="e0fc0-206">Параметры расширяемой системы подсистемы хранилища</span><span class="sxs-lookup"><span data-stu-id="e0fc0-206">Extensible Storage Engine System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
