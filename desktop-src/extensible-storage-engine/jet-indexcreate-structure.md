---
description: 'Дополнительные сведения: структура JET_INDEXCREATE'
title: Структура JET_INDEXCREATE
TOCTitle: JET_INDEXCREATE Structure
ms:assetid: 0c55f25c-d42a-49ba-a1fe-549850fdc9a6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269186(v=EXCHG.10)
ms:contentKeyID: 32765489
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4c465d81dce628497b1b9210fb08b37a3003e2e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815608"
---
# <a name="jet_indexcreate-structure"></a><span data-ttu-id="16113-103">Структура JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="16113-103">JET_INDEXCREATE Structure</span></span>


<span data-ttu-id="16113-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="16113-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="16113-105">Структура **JET_INDEXCREATE** содержит сведения, необходимые для создания индекса данных в базе данных подсистемы расширенного хранилища (ESE).</span><span class="sxs-lookup"><span data-stu-id="16113-105">The **JET_INDEXCREATE** structure contains the information needed to create an index over data in an Extensible Storage Engine (ESE) database.</span></span> <span data-ttu-id="16113-106">Структура используется такими функциями, как [JetCreateIndex2](./jetcreateindex2-function.md), и в таких структурах, как [JET_TABLECREATE](./jet-tablecreate-structure.md) и [JET_TABLECREATE2](./jet-tablecreate2-structure.md).</span><span class="sxs-lookup"><span data-stu-id="16113-106">The structure is used by functions such as [JetCreateIndex2](./jetcreateindex2-function.md), and in structures such as [JET_TABLECREATE](./jet-tablecreate-structure.md) and [JET_TABLECREATE2](./jet-tablecreate2-structure.md).</span></span>

``` c++
typedef struct tagJET_INDEXCREATE {
  unsigned long cbStruct;
  tchar* szIndexName;
  tchar* szKey;
  unsigned long cbKey;
  JET_GRBIT grbit;
  unsigned long ulDensity;
  union {
    unsigned long lcid;
    JET_UNICODEINDEX* pidxunicode;
  };
  union {
    unsigned long cbVarSegMac;
    JET_TUPLELIMITS* ptuplelimits;
  };
  JET_CONDITIONALCOLUMN* rgconditionalcolumn;
  unsigned long cConditionalColumn;
  JET_ERR err;
  unsigned long cbKeyMost;
} JET_INDEXCREATE;
```

### <a name="members"></a><span data-ttu-id="16113-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="16113-107">Members</span></span>

<span data-ttu-id="16113-108">**кбструкт**</span><span class="sxs-lookup"><span data-stu-id="16113-108">**cbStruct**</span></span>

<span data-ttu-id="16113-109">Размер данной структуры (в байтах).</span><span class="sxs-lookup"><span data-stu-id="16113-109">The size, in bytes, of this structure.</span></span> <span data-ttu-id="16113-110">Присвойте этому элементу значение sizeof (JET_INDEXCREATE).</span><span class="sxs-lookup"><span data-stu-id="16113-110">Set this member to sizeof( JET_INDEXCREATE ).</span></span>

<span data-ttu-id="16113-111">**сзиндекснаме**</span><span class="sxs-lookup"><span data-stu-id="16113-111">**szIndexName**</span></span>

<span data-ttu-id="16113-112">Имя создаваемого индекса.</span><span class="sxs-lookup"><span data-stu-id="16113-112">The name of the index to create.</span></span>

<span data-ttu-id="16113-113">Имя индекса должно соответствовать следующим условиям.</span><span class="sxs-lookup"><span data-stu-id="16113-113">The name of the index must meet the following conditions:</span></span>

  - <span data-ttu-id="16113-114">Оно должно быть меньше JET_cbNameMost, не включая завершающее значение null.</span><span class="sxs-lookup"><span data-stu-id="16113-114">It must be less than JET_cbNameMost, not including the terminating null.</span></span>

  - <span data-ttu-id="16113-115">Оно должно состоять из следующих символов: от 0 (нуля) до 9, от A до Z, от a до z и всех остальных знаков препинания, кроме " \! ".</span><span class="sxs-lookup"><span data-stu-id="16113-115">It must consist of the following characters: 0 (zero) through 9, A through Z, a through z, and all other punctuation except for "\!"</span></span> <span data-ttu-id="16113-116">(восклицательный знак), "," (запятая), " \[ " (открывающая скобка) и " \] " (закрывающая скобка), т. е. символы ASCII 0x20, 0x22 до 0x2D, 0x2F через 0x5A, 0x5c, 0x5d до 0x7F.</span><span class="sxs-lookup"><span data-stu-id="16113-116">(exclamation point), "," (comma), "\[" (opening bracket), and "\]" (closing bracket) — that is, ASCII characters 0x20, 0x22 through 0x2d, 0x2f through 0x5a, 0x5c, 0x5d through 0x7f.</span></span>

  - <span data-ttu-id="16113-117">Оно не должно начинаться с пробела.</span><span class="sxs-lookup"><span data-stu-id="16113-117">It must not begin with a space.</span></span>

  - <span data-ttu-id="16113-118">Он должен содержать по крайней мере один непробелный символ.</span><span class="sxs-lookup"><span data-stu-id="16113-118">It must consist of at least one nonspace character.</span></span>

<span data-ttu-id="16113-119">**сзкэй**</span><span class="sxs-lookup"><span data-stu-id="16113-119">**szKey**</span></span>

<span data-ttu-id="16113-120">Указатель на строку токена с разделителями null, завершающуюся символом двойного значения NULL.</span><span class="sxs-lookup"><span data-stu-id="16113-120">A pointer to a double-null-terminated string of null-delimited tokens.</span></span>

