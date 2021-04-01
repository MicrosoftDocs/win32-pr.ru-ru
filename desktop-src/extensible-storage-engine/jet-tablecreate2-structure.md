---
description: 'Дополнительные сведения: структура JET_TABLECREATE2'
title: Структура JET_TABLECREATE2
TOCTitle: JET_TABLECREATE2 Structure
ms:assetid: 2029e684-0d10-44e7-8033-d9cdbdffd7a4
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269203(v=EXCHG.10)
ms:contentKeyID: 32765506
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
ms.openlocfilehash: d7ce983d393954c0d82f0d4e43108ff845d31571
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913755"
---
# <a name="jet_tablecreate2-structure"></a><span data-ttu-id="fc26c-103">Структура JET_TABLECREATE2</span><span class="sxs-lookup"><span data-stu-id="fc26c-103">JET_TABLECREATE2 Structure</span></span>


<span data-ttu-id="fc26c-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="fc26c-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_tablecreate2-structure"></a><span data-ttu-id="fc26c-105">Структура JET_TABLECREATE2</span><span class="sxs-lookup"><span data-stu-id="fc26c-105">JET_TABLECREATE2 Structure</span></span>

<span data-ttu-id="fc26c-106">Структура **JET_TABLECREATE2** содержит сведения, необходимые для создания таблицы, заполненной столбцами и индексами в базе данных ESE, которая обозначает функцию обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="fc26c-106">The **JET_TABLECREATE2** structure contains the information that is needed to create a table populated with columns and indexes in an ESE database, and that designates a callback function.</span></span> <span data-ttu-id="fc26c-107">Структура **JET_TABLECREATE2** используется [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md).</span><span class="sxs-lookup"><span data-stu-id="fc26c-107">The **JET_TABLECREATE2** structure is used by [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md).</span></span>

<span data-ttu-id="fc26c-108">**Windows XP:** Структура **JET_TABLECREATE2** появилась в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="fc26c-108">**Windows XP:** The **JET_TABLECREATE2** structure is introduced in Windows XP.</span></span>

```cpp
    typedef struct tagJET_TABLECREATE2 {
      unsigned long cbStruct;
      tchar* szTableName;
      tchar* szTemplateTableName;
      unsigned long ulPages;
      unsigned long ulDensity;
      JET_COLUMNCREATE* rgcolumncreate;
      unsigned long cColumns;
      JET_INDEXCREATE* rgindexcreate;
      unsigned long cIndexes;
      tchar* szCallback;
      JET_CBTYP cbtyp;
      JET_GRBIT grbit;
      JET_TABLEID tableid;
      unsigned long cCreated;
    } JET_TABLECREATE2;
```

### <a name="members"></a><span data-ttu-id="fc26c-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="fc26c-109">Members</span></span>

<span data-ttu-id="fc26c-110">**кбструкт**</span><span class="sxs-lookup"><span data-stu-id="fc26c-110">**cbStruct**</span></span>

<span data-ttu-id="fc26c-111">Размер этой структуры в байтах (для будущего расширения).</span><span class="sxs-lookup"><span data-stu-id="fc26c-111">The size of this structure in bytes (for future expansion).</span></span> <span data-ttu-id="fc26c-112">Он должен иметь значение sizeof (JET_TABLECREATE2) в байтах.</span><span class="sxs-lookup"><span data-stu-id="fc26c-112">It must be set to sizeof( JET_TABLECREATE2 ) in bytes.</span></span>

<span data-ttu-id="fc26c-113">**сзтабленаме**</span><span class="sxs-lookup"><span data-stu-id="fc26c-113">**szTableName**</span></span>

<span data-ttu-id="fc26c-114">Имя создаваемой таблицы.</span><span class="sxs-lookup"><span data-stu-id="fc26c-114">The name of table to create.</span></span>

<span data-ttu-id="fc26c-115">Имя должно соответствовать следующим условиям:</span><span class="sxs-lookup"><span data-stu-id="fc26c-115">The name must use meet the following conditions:</span></span>

  - <span data-ttu-id="fc26c-116">Иметь значение меньше JET_cbNameMost, не включая завершающее значение NULL.</span><span class="sxs-lookup"><span data-stu-id="fc26c-116">Have a value less than JET_cbNameMost, not including the terminating NULL.</span></span>

