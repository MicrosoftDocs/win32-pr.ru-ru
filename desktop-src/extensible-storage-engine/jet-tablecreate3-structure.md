---
description: 'Дополнительные сведения: структура JET_TABLECREATE3'
title: Структура JET_TABLECREATE3
TOCTitle: JET_TABLECREATE3 Structure
ms:assetid: 61909569-e704-494b-a56d-b64d1a2ee157
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269264(v=EXCHG.10)
ms:contentKeyID: 32765566
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
ms.openlocfilehash: 587649b592f2b0d213a481c3bfbecc723240e486
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701362"
---
# <a name="jet_tablecreate3-structure"></a><span data-ttu-id="79d9a-103">Структура JET_TABLECREATE3</span><span class="sxs-lookup"><span data-stu-id="79d9a-103">JET_TABLECREATE3 Structure</span></span>


<span data-ttu-id="79d9a-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="79d9a-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="79d9a-105">Структура **JET_TABLECREATE3** содержит сведения, необходимые для создания таблицы, заполненной столбцами и индексами в базе данных ESE, которая обозначает функцию обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="79d9a-105">The **JET_TABLECREATE3** structure contains the information that is needed to create a table populated with columns and indexes in an Extensible Storage Engine (ESE) database, and that designates a callback function.</span></span> <span data-ttu-id="79d9a-106">Структура **JET_TABLECREATE3** используется функцией [JetCreateTableColumnIndex3](./jetcreatetablecolumnindex3-function.md) .</span><span class="sxs-lookup"><span data-stu-id="79d9a-106">The **JET_TABLECREATE3** structure is used by the [JetCreateTableColumnIndex3](./jetcreatetablecolumnindex3-function.md) function.</span></span>

<span data-ttu-id="79d9a-107">Структура **JET_TABLECREATE3** была введена в операционной системе Windows 7.</span><span class="sxs-lookup"><span data-stu-id="79d9a-107">The **JET_TABLECREATE3** structure was introduced in the Windows 7 operating system.</span></span>

``` cpp
typedef struct tagJET_TABLECREATE3 {
  unsigned long cbStruct;
  tchar* szTableName;
  tchar* szTemplateTableName;
  unsigned long ulPages;
  unsigned long ulDensity;
  JET_COLUMNCREATE* rgcolumncreate;
  unsigned long cColumns;
    JET_INDEXCREATE2* rgindexcreate;
  unsigned long cIndexes;
  tchar* szCallback;
  JET_CBTYP cbtyp;
  JET_GRBIT grbit;
  JET_TABLEID tableid;
  un  JET_GRBIT grbit;
  JET_SPACEHINTS* pSeqSpacehints;
  JET_SPACEHINTS* pLVSpacehints;
  unsigned long cbSeparateLV;
  JET_TABLEID tableid;
  unsigned long cCreated;
} JET_TABLECREATE3;>
```

### <a name="members"></a><span data-ttu-id="79d9a-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="79d9a-108">Members</span></span>

<span data-ttu-id="79d9a-109">**кбструкт**</span><span class="sxs-lookup"><span data-stu-id="79d9a-109">**cbStruct**</span></span>

<span data-ttu-id="79d9a-110">Размер этой структуры в байтах (для будущего расширения).</span><span class="sxs-lookup"><span data-stu-id="79d9a-110">The size of this structure in bytes (for future expansion).</span></span> <span data-ttu-id="79d9a-111">Он должен иметь значение sizeof (JET_TABLECREATE3) в байтах.</span><span class="sxs-lookup"><span data-stu-id="79d9a-111">It must be set to sizeof( JET_TABLECREATE3 ) in bytes.</span></span>

<span data-ttu-id="79d9a-112">**сзтабленаме**</span><span class="sxs-lookup"><span data-stu-id="79d9a-112">**szTableName**</span></span>

