---
description: 'Дополнительные сведения: структура JET_INDEXCREATE2'
title: Структура JET_INDEXCREATE2
TOCTitle: JET_INDEXCREATE2 Structure
ms:assetid: c574500e-8695-4f29-8e9d-6dff987af2a2
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294082(v=EXCHG.10)
ms:contentKeyID: 32765697
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
ms.openlocfilehash: ac0d9a40e159a8aa5054228d18e431cee8d0319f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999727"
---
# <a name="jet_indexcreate2-structure"></a><span data-ttu-id="cb03e-103">Структура JET_INDEXCREATE2</span><span class="sxs-lookup"><span data-stu-id="cb03e-103">JET_INDEXCREATE2 Structure</span></span>


<span data-ttu-id="cb03e-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="cb03e-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="cb03e-105">Структура **JET_INDEXCREATE2** содержит сведения, необходимые для создания индекса данных в базе данных подсистемы расширенного хранилища (ESE).</span><span class="sxs-lookup"><span data-stu-id="cb03e-105">The **JET_INDEXCREATE2** structure contains the information that is required to create an index over data in an Extensible Storage Engine (ESE) database.</span></span> <span data-ttu-id="cb03e-106">Структура используется такими функциями, как [JetCreateIndex2](./jetcreateindex2-function.md), и в таких структурах, как [JET_TABLECREATE](./jet-tablecreate-structure.md) и [JET_TABLECREATE2](./jet-tablecreate2-structure.md).</span><span class="sxs-lookup"><span data-stu-id="cb03e-106">The structure is used by functions such as [JetCreateIndex2](./jetcreateindex2-function.md), and in structures such as [JET_TABLECREATE](./jet-tablecreate-structure.md) and [JET_TABLECREATE2](./jet-tablecreate2-structure.md).</span></span>

<span data-ttu-id="cb03e-107">Структура **JET_INDEXCREATE2** была введена в операционной системе Windows 7.</span><span class="sxs-lookup"><span data-stu-id="cb03e-107">The **JET_INDEXCREATE2** structure was introduced in the Windows 7 operating system.</span></span>

```cpp
typedef struct tagJET_INDEXCREATE2 {
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
  JET_SPACEHINTS* pSpacehints;
} JET_INDEXCREATE;
```

### <a name="members"></a><span data-ttu-id="cb03e-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="cb03e-108">Members</span></span>

<span data-ttu-id="cb03e-109">**кбструкт**</span><span class="sxs-lookup"><span data-stu-id="cb03e-109">**cbStruct**</span></span>

<span data-ttu-id="cb03e-110">Размер данной структуры (в байтах).</span><span class="sxs-lookup"><span data-stu-id="cb03e-110">The size, in bytes, of this structure.</span></span> <span data-ttu-id="cb03e-111">Присвойте этому элементу значение sizeof (JET_INDEXCREATE2).</span><span class="sxs-lookup"><span data-stu-id="cb03e-111">Set this member to sizeof( JET_INDEXCREATE2 ).</span></span>

<span data-ttu-id="cb03e-112">**сзиндекснаме**</span><span class="sxs-lookup"><span data-stu-id="cb03e-112">**szIndexName**</span></span>

<span data-ttu-id="cb03e-113">Имя создаваемого индекса.</span><span class="sxs-lookup"><span data-stu-id="cb03e-113">The name of the index to create.</span></span>

<span data-ttu-id="cb03e-114">Имя должно соответствовать следующим условиям.</span><span class="sxs-lookup"><span data-stu-id="cb03e-114">The name should meet the following conditions:</span></span>

  - <span data-ttu-id="cb03e-115">Оно должно быть меньше JET_cbNameMost, не включая завершающее значение null.</span><span class="sxs-lookup"><span data-stu-id="cb03e-115">It should be less than JET_cbNameMost, not including the terminating null.</span></span>

  - <span data-ttu-id="cb03e-116">Он должен состоять из следующего набора символов: от 0 (нуля) до 9, от A до Z, от a до z и всех остальных знаков препинания, за исключением " \! "</span><span class="sxs-lookup"><span data-stu-id="cb03e-116">It must consist of the following set of characters: 0 (zero) through 9, A through Z, a through z, and all other punctuation except for "\!"</span></span> <span data-ttu-id="cb03e-117">(восклицательный знак), "," (запятая), " \[ " (открывающая скобка) и " \] " (закрывающая скобка), т. е. символы ASCII 0x20, 0x22 до 0x2D, 0x2F через 0x5A, 0x5c и 0x5d до 0x7F.</span><span class="sxs-lookup"><span data-stu-id="cb03e-117">(exclamation point), "," (comma), "\[" (opening bracket), and "\]" (closing bracket) — that is, ASCII characters 0x20, 0x22 through 0x2d, 0x2f through 0x5a, 0x5c, and 0x5d through 0x7f.</span></span>

  - <span data-ttu-id="cb03e-118">Оно не должно начинаться с пробела.</span><span class="sxs-lookup"><span data-stu-id="cb03e-118">It must not begin with a space.</span></span>

  - <span data-ttu-id="cb03e-119">Он должен содержать по крайней мере один символ, не являющийся пробелом.</span><span class="sxs-lookup"><span data-stu-id="cb03e-119">It must contain at least one non-space character.</span></span>

<span data-ttu-id="cb03e-120">**сзкэй**</span><span class="sxs-lookup"><span data-stu-id="cb03e-120">**szKey**</span></span>

<span data-ttu-id="cb03e-121">Указатель на строку токена с разделителями null, завершающуюся символом двойного значения NULL.</span><span class="sxs-lookup"><span data-stu-id="cb03e-121">A pointer to a double-null-terminated string of null-delimited tokens.</span></span>

