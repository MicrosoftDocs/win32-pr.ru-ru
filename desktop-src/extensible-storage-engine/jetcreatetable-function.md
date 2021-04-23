---
description: Дополнительные сведения о функции Жеткреатетабле
title: Функция JetCreateTable
TOCTitle: JetCreateTable Function
ms:assetid: 28455b8b-0000-4bd5-a3ca-e1ef0446ee07
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269210(v=EXCHG.10)
ms:contentKeyID: 32765513
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateTableW
- JetCreateTable
- JetCreateTableA
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6f385cfd668af934bfde2669277db7ed048a1fa8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105713072"
---
# <a name="jetcreatetable-function"></a><span data-ttu-id="75835-103">Функция JetCreateTable</span><span class="sxs-lookup"><span data-stu-id="75835-103">JetCreateTable Function</span></span>


<span data-ttu-id="75835-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="75835-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetcreatetable-function"></a><span data-ttu-id="75835-105">Функция JetCreateTable</span><span class="sxs-lookup"><span data-stu-id="75835-105">JetCreateTable Function</span></span>

<span data-ttu-id="75835-106">Функция **жеткреатетабле** создает пустую таблицу в базе данных ESE.</span><span class="sxs-lookup"><span data-stu-id="75835-106">The **JetCreateTable** function creates an empty table in an ESE database.</span></span>

```cpp
    JET_ERR JET_API JetCreateTable(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          const tchar* szTableName,
      __in          unsigned long lPages,
      __in          unsigned long lDensity,
      __out         JET_TABLEID* ptableid
    );
```

### <a name="parameters"></a><span data-ttu-id="75835-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="75835-107">Parameters</span></span>

<span data-ttu-id="75835-108">*сесид*</span><span class="sxs-lookup"><span data-stu-id="75835-108">*sesid*</span></span>

<span data-ttu-id="75835-109">Используемый контекст сеанса базы данных.</span><span class="sxs-lookup"><span data-stu-id="75835-109">The database session context to use.</span></span>

<span data-ttu-id="75835-110">*DBID*</span><span class="sxs-lookup"><span data-stu-id="75835-110">*dbid*</span></span>

<span data-ttu-id="75835-111">Используемый идентификатор базы данных.</span><span class="sxs-lookup"><span data-stu-id="75835-111">The database identifier to use.</span></span>

<span data-ttu-id="75835-112">*сзтабленаме*</span><span class="sxs-lookup"><span data-stu-id="75835-112">*szTableName*</span></span>

<span data-ttu-id="75835-113">Имя создаваемого индекса.</span><span class="sxs-lookup"><span data-stu-id="75835-113">The name of the index to create.</span></span>

<span data-ttu-id="75835-114">Имя должно быть отформатировано в соответствии со следующими правилами:</span><span class="sxs-lookup"><span data-stu-id="75835-114">The name must be formatted according to the following rules:</span></span>

  - <span data-ttu-id="75835-115">Должно быть меньше JET_cbNameMost, не включая завершающее значение NULL.</span><span class="sxs-lookup"><span data-stu-id="75835-115">Be less than JET_cbNameMost, not including the terminating NULL.</span></span>

  - <span data-ttu-id="75835-116">Должен состоять из следующего набора символов: от 0 до 9, от A до Z, от a до z и всех остальных знаков препинания, кроме " \! "</span><span class="sxs-lookup"><span data-stu-id="75835-116">Be made of the following set of characters: 0 through 9, A through Z, a through z, and all other punctuation except for "\!"</span></span> <span data-ttu-id="75835-117">(восклицательный знак), "," (запятая), " \[ " (открывающая скобка) и " \] " (закрывающая скобка), т. е. символы ASCII 0x20, 0x22 до 0x2D, 0x2F через 0x5A, 0x5c, 0x5d до 0x7F.</span><span class="sxs-lookup"><span data-stu-id="75835-117">(exclamation point), "," (comma), "\[" (opening bracket), and "\]" (closing bracket) — that is, ASCII characters 0x20, 0x22 through 0x2d, 0x2f through 0x5a, 0x5c, 0x5d through 0x7f.</span></span>

  - <span data-ttu-id="75835-118">Не должно начинаться с пробела.</span><span class="sxs-lookup"><span data-stu-id="75835-118">Not begin with a space.</span></span>

  - <span data-ttu-id="75835-119">Состоять по крайней мере из одного символа, не являющегося пробелом.</span><span class="sxs-lookup"><span data-stu-id="75835-119">Be made of at least one non-space character.</span></span>

<span data-ttu-id="75835-120">*лпажес*</span><span class="sxs-lookup"><span data-stu-id="75835-120">*lPages*</span></span>