<span data-ttu-id="79d9a-113">Имя создаваемой таблицы.</span><span class="sxs-lookup"><span data-stu-id="79d9a-113">The name of the table to create.</span></span>

<span data-ttu-id="79d9a-114">Имя должно соответствовать следующим условиям.</span><span class="sxs-lookup"><span data-stu-id="79d9a-114">The name must meet the following conditions:</span></span>

  - <span data-ttu-id="79d9a-115">Значение должно быть меньше JET_cbNameMost, не включая завершающее значение null.</span><span class="sxs-lookup"><span data-stu-id="79d9a-115">It must have a value that is less than JET_cbNameMost, not including the terminating null.</span></span>

  - <span data-ttu-id="79d9a-116">Он должен состоять из следующего набора символов: от 0 до 9, от A до Z, от a до z и всех остальных знаков препинания, кроме восклицательного знака ( \! ), запятой (,), открывающей квадратной скобки ( \[ ) и закрывающей скобки ( \] );</span><span class="sxs-lookup"><span data-stu-id="79d9a-116">It must consist of the following set of characters: 0 through 9, A through Z, a through z, and all other punctuation except for exclamation point (\!), comma (,), opening bracket (\[), and closing bracket (\]); that is, ASCII characters 0x20, 0x22 through 0x2d, 0x2f through 0x5a, 0x5c, and 0x5d through 0x7f.</span></span>

  - <span data-ttu-id="79d9a-117">Оно не должно начинаться с пробела.</span><span class="sxs-lookup"><span data-stu-id="79d9a-117">It must not begin with a space.</span></span>

  - <span data-ttu-id="79d9a-118">Оно должно состоять по крайней мере из одного символа, не являющегося пробелом.</span><span class="sxs-lookup"><span data-stu-id="79d9a-118">It must consist of at least one non-space character.</span></span>

<span data-ttu-id="79d9a-119">**сзтемплатетабленаме**</span><span class="sxs-lookup"><span data-stu-id="79d9a-119">**szTemplateTableName**</span></span>

<span data-ttu-id="79d9a-120">Имя существующей таблицы, из которой наследуется базовый язык описания данных (DDL).</span><span class="sxs-lookup"><span data-stu-id="79d9a-120">The name of an existing table from which to inherit the base data definition language (DDL).</span></span> <span data-ttu-id="79d9a-121">Использование таблицы шаблонов позволяет легко создавать множество таблиц с одинаковыми столбцами и индексами.</span><span class="sxs-lookup"><span data-stu-id="79d9a-121">Use of a template table allows for the easy creation of many tables with identical columns and indexes.</span></span>

<span data-ttu-id="79d9a-122">**улпажес**</span><span class="sxs-lookup"><span data-stu-id="79d9a-122">**ulPages**</span></span>

<span data-ttu-id="79d9a-123">Начальное число страниц базы данных, выделяемых для таблицы.</span><span class="sxs-lookup"><span data-stu-id="79d9a-123">The initial number of database pages to allocate for the table.</span></span> <span data-ttu-id="79d9a-124">Указание числа больше единицы может сократить фрагментацию, если в эту таблицу вставлено много строк.</span><span class="sxs-lookup"><span data-stu-id="79d9a-124">Specifying a number larger than one can reduce fragmentation if many rows are inserted into this table.</span></span>

<span data-ttu-id="79d9a-125">**улденсити**</span><span class="sxs-lookup"><span data-stu-id="79d9a-125">**ulDensity**</span></span>

<span data-ttu-id="79d9a-126">Плотность таблицы в процентных точках.</span><span class="sxs-lookup"><span data-stu-id="79d9a-126">The table density, in percentage points.</span></span> <span data-ttu-id="79d9a-127">Число должно быть либо 0, либо находиться в диапазоне от 20 до 100.</span><span class="sxs-lookup"><span data-stu-id="79d9a-127">The number must be either 0 or in the range of 20 through 100.</span></span> <span data-ttu-id="79d9a-128">Передача значения 0 означает, что должно использоваться значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="79d9a-128">Passing 0 means that the default value should be used.</span></span> <span data-ttu-id="79d9a-129">Значение по умолчанию равно 80.</span><span class="sxs-lookup"><span data-stu-id="79d9a-129">The default value is 80.</span></span>