<!-- end list -->

  - <span data-ttu-id="fc26c-117">Состоит из следующего набора символов: от 0 до 9, от A до Z, от a до z и всех остальных знаков препинания, за исключением восклицательного знака ( \! ), запятой (,), открывающей квадратной скобки ( \[ ) и закрывающей квадратной скобки ( \] ), то есть символов ASCII 0x20, 0x22 через 0x2D, 0x2F через 0x5A, 0x5c и 0x5d до 0x7F.</span><span class="sxs-lookup"><span data-stu-id="fc26c-117">Consist of the following set of characters: 0 through 9, A through Z, a through z, and all other punctuation except for exclamation point (\!), comma (,), opening bracket (\[), and closing bracket (\]), that is, ASCII characters 0x20, 0x22 through 0x2d, 0x2f through 0x5a, 0x5c, and 0x5d through 0x7f.</span></span>

<!-- end list -->

  - <span data-ttu-id="fc26c-118">Не должно начинаться с пробела.</span><span class="sxs-lookup"><span data-stu-id="fc26c-118">Not begin with a space.</span></span>

<!-- end list -->

  - <span data-ttu-id="fc26c-119">Состоит по крайней мере один символ, не являющийся пробелом.</span><span class="sxs-lookup"><span data-stu-id="fc26c-119">Consist of at least one non-space character.</span></span>

<span data-ttu-id="fc26c-120">**сзтемплатетабленаме**</span><span class="sxs-lookup"><span data-stu-id="fc26c-120">**szTemplateTableName**</span></span>

<span data-ttu-id="fc26c-121">Имя уже существующей таблицы, из которой наследуются базовые DDL (язык описания данных).</span><span class="sxs-lookup"><span data-stu-id="fc26c-121">The name of an already-existing table from which to inherit base DDL (Data Definition Language).</span></span> <span data-ttu-id="fc26c-122">Использование таблицы шаблонов позволяет легко создавать множество таблиц с одинаковыми столбцами и индексами.</span><span class="sxs-lookup"><span data-stu-id="fc26c-122">Using a template table allows easy creation of many tables with identical columns and indexes.</span></span>

<span data-ttu-id="fc26c-123">**улпажес**</span><span class="sxs-lookup"><span data-stu-id="fc26c-123">**ulPages**</span></span>

<span data-ttu-id="fc26c-124">Начальное число страниц базы данных, выделяемых для таблицы.</span><span class="sxs-lookup"><span data-stu-id="fc26c-124">The initial number of database pages to allocate for the table.</span></span> <span data-ttu-id="fc26c-125">Указание числа больше единицы может сократить фрагментацию, если в эту таблицу вставлено много строк.</span><span class="sxs-lookup"><span data-stu-id="fc26c-125">Specifying a number larger than one can reduce fragmentation if many rows are inserted into this table.</span></span>

<span data-ttu-id="fc26c-126">**улденсити**</span><span class="sxs-lookup"><span data-stu-id="fc26c-126">**ulDensity**</span></span>

<span data-ttu-id="fc26c-127">Плотность таблицы в процентных точках.</span><span class="sxs-lookup"><span data-stu-id="fc26c-127">The table density, in percentage points.</span></span> <span data-ttu-id="fc26c-128">Число должно быть либо 0, либо находиться в диапазоне от 20 до 100.</span><span class="sxs-lookup"><span data-stu-id="fc26c-128">The number must be either 0 or in the range of 20 through 100.</span></span> <span data-ttu-id="fc26c-129">Передача значения 0 означает, что должно использоваться значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fc26c-129">Passing 0 means that the default value should be used.</span></span> <span data-ttu-id="fc26c-130">Значение по умолчанию — 80.</span><span class="sxs-lookup"><span data-stu-id="fc26c-130">The default is 80.</span></span>

<span data-ttu-id="fc26c-131">**ргколумнкреате**</span><span class="sxs-lookup"><span data-stu-id="fc26c-131">**rgcolumncreate**</span></span>