<span data-ttu-id="16113-121">Каждый токен имеет форму " \<direction-specifier\> \<column-name\> ", где Direction-спецификация имеет значение "+" или "-".</span><span class="sxs-lookup"><span data-stu-id="16113-121">Each token is of the form "\<direction-specifier\>\<column-name\>", where direction-specification is either "+" or "-".</span></span> <span data-ttu-id="16113-122">Например, **сзкэй** "+ ABC \\ 0-DEF \\ 0 + GHI \\ 0" будет индексировать три столбца "ABC" (в порядке возрастания), "def" (в убывающем порядке) и "GHI" (в возрастающем порядке).</span><span class="sxs-lookup"><span data-stu-id="16113-122">For example, a **szKey** of "+abc\\0-def\\0+ghi\\0" will index over the three columns "abc" (in ascending order), "def" (in descending order), and "ghi" (in ascending order).</span></span> <span data-ttu-id="16113-123">В языке C строковые литералы имеют подразумеваемый знак завершения **null** ; Поэтому приведенная выше строка будет заканчиваться двойным значением NULL.</span><span class="sxs-lookup"><span data-stu-id="16113-123">In the C language, string literals have an implied **NULL** terminator; therefore, the above string will be terminated by a double-NULL.</span></span>

<span data-ttu-id="16113-124">Число столбцов, указанное в **сзкэй** , не может превышать значение **JET_ccolKeyMost** (константа, зависящее от версии).</span><span class="sxs-lookup"><span data-stu-id="16113-124">The number of columns specified in **szKey** may not exceed the value of **JET_ccolKeyMost** (a version-dependent constant).</span></span>

<span data-ttu-id="16113-125">По крайней мере один столбец должен иметь имя в **сзкэй**.</span><span class="sxs-lookup"><span data-stu-id="16113-125">At least one column must be named in **szKey**.</span></span>

<span data-ttu-id="16113-126">Устаревшее поведение. после символа-конца с двойным НУЛЕМ можно указать идентификатор языка (слово, которое передается в МАКЕЛЦИД (LangID, SORT_DEFAULT)) в качестве способа указания кода языка для индекса.</span><span class="sxs-lookup"><span data-stu-id="16113-126">Obsolete behavior: After the double-NULL terminator, it is possible to specify a language ID (a WORD which gets passed into MAKELCID( langid, SORT_DEFAULT ) ) as a way to specify the LCID for the index.</span></span> <span data-ttu-id="16113-127">Недопустимо указывать идентификатор языка в **сзкэй** и LCID в [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) (путем установки JET_bitIndexUnicode в *грбит*).</span><span class="sxs-lookup"><span data-stu-id="16113-127">It is illegal to specify both a language ID in **szKey** and an LCID in [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) (by setting JET_bitIndexUnicode in *grbit*).</span></span>

<span data-ttu-id="16113-128">Устарело: после идентификатора языка можно передать **кбварсегмак** как ushort.</span><span class="sxs-lookup"><span data-stu-id="16113-128">Deprecated: After the language ID, it is possible to pass **cbVarSegMac** as a USHORT.</span></span> <span data-ttu-id="16113-129">Поведение не определено, если USHORT задан как в **сзкэй** , так и при задании **кбварсегмак** в структуре.</span><span class="sxs-lookup"><span data-stu-id="16113-129">The behavior is undefined if the USHORT is set both in **szKey** and if **cbVarSegMac** is set in the structure.</span></span>

<span data-ttu-id="16113-130">**cbKey**</span><span class="sxs-lookup"><span data-stu-id="16113-130">**cbKey**</span></span>

<span data-ttu-id="16113-131">Длина **сзкэй** в байтах, включая два завершающих значения NULL.</span><span class="sxs-lookup"><span data-stu-id="16113-131">The length, in bytes, of **szKey** including the two terminating nulls.</span></span>

<span data-ttu-id="16113-132">**грбит**</span><span class="sxs-lookup"><span data-stu-id="16113-132">**grbit**</span></span>