<span data-ttu-id="79d9a-130">**ргколумнкреате**</span><span class="sxs-lookup"><span data-stu-id="79d9a-130">**rgcolumncreate**</span></span>

<span data-ttu-id="79d9a-131">Массив структур [JET_COLUMNCREATE](./jet-columncreate-structure.md) , каждый из которых соответствует столбцу, создаваемому в новой таблице.</span><span class="sxs-lookup"><span data-stu-id="79d9a-131">An array of [JET_COLUMNCREATE](./jet-columncreate-structure.md) structures, each of which corresponds to a column to be created in the new table.</span></span>

<span data-ttu-id="79d9a-132">**кколумнс**</span><span class="sxs-lookup"><span data-stu-id="79d9a-132">**cColumns**</span></span>

<span data-ttu-id="79d9a-133">Число элементов [JET_COLUMNCREATE](./jet-columncreate-structure.md) в параметре *ргколумнкреате* .</span><span class="sxs-lookup"><span data-stu-id="79d9a-133">The number of [JET_COLUMNCREATE](./jet-columncreate-structure.md) elements in the *rgcolumncreate* parameter.</span></span>

<span data-ttu-id="79d9a-134">**ргиндекскреате**</span><span class="sxs-lookup"><span data-stu-id="79d9a-134">**rgindexcreate**</span></span>

<span data-ttu-id="79d9a-135">Массив структур [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) , каждый из которых соответствует индексу, создаваемому в новой таблице.</span><span class="sxs-lookup"><span data-stu-id="79d9a-135">An array of [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) structures, each of which corresponds to an index to be created in the new table.</span></span>

<span data-ttu-id="79d9a-136">**Циндексес**</span><span class="sxs-lookup"><span data-stu-id="79d9a-136">**cIndexes**</span></span>

<span data-ttu-id="79d9a-137">Число элементов [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) в параметре *ргиндекскреате* .</span><span class="sxs-lookup"><span data-stu-id="79d9a-137">The number of [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) elements in the *rgindexcreate* parameter.</span></span>

<span data-ttu-id="79d9a-138">**сзкаллбакк**</span><span class="sxs-lookup"><span data-stu-id="79d9a-138">**szCallback**</span></span>

<span data-ttu-id="79d9a-139">Функция, которая вызывается во время определенных событий.</span><span class="sxs-lookup"><span data-stu-id="79d9a-139">The function that gets called during certain events.</span></span> <span data-ttu-id="79d9a-140">**кбтип** определяет, когда будет вызвана функция обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="79d9a-140">**cbtyp** determines when the callback function will be called.</span></span>

<span data-ttu-id="79d9a-141">Формат **сзкаллбакк** должен быть " \! функция модуля", например "Альфа \! -версия" — бета-функция в модуле с именем "Alpha".</span><span class="sxs-lookup"><span data-stu-id="79d9a-141">The format of **szCallback** must be "module\!function" — for example, "alpha\!beta" refers to the beta function in the module named "alpha".</span></span>

<span data-ttu-id="79d9a-142">Прототип функции должен соответствовать функции обратного вызова [JET_CALLBACK](./jet-callback-callback-function.md) .</span><span class="sxs-lookup"><span data-stu-id="79d9a-142">The prototype of the function must match the [JET_CALLBACK](./jet-callback-callback-function.md) callback function.</span></span>

<span data-ttu-id="79d9a-143">**кбтип**</span><span class="sxs-lookup"><span data-stu-id="79d9a-143">**cbtyp**</span></span>