<span data-ttu-id="fc26c-132">Массив структур [JET_COLUMNCREATE](./jet-columncreate-structure.md) , каждый из которых соответствует столбцу, создаваемому в новой таблице.</span><span class="sxs-lookup"><span data-stu-id="fc26c-132">An array of [JET_COLUMNCREATE](./jet-columncreate-structure.md) structures, each of which corresponds to a column to be created in the new table.</span></span>

<span data-ttu-id="fc26c-133">**кколумнс**</span><span class="sxs-lookup"><span data-stu-id="fc26c-133">**cColumns**</span></span>

<span data-ttu-id="fc26c-134">число элементов [JET_COLUMNCREATE](./jet-columncreate-structure.md) в **ргколумнкреате**.</span><span class="sxs-lookup"><span data-stu-id="fc26c-134">the number of [JET_COLUMNCREATE](./jet-columncreate-structure.md) elements in **rgcolumncreate**.</span></span>

<span data-ttu-id="fc26c-135">**ргиндекскреате**</span><span class="sxs-lookup"><span data-stu-id="fc26c-135">**rgindexcreate**</span></span>

<span data-ttu-id="fc26c-136">Массив структур [JET_INDEXCREATE](./jet-indexcreate-structure.md) , каждый из которых соответствует индексу, создаваемому в новой таблице.</span><span class="sxs-lookup"><span data-stu-id="fc26c-136">An array of [JET_INDEXCREATE](./jet-indexcreate-structure.md) structures, each of which corresponds to an index to be created in the new table.</span></span>

<span data-ttu-id="fc26c-137">**Циндексес**</span><span class="sxs-lookup"><span data-stu-id="fc26c-137">**cIndexes**</span></span>

<span data-ttu-id="fc26c-138">Число элементов [JET_INDEXCREATE](./jet-indexcreate-structure.md) в **ргиндекскреате**.</span><span class="sxs-lookup"><span data-stu-id="fc26c-138">The number of [JET_INDEXCREATE](./jet-indexcreate-structure.md) elements in **rgindexcreate**.</span></span>

<span data-ttu-id="fc26c-139">**сзкаллбакк**</span><span class="sxs-lookup"><span data-stu-id="fc26c-139">**szCallback**</span></span>

<span data-ttu-id="fc26c-140">Функция, которая вызывается во время определенных событий.</span><span class="sxs-lookup"><span data-stu-id="fc26c-140">The function that gets called during certain events.</span></span> <span data-ttu-id="fc26c-141">**кбтип** определяет, когда будет вызвана функция обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="fc26c-141">**cbtyp** determines when the callback function will be called.</span></span>

<span data-ttu-id="fc26c-142">Формат **сзкаллбакк** должен быть " \! функция модуля", например "Альфа \! -версия" — бета-функция в модуле с именем "Alpha".</span><span class="sxs-lookup"><span data-stu-id="fc26c-142">The format of **szCallback** must be "module\!function"—for example, "alpha\!beta" refers to the beta function in the module named "alpha".</span></span> <span data-ttu-id="fc26c-143">Прототип функции должен соответствовать [JET_CALLBACK](./jet-callback-callback-function.md).</span><span class="sxs-lookup"><span data-stu-id="fc26c-143">The prototype of the function must match [JET_CALLBACK](./jet-callback-callback-function.md).</span></span> <span data-ttu-id="fc26c-144">Дополнительные сведения см. в разделе [JET_CALLBACK](./jet-callback-callback-function.md).</span><span class="sxs-lookup"><span data-stu-id="fc26c-144">For more information, see [JET_CALLBACK](./jet-callback-callback-function.md).</span></span>

<span data-ttu-id="fc26c-145">**кбтип**</span><span class="sxs-lookup"><span data-stu-id="fc26c-145">**cbtyp**</span></span>

