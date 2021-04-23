---
description: Дополнительные сведения о функции JetCreateIndex4W
title: Функция JetCreateIndex4W
TOCTitle: JetCreateIndex4W Function
ms:assetid: 968745a2-66ce-4c7f-ab5b-43282adc5313
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835044(v=EXCHG.10)
ms:contentKeyID: 49894666
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetCreateIndex4W
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9a4c7671cbe361b6214552f4c611cd1706c0e48d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712511"
---
# <a name="jetcreateindex4w-function"></a><span data-ttu-id="77bee-103">Функция JetCreateIndex4W</span><span class="sxs-lookup"><span data-stu-id="77bee-103">JetCreateIndex4W Function</span></span>


<span data-ttu-id="77bee-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="77bee-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="77bee-105">Функция **JetCreateIndex4W** создает индексы данных в базе данных подсистемы расширенного хранилища (ESE), которую можно использовать для быстрого поиска конкретных данных.</span><span class="sxs-lookup"><span data-stu-id="77bee-105">The **JetCreateIndex4W** function creates indexes over data in an Extensible Storage Engine (ESE) database, which can be used to locate specific data quickly.</span></span>

<span data-ttu-id="77bee-106">Функция **JetCreateIndex4W** была введена в операционной системе Windows 8.</span><span class="sxs-lookup"><span data-stu-id="77bee-106">The **JetCreateIndex4W** function was introduced in the Windows 8 operating system.</span></span>

``` c++
JET_ERR JET_API JetCreateIndex4W(
  __in          JET_SESID sesid,
  __in          JET_TABLEID tableid,
  __in          JET_INDEXCREATE2* pindexcreate,
  __in          unsigned long cIndexCreate
);
```

### <a name="parameters"></a><span data-ttu-id="77bee-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="77bee-107">Parameters</span></span>

<span data-ttu-id="77bee-108">*сесид*</span><span class="sxs-lookup"><span data-stu-id="77bee-108">*sesid*</span></span>

<span data-ttu-id="77bee-109">Контекст сеанса базы данных, используемый для вызова API.</span><span class="sxs-lookup"><span data-stu-id="77bee-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="77bee-110">*TableID*</span><span class="sxs-lookup"><span data-stu-id="77bee-110">*tableid*</span></span>

<span data-ttu-id="77bee-111">Таблица, в которой будет создан индекс.</span><span class="sxs-lookup"><span data-stu-id="77bee-111">The table on which the index will be created.</span></span>

<span data-ttu-id="77bee-112">*пиндекскреате*</span><span class="sxs-lookup"><span data-stu-id="77bee-112">*pindexcreate*</span></span>

<span data-ttu-id="77bee-113">Массив структур [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) , каждый из которых определяет создаваемый индекс.</span><span class="sxs-lookup"><span data-stu-id="77bee-113">An array of [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) structures, each of which defines an index to be created.</span></span>

<span data-ttu-id="77bee-114">*Циндекскреате*</span><span class="sxs-lookup"><span data-stu-id="77bee-114">*cIndexCreate*</span></span>

<span data-ttu-id="77bee-115">Число элементов в массиве *пиндекскреате* .</span><span class="sxs-lookup"><span data-stu-id="77bee-115">The number of elements in the *pindexcreate* array.</span></span>

### <a name="return-value"></a><span data-ttu-id="77bee-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="77bee-116">Return value</span></span>