<span data-ttu-id="79d9a-144">Описывает тип функции обратного вызова, обозначенной **сзкаллбакк**.</span><span class="sxs-lookup"><span data-stu-id="79d9a-144">Describes the type of callback function designated by **szCallback**.</span></span> <span data-ttu-id="79d9a-145">Дополнительные сведения см. в разделе [JET_CBTYP](./jet-cbtyp.md).</span><span class="sxs-lookup"><span data-stu-id="79d9a-145">For more information, see [JET_CBTYP](./jet-cbtyp.md).</span></span>

<span data-ttu-id="79d9a-146">Это битовое значение состоит из одного или нескольких битовых значений, перечисленных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="79d9a-146">This bitfield is composed of one or more of the bit values listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="79d9a-147">Значение</span><span class="sxs-lookup"><span data-stu-id="79d9a-147">Value</span></span></p></th>
<th><p><span data-ttu-id="79d9a-148">Значение</span><span class="sxs-lookup"><span data-stu-id="79d9a-148">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="79d9a-149">JET_cbtypFinalize</span><span class="sxs-lookup"><span data-stu-id="79d9a-149">JET_cbtypFinalize</span></span></p></td>
<td><p><span data-ttu-id="79d9a-150">Функция обратного вызова вызывается, когда столбец, который может быть завершен, имеет нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="79d9a-150">The callback function will be called when a column that can be finalized has gone to zero.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79d9a-151">JET_cbtypBeforeInsert</span><span class="sxs-lookup"><span data-stu-id="79d9a-151">JET_cbtypBeforeInsert</span></span></p></td>
<td><p><span data-ttu-id="79d9a-152">Перед вставкой записи будет вызвана функция обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="79d9a-152">The callback function will be called prior to record insertion.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="79d9a-153">JET_cbtypAfterInsert</span><span class="sxs-lookup"><span data-stu-id="79d9a-153">JET_cbtypAfterInsert</span></span></p></td>
<td><p><span data-ttu-id="79d9a-154">Функция обратного вызова будет вызываться после завершения вставки записи ядром СУБД.</span><span class="sxs-lookup"><span data-stu-id="79d9a-154">The callback function will be called after the database engine has finished inserting a record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79d9a-155">JET_cbtypBeforeReplace</span><span class="sxs-lookup"><span data-stu-id="79d9a-155">JET_cbtypBeforeReplace</span></span></p></td>
<td><p><span data-ttu-id="79d9a-156">Функция обратного вызова будет вызвана до изменения записи.</span><span class="sxs-lookup"><span data-stu-id="79d9a-156">The callback function will be called prior to the modification of a record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="79d9a-157">JET_cbtypAfterReplace</span><span class="sxs-lookup"><span data-stu-id="79d9a-157">JET_cbtypAfterReplace</span></span></p></td>
<td><p><span data-ttu-id="79d9a-158">Функция обратного вызова будет вызвана после завершения изменения записи.</span><span class="sxs-lookup"><span data-stu-id="79d9a-158">The callback function will be called after finishing the modification of a record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79d9a-159">JET_cbtypBeforeDelete</span><span class="sxs-lookup"><span data-stu-id="79d9a-159">JET_cbtypBeforeDelete</span></span></p></td>
<td><p><span data-ttu-id="79d9a-160">Функция обратного вызова будет вызвана до удаления записи.</span><span class="sxs-lookup"><span data-stu-id="79d9a-160">The callback function will be called prior to the deletion of a record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="79d9a-161">JET_cbtypAfterDelete</span><span class="sxs-lookup"><span data-stu-id="79d9a-161">JET_cbtypAfterDelete</span></span></p></td>
<td><p><span data-ttu-id="79d9a-162">Функция обратного вызова будет вызвана после удаления записи.</span><span class="sxs-lookup"><span data-stu-id="79d9a-162">The callback function will be called after a record has been deleted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79d9a-163">JET_cbtypUserDefinedDefaultValue</span><span class="sxs-lookup"><span data-stu-id="79d9a-163">JET_cbtypUserDefinedDefaultValue</span></span></p></td>
<td><p><span data-ttu-id="79d9a-164">Функция обратного вызова будет вызываться для вычисления определяемого пользователем значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="79d9a-164">The callback function will be called to calculate a user-defined default.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="79d9a-165">JET_cbtypFreeCursorLS</span><span class="sxs-lookup"><span data-stu-id="79d9a-165">JET_cbtypFreeCursorLS</span></span></p></td>
<td><p><span data-ttu-id="79d9a-166">Функция обратного вызова будет вызываться, когда необходимо освободить локальное хранилище, связанное с курсором.</span><span class="sxs-lookup"><span data-stu-id="79d9a-166">The callback function will be called when the local storage that is associated with a cursor must be freed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79d9a-167">JET_cbtypFreeTableLS</span><span class="sxs-lookup"><span data-stu-id="79d9a-167">JET_cbtypFreeTableLS</span></span></p></td>
<td><p><span data-ttu-id="79d9a-168">Функция обратного вызова будет вызываться, когда локальное хранилище, связанное с таблицей, должно быть освобождено.</span><span class="sxs-lookup"><span data-stu-id="79d9a-168">The callback function will be called when the local storage that is associated with a table must be freed.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="79d9a-169">**грбит**</span><span class="sxs-lookup"><span data-stu-id="79d9a-169">**grbit**</span></span>