<span data-ttu-id="16113-133">Группа битов, которая содержит ноль или более значений, перечисленных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="16113-133">A group of bits that includes zero or more of the values listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="16113-134">Значение</span><span class="sxs-lookup"><span data-stu-id="16113-134">Value</span></span></p></th>
<th><p><span data-ttu-id="16113-135">Значение</span><span class="sxs-lookup"><span data-stu-id="16113-135">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="16113-136">JET_bitIndexUnique</span><span class="sxs-lookup"><span data-stu-id="16113-136">JET_bitIndexUnique</span></span></p></td>
<td><p><span data-ttu-id="16113-137">Дублирующиеся записи индекса (ключи) не допускаются.</span><span class="sxs-lookup"><span data-stu-id="16113-137">Duplicate index entries (keys) are not allowed.</span></span> <span data-ttu-id="16113-138">Это применяется при вызове <a href="gg269288(v=exchg.10).md">жетупдате</a> , а не при вызове <a href="gg294137(v=exchg.10).md">жетсетколумн</a> .</span><span class="sxs-lookup"><span data-stu-id="16113-138">This is enforced when <a href="gg269288(v=exchg.10).md">JetUpdate</a> is called, not when <a href="gg294137(v=exchg.10).md">JetSetColumn</a> is called.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="16113-139">JET_bitIndexPrimary</span><span class="sxs-lookup"><span data-stu-id="16113-139">JET_bitIndexPrimary</span></span></p></td>
<td><p><span data-ttu-id="16113-140">Индекс является первичным (кластеризованным) индексом.</span><span class="sxs-lookup"><span data-stu-id="16113-140">The index is a primary (clustered) index.</span></span> <span data-ttu-id="16113-141">Каждая таблица должна иметь ровно один первичный индекс.</span><span class="sxs-lookup"><span data-stu-id="16113-141">Every table must have exactly one primary index.</span></span> <span data-ttu-id="16113-142">Если первичный индекс явно не определен в таблице, ядро СУБД создаст собственный первичный индекс.</span><span class="sxs-lookup"><span data-stu-id="16113-142">If no primary index is explicitly defined over a table, the database engine will create its own primary index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="16113-143">JET_bitIndexDisallowNull</span><span class="sxs-lookup"><span data-stu-id="16113-143">JET_bitIndexDisallowNull</span></span></p></td>
<td><p><span data-ttu-id="16113-144">Ни один из столбцов, по которым создается индекс, не может содержать значение <strong>null</strong> .</span><span class="sxs-lookup"><span data-stu-id="16113-144">None of the columns over which the index is created can contain a <strong>NULL</strong> value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="16113-145">JET_bitIndexIgnoreNull</span><span class="sxs-lookup"><span data-stu-id="16113-145">JET_bitIndexIgnoreNull</span></span></p></td>
<td><p><span data-ttu-id="16113-146">Не добавляйте элемент индекса для строки, если все индексируемые столбцы имеют <strong>значение NULL</strong>.</span><span class="sxs-lookup"><span data-stu-id="16113-146">Do not add an index entry for a row if all of the columns being indexed are <strong>NULL</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="16113-147">JET_bitIndexIgnoreAnyNull</span><span class="sxs-lookup"><span data-stu-id="16113-147">JET_bitIndexIgnoreAnyNull</span></span></p></td>
<td><p><span data-ttu-id="16113-148">Не добавляйте элемент индекса для строки, если какие-либо индексируемые столбцы имеют <strong>значение NULL</strong>.</span><span class="sxs-lookup"><span data-stu-id="16113-148">Do not add an index entry for a row if any of the columns being indexed are <strong>NULL</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="16113-149">JET_bitIndexIgnoreFirstNull</span><span class="sxs-lookup"><span data-stu-id="16113-149">JET_bitIndexIgnoreFirstNull</span></span></p></td>
<td><p><span data-ttu-id="16113-150">Не добавляйте элемент индекса для строки, если первый индексируемый столбец имеет <strong>значение NULL</strong>.</span><span class="sxs-lookup"><span data-stu-id="16113-150">Do not add an index entry for a row if the first column being indexed is <strong>NULL</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="16113-151">JET_bitIndexLazyFlush</span><span class="sxs-lookup"><span data-stu-id="16113-151">JET_bitIndexLazyFlush</span></span></p></td>
<td><p><span data-ttu-id="16113-152">Операции с индексами будут протоколироваться неактивно.</span><span class="sxs-lookup"><span data-stu-id="16113-152">Index operations will be logged lazily.</span></span></p>
<p><span data-ttu-id="16113-153">JET_bitIndexLazyFlush не влияет на отложенность обновлений данных.</span><span class="sxs-lookup"><span data-stu-id="16113-153">JET_bitIndexLazyFlush does not affect the laziness of data updates.</span></span> <span data-ttu-id="16113-154">Если операция индексирования прервана завершением процесса, то при мягком восстановлении все равно удастся получить целостное состояние базы данных, но индекс может отсутствовать.</span><span class="sxs-lookup"><span data-stu-id="16113-154">If the indexing operation is interrupted by process termination, Soft Recovery will still be able to able to get the database to a consistent state, but the index might not be present.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="16113-155">JET_bitIndexEmpty</span><span class="sxs-lookup"><span data-stu-id="16113-155">JET_bitIndexEmpty</span></span></p></td>
<td><p><span data-ttu-id="16113-156">Не пытайтесь построить индекс, так как все записи будут иметь <strong>значение NULL</strong>.</span><span class="sxs-lookup"><span data-stu-id="16113-156">Do not attempt to build the index, because all entries would evaluate to <strong>NULL</strong>.</span></span> <span data-ttu-id="16113-157"><strong>грбит</strong> также должен указывать JET_bitIgnoreAnyNull при передаче JET_bitIndexEmpty.</span><span class="sxs-lookup"><span data-stu-id="16113-157"><strong>grbit</strong> must also specify JET_bitIgnoreAnyNull when JET_bitIndexEmpty is passed.</span></span> <span data-ttu-id="16113-158">Это улучшение производительности.</span><span class="sxs-lookup"><span data-stu-id="16113-158">This is a performance enhancement.</span></span> <span data-ttu-id="16113-159">Например, если в таблицу добавляется новый столбец, то для него создается индекс, а все записи в таблице просматриваются, несмотря на то что они не добавляются в индекс.</span><span class="sxs-lookup"><span data-stu-id="16113-159">For example, if a new column is added to a table, an index is created over this newly added column, and all the records in the table are scanned even though they are not added to the index.</span></span> <span data-ttu-id="16113-160">При указании JET_bitIndexEmpty пропускается сканирование таблицы, что может занять длительное время.</span><span class="sxs-lookup"><span data-stu-id="16113-160">Specifying JET_bitIndexEmpty skips the scanning of the table, which could potentially take a long time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="16113-161">JET_bitIndexUnversioned</span><span class="sxs-lookup"><span data-stu-id="16113-161">JET_bitIndexUnversioned</span></span></p></td>
<td><p><span data-ttu-id="16113-162">Приводит к тому, что создание индекса станет видимым для других транзакций.</span><span class="sxs-lookup"><span data-stu-id="16113-162">Causes index creation to be visible to other transactions.</span></span> <span data-ttu-id="16113-163">Как правило, сеанс в транзакции не сможет увидеть операцию создания индекса в другом сеансе.</span><span class="sxs-lookup"><span data-stu-id="16113-163">Typically a session in a transaction will not be able to see an index creation operation in another session.</span></span> <span data-ttu-id="16113-164">Этот флаг может быть полезен, если другая транзакция, скорее всего, создаст тот же индекс.</span><span class="sxs-lookup"><span data-stu-id="16113-164">This flag can be useful if another transaction is likely to create the same index.</span></span> <span data-ttu-id="16113-165">Второй индекс-Create завершится с ошибкой, а не может вызвать множество ненужных операций с базой данных.</span><span class="sxs-lookup"><span data-stu-id="16113-165">The second index-create will fail instead of potentially causing many unnecessary database operations.</span></span> <span data-ttu-id="16113-166">Вторая транзакция может не иметь возможности немедленно использовать индекс.</span><span class="sxs-lookup"><span data-stu-id="16113-166">The second transaction might not be able to use the index immediately.</span></span> <span data-ttu-id="16113-167">Операция создания индекса должна быть завершена, прежде чем ее можно будет использовать.</span><span class="sxs-lookup"><span data-stu-id="16113-167">The index creation operation has to complete before it is usable.</span></span> <span data-ttu-id="16113-168">В настоящее время сеанс не должен находиться в транзакции, чтобы создать индекс без сведений о версии.</span><span class="sxs-lookup"><span data-stu-id="16113-168">The session must not currently be in a transaction to create an index without version information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="16113-169">JET_bitIndexSortNullsHigh</span><span class="sxs-lookup"><span data-stu-id="16113-169">JET_bitIndexSortNullsHigh</span></span></p></td>
<td><p><span data-ttu-id="16113-170">Задание этого флага приводит к сортировке значений <strong>null</strong> после данных для всех столбцов в индексе.</span><span class="sxs-lookup"><span data-stu-id="16113-170">Specifying this flag causes <strong>NULL</strong> values to be sorted after data for all columns in the index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="16113-171">JET_bitIndexUnicode</span><span class="sxs-lookup"><span data-stu-id="16113-171">JET_bitIndexUnicode</span></span></p></td>
<td><p><span data-ttu-id="16113-172">Указание этого флага влияет на интерпретацию поля объединения LCID/пидксуникде в структуре.</span><span class="sxs-lookup"><span data-stu-id="16113-172">Specifying this flag affects the interpretation of the lcid/pidxunicde union field in the structure.</span></span> <span data-ttu-id="16113-173">Установка бита означает, что поле <strong>пидксуникоде</strong> фактически указывает на структуру <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> .</span><span class="sxs-lookup"><span data-stu-id="16113-173">Setting the bit means that the <strong>pidxunicode</strong> field actually points to a <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> structure.</span></span> <span data-ttu-id="16113-174">JET_bitIndexUnicode не требуется для индексирования данных в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="16113-174">JET_bitIndexUnicode is not required in order to index Unicode data.</span></span> <span data-ttu-id="16113-175">Он используется только для настройки нормализации данных в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="16113-175">It is only used to customize the normalization of Unicode data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="16113-176">JET_bitIndexTuples</span><span class="sxs-lookup"><span data-stu-id="16113-176">JET_bitIndexTuples</span></span></p></td>
<td><p><span data-ttu-id="16113-177">Указывает, что индекс является индексом кортежа.</span><span class="sxs-lookup"><span data-stu-id="16113-177">Specifies that the index is a tuple index.</span></span> <span data-ttu-id="16113-178">Описание индекса кортежа см. в разделе <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> .</span><span class="sxs-lookup"><span data-stu-id="16113-178">See <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> for a description of a tuple index.</span></span></p>
<p><span data-ttu-id="16113-179">JET_bitIndexTuples была введена в операционной системе Windows XP.</span><span class="sxs-lookup"><span data-stu-id="16113-179">JET_bitIndexTuples was introduced in the Windows XP operating system.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="16113-180">JET_bitIndexTupleLimits</span><span class="sxs-lookup"><span data-stu-id="16113-180">JET_bitIndexTupleLimits</span></span></p></td>
<td><p><span data-ttu-id="16113-181">Указание этого флага влияет на интерпретацию поля объединения <strong>кбварсегмак/птуплелимитс</strong> в структуре.</span><span class="sxs-lookup"><span data-stu-id="16113-181">Specifying this flag affects the interpretation of the <strong>cbVarSegMac/ptuplelimits</strong> union field in the structure.</span></span> <span data-ttu-id="16113-182">Установка этого бита означает, что поле <strong>птуплелимитс</strong> действительно указывает на структуру <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> , чтобы разрешить пользовательские ограничения индекса кортежа (подразумевает JET_bitIndexTuples).</span><span class="sxs-lookup"><span data-stu-id="16113-182">Setting this bit means that the <strong>ptuplelimits</strong> field actually points to a <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure to allow custom tuple index limits (implies JET_bitIndexTuples).</span></span></p>
<p><span data-ttu-id="16113-183">JET_bitIndexTupleLimits была введена в операционную систему Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="16113-183">JET_bitIndexTupleLimits was introduced in the Windows Server 2003 operating system.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="16113-184">JET_bitIndexCrossProduct 0x00004000</span><span class="sxs-lookup"><span data-stu-id="16113-184">JET_bitIndexCrossProduct 0x00004000</span></span></p></td>
<td><p><span data-ttu-id="16113-185">Если задать этот флаг для индекса, имеющего более одного ключевого столбца, который является многозначным, будет создана запись индекса для каждого результата перекрестного произведения всех значений в этих ключевых столбцах.</span><span class="sxs-lookup"><span data-stu-id="16113-185">Specifying this flag for an index that has more than one key column that is a multivalued column will result in an index entry being created for each result of a cross product of all the values in those key columns.</span></span> <span data-ttu-id="16113-186">В противном случае индекс будет иметь только одну запись для каждого многозначного ключевого столбца, который является многозначным столбцом, и каждая из этих элементов индекса будет использовать первый многозначный из всех ключевых столбцов, которые являются многозначными столбцами.</span><span class="sxs-lookup"><span data-stu-id="16113-186">Otherwise, the index would only have one entry for each multivalue in the most significant key column that is a multivalued column and each of those index entries would use the first multivalue from any other key columns that are multivalued columns.</span></span></p>
<p><span data-ttu-id="16113-187">Например, если вы указали этот флаг для индекса по столбцу A, который имеет значения &quot; Red &quot; и &quot; Blue, &quot; а столбец B имеет значения &quot; 1 и 2, то будут &quot; &quot; &quot; созданы следующие записи индекса: &quot; Red &quot; , &quot; 1 &quot; ; &quot; красный &quot; , &quot; 2 &quot; ; &quot; синий &quot; , &quot; 1 &quot; ; &quot; синий &quot; , &quot; 2 &quot; .</span><span class="sxs-lookup"><span data-stu-id="16113-187">For example, if you specified this flag for an index over column A that has the values &quot;red&quot; and &quot;blue&quot; and over column B that has the values &quot;1&quot; and &quot;2&quot; then the following index entries would be created: &quot;red&quot;, &quot;1&quot;; &quot;red&quot;, &quot;2&quot;; &quot;blue&quot;, &quot;1&quot;; &quot;blue&quot;, &quot;2&quot;.</span></span> <span data-ttu-id="16113-188">В противном случае будут созданы следующие записи индекса: &quot; Red &quot; , &quot; 1 &quot; ; &quot; синий &quot; , &quot; 1 &quot; .</span><span class="sxs-lookup"><span data-stu-id="16113-188">Otherwise, the following index entries would be created: &quot;red&quot;, &quot;1&quot;; &quot;blue&quot;, &quot;1&quot;.</span></span></p>
<p><span data-ttu-id="16113-189">JET_bitIndexCrossProduct была введена в операционной системе Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="16113-189">JET_bitIndexCrossProduct was introduced in the Windows Vista operating system.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="16113-190">JET_bitIndexKeyMost 0x00008000</span><span class="sxs-lookup"><span data-stu-id="16113-190">JET_bitIndexKeyMost 0x00008000</span></span></p></td>
<td><p><span data-ttu-id="16113-191">При указании этого флага индекс будет использовать максимальный размер ключа, указанный в поле <strong>кбкэймост</strong> структуры.</span><span class="sxs-lookup"><span data-stu-id="16113-191">Specifying this flag will cause the index to use the maximum key size specified in the <strong>cbKeyMost</strong> field in the structure.</span></span> <span data-ttu-id="16113-192">В противном случае индекс будет использовать JET_cbKeyMost (255) в качестве максимального размера ключа.</span><span class="sxs-lookup"><span data-stu-id="16113-192">Otherwise, the index will use JET_cbKeyMost (255) as its maximum key size.</span></span></p>
<p><span data-ttu-id="16113-193">JET_bitIndexKeyMost была введена в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="16113-193">JET_bitIndexKeyMost was introduced in Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="16113-194">JET_bitIndexDisallowTruncation 0x00010000</span><span class="sxs-lookup"><span data-stu-id="16113-194">JET_bitIndexDisallowTruncation 0x00010000</span></span></p></td>
<td><p><span data-ttu-id="16113-195">При указании этого флага любое обновление индекса приведет к сбою усечения ключа с JET_errKeyTruncated.</span><span class="sxs-lookup"><span data-stu-id="16113-195">Specifying this flag will cause any update to the index that would result in a truncated key to fail with JET_errKeyTruncated.</span></span> <span data-ttu-id="16113-196">В противном случае ключи будут обрезаны без уведомления.</span><span class="sxs-lookup"><span data-stu-id="16113-196">Otherwise, keys will be silently truncated.</span></span> <span data-ttu-id="16113-197">Дополнительные сведения об усечении ключа см. в описании функции <a href="gg269329(v=exchg.10).md">жетмакекэй</a> .</span><span class="sxs-lookup"><span data-stu-id="16113-197">For more information on key truncation, see the <a href="gg269329(v=exchg.10).md">JetMakeKey</a> function.</span></span></p>
<p><span data-ttu-id="16113-198"><strong>Windows Vista: JET_bitIndexDisallowTruncation</strong> впервые появился в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="16113-198"><strong>Windows Vista:  JET_bitIndexDisallowTruncation</strong> is introduced in Windows Vista.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="16113-199">JET_bitIndexNestedTable 0x00020000</span><span class="sxs-lookup"><span data-stu-id="16113-199">JET_bitIndexNestedTable 0x00020000</span></span></p></td>
<td><p><span data-ttu-id="16113-200">Задание этого флага приведет к обновлению индекса по нескольким многозначным столбцам, но только со значениями одного <strong>итагсекуенце</strong>.</span><span class="sxs-lookup"><span data-stu-id="16113-200">Specifying this flag will cause update the index over multiple multivalued columns but only with values of same <strong>itagSequence</strong>.</span></span></p>
<p><span data-ttu-id="16113-201">JET_bitIndexNestedTable была введена в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="16113-201">JET_bitIndexNestedTable was introduced in Windows Vista.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="16113-202">**улденсити**</span><span class="sxs-lookup"><span data-stu-id="16113-202">**ulDensity**</span></span>

