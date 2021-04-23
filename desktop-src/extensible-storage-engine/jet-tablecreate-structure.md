---
description: 'Дополнительные сведения: структура JET_TABLECREATE'
title: Структура JET_TABLECREATE
TOCTitle: JET_TABLECREATE Structure
ms:assetid: ff06325c-d61e-4239-b2d4-868f557f5f76
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294146(v=EXCHG.10)
ms:contentKeyID: 32765760
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
ms.openlocfilehash: f96b73daaf446023a7fe3a5729dcb1c90b5f14e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143552"
---
# <a name="jet_tablecreate-structure"></a><span data-ttu-id="8cd3f-103">Структура JET_TABLECREATE</span><span class="sxs-lookup"><span data-stu-id="8cd3f-103">JET_TABLECREATE Structure</span></span>


<span data-ttu-id="8cd3f-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="8cd3f-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_tablecreate-structure"></a><span data-ttu-id="8cd3f-105">Структура JET_TABLECREATE</span><span class="sxs-lookup"><span data-stu-id="8cd3f-105">JET_TABLECREATE Structure</span></span>

<span data-ttu-id="8cd3f-106">Структура **JET_TABLECREATE** содержит сведения, необходимые для создания таблицы, заполненной столбцами и индексами в базе данных ESE.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-106">The **JET_TABLECREATE** structure contains the information that is necessary to create a table populated with columns and indexes in an ESE database.</span></span> <span data-ttu-id="8cd3f-107">Структура **JET_TABLECREATE** используется [жеткреатетаблеколумниндекс](./jetcreatetablecolumnindex-function.md)</span><span class="sxs-lookup"><span data-stu-id="8cd3f-107">The **JET_TABLECREATE** structure is used by [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)</span></span>

```cpp
    typedef struct tagJET_TABLECREATE {
      unsigned long cbStruct;
      tchar* szTableName;
      tchar* szTemplateTableName;
      unsigned long ulPages;
      unsigned long ulDensity;
      JET_COLUMNCREATE* rgcolumncreate;
      unsigned long cColumns;
      JET_INDEXCREATE* rgindexcreate;
      unsigned long cIndexes;
      JET_GRBIT grbit;
      JET_TABLEID tableid;
      unsigned long cCreated;
    } JET_TABLECREATE;
```

### <a name="members"></a><span data-ttu-id="8cd3f-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="8cd3f-108">Members</span></span>

<span data-ttu-id="8cd3f-109">**кбструкт**</span><span class="sxs-lookup"><span data-stu-id="8cd3f-109">**cbStruct**</span></span>

<span data-ttu-id="8cd3f-110">Размер этой структуры в байтах (для будущего расширения).</span><span class="sxs-lookup"><span data-stu-id="8cd3f-110">The size of this structure in bytes (for future expansion).</span></span> <span data-ttu-id="8cd3f-111">Он должен иметь значение sizeof (JET_TABLECREATE) в байтах.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-111">It must be set to sizeof( JET_TABLECREATE ) in bytes.</span></span>

<span data-ttu-id="8cd3f-112">**сзтабленаме**</span><span class="sxs-lookup"><span data-stu-id="8cd3f-112">**szTableName**</span></span>

<span data-ttu-id="8cd3f-113">Имя создаваемой таблицы.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-113">The name of the table to create.</span></span>

<span data-ttu-id="8cd3f-114">Имя должно соответствовать следующим условиям:</span><span class="sxs-lookup"><span data-stu-id="8cd3f-114">The name must use meet the following conditions:</span></span>

  - <span data-ttu-id="8cd3f-115">Иметь значение меньше JET_cbNameMost, не включая завершающее значение NULL.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-115">Have a value less than JET_cbNameMost, not including the terminating NULL.</span></span>

