---
description: Дополнительные сведения о функции JetCreateIndex2
title: Функция JetCreateIndex2
TOCTitle: JetCreateIndex2 Function
ms:assetid: 8810eaed-40cb-4561-aafc-9a9bbdb0d05b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269324(v=EXCHG.10)
ms:contentKeyID: 32765614
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateIndex2W
- JetCreateIndex2A
- JetCreateIndex2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 42c1eb8fa1bb7fa880cf7286a1ec472ddc7ba7fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712512"
---
# <a name="jetcreateindex2-function"></a><span data-ttu-id="9b687-103">Функция JetCreateIndex2</span><span class="sxs-lookup"><span data-stu-id="9b687-103">JetCreateIndex2 Function</span></span>


<span data-ttu-id="9b687-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="9b687-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetcreateindex2-function"></a><span data-ttu-id="9b687-105">Функция JetCreateIndex2</span><span class="sxs-lookup"><span data-stu-id="9b687-105">JetCreateIndex2 Function</span></span>

<span data-ttu-id="9b687-106">Функция **JetCreateIndex2** создает индексы для данных в базе данных ESE, которая может быть использована для быстрого выявления конкретных данных.</span><span class="sxs-lookup"><span data-stu-id="9b687-106">The **JetCreateIndex2** function creates indexes over data in an ESE database, which can be used to locate specific data quickly.</span></span>

```cpp
    JET_ERR JET_API JetCreateIndex2(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_INDEXCREATE* pindexcreate,
      __in          unsigned long cIndexCreate
    );
```

### <a name="parameters"></a><span data-ttu-id="9b687-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="9b687-107">Parameters</span></span>

<span data-ttu-id="9b687-108">*сесид*</span><span class="sxs-lookup"><span data-stu-id="9b687-108">*sesid*</span></span>

<span data-ttu-id="9b687-109">Контекст сеанса базы данных, используемый для вызова API.</span><span class="sxs-lookup"><span data-stu-id="9b687-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="9b687-110">*TableID*</span><span class="sxs-lookup"><span data-stu-id="9b687-110">*tableid*</span></span>

<span data-ttu-id="9b687-111">Таблица, в которой будет создан индекс.</span><span class="sxs-lookup"><span data-stu-id="9b687-111">The table on which the index will be created.</span></span>

<span data-ttu-id="9b687-112">*пиндекскреате*</span><span class="sxs-lookup"><span data-stu-id="9b687-112">*pindexcreate*</span></span>

<span data-ttu-id="9b687-113">Массив структур [JET_INDEXCREATE](./jet-indexcreate-structure.md) , каждый из которых определяет создаваемый индекс.</span><span class="sxs-lookup"><span data-stu-id="9b687-113">An array of [JET_INDEXCREATE](./jet-indexcreate-structure.md) structures, each of which defines an index to be created.</span></span>

<span data-ttu-id="9b687-114">*Циндекскреате*</span><span class="sxs-lookup"><span data-stu-id="9b687-114">*cIndexCreate*</span></span>

<span data-ttu-id="9b687-115">Число элементов в массиве *пиндекскреате* .</span><span class="sxs-lookup"><span data-stu-id="9b687-115">The number of elements in the *pindexcreate* array.</span></span>

### <a name="return-value"></a><span data-ttu-id="9b687-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9b687-116">Return Value</span></span>