<span data-ttu-id="cb03e-122">Каждый токен имеет форму " \<direction-specifier\> \<column-name\> ", где Direction-спецификация имеет значение "+" или "-".</span><span class="sxs-lookup"><span data-stu-id="cb03e-122">Each token is of the form "\<direction-specifier\>\<column-name\>", where direction-specification is either "+" or "-".</span></span> <span data-ttu-id="cb03e-123">Например, **сзкэй** "+ ABC \\ 0-DEF \\ 0 + GHI \\ 0" будет индексировать три столбца "ABC" (в порядке возрастания), "def" (в убывающем порядке) и "GHI" (в возрастающем порядке).</span><span class="sxs-lookup"><span data-stu-id="cb03e-123">For example, a **szKey** of "+abc\\0-def\\0+ghi\\0" will index over the three columns "abc" (in ascending order), "def" (in descending order), and "ghi" (in ascending order).</span></span> <span data-ttu-id="cb03e-124">В языке C строковые литералы имеют подразумеваемый знак завершения **null** , поэтому приведенная выше строка будет завершаться двойным значением NULL.</span><span class="sxs-lookup"><span data-stu-id="cb03e-124">In the C language, string literals have an implied **NULL** terminator, so the above string will be terminated by a double-NULL.</span></span>

<span data-ttu-id="cb03e-125">Число столбцов, указанное в **сзкэй** , не должно превышать JET_ccolKeyMost (константа, зависящая от версии).</span><span class="sxs-lookup"><span data-stu-id="cb03e-125">The number of columns specified in **szKey** must not exceed JET_ccolKeyMost (a version-dependent constant).</span></span>

<span data-ttu-id="cb03e-126">По крайней мере один столбец должен иметь имя в **сзкэй**.</span><span class="sxs-lookup"><span data-stu-id="cb03e-126">At least one column must be named in **szKey**.</span></span>

<span data-ttu-id="cb03e-127">Устаревшее поведение. после символа-конца с двойным НУЛЕМ можно указать идентификатор языка (слово, которое передается в МАКЕЛЦИД (LangID, SORT_DEFAULT)) в качестве способа указания кода языка для индекса.</span><span class="sxs-lookup"><span data-stu-id="cb03e-127">Obsolete behavior: After the double-NULL terminator, it is possible to specify a language ID (a WORD which gets passed into MAKELCID( langid, SORT_DEFAULT ) ) as a way to specify the LCID for the index.</span></span> <span data-ttu-id="cb03e-128">Недопустимо указывать идентификатор языка в **сзкэй** и LCID в [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) (путем установки JET_bitIndexUnicode в *грбит*).</span><span class="sxs-lookup"><span data-stu-id="cb03e-128">It is illegal to specify both a language ID in **szKey** and an LCID in [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) (by setting JET_bitIndexUnicode in *grbit*).</span></span>

<span data-ttu-id="cb03e-129">Устарело: после идентификатора языка можно передать **кбварсегмак** как тип данных **UShort** .</span><span class="sxs-lookup"><span data-stu-id="cb03e-129">Deprecated: After the language ID, it is possible to pass **cbVarSegMac** as a **USHORT** data type.</span></span> <span data-ttu-id="cb03e-130">Поведение не определено, если USHORT задан как в **сзкэй** , так и при задании **кбварсегмак** в структуре.</span><span class="sxs-lookup"><span data-stu-id="cb03e-130">The behavior is undefined if the USHORT is set both in **szKey** and if **cbVarSegMac** is set in the structure.</span></span>

<span data-ttu-id="cb03e-131">**cbKey**</span><span class="sxs-lookup"><span data-stu-id="cb03e-131">**cbKey**</span></span>

<span data-ttu-id="cb03e-132">Длина **сзкэй** в байтах, включая два завершающих значения NULL.</span><span class="sxs-lookup"><span data-stu-id="cb03e-132">The length, in bytes, of **szKey**, including the two terminating nulls.</span></span>

<span data-ttu-id="cb03e-133">**грбит**</span><span class="sxs-lookup"><span data-stu-id="cb03e-133">**grbit**</span></span>