<span data-ttu-id="77bee-117">Эта функция возвращает [JET_ERR](./jet-err.md) тип данных с одним из кодов возврата, перечисленных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="77bee-117">This function returns the [JET_ERR](./jet-err.md) data type with one of the return codes listed in the following table.</span></span> <span data-ttu-id="77bee-118">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="77bee-118">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="77bee-119">Код возврата</span><span class="sxs-lookup"><span data-stu-id="77bee-119">Return code</span></span></p></th>
<th><p><span data-ttu-id="77bee-120">Описание</span><span class="sxs-lookup"><span data-stu-id="77bee-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="77bee-121">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="77bee-121">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="77bee-122">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="77bee-122">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77bee-123">JET_errCannotIndex</span><span class="sxs-lookup"><span data-stu-id="77bee-123">JET_errCannotIndex</span></span></p></td>
<td><p><span data-ttu-id="77bee-124">Предпринята попытка индексирования по столбцу с использованием типа "условно-Update" или "SLV" (Обратите внимание, что столбцы SLV устарели).</span><span class="sxs-lookup"><span data-stu-id="77bee-124">An attempt was made to index over an escrow-update or SLV column (note that SLV columns are deprecated).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77bee-125">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="77bee-125">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="77bee-126">Предпринята попытка индексировать несуществующий столбец.</span><span class="sxs-lookup"><span data-stu-id="77bee-126">An attempt was made to index over a nonexistent column.</span></span> <span data-ttu-id="77bee-127">Эта ошибка также может возникнуть при попытке условного индексирования по несуществующему столбцу.</span><span class="sxs-lookup"><span data-stu-id="77bee-127">An attempt to conditionally index over a nonexistent column can also produce this error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77bee-128">JET_errDensityInvalid</span><span class="sxs-lookup"><span data-stu-id="77bee-128">JET_errDensityInvalid</span></span></p></td>
<td><p><span data-ttu-id="77bee-129">Эта ошибка будет возвращена, если элементу <strong>улденсити</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> присвоено число меньше 20 или больше 100.</span><span class="sxs-lookup"><span data-stu-id="77bee-129">This error will be returned if the <strong>ulDensity</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is set to a number less than 20 or greater than 100.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77bee-130">JET_errIndexDuplicate</span><span class="sxs-lookup"><span data-stu-id="77bee-130">JET_errIndexDuplicate</span></span></p></td>
<td><p><span data-ttu-id="77bee-131">Была выполнена попытка определить два одинаковых индекса.</span><span class="sxs-lookup"><span data-stu-id="77bee-131">An attempt to define two identical indexes was made.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77bee-132">JET_errIndexHasPrimary</span><span class="sxs-lookup"><span data-stu-id="77bee-132">JET_errIndexHasPrimary</span></span></p></td>
<td><p><span data-ttu-id="77bee-133">Предпринята попытка указать более одного первичного индекса для таблицы.</span><span class="sxs-lookup"><span data-stu-id="77bee-133">An attempt was made to specify more than one primary index for a table.</span></span> <span data-ttu-id="77bee-134">У таблицы должен быть ровно один первичный индекс.</span><span class="sxs-lookup"><span data-stu-id="77bee-134">A table must have exactly one primary index.</span></span> <span data-ttu-id="77bee-135">Если первичный индекс не указан, ядро СУБД будет прозрачно создавать его.</span><span class="sxs-lookup"><span data-stu-id="77bee-135">If no primary index is specified, the database engine will transparently create one.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77bee-136">JET_errIndexInvalidDef</span><span class="sxs-lookup"><span data-stu-id="77bee-136">JET_errIndexInvalidDef</span></span></p></td>
<td><p><span data-ttu-id="77bee-137">Указано недопустимое определение индекса.</span><span class="sxs-lookup"><span data-stu-id="77bee-137">An invalid index definition was specified.</span></span> <span data-ttu-id="77bee-138">Ниже приведены некоторые возможные причины этой ошибки.</span><span class="sxs-lookup"><span data-stu-id="77bee-138">The following are some possible reasons for this error:</span></span></p>
<ul>
<li><p><span data-ttu-id="77bee-139">Первичный индекс является условным (<strong>грбит</strong> член <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> имеет <strong>JET_bitIndexPrimary</strong> набор, а элемент <strong>ккондитионалколумн</strong> <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> больше нуля).</span><span class="sxs-lookup"><span data-stu-id="77bee-139">A primary index is conditional (<strong>grbit</strong> member of <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> has <strong>JET_bitIndexPrimary</strong> set, and the <strong>cConditionalColumn</strong> member of <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> is greater than zero).</span></span></p></li>
<li><p><span data-ttu-id="77bee-140">Применимо к версиям Windows, начиная с Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="77bee-140">Applies to versions of Windows starting with Windows Server 2003.</span></span> <span data-ttu-id="77bee-141">Предпринята попытка создать индекс кортежа с ограничениями кортежей, но без передачи сведений в элемент <strong>птуплелимитс</strong> в <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> (то есть <em>грбит</em> имеет набор <strong>JET_bitIndexTupleLimits</strong> , но указатель <strong>птуплелимитс</strong> имеет значение null).</span><span class="sxs-lookup"><span data-stu-id="77bee-141">An attempt was made to create a tuple index with tuple limits, but without passing information in the <strong>ptuplelimits</strong> member in <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> (that is, <em>grbit</em> has <strong>JET_bitIndexTupleLimits</strong> set, but the <strong>ptuplelimits</strong> pointer is null).</span></span></p></li>
<li><p><span data-ttu-id="77bee-142">Передача недопустимого определения ключа в элемент <strong>сзкэй</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> .</span><span class="sxs-lookup"><span data-stu-id="77bee-142">Passing in an invalid key definition in the <strong>szKey</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure.</span></span> <span data-ttu-id="77bee-143">Сведения о допустимых определениях см. в разделе <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>.</span><span class="sxs-lookup"><span data-stu-id="77bee-143">For information about valid definitions, see <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>.</span></span></p></li>
<li><p><span data-ttu-id="77bee-144">Установка для элемента <strong>кбварсегмак</strong> в <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> значение больше <strong>JET_cbPrimaryKeyMost</strong> (для первичного индекса) или больше <strong>JET_cbSecondaryKeyMost</strong> (для вторичного индекса).</span><span class="sxs-lookup"><span data-stu-id="77bee-144">Setting the <strong>cbVarSegMac</strong> member in <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> to be greater than <strong>JET_cbPrimaryKeyMost</strong> (for a primary index) or greater than <strong>JET_cbSecondaryKeyMost</strong> (for a secondary index).</span></span></p></li>
<li><p><span data-ttu-id="77bee-145">Передача недопустимого сочетания для определяемого пользователем индекса в Юникоде (одна из которых имеет бит <strong>JET_bitIndexUnicode</strong> , заданный в элементе <strong>грбит</strong> в <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>).</span><span class="sxs-lookup"><span data-stu-id="77bee-145">Passing an invalid combination for a user-defined Unicode index (one which has the <strong>JET_bitIndexUnicode</strong> bit set in the <strong>grbit</strong> member of <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>).</span></span> <span data-ttu-id="77bee-146">Некоторые распространенные причины могут быть вызваны тем, что поле пидксуникоде структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> имеет значение null или код LCID, указанный в структуре пидксуникоде, является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="77bee-146">Some common causes may be that the pidxunicode field of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is null, or the LCID specified in the pidxunicode structure is invalid.</span></span></p></li>
<li><p><span data-ttu-id="77bee-147">Указание многозначного столбца для первичного индекса.</span><span class="sxs-lookup"><span data-stu-id="77bee-147">Specifying a multivalued column for a primary index.</span></span></p></li>
<li><p><span data-ttu-id="77bee-148">Попытка индексировать слишком много условных столбцов.</span><span class="sxs-lookup"><span data-stu-id="77bee-148">Trying to index too many conditional columns.</span></span> <span data-ttu-id="77bee-149">Элемент <strong>ккондитионалколумн</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> не должен быть больше <strong>JET_ccolKeyMost</strong>.</span><span class="sxs-lookup"><span data-stu-id="77bee-149">The <strong>cConditionalColumn</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure must not be greater than <strong>JET_ccolKeyMost</strong>.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77bee-150">JET_errIndexTuplesInvalidLimits</span><span class="sxs-lookup"><span data-stu-id="77bee-150">JET_errIndexTuplesInvalidLimits</span></span></p></td>
<td><p><span data-ttu-id="77bee-151">Применимо к версиям Windows, начиная с Windows XP.</span><span class="sxs-lookup"><span data-stu-id="77bee-151">Applies to versions of Windows starting with Windows XP.</span></span> <span data-ttu-id="77bee-152">Указана структура <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> , а ее ограничения не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="77bee-152">A <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure was specified, and its limits are not supported.</span></span> <span data-ttu-id="77bee-153">Дополнительные сведения см. в разделе "Примечания" структуры <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> .</span><span class="sxs-lookup"><span data-stu-id="77bee-153">For more information, see the remarks section of the <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77bee-154">JET_errIndexTuplesNonUniqueOnly</span><span class="sxs-lookup"><span data-stu-id="77bee-154">JET_errIndexTuplesNonUniqueOnly</span></span></p></td>
<td><p><span data-ttu-id="77bee-155">Применимо к версиям Windows, начиная с Windows XP.</span><span class="sxs-lookup"><span data-stu-id="77bee-155">Applies to versions of Windows starting with Windows XP.</span></span> <span data-ttu-id="77bee-156">Индекс кортежа не может быть уникальным (<em>грбит</em> не должен содержать как <strong>JET_bitIndexTuples</strong> , так <strong>JET_bitIndexUnique</strong> Set).</span><span class="sxs-lookup"><span data-stu-id="77bee-156">A tuple index cannot be unique (<em>grbit</em> must not have both <strong>JET_bitIndexTuples</strong> and <strong>JET_bitIndexUnique</strong> set).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77bee-157">JET_errIndexTuplesOneColumnOnly</span><span class="sxs-lookup"><span data-stu-id="77bee-157">JET_errIndexTuplesOneColumnOnly</span></span></p></td>
<td><p><span data-ttu-id="77bee-158">Применимо к версиям Windows, начиная с Windows XP.</span><span class="sxs-lookup"><span data-stu-id="77bee-158">Applies to versions of Windows starting with Windows XP.</span></span> <span data-ttu-id="77bee-159">Индекс кортежа может находиться только в одном столбце (то есть элемент <strong>грбит</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> имеет <strong>JET_bitIndexTuples</strong> набор, а элемент <strong>сзкэй</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> указывает более одного столбца).</span><span class="sxs-lookup"><span data-stu-id="77bee-159">A tuple index can only be over a single column (that is, the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure has <strong>JET_bitIndexTuples</strong> set, and the <strong>szKey</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure specifies more than one column).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77bee-160">JET_errIndexTuplesSecondaryIndexOnly</span><span class="sxs-lookup"><span data-stu-id="77bee-160">JET_errIndexTuplesSecondaryIndexOnly</span></span></p></td>
<td><p><span data-ttu-id="77bee-161">Применимо к версиям Windows, начиная с Windows XP.</span><span class="sxs-lookup"><span data-stu-id="77bee-161">Applies to versions of Windows starting with Windows XP.</span></span> <span data-ttu-id="77bee-162">Индекс кортежа не может быть первичным индексом (т. е. элемент <strong>грбит</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> не должен иметь одновременно <strong>JET_bitIndexPrimary</strong> и <strong>JET_bitIndexTuples</strong> ).</span><span class="sxs-lookup"><span data-stu-id="77bee-162">A tuple index cannot be a primary index (that is, the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure must not have both <strong>JET_bitIndexPrimary</strong> and <strong>JET_bitIndexTuples</strong> set).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77bee-163">JET_errIndexTuplesTextColumnsOnly</span><span class="sxs-lookup"><span data-stu-id="77bee-163">JET_errIndexTuplesTextColumnsOnly</span></span></p></td>
<td><p><span data-ttu-id="77bee-164">Применимо к версиям Windows, начиная с Windows XP.</span><span class="sxs-lookup"><span data-stu-id="77bee-164">Applies to versions of Windows starting with Windows XP.</span></span> <span data-ttu-id="77bee-165">Индекс кортежа может находиться только в тексте или столбце Юникода.</span><span class="sxs-lookup"><span data-stu-id="77bee-165">A tuple index can only be on a text or Unicode column.</span></span> <span data-ttu-id="77bee-166">Попытка индексировать другие столбцы (например, двоичные столбцы) приведет к <strong>JET_errIndexTuplesTextColumnsOnly</strong>.</span><span class="sxs-lookup"><span data-stu-id="77bee-166">An attempt to index other columns (for example, binary columns) will result in <strong>JET_errIndexTuplesTextColumnsOnly</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77bee-167">JET_errIndexTuplesVarSegMacNotAllowed</span><span class="sxs-lookup"><span data-stu-id="77bee-167">JET_errIndexTuplesVarSegMacNotAllowed</span></span></p></td>
<td><p><span data-ttu-id="77bee-168">Применимо к версиям Windows, начиная с Windows XP.</span><span class="sxs-lookup"><span data-stu-id="77bee-168">Applies to versions of Windows starting with Windows XP.</span></span> <span data-ttu-id="77bee-169">Индекс кортежа не позволяет установить элемент <strong>кбварсегмак</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> .</span><span class="sxs-lookup"><span data-stu-id="77bee-169">A tuple index does not allow the <strong>cbVarSegMac</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure to be set.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77bee-170">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="77bee-170">JET_errInTransaction</span></span></p></td>
<td><p><span data-ttu-id="77bee-171">Предпринята попытка создать индекс без сведений о версии во время транзакции.</span><span class="sxs-lookup"><span data-stu-id="77bee-171">An attempt was made to create an index without version information while in a transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77bee-172">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="77bee-172">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="77bee-173">Определение индекса недопустимо, так как элемент <strong>грбит</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> содержит неправильные значения.</span><span class="sxs-lookup"><span data-stu-id="77bee-173">The index definition is invalid because the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure contains inconsistent values.</span></span> <span data-ttu-id="77bee-174">Ниже приведены некоторые возможные причины.</span><span class="sxs-lookup"><span data-stu-id="77bee-174">The following are some possible reasons:</span></span></p>
<ul>
<li><p><span data-ttu-id="77bee-175">В первичном индексе указан бит игнорирования (JET_bitIndexPrimary был передан с одним из <strong>JET_bitIndexIgnoreNull</strong>, <strong>JET_bitIndexIgnoreAnyNull</strong>или <strong>JET_bitIndexIgnoreFirstNull</strong>).</span><span class="sxs-lookup"><span data-stu-id="77bee-175">A primary index had an ignore bit specified (JET_bitIndexPrimary was passed with one of <strong>JET_bitIndexIgnoreNull</strong>, <strong>JET_bitIndexIgnoreAnyNull</strong>, or <strong>JET_bitIndexIgnoreFirstNull</strong>).</span></span></p></li>
<li><p><span data-ttu-id="77bee-176">Пустой индекс не игнорирует какие-либо поля null (т. е. элемент <strong>грбит</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> <strong>JET_bitIndexEmpty</strong> задан, но не имеет набора <strong>JET_bitIndexIgnoreAnyNull</strong> ).</span><span class="sxs-lookup"><span data-stu-id="77bee-176">An empty index does not ignore any null fields (that is, <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure has <strong>JET_bitIndexEmpty</strong> set, but does not have <strong>JET_bitIndexIgnoreAnyNull</strong> set).</span></span></p></li>
<li><p><span data-ttu-id="77bee-177">Передача структуры <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> с недопустимым элементом <strong>грбит</strong> .</span><span class="sxs-lookup"><span data-stu-id="77bee-177">Passing in a <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> structure with an invalid <strong>grbit</strong> member.</span></span> <span data-ttu-id="77bee-178">См. <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a>.</span><span class="sxs-lookup"><span data-stu-id="77bee-178">See <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a>.</span></span></p></li>
</ul>
<p><span data-ttu-id="77bee-179">При создании нескольких индексов одновременно (то есть если параметр <em>Циндекскреате</em> больше единицы) ни один из индексов не может содержать следующие биты:</span><span class="sxs-lookup"><span data-stu-id="77bee-179">When creating several indexes at once (that is, if the <em>cIndexCreate</em> parameter is greater than one), none of the indexes may contain any of the following bits:</span></span></p>
<ul>
<li><p><span data-ttu-id="77bee-180"><strong>JET_bitIndexPrimary</strong></span><span class="sxs-lookup"><span data-stu-id="77bee-180"><strong>JET_bitIndexPrimary</strong></span></span></p></li>
<li><p><span data-ttu-id="77bee-181"><strong>JET_bitIndexUnversioned</strong></span><span class="sxs-lookup"><span data-stu-id="77bee-181"><strong>JET_bitIndexUnversioned</strong></span></span></p></li>
<li><p><span data-ttu-id="77bee-182"><strong>JET_bitIndexEmpty</strong></span><span class="sxs-lookup"><span data-stu-id="77bee-182"><strong>JET_bitIndexEmpty</strong></span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77bee-183">JET_errInvalidLanguageId</span><span class="sxs-lookup"><span data-stu-id="77bee-183">JET_errInvalidLanguageId</span></span></p></td>
<td><p><span data-ttu-id="77bee-184">Передан недопустимый код локали (LCID) (с помощью элемента <strong>LCID</strong> в структуре <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> , которой элемент <strong>пидксуникоде</strong> в структуре <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> содержит указатель на или с помощью элемента <strong>LCID</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ).</span><span class="sxs-lookup"><span data-stu-id="77bee-184">An invalid Locale ID (LCID) was passed in (either through the <strong>lcid</strong> member in the <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> structure, which the <strong>pidxunicode</strong> member in the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure contains a pointer to, or through the <strong>lcid</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77bee-185">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="77bee-185">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="77bee-186">Указано недопустимое имя индекса.</span><span class="sxs-lookup"><span data-stu-id="77bee-186">An invalid index name was specified.</span></span> <span data-ttu-id="77bee-187">Дополнительные сведения см. в разделе <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> .</span><span class="sxs-lookup"><span data-stu-id="77bee-187">See <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> for more details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77bee-188">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="77bee-188">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="77bee-189">В API передан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="77bee-189">An invalid parameter was passed into the API.</span></span> <span data-ttu-id="77bee-190">Ниже приведены некоторые причины, по которым может быть возвращена эта ошибка:</span><span class="sxs-lookup"><span data-stu-id="77bee-190">The following are some reasons why this error may be returned:</span></span></p>
<ul>
<li><p><span data-ttu-id="77bee-191">Поле <strong>cbKey</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> имеет значение 0.</span><span class="sxs-lookup"><span data-stu-id="77bee-191">The <strong>cbKey</strong> field of a <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is set to zero.</span></span></p></li>
<li><p><span data-ttu-id="77bee-192">Элементу <strong>кбструкт</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> не присвоено значение sizeof (JET_INDEXCREATE2).</span><span class="sxs-lookup"><span data-stu-id="77bee-192">The <strong>cbStruct</strong> member of a <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is not set to sizeof(JET_INDEXCREATE2).</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77bee-193">JET_errUnicodeTranslationFail</span><span class="sxs-lookup"><span data-stu-id="77bee-193">JET_errUnicodeTranslationFail</span></span></p></td>
<td><p><span data-ttu-id="77bee-194">Произошла ошибка при попытке нормализовать столбец в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="77bee-194">An error occurred while trying to normalize a Unicode column.</span></span> <span data-ttu-id="77bee-195">Это может быть вызвано недостатком системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="77bee-195">This can be caused by running out of system resources.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77bee-196">JET_errSpaceHintsInvalid</span><span class="sxs-lookup"><span data-stu-id="77bee-196">JET_errSpaceHintsInvalid</span></span></p></td>
<td><p><span data-ttu-id="77bee-197">Неверное или неправильное действие элемента структуры подсказок пространства JET.</span><span class="sxs-lookup"><span data-stu-id="77bee-197">An element of the JET space hints structure was not correct or actionable.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="77bee-198">Комментарии</span><span class="sxs-lookup"><span data-stu-id="77bee-198">Remarks</span></span>

<span data-ttu-id="77bee-199">Функция **JetCreateIndex4W** выполняет итерацию индексов, заданных в параметре *пиндекскреате* , и иногда прерывается при первом сбое.</span><span class="sxs-lookup"><span data-stu-id="77bee-199">The **JetCreateIndex4W** function iterates through the indexes given in the *pindexcreate* parameter, and will sometimes abort on the first failure.</span></span> <span data-ttu-id="77bee-200">Любые индексы после первого индекса с ошибкой могут не попытаться, несмотря на то, что элемент **Err** структуры [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) содержит JET_errSuccess.</span><span class="sxs-lookup"><span data-stu-id="77bee-200">Any indexes after the first index with an error may not have been attempted, even though the **err** member of the [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) structure contains JET_errSuccess.</span></span>

#### <a name="requirements"></a><span data-ttu-id="77bee-201">Требования</span><span class="sxs-lookup"><span data-stu-id="77bee-201">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="77bee-202"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="77bee-202"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="77bee-203">Требуется Windows 8.</span><span class="sxs-lookup"><span data-stu-id="77bee-203">Requires Windows 8.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77bee-204"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="77bee-204"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="77bee-205">Требуется Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="77bee-205">Requires Windows Server 2012.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77bee-206"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="77bee-206"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="77bee-207">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="77bee-207">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77bee-208"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="77bee-208"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="77bee-209">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="77bee-209">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77bee-210"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="77bee-210"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="77bee-211">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="77bee-211">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="77bee-212">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="77bee-212">See also</span></span>

[<span data-ttu-id="77bee-213">JET_CONDITIONALCOLUMN</span><span class="sxs-lookup"><span data-stu-id="77bee-213">JET_CONDITIONALCOLUMN</span></span>](./jet-conditionalcolumn-structure.md)  
[<span data-ttu-id="77bee-214">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="77bee-214">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="77bee-215">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="77bee-215">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="77bee-216">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="77bee-216">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="77bee-217">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="77bee-217">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="77bee-218">JET_INDEXCREATE2</span><span class="sxs-lookup"><span data-stu-id="77bee-218">JET_INDEXCREATE2</span></span>](./jet-indexcreate2-structure.md)  
[<span data-ttu-id="77bee-219">жеткреатеиндекс</span><span class="sxs-lookup"><span data-stu-id="77bee-219">JetCreateIndex</span></span>](./jetcreateindex-function.md)  
[<span data-ttu-id="77bee-220">жеткреатетаблеколумниндекс</span><span class="sxs-lookup"><span data-stu-id="77bee-220">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="77bee-221">JetCreateTableColumnIndex2</span><span class="sxs-lookup"><span data-stu-id="77bee-221">JetCreateTableColumnIndex2</span></span>](./jetcreatetablecolumnindex2-function.md)  
[<span data-ttu-id="77bee-222">JET_SPACEHINTS</span><span class="sxs-lookup"><span data-stu-id="77bee-222">JET_SPACEHINTS</span></span>](./jet-spacehints-structure.md)