<span data-ttu-id="9b687-117">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="9b687-117">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="9b687-118">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="9b687-118">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9b687-119">Код возврата</span><span class="sxs-lookup"><span data-stu-id="9b687-119">Return code</span></span></p></th>
<th><p><span data-ttu-id="9b687-120">Описание</span><span class="sxs-lookup"><span data-stu-id="9b687-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9b687-121">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="9b687-121">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="9b687-122">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="9b687-122">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b687-123">JET_errCannotIndex</span><span class="sxs-lookup"><span data-stu-id="9b687-123">JET_errCannotIndex</span></span></p></td>
<td><p><span data-ttu-id="9b687-124">Предпринята попытка индексирования по столбцу с использованием типа "условно-Update" или "SLV" (Обратите внимание, что столбцы SLV устарели).</span><span class="sxs-lookup"><span data-stu-id="9b687-124">An attempt was made to index over an escrow-update or SLV column (note that SLV columns are deprecated).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b687-125">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="9b687-125">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="9b687-126">Предпринята попытка индексировать несуществующий столбец.</span><span class="sxs-lookup"><span data-stu-id="9b687-126">An attempt was made to index over a non-existent column.</span></span> <span data-ttu-id="9b687-127">Эта ошибка также может возникнуть при попытке условного индексирования по несуществующему столбцу.</span><span class="sxs-lookup"><span data-stu-id="9b687-127">Attempting to conditionally index over a non-existent column can also produce this error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b687-128">JET_errDensityInvalid</span><span class="sxs-lookup"><span data-stu-id="9b687-128">JET_errDensityInvalid</span></span></p></td>
<td><p><span data-ttu-id="9b687-129">Эта ошибка будет возвращена, если элементу <strong>улденсити</strong> структуры <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> присвоено число меньше 20 или больше 100.</span><span class="sxs-lookup"><span data-stu-id="9b687-129">This error will be returned if the <strong>ulDensity</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure is set to a number less than 20 or more than 100.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b687-130">JET_errIndexDuplicate</span><span class="sxs-lookup"><span data-stu-id="9b687-130">JET_errIndexDuplicate</span></span></p></td>
<td><p><span data-ttu-id="9b687-131">Была выполнена попытка определить два одинаковых индекса.</span><span class="sxs-lookup"><span data-stu-id="9b687-131">An attempt to define two identical indexes was made.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b687-132">JET_errIndexHasPrimary</span><span class="sxs-lookup"><span data-stu-id="9b687-132">JET_errIndexHasPrimary</span></span></p></td>
<td><p><span data-ttu-id="9b687-133">Предпринята попытка указать более одного первичного индекса для таблицы.</span><span class="sxs-lookup"><span data-stu-id="9b687-133">An attempt was made to specify more than one primary index for a table.</span></span> <span data-ttu-id="9b687-134">У таблицы должен быть ровно один первичный индекс.</span><span class="sxs-lookup"><span data-stu-id="9b687-134">A table must have exactly one primary index.</span></span> <span data-ttu-id="9b687-135">Если первичный индекс не указан, ядро СУБД будет прозрачно создавать его.</span><span class="sxs-lookup"><span data-stu-id="9b687-135">If no primary index is specified, the database engine will transparently create one.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b687-136">JET_errIndexInvalidDef</span><span class="sxs-lookup"><span data-stu-id="9b687-136">JET_errIndexInvalidDef</span></span></p></td>
<td><p><span data-ttu-id="9b687-137">Указано недопустимое определение индекса.</span><span class="sxs-lookup"><span data-stu-id="9b687-137">An invalid index definition was specified.</span></span> <span data-ttu-id="9b687-138">Ниже приведены некоторые возможные причины получения этой ошибки:</span><span class="sxs-lookup"><span data-stu-id="9b687-138">Some of the possible reasons for receiving this error are:</span></span></p>
<ul>
<li><p><span data-ttu-id="9b687-139">Первичный индекс является условным (<strong>грбит</strong> член <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> имеет JET_bitIndexPrimary набор, а элемент <strong>ккондитионалколумн</strong> <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> больше нуля).</span><span class="sxs-lookup"><span data-stu-id="9b687-139">A primary index is conditional (<strong>grbit</strong> member of <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> has JET_bitIndexPrimary set, and the <strong>cConditionalColumn</strong> member of <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> is greater than zero).</span></span></p></li>
<li><p><span data-ttu-id="9b687-140">Windows Server 2003 и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="9b687-140">Windows Server 2003 and later.</span></span> <span data-ttu-id="9b687-141">Попытка создать индекс кортежа с ограничениями кортежей, но без передачи сведений в элемент <strong>птуплелимитс</strong> в <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> (то есть <em>грбит</em> имеет набор JET_bitIndexTupleLimits, но указатель <strong>птуплелимитс</strong> имеет значение null).</span><span class="sxs-lookup"><span data-stu-id="9b687-141">Attempting to create a tuple index with tuple limits, but without passing information in the <strong>ptuplelimits</strong> member in <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> (that is, <em>grbit</em> has JET_bitIndexTupleLimits set, but the <strong>ptuplelimits</strong> pointer is NULL).</span></span></p></li>
<li><p><span data-ttu-id="9b687-142">Передача недопустимого определения ключа в элемент <strong>сзкэй</strong> структуры <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</span><span class="sxs-lookup"><span data-stu-id="9b687-142">Passing in an invalid key definition in the <strong>szKey</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure.</span></span> <span data-ttu-id="9b687-143">Описание допустимых определений см. в разделе <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</span><span class="sxs-lookup"><span data-stu-id="9b687-143">See <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> for a discussion of valid definitions.</span></span></p></li>
<li><p><span data-ttu-id="9b687-144">Установка для элемента <strong>кбварсегмак</strong> в <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> значение больше JET_cbPrimaryKeyMost (для первичного индекса) или больше JET_cbSecondaryKeyMost (для вторичного индекса).</span><span class="sxs-lookup"><span data-stu-id="9b687-144">Setting the <strong>cbVarSegMac</strong> member in <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> to be greater than JET_cbPrimaryKeyMost (for a primary index) or greater than JET_cbSecondaryKeyMost (for a secondary index).</span></span></p></li>
<li><p><span data-ttu-id="9b687-145">Передача недопустимого сочетания для определяемого пользователем индекса в Юникоде (одна из которых имеет бит JET_bitIndexUnicode, заданный в элементе <strong>грбит</strong> в <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>).</span><span class="sxs-lookup"><span data-stu-id="9b687-145">Passing an invalid combination for a user-defined Unicode index (one which has the JET_bitIndexUnicode bit set in the <strong>grbit</strong> member of <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>).</span></span> <span data-ttu-id="9b687-146">Некоторые распространенные причины могут быть вызваны тем, что поле пидксуникоде структуры <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> имеет значение null или код LCID, указанный в структуре пидксуникоде, является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="9b687-146">Some common causes may be that the pidxunicode field of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure is NULL, or the LCID specified in the pidxunicode structure is invalid.</span></span></p></li>
<li><p><span data-ttu-id="9b687-147">Указание столбца с несколькими значениями для первичного индекса.</span><span class="sxs-lookup"><span data-stu-id="9b687-147">Specifying a multi-valued column for a primary index.</span></span></p></li>
<li><p><span data-ttu-id="9b687-148">Попытка индексировать слишком много условных столбцов.</span><span class="sxs-lookup"><span data-stu-id="9b687-148">Trying to index too many conditional columns.</span></span> <span data-ttu-id="9b687-149">Элемент <strong>ккондитионалколумн</strong> структуры <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> не должен быть больше JET_ccolKeyMost.</span><span class="sxs-lookup"><span data-stu-id="9b687-149">The <strong>cConditionalColumn</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure must not be greater than JET_ccolKeyMost.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b687-150">JET_errIndexTuplesInvalidLimits</span><span class="sxs-lookup"><span data-stu-id="9b687-150">JET_errIndexTuplesInvalidLimits</span></span></p></td>
<td><p><span data-ttu-id="9b687-151">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="9b687-151">Windows XP and later.</span></span> <span data-ttu-id="9b687-152">Указана структура <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> , а ее ограничения не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="9b687-152">A <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure was specified, and its limits are not supported.</span></span> <span data-ttu-id="9b687-153">См. раздел "Примечания" структуры <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> .</span><span class="sxs-lookup"><span data-stu-id="9b687-153">See the remarks section of the <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b687-154">JET_errIndexTuplesNonUniqueOnly</span><span class="sxs-lookup"><span data-stu-id="9b687-154">JET_errIndexTuplesNonUniqueOnly</span></span></p></td>
<td><p><span data-ttu-id="9b687-155">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="9b687-155">Windows XP and later.</span></span> <span data-ttu-id="9b687-156">Индекс кортежа не может быть уникальным (<em>грбит</em> не должен содержать как JET_bitIndexTuples, так JET_bitIndexUnique Set).</span><span class="sxs-lookup"><span data-stu-id="9b687-156">A tuple index cannot be unique (<em>grbit</em> must not have both JET_bitIndexTuples and JET_bitIndexUnique set).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b687-157">JET_errIndexTuplesOneColumnOnly</span><span class="sxs-lookup"><span data-stu-id="9b687-157">JET_errIndexTuplesOneColumnOnly</span></span></p></td>
<td><p><span data-ttu-id="9b687-158">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="9b687-158">Windows XP and later.</span></span> <span data-ttu-id="9b687-159">Индекс кортежа может находиться только в одном столбце (то есть элемент <strong>грбит</strong> структуры <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> имеет JET_bitIndexTuples набор, а элемент <strong>сзкэй</strong> структуры <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> указывает более одного столбца).</span><span class="sxs-lookup"><span data-stu-id="9b687-159">A tuple index can only be over a single column (that is, the <strong>grbit</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure has JET_bitIndexTuples set, and the <strong>szKey</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure specifies more than one column).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b687-160">JET_errIndexTuplesSecondaryIndexOnly</span><span class="sxs-lookup"><span data-stu-id="9b687-160">JET_errIndexTuplesSecondaryIndexOnly</span></span></p></td>
<td><p><span data-ttu-id="9b687-161">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="9b687-161">Windows XP and later.</span></span> <span data-ttu-id="9b687-162">Индекс кортежа не может быть первичным индексом (т. е. элемент <strong>грбит</strong> структуры <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> не должен иметь одновременно JET_bitIndexPrimary и JET_bitIndexTuples).</span><span class="sxs-lookup"><span data-stu-id="9b687-162">A tuple index cannot be a primary index (that is, the <strong>grbit</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure must not have both JET_bitIndexPrimary and JET_bitIndexTuples set).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b687-163">JET_errIndexTuplesTextColumnsOnly</span><span class="sxs-lookup"><span data-stu-id="9b687-163">JET_errIndexTuplesTextColumnsOnly</span></span></p></td>
<td><p><span data-ttu-id="9b687-164">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="9b687-164">Windows XP and later.</span></span> <span data-ttu-id="9b687-165">Индекс кортежа может находиться только в тексте или столбце Юникода.</span><span class="sxs-lookup"><span data-stu-id="9b687-165">A tuple index can only be on a text or Unicode column.</span></span> <span data-ttu-id="9b687-166">Попытка индексировать другие столбцы (например, двоичные столбцы) приведет к JET_errIndexTuplesTextColumnsOnly.</span><span class="sxs-lookup"><span data-stu-id="9b687-166">An attempt to index other columns (for example, binary columns) will result in JET_errIndexTuplesTextColumnsOnly.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b687-167">JET_errIndexTuplesVarSegMacNotAllowed</span><span class="sxs-lookup"><span data-stu-id="9b687-167">JET_errIndexTuplesVarSegMacNotAllowed</span></span></p></td>
<td><p><span data-ttu-id="9b687-168">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="9b687-168">Windows XP and later.</span></span> <span data-ttu-id="9b687-169">Индекс кортежа не позволяет установить элемент <strong>кбварсегмак</strong> структуры <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</span><span class="sxs-lookup"><span data-stu-id="9b687-169">A tuple index does not allow the <strong>cbVarSegMac</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure to be set.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b687-170">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="9b687-170">JET_errInTransaction</span></span></p></td>
<td><p><span data-ttu-id="9b687-171">Предпринята попытка создать индекс без сведений о версии во время транзакции.</span><span class="sxs-lookup"><span data-stu-id="9b687-171">An attempt was made to create an index without version information while in a transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b687-172">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="9b687-172">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="9b687-173">Определение индекса недопустимо, так как элемент <strong>грбит</strong> структуры <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> содержит неправильные значения.</span><span class="sxs-lookup"><span data-stu-id="9b687-173">The index definition is invalid because the <strong>grbit</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure contains inconsistent values.</span></span> <span data-ttu-id="9b687-174">Возможные причины:</span><span class="sxs-lookup"><span data-stu-id="9b687-174">Some possible reasons are:</span></span></p>
<ul>
<li><p><span data-ttu-id="9b687-175">В первичном индексе указан бит игнорирования (JET_bitIndexPrimary был передан с одним из JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull или JET_bitIndexIgnoreFirstNull).</span><span class="sxs-lookup"><span data-stu-id="9b687-175">A primary index had an ignore bit specified (JET_bitIndexPrimary was passed with one of JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull, or JET_bitIndexIgnoreFirstNull).</span></span></p></li>
<li><p><span data-ttu-id="9b687-176">Пустой индекс не игнорирует какие-либо поля NULL (т. е. элемент <strong>грбит</strong> структуры <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> JET_bitIndexEmpty задан, но не имеет набора JET_bitIndexIgnoreAnyNull).</span><span class="sxs-lookup"><span data-stu-id="9b687-176">An empty index does not ignore any NULL fields (that is, <strong>grbit</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure has JET_bitIndexEmpty set, but does not have JET_bitIndexIgnoreAnyNull set).</span></span></p></li>
<li><p><span data-ttu-id="9b687-177">Передача структуры <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> с недопустимым элементом <strong>грбит</strong> .</span><span class="sxs-lookup"><span data-stu-id="9b687-177">Passing in a <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> structure with an invalid <strong>grbit</strong> member.</span></span> <span data-ttu-id="9b687-178">См. <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a>.</span><span class="sxs-lookup"><span data-stu-id="9b687-178">See <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a>.</span></span></p></li>
</ul>
<p><span data-ttu-id="9b687-179">При создании нескольких индексов одновременно (то есть если параметр <em>Циндекскреате</em> больше единицы) ни один из индексов не может содержать следующие биты:</span><span class="sxs-lookup"><span data-stu-id="9b687-179">When creating several indexes at once (that is, if the <em>cIndexCreate</em> parameter is greater than one), none of the indexes may contain any of the following bits:</span></span></p>
<ul>
<li><p><span data-ttu-id="9b687-180">JET_bitIndexPrimary</span><span class="sxs-lookup"><span data-stu-id="9b687-180">JET_bitIndexPrimary</span></span></p></li>
<li><p><span data-ttu-id="9b687-181">JET_bitIndexUnversioned</span><span class="sxs-lookup"><span data-stu-id="9b687-181">JET_bitIndexUnversioned</span></span></p></li>
<li><p><span data-ttu-id="9b687-182">JET_bitIndexEmpty</span><span class="sxs-lookup"><span data-stu-id="9b687-182">JET_bitIndexEmpty</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b687-183">JET_errInvalidLanguageId</span><span class="sxs-lookup"><span data-stu-id="9b687-183">JET_errInvalidLanguageId</span></span></p></td>
<td><p><span data-ttu-id="9b687-184">Передан недопустимый код локали (LCID) (с помощью элемента <strong>LCID</strong> в структуре <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> , которой элемент <strong>пидксуникоде</strong> в структуре <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> содержит указатель на или с помощью элемента <strong>LCID</strong> структуры <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> ).</span><span class="sxs-lookup"><span data-stu-id="9b687-184">An invalid Locale ID (LCID) was passed in (either through the <strong>lcid</strong> member in the <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> structure, which the <strong>pidxunicode</strong> member in the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure contains a pointer to, or through the <strong>lcid</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b687-185">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="9b687-185">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="9b687-186">Указано недопустимое имя индекса.</span><span class="sxs-lookup"><span data-stu-id="9b687-186">An invalid index name was specified.</span></span> <span data-ttu-id="9b687-187">Дополнительные сведения см. в разделе <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</span><span class="sxs-lookup"><span data-stu-id="9b687-187">See <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> for more details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b687-188">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="9b687-188">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="9b687-189">В API передан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="9b687-189">An invalid parameter was passed into the API.</span></span> <span data-ttu-id="9b687-190">Ниже приведены некоторые причины, по которым эта ошибка может быть возвращена.</span><span class="sxs-lookup"><span data-stu-id="9b687-190">Some of the reasons this error may be returned are:</span></span></p>
<ul>
<li><p><span data-ttu-id="9b687-191">Поле <strong>cbKey</strong> структуры <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> имеет значение 0.</span><span class="sxs-lookup"><span data-stu-id="9b687-191">The <strong>cbKey</strong> field of a <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure is set to zero.</span></span></p></li>
<li><p><span data-ttu-id="9b687-192">Элементу <strong>кбструкт</strong> структуры <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> не присвоено значение sizeof (<a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> ).</span><span class="sxs-lookup"><span data-stu-id="9b687-192">The <strong>cbStruct</strong> member of a <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure is not set to sizeof(<a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> ).</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b687-193">JET_errUnicodeTranslationFail</span><span class="sxs-lookup"><span data-stu-id="9b687-193">JET_errUnicodeTranslationFail</span></span></p></td>
<td><p><span data-ttu-id="9b687-194">Произошла ошибка при попытке нормализовать столбец в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="9b687-194">An error occurred attempting to normalize a Unicode column.</span></span> <span data-ttu-id="9b687-195">Это может быть вызвано недостатком системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9b687-195">This can be caused by running out of system resources.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="9b687-196">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9b687-196">Remarks</span></span>

<span data-ttu-id="9b687-197">Возвращаемое значение JET_errSuccess при успешном завершении всех указанных индексов.</span><span class="sxs-lookup"><span data-stu-id="9b687-197">The return value is JET_errSuccess on successful completion of all indexes specified.</span></span>

<span data-ttu-id="9b687-198">**JetCreateIndex2** перебирает индексы, заданные в **пиндекскреате**, и иногда прерываются при первом сбое.</span><span class="sxs-lookup"><span data-stu-id="9b687-198">**JetCreateIndex2** iterates through the indexes given in **pindexcreate**, and will sometimes abort on the first failure.</span></span> <span data-ttu-id="9b687-199">Любые индексы после первого индекса с ошибкой могут не попытаться, несмотря на то, что элемент **Err** структуры [JET_INDEXCREATE](./jet-indexcreate-structure.md) содержит JET_errSuccess.</span><span class="sxs-lookup"><span data-stu-id="9b687-199">Any indexes after the first index with an error may not have been attempted, even though the **err** member of the [JET_INDEXCREATE](./jet-indexcreate-structure.md) structure contains JET_errSuccess.</span></span>

#### <a name="requirements"></a><span data-ttu-id="9b687-200">Требования</span><span class="sxs-lookup"><span data-stu-id="9b687-200">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9b687-201"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="9b687-201"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="9b687-202">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="9b687-202">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b687-203"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="9b687-203"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="9b687-204">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="9b687-204">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b687-205"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="9b687-205"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="9b687-206">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="9b687-206">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b687-207"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="9b687-207"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="9b687-208">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="9b687-208">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b687-209"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="9b687-209"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="9b687-210">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="9b687-210">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b687-211"><strong>Юникод</strong></span><span class="sxs-lookup"><span data-stu-id="9b687-211"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="9b687-212">Реализуется как <strong>JetCreateIndex2W</strong> (Юникод) и <strong>JetCreateIndex2A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="9b687-212">Implemented as <strong>JetCreateIndex2W</strong> (Unicode) and <strong>JetCreateIndex2A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="9b687-213">См. также:</span><span class="sxs-lookup"><span data-stu-id="9b687-213">See Also</span></span>

[<span data-ttu-id="9b687-214">JET_CONDITIONALCOLUMN</span><span class="sxs-lookup"><span data-stu-id="9b687-214">JET_CONDITIONALCOLUMN</span></span>](./jet-conditionalcolumn-structure.md)  
[<span data-ttu-id="9b687-215">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="9b687-215">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="9b687-216">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="9b687-216">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="9b687-217">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="9b687-217">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="9b687-218">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="9b687-218">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="9b687-219">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="9b687-219">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)  
[<span data-ttu-id="9b687-220">жеткреатеиндекс</span><span class="sxs-lookup"><span data-stu-id="9b687-220">JetCreateIndex</span></span>](./jetcreateindex-function.md)  
[<span data-ttu-id="9b687-221">жеткреатетаблеколумниндекс</span><span class="sxs-lookup"><span data-stu-id="9b687-221">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="9b687-222">JetCreateTableColumnIndex2</span><span class="sxs-lookup"><span data-stu-id="9b687-222">JetCreateTableColumnIndex2</span></span>](./jetcreatetablecolumnindex2-function.md)