<span data-ttu-id="79d9a-170">Группа битов, содержащая ноль или более значений параметров вызова, перечисленных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="79d9a-170">A group of bits that contains zero or more of the call option values listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="79d9a-171">Значение</span><span class="sxs-lookup"><span data-stu-id="79d9a-171">Value</span></span></p></th>
<th><p><span data-ttu-id="79d9a-172">Значение</span><span class="sxs-lookup"><span data-stu-id="79d9a-172">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="79d9a-173">JET_bitTableCreateFixedDDL</span><span class="sxs-lookup"><span data-stu-id="79d9a-173">JET_bitTableCreateFixedDDL</span></span></p></td>
<td><p><span data-ttu-id="79d9a-174">Предотвращает выполнение DDL-операций в таблице (например, добавление или удаление столбцов).</span><span class="sxs-lookup"><span data-stu-id="79d9a-174">Prevents DDL operations on the table (such as adding or removing columns).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79d9a-175">JET_bitTableCreateTemplateTable</span><span class="sxs-lookup"><span data-stu-id="79d9a-175">JET_bitTableCreateTemplateTable</span></span></p></td>
<td><p><span data-ttu-id="79d9a-176">Приводит к тому, что таблица будет таблицей шаблонов.</span><span class="sxs-lookup"><span data-stu-id="79d9a-176">Causes the table to be a template table.</span></span> <span data-ttu-id="79d9a-177">Новые таблицы могут затем указать имя этой таблицы в качестве таблицы шаблонов.</span><span class="sxs-lookup"><span data-stu-id="79d9a-177">New tables can then specify the name of this table as their template table.</span></span> <span data-ttu-id="79d9a-178">Параметр JET_bitTableCreateTemplateTable подразумевает JET_bitTableCreateFixedDDL.</span><span class="sxs-lookup"><span data-stu-id="79d9a-178">Setting JET_bitTableCreateTemplateTable implies JET_bitTableCreateFixedDDL.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="79d9a-179">JET_bitTableCreateNoFixedVarColumnsInDerivedTables</span><span class="sxs-lookup"><span data-stu-id="79d9a-179">JET_bitTableCreateNoFixedVarColumnsInDerivedTables</span></span></p></td>
<td><p><span data-ttu-id="79d9a-180">Должен использоваться в сочетании с JET_bitTableCreateTemplateTable.</span><span class="sxs-lookup"><span data-stu-id="79d9a-180">Must be used in conjunction with JET_bitTableCreateTemplateTable.</span></span> <span data-ttu-id="79d9a-181">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="79d9a-181">Deprecated.</span></span> <span data-ttu-id="79d9a-182">Не используется.</span><span class="sxs-lookup"><span data-stu-id="79d9a-182">Do not use.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="79d9a-183">**псекспацехинтс**</span><span class="sxs-lookup"><span data-stu-id="79d9a-183">**pSeqSpacehints**</span></span>