<!-- end list -->

  - <span data-ttu-id="8cd3f-116">Состоит из следующего набора символов: от 0 до 9, от A до Z, от a до z и всех остальных знаков препинания, за исключением восклицательного знака ( \! ), запятой (,), открывающей квадратной скобки ( \[ ) и закрывающей квадратной скобки ( \] ), то есть символов ASCII 0x20, 0x22 через 0x2D, 0x2F через 0x5A, 0x5c и 0x5d до 0x7F.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-116">Consist of the following set of characters: 0 through 9, A through Z, a through z, and all other punctuation except for exclamation point (\!), comma (,), opening bracket (\[), and closing bracket (\]), that is, ASCII characters 0x20, 0x22 through 0x2d, 0x2f through 0x5a, 0x5c, and 0x5d through 0x7f.</span></span>

<!-- end list -->

  - <span data-ttu-id="8cd3f-117">Не должно начинаться с пробела.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-117">Not begin with a space.</span></span>

<!-- end list -->

  - <span data-ttu-id="8cd3f-118">Состоит по крайней мере один символ, не являющийся пробелом.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-118">Consist of at least one non-space character.</span></span>

<span data-ttu-id="8cd3f-119">**сзтемплатетабленаме**</span><span class="sxs-lookup"><span data-stu-id="8cd3f-119">**szTemplateTableName**</span></span>

<span data-ttu-id="8cd3f-120">Имя уже существующей таблицы, из которой наследуются базовые DDL (язык описания данных).</span><span class="sxs-lookup"><span data-stu-id="8cd3f-120">The name of an already-existing table from which to inherit base DDL (Data Definition Language).</span></span> <span data-ttu-id="8cd3f-121">Использование таблицы шаблонов позволяет легко создавать множество таблиц с одинаковыми столбцами и индексами.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-121">Use of a template table allows for the easy creation of many tables with identical columns and indexes.</span></span>

<span data-ttu-id="8cd3f-122">**улпажес**</span><span class="sxs-lookup"><span data-stu-id="8cd3f-122">**ulPages**</span></span>

<span data-ttu-id="8cd3f-123">Начальное число страниц базы данных, выделяемых для таблицы.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-123">The initial number of database pages to allocate for the table.</span></span> <span data-ttu-id="8cd3f-124">Указание числа больше единицы может сократить фрагментацию, если в эту таблицу вставлено много строк.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-124">Specifying a number larger than one can reduce fragmentation if many rows are inserted into this table.</span></span>

<span data-ttu-id="8cd3f-125">**улденсити**</span><span class="sxs-lookup"><span data-stu-id="8cd3f-125">**ulDensity**</span></span>

<span data-ttu-id="8cd3f-126">Плотность таблицы в процентных точках.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-126">The table density, in percentage points.</span></span> <span data-ttu-id="8cd3f-127">Число должно быть либо 0, либо находиться в диапазоне от 20 до 100.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-127">The number must be either 0 or in the range of 20 through 100.</span></span> <span data-ttu-id="8cd3f-128">Передача значения 0 означает, что должно использоваться значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-128">Passing 0 means that the default value should be used.</span></span> <span data-ttu-id="8cd3f-129">Значение по умолчанию — 80.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-129">The default is 80.</span></span>

<span data-ttu-id="8cd3f-130">**ргколумнкреате**</span><span class="sxs-lookup"><span data-stu-id="8cd3f-130">**rgcolumncreate**</span></span>

<span data-ttu-id="8cd3f-131">Массив структур [JET_COLUMNCREATE](./jet-columncreate-structure.md) , каждый из которых соответствует столбцу, создаваемому в новой таблице.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-131">An array of [JET_COLUMNCREATE](./jet-columncreate-structure.md) structures, each of which corresponds to a column to be created in the new table.</span></span>

<span data-ttu-id="8cd3f-132">**кколумнс**</span><span class="sxs-lookup"><span data-stu-id="8cd3f-132">**cColumns**</span></span>