<span data-ttu-id="75835-121">Начальное число страниц базы данных, выделяемых для таблицы.</span><span class="sxs-lookup"><span data-stu-id="75835-121">The initial number of database pages to allocate for the table.</span></span> <span data-ttu-id="75835-122">Указание числа больше единицы может сократить фрагментацию, если в эту таблицу вставлено много строк.</span><span class="sxs-lookup"><span data-stu-id="75835-122">Specifying a number larger than one can reduce fragmentation if many rows are inserted into this table.</span></span>

<span data-ttu-id="75835-123">*лденсити*</span><span class="sxs-lookup"><span data-stu-id="75835-123">*lDensity*</span></span>

<span data-ttu-id="75835-124">Плотность таблицы в процентных точках.</span><span class="sxs-lookup"><span data-stu-id="75835-124">The table density, in percentage points.</span></span> <span data-ttu-id="75835-125">Число должно быть либо 0, либо находиться в диапазоне от 20 до 100.</span><span class="sxs-lookup"><span data-stu-id="75835-125">The number must be either 0 or in the range of 20 through 100.</span></span> <span data-ttu-id="75835-126">Передача значения 0 означает, что должно использоваться значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="75835-126">Passing 0 means that the default value should be used.</span></span> <span data-ttu-id="75835-127">Значение по умолчанию — 80.</span><span class="sxs-lookup"><span data-stu-id="75835-127">The default is 80.</span></span>

<span data-ttu-id="75835-128">*pTableID*</span><span class="sxs-lookup"><span data-stu-id="75835-128">*ptableid*</span></span>

<span data-ttu-id="75835-129">При успешном выполнении в этом поле возвращается идентификатор таблицы.</span><span class="sxs-lookup"><span data-stu-id="75835-129">On success, the table identifier is returned in this field.</span></span> <span data-ttu-id="75835-130">Значение не определено, если API не возвращает JET_errSuccess.</span><span class="sxs-lookup"><span data-stu-id="75835-130">The value is undefined if the API does not return JET_errSuccess.</span></span>

### <a name="return-value"></a><span data-ttu-id="75835-131">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="75835-131">Return Value</span></span>