<span data-ttu-id="79d9a-184">Указатель на структуру [JET_SPACEHINTS](./jet-spacehints-structure.md) для последовательного индекса по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="79d9a-184">A pointer to a [JET_SPACEHINTS](./jet-spacehints-structure.md) structure for default sequential index.</span></span>

<span data-ttu-id="79d9a-185">**псекспацехинтс** появился в Windows 7.</span><span class="sxs-lookup"><span data-stu-id="79d9a-185">**pSeqSpacehints** was introduced in Windows 7.</span></span>

<span data-ttu-id="79d9a-186">**плвспацехинтс**</span><span class="sxs-lookup"><span data-stu-id="79d9a-186">**pLVSpacehints**</span></span>

<span data-ttu-id="79d9a-187">Указатель на структуру [JET_SPACEHINTS](./jet-spacehints-structure.md) для разделенного дерева длинного значения.</span><span class="sxs-lookup"><span data-stu-id="79d9a-187">A pointer to a [JET_SPACEHINTS](./jet-spacehints-structure.md) structure for a Separated Long Value tree.</span></span>

<span data-ttu-id="79d9a-188">**плвспацехинтс** появился в Windows 7.</span><span class="sxs-lookup"><span data-stu-id="79d9a-188">**pLVSpacehints** was introduced in Windows 7.</span></span>

<span data-ttu-id="79d9a-189">**кбсепарателв**</span><span class="sxs-lookup"><span data-stu-id="79d9a-189">**cbSeparateLV**</span></span>

<span data-ttu-id="79d9a-190">Размер для отделения встроенной функции LV от основной записи.</span><span class="sxs-lookup"><span data-stu-id="79d9a-190">The size to separate an intrinsic LV from the primary record.</span></span> <span data-ttu-id="79d9a-191">Любая структура с длинным значением c для разделенного дерева LV.</span><span class="sxs-lookup"><span data-stu-id="79d9a-191">Any long-value c structure for a Separated LV tree.</span></span> <span data-ttu-id="79d9a-192">Дополнительные сведения см. в разделе NG-value в [JET_SPACEHINTS](./jet-spacehints-structure.md).</span><span class="sxs-lookup"><span data-stu-id="79d9a-192">For more information, see ng-value in [JET_SPACEHINTS](./jet-spacehints-structure.md).</span></span> <span data-ttu-id="79d9a-193">Столбцы с длинными значениями меньше этого значения могут быть разделены, если запись становится слишком большой.</span><span class="sxs-lookup"><span data-stu-id="79d9a-193">Long-value columns smaller than this value may be separated if the record becomes too large.</span></span>

<span data-ttu-id="79d9a-194">**кбсепарателв** появился в Windows 7.</span><span class="sxs-lookup"><span data-stu-id="79d9a-194">**cbSeparateLV** was introduced in Windows 7.</span></span>

<span data-ttu-id="79d9a-195">**TableID**</span><span class="sxs-lookup"><span data-stu-id="79d9a-195">**tableid**</span></span>

<span data-ttu-id="79d9a-196">Поле вывода, которое содержит [JET_TABLEID](./jet-tableid.md) новой таблицы, если вызов API выполнен.</span><span class="sxs-lookup"><span data-stu-id="79d9a-196">An output field that holds the [JET_TABLEID](./jet-tableid.md) of the new table if the API call succeeds.</span></span> <span data-ttu-id="79d9a-197">Если вызов API завершается неудачей, значение не определено.</span><span class="sxs-lookup"><span data-stu-id="79d9a-197">If the API call fails, the value is undefined.</span></span> <span data-ttu-id="79d9a-198">Эта таблица открыта только для использования.</span><span class="sxs-lookup"><span data-stu-id="79d9a-198">This table is opened exclusively.</span></span>