<span data-ttu-id="cb03e-134">Группа битов, которая содержит ноль или более параметров значения, перечисленных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="cb03e-134">A group of bits that contain zero or more of the value options that are listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cb03e-135">Значение</span><span class="sxs-lookup"><span data-stu-id="cb03e-135">Value</span></span></p></th>
<th><p><span data-ttu-id="cb03e-136">Значение</span><span class="sxs-lookup"><span data-stu-id="cb03e-136">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cb03e-137">JET_bitIndexUnique</span><span class="sxs-lookup"><span data-stu-id="cb03e-137">JET_bitIndexUnique</span></span></p></td>
<td><p><span data-ttu-id="cb03e-138">Дублирующиеся записи индекса (ключи) запрещены.</span><span class="sxs-lookup"><span data-stu-id="cb03e-138">Duplicate index entries (keys) are disallowed.</span></span> <span data-ttu-id="cb03e-139">Это применяется при вызове <a href="gg269288(v=exchg.10).md">жетупдате</a> , а не при вызове <a href="gg294137(v=exchg.10).md">жетсетколумн</a> .</span><span class="sxs-lookup"><span data-stu-id="cb03e-139">This is enforced when <a href="gg269288(v=exchg.10).md">JetUpdate</a> is called, not when <a href="gg294137(v=exchg.10).md">JetSetColumn</a> is called.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb03e-140">JET_bitIndexPrimary</span><span class="sxs-lookup"><span data-stu-id="cb03e-140">JET_bitIndexPrimary</span></span></p></td>
<td><p><span data-ttu-id="cb03e-141">Индекс является первичным (кластеризованным) индексом.</span><span class="sxs-lookup"><span data-stu-id="cb03e-141">The index is a primary (clustered) index.</span></span> <span data-ttu-id="cb03e-142">Каждая таблица должна иметь ровно один первичный индекс.</span><span class="sxs-lookup"><span data-stu-id="cb03e-142">Every table must have exactly one primary index.</span></span> <span data-ttu-id="cb03e-143">Если первичный индекс явно не определен в таблице, ядро СУБД создаст собственный первичный индекс.</span><span class="sxs-lookup"><span data-stu-id="cb03e-143">If no primary index is explicitly defined over a table, the database engine will create its own primary index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb03e-144">JET_bitIndexDisallowNull</span><span class="sxs-lookup"><span data-stu-id="cb03e-144">JET_bitIndexDisallowNull</span></span></p></td>
<td><p><span data-ttu-id="cb03e-145">Ни один из столбцов, по которым создается индекс, может содержать значение <strong>null</strong> .</span><span class="sxs-lookup"><span data-stu-id="cb03e-145">None of the columns over which the index is created may contain a <strong>NULL</strong> value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb03e-146">JET_bitIndexIgnoreNull</span><span class="sxs-lookup"><span data-stu-id="cb03e-146">JET_bitIndexIgnoreNull</span></span></p></td>
<td><p><span data-ttu-id="cb03e-147">Не добавляйте элемент индекса для строки, если все индексируемые столбцы имеют <strong>значение NULL</strong>.</span><span class="sxs-lookup"><span data-stu-id="cb03e-147">Do not add an index entry for a row if all of the columns being indexed are <strong>NULL</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb03e-148">JET_bitIndexIgnoreAnyNull</span><span class="sxs-lookup"><span data-stu-id="cb03e-148">JET_bitIndexIgnoreAnyNull</span></span></p></td>
<td><p><span data-ttu-id="cb03e-149">Не добавляйте элемент индекса для строки, если какие-либо индексируемые столбцы имеют <strong>значение NULL</strong>.</span><span class="sxs-lookup"><span data-stu-id="cb03e-149">Do not add an index entry for a row if any of the columns being indexed are <strong>NULL</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb03e-150">JET_bitIndexIgnoreFirstNull</span><span class="sxs-lookup"><span data-stu-id="cb03e-150">JET_bitIndexIgnoreFirstNull</span></span></p></td>
<td><p><span data-ttu-id="cb03e-151">Не добавляйте элемент индекса для строки, если первый индексируемый столбец имеет <strong>значение NULL</strong>.</span><span class="sxs-lookup"><span data-stu-id="cb03e-151">Do not add an index entry for a row if the first column being indexed is <strong>NULL</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb03e-152">JET_bitIndexLazyFlush</span><span class="sxs-lookup"><span data-stu-id="cb03e-152">JET_bitIndexLazyFlush</span></span></p></td>
<td><p><span data-ttu-id="cb03e-153">Указывает, что операции с индексами будут регистрироваться неактивно.</span><span class="sxs-lookup"><span data-stu-id="cb03e-153">Specifies that the index operations will be logged lazily.</span></span></p>
<p><span data-ttu-id="cb03e-154">JET_bitIndexLazyFlush не влияет на отложенность обновлений данных.</span><span class="sxs-lookup"><span data-stu-id="cb03e-154">JET_bitIndexLazyFlush does not affect the laziness of data updates.</span></span> <span data-ttu-id="cb03e-155">Если операция индексирования прервана завершением процесса, то при мягком восстановлении все равно удастся получить целостное состояние базы данных, но индекс может отсутствовать.</span><span class="sxs-lookup"><span data-stu-id="cb03e-155">If the indexing operation is interrupted by process termination, Soft Recovery will still be able to able to get the database to a consistent state, but the index may not be present.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb03e-156">JET_bitIndexEmpty</span><span class="sxs-lookup"><span data-stu-id="cb03e-156">JET_bitIndexEmpty</span></span></p></td>
<td><p><span data-ttu-id="cb03e-157">Не пытайтесь построить индекс, так как все записи будут иметь <strong>значение NULL</strong>.</span><span class="sxs-lookup"><span data-stu-id="cb03e-157">Do not try to build the index, because all entries would evaluate to <strong>NULL</strong>.</span></span> <span data-ttu-id="cb03e-158"><strong>грбит</strong> НЕОБХОДИМО также указать JET_bitIgnoreAnyNull при передаче JET_bitIndexEmpty.</span><span class="sxs-lookup"><span data-stu-id="cb03e-158"><strong>grbit</strong> MUST also specify JET_bitIgnoreAnyNull when JET_bitIndexEmpty is passed.</span></span> <span data-ttu-id="cb03e-159">Это улучшение производительности.</span><span class="sxs-lookup"><span data-stu-id="cb03e-159">This is a performance enhancement.</span></span> <span data-ttu-id="cb03e-160">Например, если новый столбец добавляется в таблицу, а затем создается индекс поверх этого вновь добавленного столбца, то все записи в таблице просматриваются, даже если они не добавляются в индекс.</span><span class="sxs-lookup"><span data-stu-id="cb03e-160">For example, if a new column is added to a table, and then an index is created over this newly added column, all the records in the table are scanned even though they are not added to the index.</span></span> <span data-ttu-id="cb03e-161">При указании JET_bitIndexEmpty пропускается сканирование таблицы, что может занять длительное время.</span><span class="sxs-lookup"><span data-stu-id="cb03e-161">Specifying JET_bitIndexEmpty skips the scanning of the table, which could potentially take a long time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb03e-162">JET_bitIndexUnversioned</span><span class="sxs-lookup"><span data-stu-id="cb03e-162">JET_bitIndexUnversioned</span></span></p></td>
<td><p><span data-ttu-id="cb03e-163">JET_bitIndexUnversioned приводит к тому, что создание индекса станет видимым для других транзакций.</span><span class="sxs-lookup"><span data-stu-id="cb03e-163">JET_bitIndexUnversioned causes index creation to be visible to other transactions.</span></span> <span data-ttu-id="cb03e-164">Как правило, сеанс в транзакции не сможет увидеть операцию создания индекса в другом сеансе.</span><span class="sxs-lookup"><span data-stu-id="cb03e-164">Ordinarily, a session in a transaction will not be able to see an index creation operation in another session.</span></span> <span data-ttu-id="cb03e-165">Этот флаг может быть полезен, если другая транзакция, скорее всего, создаст тот же индекс.</span><span class="sxs-lookup"><span data-stu-id="cb03e-165">This flag can be useful if another transaction is likely to create the same index.</span></span> <span data-ttu-id="cb03e-166">Второй индекс-Create просто завершится сбоем, а не может вызвать множество ненужных операций с базой данных.</span><span class="sxs-lookup"><span data-stu-id="cb03e-166">The second index-create will simply fail instead of potentially causing many unnecessary database operations.</span></span> <span data-ttu-id="cb03e-167">Вторая транзакция может не иметь возможности немедленно использовать индекс.</span><span class="sxs-lookup"><span data-stu-id="cb03e-167">The second transaction may not be able to use the index immediately.</span></span> <span data-ttu-id="cb03e-168">Операция создания индекса должна быть завершена, прежде чем ее можно будет использовать.</span><span class="sxs-lookup"><span data-stu-id="cb03e-168">The index creation operation has to complete before it is usable.</span></span> <span data-ttu-id="cb03e-169">В настоящее время сеанс не должен находиться в транзакции, чтобы создать индекс без сведений о версии.</span><span class="sxs-lookup"><span data-stu-id="cb03e-169">The session must not currently be in a transaction to create an index without version information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb03e-170">JET_bitIndexSortNullsHigh</span><span class="sxs-lookup"><span data-stu-id="cb03e-170">JET_bitIndexSortNullsHigh</span></span></p></td>
<td><p><span data-ttu-id="cb03e-171">Задание этого флага приводит к сортировке значений <strong>null</strong> после данных для всех столбцов в индексе.</span><span class="sxs-lookup"><span data-stu-id="cb03e-171">Specifying this flag causes <strong>NULL</strong> values to be sorted after data for all columns in the index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb03e-172">JET_bitIndexUnicode</span><span class="sxs-lookup"><span data-stu-id="cb03e-172">JET_bitIndexUnicode</span></span></p></td>
<td><p><span data-ttu-id="cb03e-173">Указание этого флага влияет на интерпретацию поля объединения LCID/пидксуникде в структуре.</span><span class="sxs-lookup"><span data-stu-id="cb03e-173">Specifying this flag affects the interpretation of the lcid/pidxunicde union field in the structure.</span></span> <span data-ttu-id="cb03e-174">Установка бита означает, что поле пидксуникоде фактически указывает на структуру <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> .</span><span class="sxs-lookup"><span data-stu-id="cb03e-174">Setting the bit means that the pidxunicode field actually points to a <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> structure.</span></span> <span data-ttu-id="cb03e-175">JET_bitIndexUnicode не требуется для индексирования данных в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="cb03e-175">JET_bitIndexUnicode is not required to index Unicode data.</span></span> <span data-ttu-id="cb03e-176">Это необходимо только для настройки нормализации данных в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="cb03e-176">It is only needed to customize the normalization of Unicode data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb03e-177">JET_bitIndexTuples</span><span class="sxs-lookup"><span data-stu-id="cb03e-177">JET_bitIndexTuples</span></span></p></td>
<td><p><span data-ttu-id="cb03e-178">Указывает, что индекс является индексом кортежа.</span><span class="sxs-lookup"><span data-stu-id="cb03e-178">Specifies that the index is a tuple index.</span></span> <span data-ttu-id="cb03e-179">Описание индекса кортежа см. в разделе <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> .</span><span class="sxs-lookup"><span data-stu-id="cb03e-179">See <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> for a description of a tuple index.</span></span></p>
<p><span data-ttu-id="cb03e-180">Значение JET_bitIndexTuples было введено в операционной системе Windows XP.</span><span class="sxs-lookup"><span data-stu-id="cb03e-180">The JET_bitIndexTuples value was introduced in the Windows XP operating system.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb03e-181">JET_bitIndexTupleLimits</span><span class="sxs-lookup"><span data-stu-id="cb03e-181">JET_bitIndexTupleLimits</span></span></p></td>
<td><p><span data-ttu-id="cb03e-182">Указание этого флага влияет на интерпретацию поля объединения <strong>кбварсегмак/птуплелимитс</strong> в структуре.</span><span class="sxs-lookup"><span data-stu-id="cb03e-182">Specifying this flag affects the interpretation of the <strong>cbVarSegMac/ptuplelimits</strong> union field in the structure.</span></span> <span data-ttu-id="cb03e-183">Установка этого бита означает, что поле <strong>птуплелимитс</strong> действительно указывает на структуру <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> , чтобы разрешить пользовательские ограничения индекса кортежа (подразумевает JET_bitIndexTuples).</span><span class="sxs-lookup"><span data-stu-id="cb03e-183">Setting this bit means that the <strong>ptuplelimits</strong> field actually points to a <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure to allow custom tuple index limits (implies JET_bitIndexTuples).</span></span></p>
<p><span data-ttu-id="cb03e-184">Значение <strong>JET_bitIndexTupleLimits</strong> было введено в операционной системе Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="cb03e-184">The <strong>JET_bitIndexTupleLimits</strong> value was introduced in the Windows Server 2003 operating system.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb03e-185">JET_bitIndexCrossProduct</span><span class="sxs-lookup"><span data-stu-id="cb03e-185">JET_bitIndexCrossProduct</span></span><br />
<span data-ttu-id="cb03e-186">0x00004000</span><span class="sxs-lookup"><span data-stu-id="cb03e-186">0x00004000</span></span></p></td>
<td><p><span data-ttu-id="cb03e-187">Если задать этот флаг для индекса, имеющего более одного ключевого столбца, который является многозначным, будет создана запись индекса для каждого результата перекрестного произведения всех значений в этих ключевых столбцах.</span><span class="sxs-lookup"><span data-stu-id="cb03e-187">Specifying this flag for an index that has more than one key column that is a multivalued column will result in an index entry being created for each result of a cross product of all the values in those key columns.</span></span> <span data-ttu-id="cb03e-188">В противном случае индекс будет иметь только одну запись для каждого многозначного ключевого столбца, который является многозначным столбцом, и каждая из этих элементов индекса будет использовать первый многозначный из всех ключевых столбцов, которые являются многозначными столбцами.</span><span class="sxs-lookup"><span data-stu-id="cb03e-188">Otherwise, the index would only have one entry for each multivalue in the most significant key column that is a multivalued column and each of those index entries would use the first multivalue from any other key columns that are multi valued columns.</span></span></p>
<p><span data-ttu-id="cb03e-189">Например, если вы указали этот флаг для индекса для столбца A, который имеет значения &quot; Red &quot; и Blue &quot; , &quot; а столбец B со значениями &quot; 1 &quot; и &quot; 2 &quot; , будут созданы следующие записи индекса: &quot; Red &quot; , &quot; 1 &quot; ; &quot; красный &quot; , &quot; 2 &quot; ; &quot; синий &quot; , &quot; 1 &quot; ; &quot; синий &quot; , &quot; 2 &quot; .</span><span class="sxs-lookup"><span data-stu-id="cb03e-189">For example, if you specified this flag for an index over column A that has the values &quot;red&quot; and &quot;blue&quot; and over column B that has the values &quot;1&quot; and &quot;2&quot;, the following index entries would be created: &quot;red&quot;, &quot;1&quot;; &quot;red&quot;, &quot;2&quot;; &quot;blue&quot;, &quot;1&quot;; &quot;blue&quot;, &quot;2&quot;.</span></span> <span data-ttu-id="cb03e-190">В противном случае будут созданы следующие записи индекса: &quot; Red &quot; , &quot; 1 &quot; ; &quot; синий &quot; , &quot; 1 &quot; .</span><span class="sxs-lookup"><span data-stu-id="cb03e-190">Otherwise, the following index entries would be created: &quot;red&quot;, &quot;1&quot;; &quot;blue&quot;, &quot;1&quot;.</span></span></p>
<p><span data-ttu-id="cb03e-191">Значение <strong>JET_bitIndexCrossProduct</strong> было введено в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="cb03e-191">The <strong>JET_bitIndexCrossProduct</strong> value was introduced in Windows Vista.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb03e-192">JET_bitIndexKeyMost</span><span class="sxs-lookup"><span data-stu-id="cb03e-192">JET_bitIndexKeyMost</span></span><br />
<span data-ttu-id="cb03e-193">0x00008000</span><span class="sxs-lookup"><span data-stu-id="cb03e-193">0x00008000</span></span></p></td>
<td><p><span data-ttu-id="cb03e-194">При указании этого флага индекс будет использовать максимальный размер ключа, указанный в поле <strong>кбкэймост</strong> структуры.</span><span class="sxs-lookup"><span data-stu-id="cb03e-194">Specifying this flag will cause the index to use the maximum key size specified in the <strong>cbKeyMost</strong> field in the structure.</span></span> <span data-ttu-id="cb03e-195">В противном случае индекс будет использовать JET_cbKeyMost (255) в качестве максимального размера ключа.</span><span class="sxs-lookup"><span data-stu-id="cb03e-195">Otherwise, the index will use JET_cbKeyMost (255) as its maximum key size.</span></span></p>
<p><span data-ttu-id="cb03e-196">Значение <strong>JET_bitIndexKeyMost</strong> было введено в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="cb03e-196">The <strong>JET_bitIndexKeyMost</strong> value was introduced in Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb03e-197">JET_bitIndexDisallowTruncation</span><span class="sxs-lookup"><span data-stu-id="cb03e-197">JET_bitIndexDisallowTruncation</span></span><br />
<span data-ttu-id="cb03e-198">0x00010000</span><span class="sxs-lookup"><span data-stu-id="cb03e-198">0x00010000</span></span></p></td>
<td><p><span data-ttu-id="cb03e-199">При указании этого флага любое обновление индекса приведет к сбою усечения ключа с кодом ответа JET_errKeyTruncated.</span><span class="sxs-lookup"><span data-stu-id="cb03e-199">Specifying this flag will cause any update to the index that would result in a truncated key to fail with the JET_errKeyTruncated response code.</span></span> <span data-ttu-id="cb03e-200">В противном случае ключи будут обрезаны без уведомления.</span><span class="sxs-lookup"><span data-stu-id="cb03e-200">Otherwise, keys will be silently truncated.</span></span> <span data-ttu-id="cb03e-201">Дополнительные сведения о усечении ключа см. в разделе <a href="gg269329(v=exchg.10).md">жетмакекэй</a>.</span><span class="sxs-lookup"><span data-stu-id="cb03e-201">For more information about key truncation, see <a href="gg269329(v=exchg.10).md">JetMakeKey</a>.</span></span></p>
<p><span data-ttu-id="cb03e-202">Значение <strong>JET_bitIndexDisallowTruncation</strong> было введено в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="cb03e-202">The <strong>JET_bitIndexDisallowTruncation</strong> value was introduced in Windows Vista.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cb03e-203">**улденсити**</span><span class="sxs-lookup"><span data-stu-id="cb03e-203">**ulDensity**</span></span>