<span data-ttu-id="8cd3f-133">Число элементов [JET_COLUMNCREATE](./jet-columncreate-structure.md) в **ргколумнкреате**.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-133">The number of [JET_COLUMNCREATE](./jet-columncreate-structure.md) elements in **rgcolumncreate**.</span></span>

<span data-ttu-id="8cd3f-134">**ргиндекскреате**</span><span class="sxs-lookup"><span data-stu-id="8cd3f-134">**rgindexcreate**</span></span>

<span data-ttu-id="8cd3f-135">Массив структур [JET_INDEXCREATE](./jet-indexcreate-structure.md) , каждый из которых соответствует индексу, создаваемому в новой таблице.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-135">An array of [JET_INDEXCREATE](./jet-indexcreate-structure.md) structures, each of which corresponds to an index to be created in the new table.</span></span>

<span data-ttu-id="8cd3f-136">**Циндексес**</span><span class="sxs-lookup"><span data-stu-id="8cd3f-136">**cIndexes**</span></span>

<span data-ttu-id="8cd3f-137">Число элементов [JET_INDEXCREATE](./jet-indexcreate-structure.md) в **ргиндекскреате**.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-137">The number of [JET_INDEXCREATE](./jet-indexcreate-structure.md) elements in **rgindexcreate**.</span></span>

<span data-ttu-id="8cd3f-138">**грбит**</span><span class="sxs-lookup"><span data-stu-id="8cd3f-138">**grbit**</span></span>

<span data-ttu-id="8cd3f-139">Группа битов, содержащая параметры для этого вызова, которые содержат ноль или более следующих значений.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-139">A group of bits that contain the options for this call, which include zero or more of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8cd3f-140">Значение</span><span class="sxs-lookup"><span data-stu-id="8cd3f-140">Value</span></span></p></th>
<th><p><span data-ttu-id="8cd3f-141">Значение</span><span class="sxs-lookup"><span data-stu-id="8cd3f-141">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8cd3f-142">JET_bitTableCreateFixedDDL</span><span class="sxs-lookup"><span data-stu-id="8cd3f-142">JET_bitTableCreateFixedDDL</span></span></p></td>
<td><p><span data-ttu-id="8cd3f-143">Параметр JET_bitTableCreateFixedDDL предотвращает выполнение DDL-операций в таблице (например, добавление или удаление столбцов).</span><span class="sxs-lookup"><span data-stu-id="8cd3f-143">Setting JET_bitTableCreateFixedDDL prevents DDL operations on the table (such as adding or removing columns).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8cd3f-144">JET_bitTableCreateTemplateTable</span><span class="sxs-lookup"><span data-stu-id="8cd3f-144">JET_bitTableCreateTemplateTable</span></span></p></td>
<td><p><span data-ttu-id="8cd3f-145">Параметр JET_bitTableCreateTemplateTable приводит к тому, что таблица будет таблицей шаблонов.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-145">Setting JET_bitTableCreateTemplateTable causes the table to be a template table.</span></span> <span data-ttu-id="8cd3f-146">Новые таблицы могут затем указать имя этой таблицы в качестве таблицы шаблонов.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-146">New tables can then specify the name of this table as their template table.</span></span> <span data-ttu-id="8cd3f-147">Параметр JET_bitTableCreateTemplateTable подразумевает JET_bitTableCreateFixedDDL.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-147">Setting JET_bitTableCreateTemplateTable implies JET_bitTableCreateFixedDDL.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8cd3f-148">JET_bitTableCreateNoFixedVarColumnsInDerivedTables</span><span class="sxs-lookup"><span data-stu-id="8cd3f-148">JET_bitTableCreateNoFixedVarColumnsInDerivedTables</span></span></p></td>
<td><p><span data-ttu-id="8cd3f-149">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-149">Deprecated.</span></span> <span data-ttu-id="8cd3f-150">Не используется.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-150">Do not use.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8cd3f-151">**TableID**</span><span class="sxs-lookup"><span data-stu-id="8cd3f-151">**tableid**</span></span>