<span data-ttu-id="fc26c-146">Описывает тип функции обратного вызова, обозначенной **сзкаллбакк**.</span><span class="sxs-lookup"><span data-stu-id="fc26c-146">Describes the type of callback function designated by **szCallback**.</span></span> <span data-ttu-id="fc26c-147">Дополнительные сведения см. в разделе [JET_CBTYP](./jet-cbtyp.md).</span><span class="sxs-lookup"><span data-stu-id="fc26c-147">For more information, see [JET_CBTYP](./jet-cbtyp.md).</span></span> <span data-ttu-id="fc26c-148">Это битовое поле состоит из одного или нескольких следующих битов.</span><span class="sxs-lookup"><span data-stu-id="fc26c-148">This bitfield is composed of one or more of the following bits.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fc26c-149">Значение</span><span class="sxs-lookup"><span data-stu-id="fc26c-149">Value</span></span></p></th>
<th><p><span data-ttu-id="fc26c-150">Значение</span><span class="sxs-lookup"><span data-stu-id="fc26c-150">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fc26c-151">JET_cbtypFinalize</span><span class="sxs-lookup"><span data-stu-id="fc26c-151">JET_cbtypFinalize</span></span></p></td>
<td><p><span data-ttu-id="fc26c-152">Функция обратного вызова вызывается, когда столбец, который может быть завершен, имеет нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="fc26c-152">The callback function will be called when a column that can be finalized has gone to zero.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc26c-153">JET_cbtypBeforeInsert</span><span class="sxs-lookup"><span data-stu-id="fc26c-153">JET_cbtypBeforeInsert</span></span></p></td>
<td><p><span data-ttu-id="fc26c-154">Перед вставкой записи будет вызвана функция обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="fc26c-154">The callback function will be called prior to record insertion.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc26c-155">JET_cbtypAfterInsert</span><span class="sxs-lookup"><span data-stu-id="fc26c-155">JET_cbtypAfterInsert</span></span></p></td>
<td><p><span data-ttu-id="fc26c-156">Функция обратного вызова будет вызываться по завершении вставки записи ядром СУБД.</span><span class="sxs-lookup"><span data-stu-id="fc26c-156">The callback function will be called once the database engine has finished inserting a record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc26c-157">JET_cbtypBeforeReplace</span><span class="sxs-lookup"><span data-stu-id="fc26c-157">JET_cbtypBeforeReplace</span></span></p></td>
<td><p><span data-ttu-id="fc26c-158">Функция обратного вызова будет вызвана до изменения записи.</span><span class="sxs-lookup"><span data-stu-id="fc26c-158">The callback function will be called prior to modification of a record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc26c-159">JET_cbtypAfterReplace</span><span class="sxs-lookup"><span data-stu-id="fc26c-159">JET_cbtypAfterReplace</span></span></p></td>
<td><p><span data-ttu-id="fc26c-160">Функция обратного вызова будет вызвана после завершения изменения записи.</span><span class="sxs-lookup"><span data-stu-id="fc26c-160">The callback function will be called after finishing modification of a record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc26c-161">JET_cbtypBeforeDelete</span><span class="sxs-lookup"><span data-stu-id="fc26c-161">JET_cbtypBeforeDelete</span></span></p></td>
<td><p><span data-ttu-id="fc26c-162">Перед удалением записи будет вызвана функция обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="fc26c-162">The callback function will be called prior to deletion of a record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc26c-163">JET_cbtypAfterDelete</span><span class="sxs-lookup"><span data-stu-id="fc26c-163">JET_cbtypAfterDelete</span></span></p></td>
<td><p><span data-ttu-id="fc26c-164">Функция обратного вызова будет вызвана после удаления записи.</span><span class="sxs-lookup"><span data-stu-id="fc26c-164">The callback function will be called after a record has been deleted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc26c-165">JET_cbtypUserDefinedDefaultValue</span><span class="sxs-lookup"><span data-stu-id="fc26c-165">JET_cbtypUserDefinedDefaultValue</span></span></p></td>
<td><p><span data-ttu-id="fc26c-166">Функция обратного вызова будет вызываться для вычисления определяемого пользователем значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fc26c-166">The callback function will be called to calculate a user-defined default.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc26c-167">JET_cbtypOnlineDefragCompleted</span><span class="sxs-lookup"><span data-stu-id="fc26c-167">JET_cbtypOnlineDefragCompleted</span></span></p></td>
<td><p><span data-ttu-id="fc26c-168">Функция обратного вызова будет вызываться после завершения вызова <a href="gg294095(v=exchg.10).md">JetDefragment2</a> .</span><span class="sxs-lookup"><span data-stu-id="fc26c-168">The callback function will be called after a call to <a href="gg294095(v=exchg.10).md">JetDefragment2</a> has completed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc26c-169">JET_cbtypFreeCursorLS</span><span class="sxs-lookup"><span data-stu-id="fc26c-169">JET_cbtypFreeCursorLS</span></span></p></td>
<td><p><span data-ttu-id="fc26c-170">Функция обратного вызова будет вызываться, когда необходимо освободить локальное хранилище, связанное с курсором.</span><span class="sxs-lookup"><span data-stu-id="fc26c-170">The callback function will be called when the local storage that is associated with a cursor must be freed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc26c-171">JET_cbtypFreeTableLS</span><span class="sxs-lookup"><span data-stu-id="fc26c-171">JET_cbtypFreeTableLS</span></span></p></td>
<td><p><span data-ttu-id="fc26c-172">Функция обратного вызова будет вызываться, когда локальное хранилище, связанное с таблицей, должно быть освобождено.</span><span class="sxs-lookup"><span data-stu-id="fc26c-172">The callback function will be called when the local storage that is associated with a table must be freed.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="fc26c-173">**грбит**</span><span class="sxs-lookup"><span data-stu-id="fc26c-173">**grbit**</span></span>