<span data-ttu-id="cb03e-204">Процентная плотность начального дерева B +.</span><span class="sxs-lookup"><span data-stu-id="cb03e-204">The percentage density of the initial index B+ tree.</span></span> <span data-ttu-id="cb03e-205">При указании числа меньше 100 используется больше места для первоначального создания индекса, но обеспечивается дальнейшее увеличение индекса, что позволяет избежать внутренней фрагментации.</span><span class="sxs-lookup"><span data-stu-id="cb03e-205">Specifying a number less than 100 uses up more space to create the index initially, but allows future growth of the index to be in place, thus avoiding internal fragmentation.</span></span>

<span data-ttu-id="cb03e-206">**lcid**</span><span class="sxs-lookup"><span data-stu-id="cb03e-206">**lcid**</span></span>

<span data-ttu-id="cb03e-207">Код локали (LCID), используемый при нормализации данных, если значение JET_bitIndexUnicode не указано в параметре *грбит* .</span><span class="sxs-lookup"><span data-stu-id="cb03e-207">The locale identifier (LCID) to use when normalizing the data when the JET_bitIndexUnicode value is not specified in the *grbit* parameter.</span></span> <span data-ttu-id="cb03e-208">Код языка (LCID) влияет на нормализацию, если индекс превышает столбцы в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="cb03e-208">The LCID affects the normalization if the index is over Unicode columns.</span></span>