<span data-ttu-id="16113-203">Процентная плотность начального дерева B +.</span><span class="sxs-lookup"><span data-stu-id="16113-203">The percentage density of the initial index B+ tree.</span></span> <span data-ttu-id="16113-204">При указании числа меньше 100 используется больше места для первоначального создания индекса, но обеспечивается дальнейшее увеличение индекса, что позволяет избежать внутренней фрагментации.</span><span class="sxs-lookup"><span data-stu-id="16113-204">Specifying a number less than 100 uses up more space to create the index initially, but allows future growth of the index to be in place, thus avoiding internal fragmentation.</span></span>

<span data-ttu-id="16113-205">**lcid**</span><span class="sxs-lookup"><span data-stu-id="16113-205">**lcid**</span></span>

<span data-ttu-id="16113-206">Код локали (LCID), используемый при нормализации данных, если значение JET_bitIndexUnicode не указано в параметре *грбит* .</span><span class="sxs-lookup"><span data-stu-id="16113-206">The locale identifier (LCID) to use when normalizing the data when the JET_bitIndexUnicode value is not specified in the *grbit* parameter.</span></span> <span data-ttu-id="16113-207">Код языка (LCID) влияет на нормализацию, если индекс превышает столбцы в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="16113-207">The LCID affects the normalization if the index is over Unicode columns.</span></span>