<span data-ttu-id="fc26c-174">Группа битов, содержащая параметры для этого вызова, которые содержат ноль или более следующих значений.</span><span class="sxs-lookup"><span data-stu-id="fc26c-174">A group of bits that contain the options for this call, which include zero or more of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fc26c-175">Значение</span><span class="sxs-lookup"><span data-stu-id="fc26c-175">Value</span></span></p></th>
<th><p><span data-ttu-id="fc26c-176">Значение</span><span class="sxs-lookup"><span data-stu-id="fc26c-176">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fc26c-177">JET_bitTableCreateFixedDDL</span><span class="sxs-lookup"><span data-stu-id="fc26c-177">JET_bitTableCreateFixedDDL</span></span></p></td>
<td><p><span data-ttu-id="fc26c-178">Параметр JET_bitTableCreateFixedDDL предотвращает выполнение DDL-операций в таблице (например, добавление или удаление столбцов).</span><span class="sxs-lookup"><span data-stu-id="fc26c-178">Setting JET_bitTableCreateFixedDDL prevents DDL operations on the table (such as adding or removing columns).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc26c-179">JET_bitTableCreateTemplateTable</span><span class="sxs-lookup"><span data-stu-id="fc26c-179">JET_bitTableCreateTemplateTable</span></span></p></td>
<td><p><span data-ttu-id="fc26c-180">Параметр JET_bitTableCreateTemplateTable приводит к тому, что таблица будет таблицей шаблонов.</span><span class="sxs-lookup"><span data-stu-id="fc26c-180">Setting JET_bitTableCreateTemplateTable causes the table to be a template table.</span></span> <span data-ttu-id="fc26c-181">Новые таблицы могут затем указать имя этой таблицы в качестве таблицы шаблонов.</span><span class="sxs-lookup"><span data-stu-id="fc26c-181">New tables can then specify the name of this table as their template table.</span></span> <span data-ttu-id="fc26c-182">Параметр JET_bitTableCreateTemplateTable подразумевает JET_bitTableCreateFixedDDL.</span><span class="sxs-lookup"><span data-stu-id="fc26c-182">Setting JET_bitTableCreateTemplateTable implies JET_bitTableCreateFixedDDL.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc26c-183">JET_bitTableCreateNoFixedVarColumnsInDerivedTables</span><span class="sxs-lookup"><span data-stu-id="fc26c-183">JET_bitTableCreateNoFixedVarColumnsInDerivedTables</span></span></p></td>
<td><p><span data-ttu-id="fc26c-184">Должен использоваться в сочетании с JET_bitTableCreateTemplateTable.</span><span class="sxs-lookup"><span data-stu-id="fc26c-184">Must be used in conjunction with JET_bitTableCreateTemplateTable.</span></span> <span data-ttu-id="fc26c-185">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="fc26c-185">Deprecated.</span></span> <span data-ttu-id="fc26c-186">Не используется.</span><span class="sxs-lookup"><span data-stu-id="fc26c-186">Do not use.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="fc26c-187">**TableID**</span><span class="sxs-lookup"><span data-stu-id="fc26c-187">**tableid**</span></span>