<span data-ttu-id="cb03e-209">**пидксуникоде**</span><span class="sxs-lookup"><span data-stu-id="cb03e-209">**pidxunicode**</span></span>

<span data-ttu-id="cb03e-210">Указатель на структуру [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) , если значение JET_bitIndexUnicode задано в параметре *грбит* .</span><span class="sxs-lookup"><span data-stu-id="cb03e-210">A pointer to a [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) structure if the JET_bitIndexUnicode value is specified in the *grbit* parameter.</span></span> <span data-ttu-id="cb03e-211">Это позволяет пользователю указать пользовательские флаги, которые передаются функции [LCMapString завершилось ошибкой](https://msdn.microsoft.com/library/dd318700\(vs.85\).aspx) во время нормализации Юникода.</span><span class="sxs-lookup"><span data-stu-id="cb03e-211">This allows the user to specify custom flags that get passed to the [LCMapString](https://msdn.microsoft.com/library/dd318700\(vs.85\).aspx) function during Unicode normalization.</span></span>

<span data-ttu-id="cb03e-212">**кбварсегмак**</span><span class="sxs-lookup"><span data-stu-id="cb03e-212">**cbVarSegMac**</span></span>

<span data-ttu-id="cb03e-213">Максимальная длина (в байтах) каждого столбца, сохраняемого в индексе, если значение JET_bitIndexTupleLimits не указано в параметре *грбит* .</span><span class="sxs-lookup"><span data-stu-id="cb03e-213">The maximum length, in bytes, of each column to store in the index when the JET_bitIndexTupleLimits value is not specified in the *grbit* parameter.</span></span>

<span data-ttu-id="cb03e-214">Указание значения 0 (ноль) для этого поля эквивалентно следующему:</span><span class="sxs-lookup"><span data-stu-id="cb03e-214">Specifying a value of 0 (zero) for this field is equivalent to the following:</span></span>

  - <span data-ttu-id="cb03e-215">Указание JET_cbPrimaryKeyMost для первичного индекса.</span><span class="sxs-lookup"><span data-stu-id="cb03e-215">Specifying JET_cbPrimaryKeyMost for a primary index.</span></span>

  - <span data-ttu-id="cb03e-216">Указание JET_cbSecondaryKeyMost для вторичного индекса.</span><span class="sxs-lookup"><span data-stu-id="cb03e-216">Specifying JET_cbSecondaryKeyMost for a secondary index.</span></span>

<span data-ttu-id="cb03e-217">**птуплелимитс**</span><span class="sxs-lookup"><span data-stu-id="cb03e-217">**ptuplelimits**</span></span>

<span data-ttu-id="cb03e-218">Указатель на структуру [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) , если значение JET_bitIndexTupleLimits задано в параметре *грбит* .</span><span class="sxs-lookup"><span data-stu-id="cb03e-218">A pointer to a [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) structure if the JET_bitIndexTupleLimits value is specified in the *grbit* parameter.</span></span>

<span data-ttu-id="cb03e-219">**птуплелимитс** появился в Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="cb03e-219">**ptuplelimits** was introduced in Windows Server 2003.</span></span>

<span data-ttu-id="cb03e-220">**ргкондитионалколумн**</span><span class="sxs-lookup"><span data-stu-id="cb03e-220">**rgconditionalcolumn**</span></span>

<span data-ttu-id="cb03e-221">Необязательный параметр для массива структур [JET_CONDITIONALCOLUMN](./jet-conditionalcolumn-structure.md) , которые используются для указания условных столбцов в индексе.</span><span class="sxs-lookup"><span data-stu-id="cb03e-221">An optional parameter to an array of [JET_CONDITIONALCOLUMN](./jet-conditionalcolumn-structure.md) structures, which are used to specify the conditional columns in the index.</span></span>

<span data-ttu-id="cb03e-222">**ккондитионалколумн**</span><span class="sxs-lookup"><span data-stu-id="cb03e-222">**cConditionalColumn**</span></span>

<span data-ttu-id="cb03e-223">Число структур в массиве **ргкондитионалколумн** .</span><span class="sxs-lookup"><span data-stu-id="cb03e-223">The count of structures in the **rgconditionalcolumn** array.</span></span>

<span data-ttu-id="cb03e-224">**Err**</span><span class="sxs-lookup"><span data-stu-id="cb03e-224">**err**</span></span>

<span data-ttu-id="cb03e-225">Содержит код возврата для создания этого индекса.</span><span class="sxs-lookup"><span data-stu-id="cb03e-225">Contains the return code for creating this index.</span></span>

<span data-ttu-id="cb03e-226">**кбкэймост**</span><span class="sxs-lookup"><span data-stu-id="cb03e-226">**cbKeyMost**</span></span>

<span data-ttu-id="cb03e-227">Указывает максимально допустимый размер (в байтах) для ключей в индексе.</span><span class="sxs-lookup"><span data-stu-id="cb03e-227">Specifies the maximum allowable size, in bytes, for keys in the index.</span></span> <span data-ttu-id="cb03e-228">Этот параметр игнорируется, если JET_bitIndexKeyMost не указан в параметре *грбит* .</span><span class="sxs-lookup"><span data-stu-id="cb03e-228">This parameter is ignored if JET_bitIndexKeyMost is not specified in *grbit* parameter.</span></span> <span data-ttu-id="cb03e-229">Если этот параметр имеет значение 0, а JET_bitIndexKeyMost указан в члене *грбит* , вызывающая функция завершится ошибкой с JET_err_InvalidDef.</span><span class="sxs-lookup"><span data-stu-id="cb03e-229">If this parameter is set to zero, and JET_bitIndexKeyMost is specified in the *grbit* member, the calling function will fail with JET_err_InvalidDef.</span></span>

<span data-ttu-id="cb03e-230">Минимальный поддерживаемый максимальный размер ключа — JET_cbKeyMostMin (255), который является устаревшим максимальным размером ключа.</span><span class="sxs-lookup"><span data-stu-id="cb03e-230">The minimum supported maximum key size is JET_cbKeyMostMin (255), which is the legacy maximum key size.</span></span>

<span data-ttu-id="cb03e-231">Максимальный размер ключа зависит от размера страницы базы данных (JET_paramDatabasePageSize) следующим образом:</span><span class="sxs-lookup"><span data-stu-id="cb03e-231">The maximum key size is dependent on the database page size (JET_paramDatabasePageSize) as follows:</span></span>

  - <span data-ttu-id="cb03e-232">Если JET_paramDatabasePageSize = 2048, то JET_cbKeyMostMin (255) \< =  **кбкэймост** \< = JET_cbKeyMost2KBytePage (500)</span><span class="sxs-lookup"><span data-stu-id="cb03e-232">If JET_paramDatabasePageSize = 2048 then JET_cbKeyMostMin (255) \<= **cbKeyMost** \<= JET_cbKeyMost2KBytePage (500)</span></span>

  - <span data-ttu-id="cb03e-233">Если JET_paramDatabasePageSize = 4096, то JET_cbKeyMostMin (255) \< =  **кбкэймост** \< = JET_cbKeyMost4KBytePage (1000)</span><span class="sxs-lookup"><span data-stu-id="cb03e-233">If JET_paramDatabasePageSize = 4096 then JET_cbKeyMostMin (255) \<= **cbKeyMost** \<= JET_cbKeyMost4KBytePage (1000)</span></span>

  - <span data-ttu-id="cb03e-234">Если JET_paramDatabasePageSize = 8192, то JET_cbKeyMostMin (255) \< =  **кбкэймост** \< = JET_cbKeyMost8KBytePage (2000)</span><span class="sxs-lookup"><span data-stu-id="cb03e-234">If JET_paramDatabasePageSize = 8192 then JET_cbKeyMostMin (255) \<= **cbKeyMost** \<= JET_cbKeyMost8KBytePage (2000)</span></span>

<span data-ttu-id="cb03e-235">Максимальный поддерживаемый максимальный размер ключа для экземпляра можно также прочитать из системного параметра JET_paramKeyMost.</span><span class="sxs-lookup"><span data-stu-id="cb03e-235">The maximum supported maximum key size for the instance can also be read from the JET_paramKeyMost system parameter.</span></span>

<span data-ttu-id="cb03e-236">**кбкэймост** появился в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="cb03e-236">**cbKeyMost** was introduced in Windows Vista.</span></span>

<span data-ttu-id="cb03e-237">**пспацехинтс**</span><span class="sxs-lookup"><span data-stu-id="cb03e-237">**pSpacehints**</span></span>

<span data-ttu-id="cb03e-238">Указатель на структуру [JET_SPACEHINTS](./jet-spacehints-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="cb03e-238">A pointer to a [JET_SPACEHINTS](./jet-spacehints-structure.md) structure.</span></span>

<span data-ttu-id="cb03e-239">**пспацехинтс** появился в Windows 7.</span><span class="sxs-lookup"><span data-stu-id="cb03e-239">**pSpacehints** was introduced in Windows 7.</span></span>

### <a name="remarks"></a><span data-ttu-id="cb03e-240">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cb03e-240">Remarks</span></span>

<span data-ttu-id="cb03e-241">ESE поддерживает индексирование по ключевым столбцам, содержащим несколько значений.</span><span class="sxs-lookup"><span data-stu-id="cb03e-241">ESE supports indexing over key columns containing multiple values.</span></span> <span data-ttu-id="cb03e-242">Чтобы использовать эту функцию, столбец должен быть типом столбца с тегами (JET_bitColumnTagged) и должен быть помечен для индексации нескольких значений с помощью JET_bitColumnMultiValued.</span><span class="sxs-lookup"><span data-stu-id="cb03e-242">To use this feature, the column must be a tagged column type (JET_bitColumnTagged), and it must be flagged to have its multiple values indexed with JET_bitColumnMultiValued.</span></span> <span data-ttu-id="cb03e-243">В версиях Windows, предшествующих Windows Vista, значения в индексе будут развернуты только в первом многозначном ключевом столбце индекса.</span><span class="sxs-lookup"><span data-stu-id="cb03e-243">In versions of Windows earlier than Windows Vista, only the first multivalued key column in the index will have its values expanded in the index.</span></span> <span data-ttu-id="cb03e-244">Все другие многозначные и помеченные столбцы будут иметь только первые значения, развернутые в индексе.</span><span class="sxs-lookup"><span data-stu-id="cb03e-244">All other multivalued and tagged columns will only have their first values expanded in the index.</span></span>

<span data-ttu-id="cb03e-245">Предположим, что в таблице существуют следующие строки (столбец Alpha не является многозначным, а столбцы бета, гамма и Дельта являются многозначными), а индекс создается как "+ Альфа \\ 0 + бета-версия \\ 0 + гамма 0 + \\ Дельта 0 \\ \\ 0":</span><span class="sxs-lookup"><span data-stu-id="cb03e-245">Assuming the following rows exist in a table (column Alpha is not multivalued, while columns Beta, Gamma, and Delta are multivalued), and an index is created as "+Alpha\\0+Beta\\0+Gamma\\0+Delta\\0\\0":</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cb03e-246">Коэффициент альфа</span><span class="sxs-lookup"><span data-stu-id="cb03e-246">Alpha</span></span></p></th>
<th><p><span data-ttu-id="cb03e-247">Бета;</span><span class="sxs-lookup"><span data-stu-id="cb03e-247">Beta</span></span></p></th>
<th><p><span data-ttu-id="cb03e-248">Gamma</span><span class="sxs-lookup"><span data-stu-id="cb03e-248">Gamma</span></span></p></th>
<th><p><span data-ttu-id="cb03e-249">Разностная версия</span><span class="sxs-lookup"><span data-stu-id="cb03e-249">Delta</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cb03e-250">1</span><span class="sxs-lookup"><span data-stu-id="cb03e-250">1</span></span></p></td>
<td><p><span data-ttu-id="cb03e-251">ABC</span><span class="sxs-lookup"><span data-stu-id="cb03e-251">ABC</span></span><br />
<span data-ttu-id="cb03e-252">GHI</span><span class="sxs-lookup"><span data-stu-id="cb03e-252">GHI</span></span><br />
<span data-ttu-id="cb03e-253">JKL</span><span class="sxs-lookup"><span data-stu-id="cb03e-253">JKL</span></span></p></td>
<td><p><span data-ttu-id="cb03e-254">MNO</span><span class="sxs-lookup"><span data-stu-id="cb03e-254">MNO</span></span><br />
<span data-ttu-id="cb03e-255">PQR</span><span class="sxs-lookup"><span data-stu-id="cb03e-255">PQR</span></span><br />
<span data-ttu-id="cb03e-256">STU</span><span class="sxs-lookup"><span data-stu-id="cb03e-256">STU</span></span></p></td>
<td><p><span data-ttu-id="cb03e-257">ввкс</span><span class="sxs-lookup"><span data-stu-id="cb03e-257">VWX</span></span><br />
<span data-ttu-id="cb03e-258">из</span><span class="sxs-lookup"><span data-stu-id="cb03e-258">YZ</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb03e-259">2</span><span class="sxs-lookup"><span data-stu-id="cb03e-259">2</span></span></p></td>
<td><p><span data-ttu-id="cb03e-260">ТОТ</span><span class="sxs-lookup"><span data-stu-id="cb03e-260">THE</span></span></p></td>
<td><p><span data-ttu-id="cb03e-261">ДОЖДЯ</span><span class="sxs-lookup"><span data-stu-id="cb03e-261">RAIN</span></span><br />
<span data-ttu-id="cb03e-262">Испания</span><span class="sxs-lookup"><span data-stu-id="cb03e-262">SPAIN</span></span></p></td>
<td><p><span data-ttu-id="cb03e-263">IN</span><span class="sxs-lookup"><span data-stu-id="cb03e-263">IN</span></span><br />
<span data-ttu-id="cb03e-264">ПОПАДАЕТ</span><span class="sxs-lookup"><span data-stu-id="cb03e-264">FALLS</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cb03e-265">Будут сохранены следующие индексные кортежи:</span><span class="sxs-lookup"><span data-stu-id="cb03e-265">The following index-tuples will be stored:</span></span>

<span data-ttu-id="cb03e-266">{1, ABC, MNO, ВВКС}</span><span class="sxs-lookup"><span data-stu-id="cb03e-266">{1,ABC,MNO,VWX}</span></span>  
<span data-ttu-id="cb03e-267">{1, GHI, MNO, ВВКС}</span><span class="sxs-lookup"><span data-stu-id="cb03e-267">{1,GHI,MNO,VWX}</span></span>  
<span data-ttu-id="cb03e-268">{1, ЖКЛ, MNO, ВВКС}</span><span class="sxs-lookup"><span data-stu-id="cb03e-268">{1,JKL,MNO,VWX}</span></span>  
<span data-ttu-id="cb03e-269">{2, ДОЖДЯ, IN}</span><span class="sxs-lookup"><span data-stu-id="cb03e-269">{2,THE,RAIN,IN}</span></span>

<span data-ttu-id="cb03e-270">Обратите внимание, что {2,, Испания, IN} не хранится, несмотря на то, что столбец Alpha во второй строке имеет один многозначный.</span><span class="sxs-lookup"><span data-stu-id="cb03e-270">Note that {2,THE,SPAIN,IN} is not stored, even though the Alpha column in the second row happens to have a single multivalue.</span></span>

<span data-ttu-id="cb03e-271">В версиях Windows, начиная с Windows Vista, все Многозначные столбцы можно расширить в индексе, указав JET_bitIndexCrossProduct.</span><span class="sxs-lookup"><span data-stu-id="cb03e-271">In versions of Windows starting with Windows Vista, all multivalued columns can be expanded in the index by specifying JET_bitIndexCrossProduct.</span></span>

### <a name="requirements"></a><span data-ttu-id="cb03e-272">Требования</span><span class="sxs-lookup"><span data-stu-id="cb03e-272">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cb03e-273"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="cb03e-273"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="cb03e-274">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="cb03e-274">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb03e-275"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="cb03e-275"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="cb03e-276">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="cb03e-276">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb03e-277"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="cb03e-277"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="cb03e-278">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="cb03e-278">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb03e-279"><strong>Юникод</strong></span><span class="sxs-lookup"><span data-stu-id="cb03e-279"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="cb03e-280">Реализуется как <strong>JET_ INDEXCREATE2_W</strong> (Юникод) и <strong>JET_ INDEXCREATE2_A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="cb03e-280">Implemented as <strong>JET_ INDEXCREATE2_W</strong> (Unicode) and <strong>JET_ INDEXCREATE2_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="cb03e-281">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cb03e-281">See also</span></span>

[<span data-ttu-id="cb03e-282">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="cb03e-282">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="cb03e-283">JET_CONDITIONALCOLUMN</span><span class="sxs-lookup"><span data-stu-id="cb03e-283">JET_CONDITIONALCOLUMN</span></span>](./jet-conditionalcolumn-structure.md)  
[<span data-ttu-id="cb03e-284">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="cb03e-284">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="cb03e-285">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="cb03e-285">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="cb03e-286">JET_TABLECREATE</span><span class="sxs-lookup"><span data-stu-id="cb03e-286">JET_TABLECREATE</span></span>](./jet-tablecreate-structure.md)  
[<span data-ttu-id="cb03e-287">JET_TABLECREATE2</span><span class="sxs-lookup"><span data-stu-id="cb03e-287">JET_TABLECREATE2</span></span>](./jet-tablecreate2-structure.md)  
[<span data-ttu-id="cb03e-288">JET_TUPLELIMITS</span><span class="sxs-lookup"><span data-stu-id="cb03e-288">JET_TUPLELIMITS</span></span>](./jet-tuplelimits-structure.md)  
[<span data-ttu-id="cb03e-289">JET_UNICODEINDEX</span><span class="sxs-lookup"><span data-stu-id="cb03e-289">JET_UNICODEINDEX</span></span>](./jet-unicodeindex-structure.md)  
[<span data-ttu-id="cb03e-290">JetCreateIndex2</span><span class="sxs-lookup"><span data-stu-id="cb03e-290">JetCreateIndex2</span></span>](./jetcreateindex2-function.md)  
[<span data-ttu-id="cb03e-291">жетсетколумн</span><span class="sxs-lookup"><span data-stu-id="cb03e-291">JetSetColumn</span></span>](./jetsetcolumn-function.md)  
[<span data-ttu-id="cb03e-292">жетупдате</span><span class="sxs-lookup"><span data-stu-id="cb03e-292">JetUpdate</span></span>](./jetupdate-function.md)