<span data-ttu-id="79d9a-199">**ккреатед**</span><span class="sxs-lookup"><span data-stu-id="79d9a-199">**cCreated**</span></span>

<span data-ttu-id="79d9a-200">Поле вывода, содержащее количество объектов, создаваемых при успешности вызова API.</span><span class="sxs-lookup"><span data-stu-id="79d9a-200">An output field that contains the count of objects that are created if the API call succeeds.</span></span> <span data-ttu-id="79d9a-201">Если вызов API завершается неудачей, значение не определено.</span><span class="sxs-lookup"><span data-stu-id="79d9a-201">If the API call fails, the value is undefined.</span></span>

<span data-ttu-id="79d9a-202">Количество создаваемых объектов равно сумме столбцов, таблиц и индексов, которые были успешно созданы.</span><span class="sxs-lookup"><span data-stu-id="79d9a-202">The count of objects that are created is equal to the sum of columns, tables, and indexes that are successfully created.</span></span>

### <a name="requirements"></a><span data-ttu-id="79d9a-203">Требования</span><span class="sxs-lookup"><span data-stu-id="79d9a-203">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="79d9a-204"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="79d9a-204"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="79d9a-205">Требуется Windows Vista или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="79d9a-205">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79d9a-206"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="79d9a-206"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="79d9a-207">Требуется Windows Server 2008 или Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="79d9a-207">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="79d9a-208"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="79d9a-208"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="79d9a-209">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="79d9a-209">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79d9a-210"><strong>Юникод</strong></span><span class="sxs-lookup"><span data-stu-id="79d9a-210"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="79d9a-211">Реализуется как <strong>JET_TABLECREATE3_W</strong> (Юникод) и <strong>JET_TABLECREATE3_A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="79d9a-211">Implemented as <strong>JET_TABLECREATE3_W</strong> (Unicode) and <strong>JET_TABLECREATE3_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="79d9a-212">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="79d9a-212">See also</span></span>

[<span data-ttu-id="79d9a-213">JET_CALLBACK</span><span class="sxs-lookup"><span data-stu-id="79d9a-213">JET_CALLBACK</span></span>](./jet-callback-callback-function.md)  
[<span data-ttu-id="79d9a-214">JET_CBTYP</span><span class="sxs-lookup"><span data-stu-id="79d9a-214">JET_CBTYP</span></span>](./jet-cbtyp.md)  
[<span data-ttu-id="79d9a-215">JET_CONDITIONALCOLUMN</span><span class="sxs-lookup"><span data-stu-id="79d9a-215">JET_CONDITIONALCOLUMN</span></span>](./jet-conditionalcolumn-structure.md)  
[<span data-ttu-id="79d9a-216">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="79d9a-216">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="79d9a-217">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="79d9a-217">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="79d9a-218">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="79d9a-218">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)  
[<span data-ttu-id="79d9a-219">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="79d9a-219">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="79d9a-220">жеткреатетабле</span><span class="sxs-lookup"><span data-stu-id="79d9a-220">JetCreateTable</span></span>](./jetcreatetable-function.md)  
[<span data-ttu-id="79d9a-221">жеткреатетаблеколумниндекс</span><span class="sxs-lookup"><span data-stu-id="79d9a-221">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="79d9a-222">JetCreateTableColumnIndex2</span><span class="sxs-lookup"><span data-stu-id="79d9a-222">JetCreateTableColumnIndex2</span></span>](./jetcreatetablecolumnindex2-function.md)  
[<span data-ttu-id="79d9a-223">JetDefragment2</span><span class="sxs-lookup"><span data-stu-id="79d9a-223">JetDefragment2</span></span>](./jetdefragment2-function.md)