<span data-ttu-id="fc26c-188">Поле вывода, которое содержит [JET_TABLEID](./jet-tableid.md) новой таблицы, если вызов API выполнен.</span><span class="sxs-lookup"><span data-stu-id="fc26c-188">An output field that holds the [JET_TABLEID](./jet-tableid.md) of the new table if the API call succeeds.</span></span> <span data-ttu-id="fc26c-189">Если вызов API завершается неудачей, значение не определено.</span><span class="sxs-lookup"><span data-stu-id="fc26c-189">If the API call fails, the value is undefined.</span></span>

<span data-ttu-id="fc26c-190">**ккреатед**</span><span class="sxs-lookup"><span data-stu-id="fc26c-190">**cCreated**</span></span>

<span data-ttu-id="fc26c-191">Поле вывода, содержащее количество объектов, создаваемых при успешности вызова API.</span><span class="sxs-lookup"><span data-stu-id="fc26c-191">An output field that contains the count of objects that are created if the API call succeeds.</span></span> <span data-ttu-id="fc26c-192">Если вызов API завершается неудачей, значение не определено.</span><span class="sxs-lookup"><span data-stu-id="fc26c-192">If the API call fails, the value is undefined.</span></span>

<span data-ttu-id="fc26c-193">Число создаваемых объектов равно сумме столбцов, таблиц и индексов, которые были успешно созданы.</span><span class="sxs-lookup"><span data-stu-id="fc26c-193">The count of objects that is created is equal to the sum of columns, tables, and indexes that are successfully created.</span></span>

### <a name="requirements"></a><span data-ttu-id="fc26c-194">Требования</span><span class="sxs-lookup"><span data-stu-id="fc26c-194">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fc26c-195"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="fc26c-195"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="fc26c-196">Требуется Windows Vista или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="fc26c-196">Requires Windows  Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc26c-197"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="fc26c-197"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="fc26c-198">Требуется Windows Server 2008 или Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="fc26c-198">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc26c-199"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="fc26c-199"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="fc26c-200">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="fc26c-200">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc26c-201"><strong>Юникод</strong></span><span class="sxs-lookup"><span data-stu-id="fc26c-201"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="fc26c-202">Реализуется как <strong>JET_TABLECREATE2_W</strong> (Юникод) и <strong>JET_TABLECREATE2_A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="fc26c-202">Implemented as <strong>JET_TABLECREATE2_W</strong> (Unicode) and <strong>JET_TABLECREATE2_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="fc26c-203">См. также:</span><span class="sxs-lookup"><span data-stu-id="fc26c-203">See Also</span></span>

[<span data-ttu-id="fc26c-204">JET_CALLBACK</span><span class="sxs-lookup"><span data-stu-id="fc26c-204">JET_CALLBACK</span></span>](./jet-callback-callback-function.md)  
[<span data-ttu-id="fc26c-205">JET_CBTYP</span><span class="sxs-lookup"><span data-stu-id="fc26c-205">JET_CBTYP</span></span>](./jet-cbtyp.md)  
[<span data-ttu-id="fc26c-206">JET_CONDITIONALCOLUMN</span><span class="sxs-lookup"><span data-stu-id="fc26c-206">JET_CONDITIONALCOLUMN</span></span>](./jet-conditionalcolumn-structure.md)  
[<span data-ttu-id="fc26c-207">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="fc26c-207">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="fc26c-208">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="fc26c-208">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="fc26c-209">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="fc26c-209">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)  
[<span data-ttu-id="fc26c-210">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="fc26c-210">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="fc26c-211">жеткреатетабле</span><span class="sxs-lookup"><span data-stu-id="fc26c-211">JetCreateTable</span></span>](./jetcreatetable-function.md)  
[<span data-ttu-id="fc26c-212">жеткреатетаблеколумниндекс</span><span class="sxs-lookup"><span data-stu-id="fc26c-212">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="fc26c-213">JetCreateTableColumnIndex2</span><span class="sxs-lookup"><span data-stu-id="fc26c-213">JetCreateTableColumnIndex2</span></span>](./jetcreatetablecolumnindex2-function.md)  
[<span data-ttu-id="fc26c-214">JetDefragment2</span><span class="sxs-lookup"><span data-stu-id="fc26c-214">JetDefragment2</span></span>](./jetdefragment2-function.md)