<span data-ttu-id="8cd3f-152">Поле вывода, которое содержит [JET_TABLEID](./jet-tableid.md) новой таблицы, если вызов API выполнен.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-152">An output field that holds the [JET_TABLEID](./jet-tableid.md) of the new table if the API call succeeds.</span></span> <span data-ttu-id="8cd3f-153">Если вызов API завершается неудачей, значение не определено.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-153">If the API call fails, the value is undefined.</span></span>

<span data-ttu-id="8cd3f-154">**ккреатед**</span><span class="sxs-lookup"><span data-stu-id="8cd3f-154">**cCreated**</span></span>

<span data-ttu-id="8cd3f-155">Поле вывода, содержащее количество объектов, созданных при успешности вызова API.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-155">An output field that contains the count of objects created if the API call succeeds.</span></span> <span data-ttu-id="8cd3f-156">Если вызов API завершается неудачей, значение не определено.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-156">If the API call fails, the value is undefined.</span></span>

<span data-ttu-id="8cd3f-157">Количество создаваемых объектов равно сумме столбцов, таблиц и индексов, которые были успешно созданы.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-157">The count of objects that are created is equal to the sum of columns, tables, and indexes that are successfully created.</span></span>

### <a name="requirements"></a><span data-ttu-id="8cd3f-158">Требования</span><span class="sxs-lookup"><span data-stu-id="8cd3f-158">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8cd3f-159"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="8cd3f-159"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="8cd3f-160">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-160">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8cd3f-161"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="8cd3f-161"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="8cd3f-162">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-162">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8cd3f-163"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="8cd3f-163"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="8cd3f-164">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="8cd3f-164">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8cd3f-165"><strong>Юникод</strong></span><span class="sxs-lookup"><span data-stu-id="8cd3f-165"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="8cd3f-166">Реализуется как <strong>JET_TABLECREATE_W</strong> (Юникод) и <strong>JET_TABLECREATE_A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="8cd3f-166">Implemented as <strong>JET_TABLECREATE_W</strong> (Unicode) and <strong>JET_TABLECREATE_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="8cd3f-167">См. также:</span><span class="sxs-lookup"><span data-stu-id="8cd3f-167">See Also</span></span>

[<span data-ttu-id="8cd3f-168">JET_CALLBACK</span><span class="sxs-lookup"><span data-stu-id="8cd3f-168">JET_CALLBACK</span></span>](./jet-callback-callback-function.md)  
[<span data-ttu-id="8cd3f-169">JET_CBTYP</span><span class="sxs-lookup"><span data-stu-id="8cd3f-169">JET_CBTYP</span></span>](./jet-cbtyp.md)  
[<span data-ttu-id="8cd3f-170">JET_CONDITIONALCOLUMN</span><span class="sxs-lookup"><span data-stu-id="8cd3f-170">JET_CONDITIONALCOLUMN</span></span>](./jet-conditionalcolumn-structure.md)  
[<span data-ttu-id="8cd3f-171">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="8cd3f-171">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="8cd3f-172">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="8cd3f-172">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="8cd3f-173">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="8cd3f-173">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="8cd3f-174">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="8cd3f-174">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)  
[<span data-ttu-id="8cd3f-175">жеткреатетабле</span><span class="sxs-lookup"><span data-stu-id="8cd3f-175">JetCreateTable</span></span>](./jetcreatetable-function.md)  
[<span data-ttu-id="8cd3f-176">жеткреатетаблеколумниндекс</span><span class="sxs-lookup"><span data-stu-id="8cd3f-176">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="8cd3f-177">JetCreateTableColumnIndex2</span><span class="sxs-lookup"><span data-stu-id="8cd3f-177">JetCreateTableColumnIndex2</span></span>](./jetcreatetablecolumnindex2-function.md)