<span data-ttu-id="75835-132">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="75835-132">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="75835-133">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="75835-133">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="75835-134">Код возврата</span><span class="sxs-lookup"><span data-stu-id="75835-134">Return code</span></span></p></th>
<th><p><span data-ttu-id="75835-135">Описание</span><span class="sxs-lookup"><span data-stu-id="75835-135">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="75835-136">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="75835-136">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="75835-137">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="75835-137">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75835-138">JET_errCallbackNotResolved</span><span class="sxs-lookup"><span data-stu-id="75835-138">JET_errCallbackNotResolved</span></span></p></td>
<td><p><span data-ttu-id="75835-139">Не удалось разрешить функцию обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="75835-139">The callback function could not be resolved.</span></span> <span data-ttu-id="75835-140">Возможно, Библиотека DLL не найдена или не найдена функция в библиотеке DLL.</span><span class="sxs-lookup"><span data-stu-id="75835-140">The DLL might not have been found, or the function in the DLL might not have been found.</span></span> <span data-ttu-id="75835-141">Если ведение журнала включено, в журнале событий будут представлены дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="75835-141">With sufficient logging enabled, the event log will provide more details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75835-142">JET_errCannotIndex</span><span class="sxs-lookup"><span data-stu-id="75835-142">JET_errCannotIndex</span></span></p></td>
<td><p><span data-ttu-id="75835-143">Предпринята попытка индексирования по столбцу с использованием типа "условно-Update" или "SLV" (Обратите внимание, что столбцы SLV устарели).</span><span class="sxs-lookup"><span data-stu-id="75835-143">An attempt was made to index over an escrow-update or SLV column (note that SLV columns are deprecated).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75835-144">JET_errCannotNestDDL</span><span class="sxs-lookup"><span data-stu-id="75835-144">JET_errCannotNestDDL</span></span></p></td>
<td><p><span data-ttu-id="75835-145">Если птаблекреате- &gt; грбит указывает JET_bitTableCreateTemplateTable, но птаблекреате- &gt; сзтемплатетабленаме имеет значение null.</span><span class="sxs-lookup"><span data-stu-id="75835-145">If ptablecreate-&gt;grbit specifies JET_bitTableCreateTemplateTable, but ptablecreate-&gt;szTemplateTableName is set to NULL.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75835-146">JET_errColumnDuplicate</span><span class="sxs-lookup"><span data-stu-id="75835-146">JET_errColumnDuplicate</span></span></p></td>
<td><p><span data-ttu-id="75835-147">Столбец уже существует.</span><span class="sxs-lookup"><span data-stu-id="75835-147">A column already exists.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75835-148">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="75835-148">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="75835-149">Предпринята попытка индексировать несуществующий столбец.</span><span class="sxs-lookup"><span data-stu-id="75835-149">An attempt was made to index over a non-existent column.</span></span> <span data-ttu-id="75835-150">Эта ошибка также может возникнуть при попытке условного индексирования по несуществующему столбцу.</span><span class="sxs-lookup"><span data-stu-id="75835-150">Attempting to conditionally index over a non-existent column can also produce this error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75835-151">JET_errColumnRedundant</span><span class="sxs-lookup"><span data-stu-id="75835-151">JET_errColumnRedundant</span></span></p></td>
<td><p><span data-ttu-id="75835-152">Была предпринята попытка добавить избыточный столбец.</span><span class="sxs-lookup"><span data-stu-id="75835-152">An attempt was made to add a redundant column.</span></span> <span data-ttu-id="75835-153">Не должно быть более одного столбца автоинкремента и не более одного столбца версий для каждой таблицы.</span><span class="sxs-lookup"><span data-stu-id="75835-153">There should be no more than one autoincrement column, and no more than one version column per table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75835-154">JET_errDensityInvalid</span><span class="sxs-lookup"><span data-stu-id="75835-154">JET_errDensityInvalid</span></span></p></td>
<td><p><span data-ttu-id="75835-155">В элементе <em>улденсити</em> в структуре <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> или <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> передана недопустимая плотность.</span><span class="sxs-lookup"><span data-stu-id="75835-155">An invalid density was passed in the <em>ulDensity</em> member in the <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> or <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75835-156">JET_errDDLNotInheritable</span><span class="sxs-lookup"><span data-stu-id="75835-156">JET_errDDLNotInheritable</span></span></p></td>
<td><p><span data-ttu-id="75835-157">Означает, что таблица, указанная в элементе <strong>сзтемплатетабленаме</strong> структуры <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> , не была помечена как таблица шаблона (т. е. в таблице не был установлен JET_bitTableCreateTemplateTable).</span><span class="sxs-lookup"><span data-stu-id="75835-157">Signifies that the table named in the <strong>szTemplateTableName</strong> member of the <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> structure was not a marked as a template table (that is, that table did not have JET_bitTableCreateTemplateTable set).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75835-158">JET_errIndexDuplicate</span><span class="sxs-lookup"><span data-stu-id="75835-158">JET_errIndexDuplicate</span></span></p></td>
<td><p><span data-ttu-id="75835-159">Предпринята попытка определить два одинаковых индекса.</span><span class="sxs-lookup"><span data-stu-id="75835-159">An attempt was made to define two identical indexes.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75835-160">JET_errIndexHasPrimary</span><span class="sxs-lookup"><span data-stu-id="75835-160">JET_errIndexHasPrimary</span></span></p></td>
<td><p><span data-ttu-id="75835-161">Предпринята попытка указать более одного первичного индекса для таблицы.</span><span class="sxs-lookup"><span data-stu-id="75835-161">An attempt was made to specify more than one primary index for a table.</span></span> <span data-ttu-id="75835-162">У таблицы должен быть ровно один первичный индекс.</span><span class="sxs-lookup"><span data-stu-id="75835-162">A table must have exactly one primary index.</span></span> <span data-ttu-id="75835-163">Если первичный индекс не указан, ядро СУБД будет прозрачно создавать его.</span><span class="sxs-lookup"><span data-stu-id="75835-163">If no primary index is specified, the database engine will transparently create one.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75835-164">JET_errIndexInvalidDef</span><span class="sxs-lookup"><span data-stu-id="75835-164">JET_errIndexInvalidDef</span></span></p></td>
<td><p><span data-ttu-id="75835-165">Указано недопустимое определение индекса.</span><span class="sxs-lookup"><span data-stu-id="75835-165">An invalid index definition was specified.</span></span> <span data-ttu-id="75835-166">Ниже приведены некоторые возможные причины получения этой ошибки:</span><span class="sxs-lookup"><span data-stu-id="75835-166">Some of the possible reasons for receiving this error are:</span></span></p>
<ul>
<li><p><span data-ttu-id="75835-167">Первичный индекс является условным (т. е. элемент <strong>грбит</strong> структуры <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> имеет JET_bitIndexPrimary Set, а член <strong>ккондитионалколумн</strong> структуры <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> больше нуля).</span><span class="sxs-lookup"><span data-stu-id="75835-167">A primary index is conditional (that is, the <strong>grbit</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure has JET_bitIndexPrimary set, and <strong>cConditionalColumn</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure is greater than zero).</span></span></p></li>
<li><p><span data-ttu-id="75835-168">Windows Server 2003 и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="75835-168">Windows Server 2003 and later.</span></span> <span data-ttu-id="75835-169">Попытка создать индекс кортежа с ограничениями кортежей, но без передачи элемента <strong>птуплелимитс</strong> в структуре <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> (т. е. элемент <strong>грбит</strong> структуры <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> имеет JET_bitIndexTupleLimits установлен, но указатель <strong>птуплелимитс</strong> имеет значение null).</span><span class="sxs-lookup"><span data-stu-id="75835-169">Attempting to create a tuple index with tuple limits, but without passing the <strong>ptuplelimits</strong> member in the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure (that is, the <strong>grbit</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure has JET_bitIndexTupleLimits set, but the <strong>ptuplelimits</strong> pointer is NULL).</span></span></p></li>
<li><p><span data-ttu-id="75835-170">Передача недопустимого определения ключа в элемент <strong>сзкэй</strong> структуры <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</span><span class="sxs-lookup"><span data-stu-id="75835-170">Passing in an invalid key definition in the <strong>szKey</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure.</span></span> <span data-ttu-id="75835-171">Описание допустимых определений см. в разделе <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</span><span class="sxs-lookup"><span data-stu-id="75835-171">See <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> for a discussion of valid definitions.</span></span></p></li>
<li><p><span data-ttu-id="75835-172">Установка для элемента <strong>кбварсегмак</strong> в <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> значение больше JET_cbPrimaryKeyMost (для первичного индекса) или больше JET_cbSecondaryKeyMost (для вторичного индекса).</span><span class="sxs-lookup"><span data-stu-id="75835-172">Setting the <strong>cbVarSegMac</strong> member in <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> to be greater than JET_cbPrimaryKeyMost (for a primary index) or greater than JET_cbSecondaryKeyMost (for a secondary index).</span></span></p></li>
<li><p><span data-ttu-id="75835-173">Передача недопустимого сочетания для определяемого пользователем индекса в Юникоде (одна из которых имеет бит JET_bitIndexUnicode, заданный в элементе <strong>грбит</strong> в <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>).</span><span class="sxs-lookup"><span data-stu-id="75835-173">Passing an invalid combination for a user-defined Unicode index (one which has the JET_bitIndexUnicode bit set in the <strong>grbit</strong> member of <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>).</span></span> <span data-ttu-id="75835-174">Некоторые распространенные причины: элемент <strong>пидксуникоде</strong> структуры <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> имеет значение null, или код LCID, указанный в структуре <strong>пидксуникоде</strong> , является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="75835-174">Some common causes include the <strong>pidxunicode</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure is NULL, or the LCID specified in the <strong>pidxunicode</strong> structure is invalid.</span></span></p></li>
<li><p><span data-ttu-id="75835-175">Указание столбца с несколькими значениями для первичного индекса.</span><span class="sxs-lookup"><span data-stu-id="75835-175">Specifying a multi-valued column for a primary index.</span></span></p></li>
<li><p><span data-ttu-id="75835-176">Попытка индексировать слишком много условных столбцов.</span><span class="sxs-lookup"><span data-stu-id="75835-176">Trying to index too many conditional columns.</span></span> <span data-ttu-id="75835-177">Элемент <strong>ккондитионалколумн</strong> структуры <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> не должен быть больше JET_ccolKeyMost.</span><span class="sxs-lookup"><span data-stu-id="75835-177">The <strong>cConditionalColumn</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure must not be greater than JET_ccolKeyMost.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75835-178">JET_errIndexTuplesInvalidLimits</span><span class="sxs-lookup"><span data-stu-id="75835-178">JET_errIndexTuplesInvalidLimits</span></span></p></td>
<td><p><span data-ttu-id="75835-179">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="75835-179">Windows XP and later.</span></span> <span data-ttu-id="75835-180">Указана структура <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> , а ее ограничения не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="75835-180">A <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure was specified, and its limits are not supported.</span></span> <span data-ttu-id="75835-181">См. раздел "Примечания" структуры <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> .</span><span class="sxs-lookup"><span data-stu-id="75835-181">See the remarks section of the <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75835-182">JET_errIndexTuplesNonUniqueOnly</span><span class="sxs-lookup"><span data-stu-id="75835-182">JET_errIndexTuplesNonUniqueOnly</span></span></p></td>
<td><p><span data-ttu-id="75835-183">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="75835-183">Windows XP and later.</span></span> <span data-ttu-id="75835-184">Индекс кортежа не может быть уникальным (т. е. элемент <em>грбит</em> структуры <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> не должен иметь одновременно JET_bitIndexPrimary и JET_bitIndexUnique).</span><span class="sxs-lookup"><span data-stu-id="75835-184">A tuple index cannot be unique (that is, the <em>grbit</em> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure must not have both JET_bitIndexPrimary and JET_bitIndexUnique set).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75835-185">JET_errIndexTuplesOneColumnOnly</span><span class="sxs-lookup"><span data-stu-id="75835-185">JET_errIndexTuplesOneColumnOnly</span></span></p></td>
<td><p><span data-ttu-id="75835-186">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="75835-186">Windows XP and later.</span></span> <span data-ttu-id="75835-187">Индекс кортежа может находиться только в одном столбце (т. е. Если элемент <strong>грбит</strong> структуры <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> JET_bitIndexTuples задан, а элемент <strong>сзкэй</strong> структуры <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> указывает более одного столбца).</span><span class="sxs-lookup"><span data-stu-id="75835-187">A tuple index can only be over a single column (that is, if the <strong>grbit</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure has JET_bitIndexTuples set, and the <strong>szKey</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure specifies more than one column).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75835-188">JET_errIndexTuplesSecondaryIndexOnly</span><span class="sxs-lookup"><span data-stu-id="75835-188">JET_errIndexTuplesSecondaryIndexOnly</span></span></p></td>
<td><p><span data-ttu-id="75835-189">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="75835-189">Windows XP and later.</span></span> <span data-ttu-id="75835-190">Индекс кортежа не может быть первичным индексом (т. е. элемент <strong>грбит</strong> структуры <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> не должен иметь одновременно JET_bitIndexPrimary и JET_bitIndexTuples).</span><span class="sxs-lookup"><span data-stu-id="75835-190">A tuple index cannot be a primary index (that is, the <strong>grbit</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure must not have both JET_bitIndexPrimary and JET_bitIndexTuples set).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75835-191">JET_errIndexTuplesVarSegMacNotAllowed</span><span class="sxs-lookup"><span data-stu-id="75835-191">JET_errIndexTuplesVarSegMacNotAllowed</span></span></p></td>
<td><p><span data-ttu-id="75835-192">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="75835-192">Windows XP and later.</span></span> <span data-ttu-id="75835-193">Индекс кортежа не позволяет установить элемент <strong>кбварсегмак</strong> структуры <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</span><span class="sxs-lookup"><span data-stu-id="75835-193">A tuple index does not allow the <strong>cbVarSegMac</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure to be set.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75835-194">JET_errIndexTuplesTextColumnsOnly</span><span class="sxs-lookup"><span data-stu-id="75835-194">JET_errIndexTuplesTextColumnsOnly</span></span></p></td>
<td><p><span data-ttu-id="75835-195">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="75835-195">Windows XP and later.</span></span> <span data-ttu-id="75835-196">Индекс кортежа может находиться только в тексте или столбце Юникода.</span><span class="sxs-lookup"><span data-stu-id="75835-196">A tuple index can only be on a text or Unicode column.</span></span> <span data-ttu-id="75835-197">Попытка индексировать другие столбцы (например, двоичные столбцы) приведет к JET_errIndexTuplesTextColumnsOnly.</span><span class="sxs-lookup"><span data-stu-id="75835-197">An attempt to index other columns (such as binary columns) will result in JET_errIndexTuplesTextColumnsOnly.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75835-198">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="75835-198">JET_errInTransaction</span></span></p></td>
<td><p><span data-ttu-id="75835-199">Предпринята попытка создать индекс без сведений о версии во время транзакции.</span><span class="sxs-lookup"><span data-stu-id="75835-199">An attempt was made to create an index without version information while in a transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75835-200">JET_errInvalidCodePage</span><span class="sxs-lookup"><span data-stu-id="75835-200">JET_errInvalidCodePage</span></span></p></td>
<td><p><span data-ttu-id="75835-201">Элементу <strong>CP</strong> структуры <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> не задана допустимая кодовая страница.</span><span class="sxs-lookup"><span data-stu-id="75835-201">The <strong>cp</strong> member of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structure was not set to a valid code page.</span></span> <span data-ttu-id="75835-202">Единственными допустимыми значениями для текстовых столбцов являются английский (1252) и Unicode (1200).</span><span class="sxs-lookup"><span data-stu-id="75835-202">The only valid values for text columns are English (1252) and Unicode (1200).</span></span> <span data-ttu-id="75835-203">Значение 0 означает, что будет использоваться по умолчанию (английский, 1252).</span><span class="sxs-lookup"><span data-stu-id="75835-203">A value of 0 means the default will be used (English, 1252).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75835-204">JET_errInvalidColumnType</span><span class="sxs-lookup"><span data-stu-id="75835-204">JET_errInvalidColumnType</span></span></p></td>
<td><p><span data-ttu-id="75835-205">Элементу <strong>колтип</strong> структуры <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> не был задан допустимый тип столбца.</span><span class="sxs-lookup"><span data-stu-id="75835-205">The <strong>coltyp</strong> member of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structure was not set to a valid column type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75835-206">JET_errInvalidCreateIndex</span><span class="sxs-lookup"><span data-stu-id="75835-206">JET_errInvalidCreateIndex</span></span></p></td>
<td><p><span data-ttu-id="75835-207">Некоторые причины этой ошибки могут возникнуть:</span><span class="sxs-lookup"><span data-stu-id="75835-207">Some of the reasons this error may occur:</span></span></p>
<ul>
<li><p><span data-ttu-id="75835-208">Элементу <strong>ргиндекскреате</strong> структуры <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> присвоено значение null.</span><span class="sxs-lookup"><span data-stu-id="75835-208">The <strong>rgindexcreate</strong> member of the <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure was set to NULL.</span></span></p></li>
<li><p><span data-ttu-id="75835-209">Элементу <strong>ргколумнкреате</strong> структуры <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> присвоено значение null.</span><span class="sxs-lookup"><span data-stu-id="75835-209">The <strong>rgcolumncreate</strong> member of the <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure was set to NULL.</span></span></p></li>
<li><p><span data-ttu-id="75835-210">Элементу <strong>кбструкт</strong> структуры <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> не было присвоено допустимое значение.</span><span class="sxs-lookup"><span data-stu-id="75835-210">The <strong>cbStruct</strong> member of a <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure was not set to a valid value.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75835-211">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="75835-211">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="75835-212">В <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> или <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a>указано недопустимое сочетание элементов <strong>грбит</strong> .</span><span class="sxs-lookup"><span data-stu-id="75835-212">An invalid combination of <strong>grbit</strong> members was specified in <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> or <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a>.</span></span></p>
<p><span data-ttu-id="75835-213">Определение индекса недопустимо, так как элемент <strong>грбит</strong> содержит неправильные значения.</span><span class="sxs-lookup"><span data-stu-id="75835-213">The index definition is invalid because the <strong>grbit</strong> member contains inconsistent values.</span></span> <span data-ttu-id="75835-214">Возможные причины:</span><span class="sxs-lookup"><span data-stu-id="75835-214">Some possible reasons are:</span></span></p>
<ul>
<li><p><span data-ttu-id="75835-215">Для первичного индекса задан бит игнорирования (то есть JET_bitIndexPrimary передан с JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull или JET_bitIndexIgnoreFirstNull).</span><span class="sxs-lookup"><span data-stu-id="75835-215">A primary index had an ignore bit specified (that is, JET_bitIndexPrimary was passed with JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull, or JET_bitIndexIgnoreFirstNull).</span></span></p></li>
<li><p><span data-ttu-id="75835-216">Пустой индекс не игнорирует все элементы NULL (т. е. элемент <strong>грбит</strong> структуры <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> JET_bitIndexEmpty установлен, но не имеет JET_bitIndexIgnoreAnyNull).</span><span class="sxs-lookup"><span data-stu-id="75835-216">An empty index does not ignore any NULL members (that is, the <strong>grbit</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure has JET_bitIndexEmpty set, but does not have JET_bitIndexIgnoreAnyNull set).</span></span></p></li>
<li><p><span data-ttu-id="75835-217">Передача структуры <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> с недопустимым элементом <strong>грбит</strong> .</span><span class="sxs-lookup"><span data-stu-id="75835-217">Passing in a <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> structure with an invalid <strong>grbit</strong> member.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75835-218">JET_errInvalidLanguageId</span><span class="sxs-lookup"><span data-stu-id="75835-218">JET_errInvalidLanguageId</span></span></p></td>
<td><p><span data-ttu-id="75835-219">Передан недопустимый код локали (LCID) (либо с помощью элемента <strong>LCID</strong> структуры <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> , на который указывает элемент <strong>пидксуникоде</strong> в структуре <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> , либо с помощью поля <strong>LCID</strong> структуры <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> ).</span><span class="sxs-lookup"><span data-stu-id="75835-219">An invalid Locale ID (LCID) was passed in (either through the <strong>lcid</strong> member of the <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> structure which is pointed to by the <strong>pidxunicode</strong> member in the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure, or through the <strong>lcid</strong> field of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75835-220">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="75835-220">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="75835-221">Указан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="75835-221">An invalid parameter was given.</span></span> <span data-ttu-id="75835-222">Возможные причины:</span><span class="sxs-lookup"><span data-stu-id="75835-222">Some possible reasons are:</span></span></p>
<ul>
<li><p><span data-ttu-id="75835-223">Элемент <strong>ргколумнкреате</strong> структуры <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> имеет значение null.</span><span class="sxs-lookup"><span data-stu-id="75835-223">The <strong>rgcolumncreate</strong> member of the <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure is NULL.</span></span></p></li>
<li><p><span data-ttu-id="75835-224">Элемент <strong>кбструкт</strong> одной из структур <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> , указанных в элементе <strong>ргколумнкреате</strong> структуры <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> , не был задан как sizeof (JET_COLUMNCREATE).</span><span class="sxs-lookup"><span data-stu-id="75835-224">The <strong>cbStruct</strong> member of one of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structures given in the <strong>rgcolumncreate</strong> member of the <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure was not set to sizeof( JET_COLUMNCREATE ).</span></span></p></li>
<li><p><span data-ttu-id="75835-225">Элемент <strong>cbKey</strong> структуры <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> имеет значение 0.</span><span class="sxs-lookup"><span data-stu-id="75835-225">The <strong>cbKey</strong> member of a <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure is set to zero.</span></span></p></li>
<li><p><span data-ttu-id="75835-226">Элементу <strong>кбструкт</strong> структуры <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> не присвоено значение sizeof (JET_INDEXCREATE).</span><span class="sxs-lookup"><span data-stu-id="75835-226">The <strong>cbStruct</strong> member of a <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure is not set to sizeof( JET_INDEXCREATE ).</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75835-227">JET_errRecordTooBig</span><span class="sxs-lookup"><span data-stu-id="75835-227">JET_errRecordTooBig</span></span></p></td>
<td><p><span data-ttu-id="75835-228">Запись слишком велика.</span><span class="sxs-lookup"><span data-stu-id="75835-228">The record is too big.</span></span> <span data-ttu-id="75835-229">Сумма элемента <strong>кбмакс</strong> структуры <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> для всех фиксированных столбцов не должна превышать определенное значение.</span><span class="sxs-lookup"><span data-stu-id="75835-229">The sum of the <strong>cbMax</strong> member of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structure for all fixed columns must not exceed a certain value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75835-230">JET_errTableDuplicate</span><span class="sxs-lookup"><span data-stu-id="75835-230">JET_errTableDuplicate</span></span></p></td>
<td><p><span data-ttu-id="75835-231">Таблица уже существует.</span><span class="sxs-lookup"><span data-stu-id="75835-231">The table already exists.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75835-232">JET_errTooManyColumns</span><span class="sxs-lookup"><span data-stu-id="75835-232">JET_errTooManyColumns</span></span></p></td>
<td><p><span data-ttu-id="75835-233">Предпринята попытка добавить в таблицу слишком много столбцов.</span><span class="sxs-lookup"><span data-stu-id="75835-233">An attempt was made to add too many columns to the table.</span></span> <span data-ttu-id="75835-234">Таблица может содержать не более JET_ccolFixedMost фиксированных столбцов, не более JET_ccolVarMost столбцов переменной длины и не более JET_ccolTaggedMost столбцов с тегами.</span><span class="sxs-lookup"><span data-stu-id="75835-234">A table can have no more than JET_ccolFixedMost fixed columns, no more than JET_ccolVarMost variable-length columns, and no more than JET_ccolTaggedMost tagged columns.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75835-235">JET_errUnicodeTranslationFail</span><span class="sxs-lookup"><span data-stu-id="75835-235">JET_errUnicodeTranslationFail</span></span></p></td>
<td><p><span data-ttu-id="75835-236">Произошла ошибка при попытке нормализовать столбец в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="75835-236">An error occurred attempting to normalize a Unicode column.</span></span> <span data-ttu-id="75835-237">Это может быть вызвано недостатком системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="75835-237">This can be caused by running out of system resources.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="75835-238">Комментарии</span><span class="sxs-lookup"><span data-stu-id="75835-238">Remarks</span></span>

<span data-ttu-id="75835-239">**Жеткреатетабле** создает таблицу, которая не содержит столбцов.</span><span class="sxs-lookup"><span data-stu-id="75835-239">**JetCreateTable** creates a table which does not contain any columns.</span></span> <span data-ttu-id="75835-240">Чтобы добавить столбцы, см. раздел [жетаддколумн](./jetaddcolumn-function.md).</span><span class="sxs-lookup"><span data-stu-id="75835-240">To add columns, see [JetAddColumn](./jetaddcolumn-function.md).</span></span>

<span data-ttu-id="75835-241">Внутренне **жеткреатетабле** вызывает [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md), заполняя структуру [JET_TABLECREATE2](./jet-tablecreate2-structure.md) следующим:</span><span class="sxs-lookup"><span data-stu-id="75835-241">Internally, **JetCreateTable** calls [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md), filling in a [JET_TABLECREATE2](./jet-tablecreate2-structure.md) structure with:</span></span>

  - <span data-ttu-id="75835-242">JET_TABLECREATE2. Кбструкт = sizeof (JET_TABLECREATE2)</span><span class="sxs-lookup"><span data-stu-id="75835-242">JET_TABLECREATE2.cbStruct = sizeof( JET_TABLECREATE2 )</span></span>

  - <span data-ttu-id="75835-243">JET_TABLECREATE2. Сзтабленаме = Сзтабленаме</span><span class="sxs-lookup"><span data-stu-id="75835-243">JET_TABLECREATE2.szTableName = szTableName</span></span>

  - <span data-ttu-id="75835-244">JET_TABLECREATE2. Улпажес = Лпаже</span><span class="sxs-lookup"><span data-stu-id="75835-244">JET_TABLECREATE2.ulPages = lPage</span></span>

  - <span data-ttu-id="75835-245">JET_TABLECREATE2. Улденсити = Лденсити</span><span class="sxs-lookup"><span data-stu-id="75835-245">JET_TABLECREATE2.ulDensity = lDensity</span></span>

  - <span data-ttu-id="75835-246">JET_TABLECREATE2. TableID = JET_tableidNil</span><span class="sxs-lookup"><span data-stu-id="75835-246">JET_TABLECREATE2.tableid = JET_tableidNil</span></span>

<span data-ttu-id="75835-247">Все остальные поля внутренней [JET_TABLECREATE2](./jet-tablecreate2-structure.md) структуры имеют нулевое значение или значение null.</span><span class="sxs-lookup"><span data-stu-id="75835-247">All the other fields of the internal [JET_TABLECREATE2](./jet-tablecreate2-structure.md) structure are set to zero or NULL.</span></span> <span data-ttu-id="75835-248">В выходных данных *pTableID* будет иметь значение JET_TABLECREATE2. TableID.</span><span class="sxs-lookup"><span data-stu-id="75835-248">On output, *ptableid* will be set to JET_TABLECREATE2.tableid.</span></span>

<span data-ttu-id="75835-249">Дополнительные сведения см. в разделе [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md) .</span><span class="sxs-lookup"><span data-stu-id="75835-249">See [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md) for more details.</span></span>

<span data-ttu-id="75835-250">Как и [жетопентабле](./jetopentable-function.md), когда приложение выполняется с использованием возвращенного элемента **tableid** из структуры [JET_TABLECREATE2](./jet-tablecreate2-structure.md) , оно обычно должно быть закрыто с помощью [жетклосетабле](./jetclosetable-function.md).</span><span class="sxs-lookup"><span data-stu-id="75835-250">Like [JetOpenTable](./jetopentable-function.md), when the application is done using the returned **tableid** member from the [JET_TABLECREATE2](./jet-tablecreate2-structure.md) structure, it should usually be closed with [JetCloseTable](./jetclosetable-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="75835-251">Требования</span><span class="sxs-lookup"><span data-stu-id="75835-251">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="75835-252"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="75835-252"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="75835-253">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="75835-253">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75835-254"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="75835-254"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="75835-255">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="75835-255">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75835-256"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="75835-256"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="75835-257">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="75835-257">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75835-258"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="75835-258"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="75835-259">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="75835-259">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75835-260"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="75835-260"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="75835-261">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="75835-261">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75835-262"><strong>Юникод</strong></span><span class="sxs-lookup"><span data-stu-id="75835-262"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="75835-263">Реализуется как <strong>жеткреатетаблев</strong> (Юникод) и <strong>жеткреатетаблеа</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="75835-263">Implemented as <strong>JetCreateTableW</strong> (Unicode) and <strong>JetCreateTableA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="75835-264">См. также:</span><span class="sxs-lookup"><span data-stu-id="75835-264">See Also</span></span>

[<span data-ttu-id="75835-265">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="75835-265">JET_DBID</span></span>](./jet-dbid.md)  
[<span data-ttu-id="75835-266">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="75835-266">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="75835-267">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="75835-267">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="75835-268">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="75835-268">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="75835-269">JET_TABLECREATE2</span><span class="sxs-lookup"><span data-stu-id="75835-269">JET_TABLECREATE2</span></span>](./jet-tablecreate2-structure.md)  
[<span data-ttu-id="75835-270">жетаддколумн</span><span class="sxs-lookup"><span data-stu-id="75835-270">JetAddColumn</span></span>](./jetaddcolumn-function.md)  
[<span data-ttu-id="75835-271">жеткреатетаблеколумниндекс</span><span class="sxs-lookup"><span data-stu-id="75835-271">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="75835-272">JetCreateTableColumnIndex2</span><span class="sxs-lookup"><span data-stu-id="75835-272">JetCreateTableColumnIndex2</span></span>](./jetcreatetablecolumnindex2-function.md)