<span data-ttu-id="16113-208">**пидксуникоде**</span><span class="sxs-lookup"><span data-stu-id="16113-208">**pidxunicode**</span></span>

<span data-ttu-id="16113-209">Указатель на структуру [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) , если значение JET_bitIndexUnicode задано в параметре *грбит* .</span><span class="sxs-lookup"><span data-stu-id="16113-209">A pointer to a [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) structure if the JET_bitIndexUnicode value is specified in the *grbit* parameter.</span></span> <span data-ttu-id="16113-210">Это позволяет пользователю указать пользовательские флаги, которые передаются функции [LCMapString завершилось ошибкой](https://msdn.microsoft.com/library/dd318700\(vs.85\).aspx) во время нормализации Юникода.</span><span class="sxs-lookup"><span data-stu-id="16113-210">This allows the user to specify custom flags that get passed to the [LCMapString](https://msdn.microsoft.com/library/dd318700\(vs.85\).aspx) function during Unicode normalization.</span></span>

<span data-ttu-id="16113-211">**кбварсегмак**</span><span class="sxs-lookup"><span data-stu-id="16113-211">**cbVarSegMac**</span></span>

<span data-ttu-id="16113-212">Максимальная длина (в байтах) каждого столбца, сохраняемого в индексе, если значение JET_bitIndexTupleLimits не указано в параметре *грбит* .</span><span class="sxs-lookup"><span data-stu-id="16113-212">The maximum length, in bytes, of each column to store in the index when the JET_bitIndexTupleLimits value is not specified in the *grbit* parameter.</span></span>

<span data-ttu-id="16113-213">Указание значения 0 (нуль) для этого поля эквивалентно следующему:</span><span class="sxs-lookup"><span data-stu-id="16113-213">Specifying a value of 0 (zero) for this field is equivalent to:</span></span>

  - <span data-ttu-id="16113-214">Указание JET_cbPrimaryKeyMost для первичного индекса.</span><span class="sxs-lookup"><span data-stu-id="16113-214">Specifying JET_cbPrimaryKeyMost for a primary index.</span></span>

  - <span data-ttu-id="16113-215">Указание JET_cbSecondaryKeyMost для вторичного индекса.</span><span class="sxs-lookup"><span data-stu-id="16113-215">Specifying JET_cbSecondaryKeyMost for a secondary index.</span></span>

<span data-ttu-id="16113-216">**птуплелимитс**</span><span class="sxs-lookup"><span data-stu-id="16113-216">**ptuplelimits**</span></span>

<span data-ttu-id="16113-217">Указатель на структуру [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) , если значение JET_bitIndexTupleLimits задано в параметре *грбит* .</span><span class="sxs-lookup"><span data-stu-id="16113-217">A pointer to a [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) structure if the JET_bitIndexTupleLimits value is specified in the *grbit* parameter.</span></span>

<span data-ttu-id="16113-218">птуплелимитс появился в Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="16113-218">ptuplelimits was introduced in Windows Server 2003.</span></span>

<span data-ttu-id="16113-219">**ргкондитионалколумн**</span><span class="sxs-lookup"><span data-stu-id="16113-219">**rgconditionalcolumn**</span></span>

<span data-ttu-id="16113-220">Необязательный параметр для массива структур [JET_CONDITIONALCOLUMN](./jet-conditionalcolumn-structure.md) , которые используются для указания условных столбцов в индексе.</span><span class="sxs-lookup"><span data-stu-id="16113-220">An optional parameter to an array of [JET_CONDITIONALCOLUMN](./jet-conditionalcolumn-structure.md) structures, which are used to specify the conditional columns in the index.</span></span>

<span data-ttu-id="16113-221">**ккондитионалколумн**</span><span class="sxs-lookup"><span data-stu-id="16113-221">**cConditionalColumn**</span></span>

<span data-ttu-id="16113-222">Число структур в массиве **ргкондитионалколумн** .</span><span class="sxs-lookup"><span data-stu-id="16113-222">The count of structures in the **rgconditionalcolumn** array.</span></span>

<span data-ttu-id="16113-223">**Err**</span><span class="sxs-lookup"><span data-stu-id="16113-223">**err**</span></span>

<span data-ttu-id="16113-224">Содержит код возврата для создания этого индекса.</span><span class="sxs-lookup"><span data-stu-id="16113-224">Contains the return code for creating this index.</span></span>

<span data-ttu-id="16113-225">**кбкэймост**</span><span class="sxs-lookup"><span data-stu-id="16113-225">**cbKeyMost**</span></span>

<span data-ttu-id="16113-226">Указывает максимально допустимый размер (в байтах) для ключей в индексе.</span><span class="sxs-lookup"><span data-stu-id="16113-226">Specifies the maximum allowable size, in bytes, for keys in the index.</span></span> <span data-ttu-id="16113-227">Этот параметр пропускается, если значение JET_bitIndexKeyMost не указано в параметре *грбит* .</span><span class="sxs-lookup"><span data-stu-id="16113-227">This parameter is ignored if the JET_bitIndexKeyMost value is not specified in the *grbit* parameter.</span></span> <span data-ttu-id="16113-228">Если этот параметр имеет значение 0, а JET_bitIndexKeyMost указан в параметре *грбит* , вызывающая функция завершится с ошибкой JET_err_InvalidDef.</span><span class="sxs-lookup"><span data-stu-id="16113-228">If this parameter is set to zero, and JET_bitIndexKeyMost is specified in the *grbit* parameter, the calling function will fail with JET_err_InvalidDef.</span></span>

<span data-ttu-id="16113-229">Минимальный поддерживаемый максимальный размер ключа — JET_cbKeyMostMin (255), который является устаревшим максимальным размером ключа.</span><span class="sxs-lookup"><span data-stu-id="16113-229">The minimum supported maximum key size is JET_cbKeyMostMin (255), which is the legacy maximum key size.</span></span>

<span data-ttu-id="16113-230">Максимальный размер ключа зависит от размера страницы базы данных (JET_paramDatabasePageSize), как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="16113-230">The maximum key size is dependent on the database page size (JET_paramDatabasePageSize), as follows:</span></span>

  - <span data-ttu-id="16113-231">Если JET_paramDatabasePageSize = 2048, то JET_cbKeyMostMin (255) \< =  **кбкэймост** \< = JET_cbKeyMost2KBytePage (500)</span><span class="sxs-lookup"><span data-stu-id="16113-231">If JET_paramDatabasePageSize = 2048 then JET_cbKeyMostMin (255) \<= **cbKeyMost** \<= JET_cbKeyMost2KBytePage (500)</span></span>

  - <span data-ttu-id="16113-232">Если JET_paramDatabasePageSize = 4096, то JET_cbKeyMostMin (255) \< =  **кбкэймост** \< = JET_cbKeyMost4KBytePage (1000)</span><span class="sxs-lookup"><span data-stu-id="16113-232">If JET_paramDatabasePageSize = 4096 then JET_cbKeyMostMin (255) \<= **cbKeyMost** \<= JET_cbKeyMost4KBytePage (1000)</span></span>

  - <span data-ttu-id="16113-233">Если JET_paramDatabasePageSize = 8192, то JET_cbKeyMostMin (255) \< =  **кбкэймост** \< = JET_cbKeyMost8KBytePage (2000)</span><span class="sxs-lookup"><span data-stu-id="16113-233">If JET_paramDatabasePageSize = 8192 then JET_cbKeyMostMin (255) \<= **cbKeyMost** \<= JET_cbKeyMost8KBytePage (2000)</span></span>

<span data-ttu-id="16113-234">Максимальный поддерживаемый размер ключа для экземпляра можно также прочитать из системного параметра JET_paramKeyMost.</span><span class="sxs-lookup"><span data-stu-id="16113-234">The maximum supported key size for the instance can also be read from the JET_paramKeyMost system parameter.</span></span>

<span data-ttu-id="16113-235">**кбкэймост** появился в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="16113-235">**cbKeyMost** was introduced in Windows Vista.</span></span>

### <a name="remarks"></a><span data-ttu-id="16113-236">Комментарии</span><span class="sxs-lookup"><span data-stu-id="16113-236">Remarks</span></span>

<span data-ttu-id="16113-237">ESE поддерживает индексирование по ключевым столбцам, содержащим несколько значений.</span><span class="sxs-lookup"><span data-stu-id="16113-237">ESE supports indexing over key columns containing multiple values.</span></span> <span data-ttu-id="16113-238">Чтобы использовать эту функцию, столбец должен быть типом столбца с тегами (JET_bitColumnTagged) и должен быть помечен для индексации нескольких значений с помощью JET_bitColumnMultiValued.</span><span class="sxs-lookup"><span data-stu-id="16113-238">To use this feature, the column must be a tagged column type (JET_bitColumnTagged), and it must be flagged to have its multiple values indexed with JET_bitColumnMultiValued.</span></span> <span data-ttu-id="16113-239">В версиях Windows, предшествующих Windows Vista, значения в индексе будут развернуты только в первом многозначном ключевом столбце индекса.</span><span class="sxs-lookup"><span data-stu-id="16113-239">In versions of Windows earlier than Windows Vista, only the first multivalued key column in the index will have its values expanded in the index.</span></span> <span data-ttu-id="16113-240">Все другие многозначные и помеченные столбцы будут иметь только первые значения, развернутые в индексе.</span><span class="sxs-lookup"><span data-stu-id="16113-240">All other multivalued and tagged columns will only have their first values expanded in the index.</span></span>

<span data-ttu-id="16113-241">Предположим, что в таблице существуют следующие строки (столбец Alpha не является многозначным, а столбцы бета, гамма и Дельта являются многозначными), а индекс создается как "+ Альфа \\ 0 + бета-версия \\ 0 + гамма 0 + \\ Дельта 0 \\ \\ 0":</span><span class="sxs-lookup"><span data-stu-id="16113-241">Assuming the following rows exist in a table (column Alpha is not multivalued, while columns Beta, Gamma, and Delta are multivalued), and an index is created as "+Alpha\\0+Beta\\0+Gamma\\0+Delta\\0\\0":</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="16113-242">Коэффициент альфа</span><span class="sxs-lookup"><span data-stu-id="16113-242">Alpha</span></span></p></th>
<th><p><span data-ttu-id="16113-243">Бета;</span><span class="sxs-lookup"><span data-stu-id="16113-243">Beta</span></span></p></th>
<th><p><span data-ttu-id="16113-244">Gamma</span><span class="sxs-lookup"><span data-stu-id="16113-244">Gamma</span></span></p></th>
<th><p><span data-ttu-id="16113-245">Разностная версия</span><span class="sxs-lookup"><span data-stu-id="16113-245">Delta</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="16113-246">1</span><span class="sxs-lookup"><span data-stu-id="16113-246">1</span></span></p></td>
<td><p><span data-ttu-id="16113-247">ABC</span><span class="sxs-lookup"><span data-stu-id="16113-247">ABC</span></span><br />
<span data-ttu-id="16113-248">GHI</span><span class="sxs-lookup"><span data-stu-id="16113-248">GHI</span></span><br />
<span data-ttu-id="16113-249">JKL</span><span class="sxs-lookup"><span data-stu-id="16113-249">JKL</span></span></p></td>
<td><p><span data-ttu-id="16113-250">MNO</span><span class="sxs-lookup"><span data-stu-id="16113-250">MNO</span></span><br />
<span data-ttu-id="16113-251">PQR</span><span class="sxs-lookup"><span data-stu-id="16113-251">PQR</span></span><br />
<span data-ttu-id="16113-252">STU</span><span class="sxs-lookup"><span data-stu-id="16113-252">STU</span></span></p></td>
<td><p><span data-ttu-id="16113-253">ввкс</span><span class="sxs-lookup"><span data-stu-id="16113-253">VWX</span></span><br />
<span data-ttu-id="16113-254">из</span><span class="sxs-lookup"><span data-stu-id="16113-254">YZ</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="16113-255">2</span><span class="sxs-lookup"><span data-stu-id="16113-255">2</span></span></p></td>
<td><p><span data-ttu-id="16113-256">ТОТ</span><span class="sxs-lookup"><span data-stu-id="16113-256">THE</span></span></p></td>
<td><p><span data-ttu-id="16113-257">ДОЖДЯ</span><span class="sxs-lookup"><span data-stu-id="16113-257">RAIN</span></span><br />
<span data-ttu-id="16113-258">Испания</span><span class="sxs-lookup"><span data-stu-id="16113-258">SPAIN</span></span></p></td>
<td><p><span data-ttu-id="16113-259">IN</span><span class="sxs-lookup"><span data-stu-id="16113-259">IN</span></span><br />
<span data-ttu-id="16113-260">ПОПАДАЕТ</span><span class="sxs-lookup"><span data-stu-id="16113-260">FALLS</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="16113-261">Будут сохранены следующие кортежи индексов:</span><span class="sxs-lookup"><span data-stu-id="16113-261">The falling index-tuples will be stored:</span></span>

<span data-ttu-id="16113-262">{1, ABC, MNO, ВВКС}</span><span class="sxs-lookup"><span data-stu-id="16113-262">{1,ABC,MNO,VWX}</span></span>  
<span data-ttu-id="16113-263">{1, GHI, MNO, ВВКС}</span><span class="sxs-lookup"><span data-stu-id="16113-263">{1,GHI,MNO,VWX}</span></span>  
<span data-ttu-id="16113-264">{1, ЖКЛ, MNO, ВВКС}</span><span class="sxs-lookup"><span data-stu-id="16113-264">{1,JKL,MNO,VWX}</span></span>  
<span data-ttu-id="16113-265">{2, ДОЖДЯ, IN}</span><span class="sxs-lookup"><span data-stu-id="16113-265">{2,THE,RAIN,IN}</span></span>

<span data-ttu-id="16113-266">Обратите внимание, что {2,, Испания, IN} не хранится, несмотря на то, что столбец Alpha во второй строке имеет один многозначный.</span><span class="sxs-lookup"><span data-stu-id="16113-266">Note that {2,THE,SPAIN,IN} is not stored, even though the Alpha column in the second row happens to have a single multivalue.</span></span>

<span data-ttu-id="16113-267">В версиях Windows, начиная с Windows Vista, все Многозначные столбцы можно расширить в индексе, указав JET_bitIndexCrossProduct.</span><span class="sxs-lookup"><span data-stu-id="16113-267">In versions of Windows starting with Windows Vista, all multivalued columns can be expanded in the index by specifying JET_bitIndexCrossProduct.</span></span>

### <a name="requirements"></a><span data-ttu-id="16113-268">Требования</span><span class="sxs-lookup"><span data-stu-id="16113-268">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="16113-269"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="16113-269"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="16113-270">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="16113-270">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="16113-271"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="16113-271"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="16113-272">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="16113-272">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="16113-273"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="16113-273"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="16113-274">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="16113-274">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="16113-275"><strong>Юникод</strong></span><span class="sxs-lookup"><span data-stu-id="16113-275"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="16113-276">Реализуется как <strong>JET_ INDEXCREATE_W</strong> (Юникод) и <strong>JET_ INDEXCREATE_A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="16113-276">Implemented as <strong>JET_ INDEXCREATE_W</strong> (Unicode) and <strong>JET_ INDEXCREATE_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="16113-277">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="16113-277">See also</span></span>

[<span data-ttu-id="16113-278">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="16113-278">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="16113-279">JET_CONDITIONALCOLUMN</span><span class="sxs-lookup"><span data-stu-id="16113-279">JET_CONDITIONALCOLUMN</span></span>](./jet-conditionalcolumn-structure.md)  
[<span data-ttu-id="16113-280">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="16113-280">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="16113-281">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="16113-281">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="16113-282">JET_TABLECREATE</span><span class="sxs-lookup"><span data-stu-id="16113-282">JET_TABLECREATE</span></span>](./jet-tablecreate-structure.md)  
[<span data-ttu-id="16113-283">JET_TABLECREATE2</span><span class="sxs-lookup"><span data-stu-id="16113-283">JET_TABLECREATE2</span></span>](./jet-tablecreate2-structure.md)  
[<span data-ttu-id="16113-284">JET_TUPLELIMITS</span><span class="sxs-lookup"><span data-stu-id="16113-284">JET_TUPLELIMITS</span></span>](./jet-tuplelimits-structure.md)  
[<span data-ttu-id="16113-285">JET_UNICODEINDEX</span><span class="sxs-lookup"><span data-stu-id="16113-285">JET_UNICODEINDEX</span></span>](./jet-unicodeindex-structure.md)  
[<span data-ttu-id="16113-286">JetCreateIndex2</span><span class="sxs-lookup"><span data-stu-id="16113-286">JetCreateIndex2</span></span>](./jetcreateindex2-function.md)  
[<span data-ttu-id="16113-287">жетсетколумн</span><span class="sxs-lookup"><span data-stu-id="16113-287">JetSetColumn</span></span>](./jetsetcolumn-function.md)  
[<span data-ttu-id="16113-288">жетупдате</span><span class="sxs-lookup"><span data-stu-id="16113-288">JetUpdate</span></span>](./jetupdate-function.md)
