---
description: Дополнительные сведения о функции JetCreateIndex3
title: Функция JetCreateIndex3
TOCTitle: JetCreateIndex3 Function
ms:assetid: bc9b940e-65c6-49d6-ad32-74434527d29f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294075(v=EXCHG.10)
ms:contentKeyID: 32765690
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateIndex3A
- JetCreateIndex3
- JetCreateIndex3W
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c4f3331a903d4885499ff6c2cd2cad0d8b8534a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346965"
---
# <a name="jetcreateindex3-function"></a><span data-ttu-id="1d6b7-103">Функция JetCreateIndex3</span><span class="sxs-lookup"><span data-stu-id="1d6b7-103">JetCreateIndex3 Function</span></span>


<span data-ttu-id="1d6b7-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="1d6b7-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetcreateindex3-function"></a><span data-ttu-id="1d6b7-105">Функция JetCreateIndex3</span><span class="sxs-lookup"><span data-stu-id="1d6b7-105">JetCreateIndex3 Function</span></span>

<span data-ttu-id="1d6b7-106">Функция **JetCreateIndex3** создает индексы для данных в базе данных ESE, которая может быть использована для быстрого выявления конкретных данных.</span><span class="sxs-lookup"><span data-stu-id="1d6b7-106">The **JetCreateIndex3** function creates indexes over data in an ESE database, which can be used to locate specific data quickly.</span></span>

<span data-ttu-id="1d6b7-107">**Windows 7: JetCreateIndex3** появился в операционной системе Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1d6b7-107">**Windows 7:  JetCreateIndex3** is introduced in the Windows 7 operating system.</span></span>

```cpp
    JET_ERR JET_API JetCreateIndex3(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_INDEXCREATE2* pindexcreate,
      __in          unsigned long cIndexCreate
    );
```

### <a name="parameters"></a><span data-ttu-id="1d6b7-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="1d6b7-108">Parameters</span></span>

<span data-ttu-id="1d6b7-109">*сесид*</span><span class="sxs-lookup"><span data-stu-id="1d6b7-109">*sesid*</span></span>

<span data-ttu-id="1d6b7-110">Контекст сеанса базы данных, используемый для вызова API.</span><span class="sxs-lookup"><span data-stu-id="1d6b7-110">The database session context to use for the API call.</span></span>

<span data-ttu-id="1d6b7-111">*TableID*</span><span class="sxs-lookup"><span data-stu-id="1d6b7-111">*tableid*</span></span>

<span data-ttu-id="1d6b7-112">Таблица, в которой будет создан индекс.</span><span class="sxs-lookup"><span data-stu-id="1d6b7-112">The table on which the index will be created.</span></span>

<span data-ttu-id="1d6b7-113">*пиндекскреате*</span><span class="sxs-lookup"><span data-stu-id="1d6b7-113">*pindexcreate*</span></span>

<span data-ttu-id="1d6b7-114">Массив структур [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) , каждый из которых определяет создаваемый индекс.</span><span class="sxs-lookup"><span data-stu-id="1d6b7-114">An array of [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) structures, each of which defines an index to be created.</span></span>

<span data-ttu-id="1d6b7-115">*Циндекскреате*</span><span class="sxs-lookup"><span data-stu-id="1d6b7-115">*cIndexCreate*</span></span>

<span data-ttu-id="1d6b7-116">Число элементов в массиве *пиндекскреате* .</span><span class="sxs-lookup"><span data-stu-id="1d6b7-116">The number of elements in the *pindexcreate* array.</span></span>

### <a name="return-value"></a><span data-ttu-id="1d6b7-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1d6b7-117">Return Value</span></span>

<span data-ttu-id="1d6b7-118">Эта функция возвращает [JET_ERR](./jet-err.md) тип данных с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="1d6b7-118">This function returns the [JET_ERR](./jet-err.md) data type with one of the following return codes.</span></span> <span data-ttu-id="1d6b7-119">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="1d6b7-119">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1d6b7-120">Код возврата</span><span class="sxs-lookup"><span data-stu-id="1d6b7-120">Return code</span></span></p></th>
<th><p><span data-ttu-id="1d6b7-121">Описание</span><span class="sxs-lookup"><span data-stu-id="1d6b7-121">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1d6b7-122">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="1d6b7-122">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="1d6b7-123">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="1d6b7-123">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d6b7-124">JET_errCannotIndex</span><span class="sxs-lookup"><span data-stu-id="1d6b7-124">JET_errCannotIndex</span></span></p></td>
<td><p><span data-ttu-id="1d6b7-125">Предпринята попытка индексирования по столбцу с использованием типа "условно-Update" или "SLV" (Обратите внимание, что столбцы SLV устарели).</span><span class="sxs-lookup"><span data-stu-id="1d6b7-125">An attempt was made to index over an escrow-update or SLV column (note that SLV columns are deprecated).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d6b7-126">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="1d6b7-126">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="1d6b7-127">Предпринята попытка индексировать несуществующий столбец.</span><span class="sxs-lookup"><span data-stu-id="1d6b7-127">An attempt was made to index over a non-existent column.</span></span> <span data-ttu-id="1d6b7-128">Эта ошибка также может возникнуть при попытке условного индексирования по несуществующему столбцу.</span><span class="sxs-lookup"><span data-stu-id="1d6b7-128">Attempting to conditionally index over a non-existent column can also produce this error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d6b7-129">JET_errDensityInvalid</span><span class="sxs-lookup"><span data-stu-id="1d6b7-129">JET_errDensityInvalid</span></span></p></td>
<td><p><span data-ttu-id="1d6b7-130">Эта ошибка будет возвращена, если элементу <strong>улденсити</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> присвоено число меньше 20 или больше 100.</span><span class="sxs-lookup"><span data-stu-id="1d6b7-130">This error will be returned if the <strong>ulDensity</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is set to a number less than 20 or greater than 100.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d6b7-131">JET_errIndexDuplicate</span><span class="sxs-lookup"><span data-stu-id="1d6b7-131">JET_errIndexDuplicate</span></span></p></td>
<td><p><span data-ttu-id="1d6b7-132">Была выполнена попытка определить два одинаковых индекса.</span><span class="sxs-lookup"><span data-stu-id="1d6b7-132">An attempt to define two identical indexes was made.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d6b7-133">JET_errIndexHasPrimary</span><span class="sxs-lookup"><span data-stu-id="1d6b7-133">JET_errIndexHasPrimary</span></span></p></td>
<td><p><span data-ttu-id="1d6b7-134">Предпринята попытка указать более одного первичного индекса для таблицы.</span><span class="sxs-lookup"><span data-stu-id="1d6b7-134">An attempt was made to specify more than one primary index for a table.</span></span> <span data-ttu-id="1d6b7-135">У таблицы должен быть ровно один первичный индекс.</span><span class="sxs-lookup"><span data-stu-id="1d6b7-135">A table must have exactly one primary index.</span></span> <span data-ttu-id="1d6b7-136">Если первичный индекс не указан, ядро СУБД будет прозрачно создавать его.</span><span class="sxs-lookup"><span data-stu-id="1d6b7-136">If no primary index is specified, the database engine will transparently create one.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d6b7-137">JET_errIndexInvalidDef</span><span class="sxs-lookup"><span data-stu-id="1d6b7-137">JET_errIndexInvalidDef</span></span></p></td>
<td><p><span data-ttu-id="1d6b7-138">Указано недопустимое определение индекса.</span><span class="sxs-lookup"><span data-stu-id="1d6b7-138">An invalid index definition was specified.</span></span> <span data-ttu-id="1d6b7-139">Ниже приведены некоторые возможные причины получения этой ошибки.</span><span class="sxs-lookup"><span data-stu-id="1d6b7-139">The following are some possible reasons for receiving this error:</span></span></p>
<ul>
<li><p><span data-ttu-id="1d6b7-140">Первичный индекс является условным (<strong>грбит</strong> член <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> имеет JET_bitIndexPrimary набор, а элемент <strong>ккондитионалколумн</strong> <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> больше нуля).</span><span class="sxs-lookup"><span data-stu-id="1d6b7-140">A primary index is conditional (<strong>grbit</strong> member of <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> has JET_bitIndexPrimary set, and the <strong>cConditionalColumn</strong> member of <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> is greater than zero).</span></span></p></li>
<li><p><span data-ttu-id="1d6b7-141">Windows Server 2003 и более поздние версии Windows.</span><span class="sxs-lookup"><span data-stu-id="1d6b7-141">Windows Server 2003 and later versions of Windows.</span></span> <span data-ttu-id="1d6b7-142">Попытка создать индекс кортежа с ограничениями кортежей, но без передачи сведений в элемент <strong>птуплелимитс</strong> в <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> (то есть <em>грбит</em> имеет набор JET_bitIndexTupleLimits, но указатель <strong>птуплелимитс</strong> имеет значение null).</span><span class="sxs-lookup"><span data-stu-id="1d6b7-142">Attempting to create a tuple index with tuple limits, but without passing information in the <strong>ptuplelimits</strong> member in <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> (that is, <em>grbit</em> has JET_bitIndexTupleLimits set, but the <strong>ptuplelimits</strong> pointer is NULL).</span></span></p></li>
<li><p><span data-ttu-id="1d6b7-143">Передача недопустимого определения ключа в элемент <strong>сзкэй</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> .</span><span class="sxs-lookup"><span data-stu-id="1d6b7-143">Passing in an invalid key definition in the <strong>szKey</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure.</span></span> <span data-ttu-id="1d6b7-144">Описание допустимых определений см. в разделе <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> .</span><span class="sxs-lookup"><span data-stu-id="1d6b7-144">See <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> for a discussion of valid definitions.</span></span></p></li>
<li><p><span data-ttu-id="1d6b7-145">Установка для элемента <strong>кбварсегмак</strong> в <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> значение больше JET_cbPrimaryKeyMost (для первичного индекса) или больше JET_cbSecondaryKeyMost (для вторичного индекса).</span><span class="sxs-lookup"><span data-stu-id="1d6b7-145">Setting the <strong>cbVarSegMac</strong> member in <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> to be greater than JET_cbPrimaryKeyMost (for a primary index) or greater than JET_cbSecondaryKeyMost (for a secondary index).</span></span></p></li>
<li><p><span data-ttu-id="1d6b7-146">Передача недопустимого сочетания для определяемого пользователем индекса в Юникоде (одна из которых имеет бит JET_bitIndexUnicode, заданный в элементе <strong>грбит</strong> в <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>).</span><span class="sxs-lookup"><span data-stu-id="1d6b7-146">Passing an invalid combination for a user-defined Unicode index (one which has the JET_bitIndexUnicode bit set in the <strong>grbit</strong> member of <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>).</span></span> <span data-ttu-id="1d6b7-147">Некоторые распространенные причины могут быть вызваны тем, что поле пидксуникоде структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> имеет значение null или код LCID, указанный в структуре пидксуникоде, является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="1d6b7-147">Some common causes may be that the pidxunicode field of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is NULL, or the LCID specified in the pidxunicode structure is invalid.</span></span></p></li>
<li><p><span data-ttu-id="1d6b7-148">Указание столбца с несколькими значениями для первичного индекса.</span><span class="sxs-lookup"><span data-stu-id="1d6b7-148">Specifying a multi-valued column for a primary index.</span></span></p></li>
<li><p><span data-ttu-id="1d6b7-149">Попытка индексировать слишком много условных столбцов.</span><span class="sxs-lookup"><span data-stu-id="1d6b7-149">Trying to index too many conditional columns.</span></span> <span data-ttu-id="1d6b7-150">Элемент <strong>ккондитионалколумн</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> не должен быть больше JET_ccolKeyMost.</span><span class="sxs-lookup"><span data-stu-id="1d6b7-150">The <strong>cConditionalColumn</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure must not be greater than JET_ccolKeyMost.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d6b7-151">JET_errIndexTuplesInvalidLimits</span><span class="sxs-lookup"><span data-stu-id="1d6b7-151">JET_errIndexTuplesInvalidLimits</span></span></p></td>
<td><p><span data-ttu-id="1d6b7-152">Windows XP и более поздние версии Windows.</span><span class="sxs-lookup"><span data-stu-id="1d6b7-152">Windows XP and later versions of Windows.</span></span> <span data-ttu-id="1d6b7-153">Указана структура <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> , а ее ограничения не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="1d6b7-153">A <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure was specified, and its limits are not supported.</span></span> <span data-ttu-id="1d6b7-154">См. раздел "Примечания" структуры <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> .</span><span class="sxs-lookup"><span data-stu-id="1d6b7-154">See the remarks section of the <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d6b7-155">JET_errIndexTuplesNonUniqueOnly</span><span class="sxs-lookup"><span data-stu-id="1d6b7-155">JET_errIndexTuplesNonUniqueOnly</span></span></p></td>
<td><p><span data-ttu-id="1d6b7-156">Windows XP и более поздние версии Windows.</span><span class="sxs-lookup"><span data-stu-id="1d6b7-156">Windows XP and later versions of Windows.</span></span> <span data-ttu-id="1d6b7-157">Индекс кортежа не может быть уникальным (<em>грбит</em> не должен содержать как JET_bitIndexTuples, так JET_bitIndexUnique Set).</span><span class="sxs-lookup"><span data-stu-id="1d6b7-157">A tuple index cannot be unique (<em>grbit</em> must not have both JET_bitIndexTuples and JET_bitIndexUnique set).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d6b7-158">JET_errIndexTuplesOneColumnOnly</span><span class="sxs-lookup"><span data-stu-id="1d6b7-158">JET_errIndexTuplesOneColumnOnly</span></span></p></td>
<td><p><span data-ttu-id="1d6b7-159">Windows XP и более поздние версии Windows.</span><span class="sxs-lookup"><span data-stu-id="1d6b7-159">Windows XP and later versions of Windows.</span></span> <span data-ttu-id="1d6b7-160">Индекс кортежа может находиться только в одном столбце (то есть элемент <strong>грбит</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> имеет JET_bitIndexTuples набор, а элемент <strong>сзкэй</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> указывает более одного столбца).</span><span class="sxs-lookup"><span data-stu-id="1d6b7-160">A tuple index can only be over a single column (that is, the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure has JET_bitIndexTuples set, and the <strong>szKey</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure specifies more than one column).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d6b7-161">JET_errIndexTuplesSecondaryIndexOnly</span><span class="sxs-lookup"><span data-stu-id="1d6b7-161">JET_errIndexTuplesSecondaryIndexOnly</span></span></p></td>
<td><p><span data-ttu-id="1d6b7-162">Windows XP и более поздние версии Windows.</span><span class="sxs-lookup"><span data-stu-id="1d6b7-162">Windows XP and later versions of Windows.</span></span> <span data-ttu-id="1d6b7-163">Индекс кортежа не может быть первичным индексом (т. е. элемент <strong>грбит</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> не должен иметь одновременно JET_bitIndexPrimary и JET_bitIndexTuples).</span><span class="sxs-lookup"><span data-stu-id="1d6b7-163">A tuple index cannot be a primary index (that is, the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure must not have both JET_bitIndexPrimary and JET_bitIndexTuples set).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d6b7-164">JET_errIndexTuplesTextColumnsOnly</span><span class="sxs-lookup"><span data-stu-id="1d6b7-164">JET_errIndexTuplesTextColumnsOnly</span></span></p></td>
<td><p><span data-ttu-id="1d6b7-165">Windows XP и более поздние версии Windows.</span><span class="sxs-lookup"><span data-stu-id="1d6b7-165">Windows XP and later versions of Windows.</span></span> <span data-ttu-id="1d6b7-166">Индекс кортежа может находиться только в тексте или столбце Юникода.</span><span class="sxs-lookup"><span data-stu-id="1d6b7-166">A tuple index can only be on a text or Unicode column.</span></span> <span data-ttu-id="1d6b7-167">Попытка индексировать другие столбцы (например, двоичные столбцы) приведет к JET_errIndexTuplesTextColumnsOnly.</span><span class="sxs-lookup"><span data-stu-id="1d6b7-167">An attempt to index other columns (for example, binary columns) will result in JET_errIndexTuplesTextColumnsOnly.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d6b7-168">JET_errIndexTuplesVarSegMacNotAllowed</span><span class="sxs-lookup"><span data-stu-id="1d6b7-168">JET_errIndexTuplesVarSegMacNotAllowed</span></span></p></td>
<td><p><span data-ttu-id="1d6b7-169">Windows XP и более поздние версии Windows.</span><span class="sxs-lookup"><span data-stu-id="1d6b7-169">Windows XP and later versions of Windows.</span></span> <span data-ttu-id="1d6b7-170">Индекс кортежа не позволяет установить элемент <strong>кбварсегмак</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> .</span><span class="sxs-lookup"><span data-stu-id="1d6b7-170">A tuple index does not allow the <strong>cbVarSegMac</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure to be set.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d6b7-171">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="1d6b7-171">JET_errInTransaction</span></span></p></td>
<td><p><span data-ttu-id="1d6b7-172">Предпринята попытка создать индекс без сведений о версии во время транзакции.</span><span class="sxs-lookup"><span data-stu-id="1d6b7-172">An attempt was made to create an index without version information while in a transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d6b7-173">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="1d6b7-173">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="1d6b7-174">Определение индекса недопустимо, так как элемент <strong>грбит</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> содержит неправильные значения.</span><span class="sxs-lookup"><span data-stu-id="1d6b7-174">The index definition is invalid because the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure contains inconsistent values.</span></span> <span data-ttu-id="1d6b7-175">Ниже приведены некоторые возможные причины.</span><span class="sxs-lookup"><span data-stu-id="1d6b7-175">The following are some possible reasons:</span></span></p>
<ul>
<li><p><span data-ttu-id="1d6b7-176">В первичном индексе указан бит игнорирования (JET_bitIndexPrimary был передан с одним из JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull или JET_bitIndexIgnoreFirstNull).</span><span class="sxs-lookup"><span data-stu-id="1d6b7-176">A primary index had an ignore bit specified (JET_bitIndexPrimary was passed with one of JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull, or JET_bitIndexIgnoreFirstNull).</span></span></p></li>
<li><p><span data-ttu-id="1d6b7-177">Пустой индекс не игнорирует какие-либо поля NULL (т. е. элемент <strong>грбит</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> JET_bitIndexEmpty задан, но не имеет набора JET_bitIndexIgnoreAnyNull).</span><span class="sxs-lookup"><span data-stu-id="1d6b7-177">An empty index does not ignore any NULL fields (that is, <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure has JET_bitIndexEmpty set, but does not have JET_bitIndexIgnoreAnyNull set).</span></span></p></li>
<li><p><span data-ttu-id="1d6b7-178">Передача структуры <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> с недопустимым элементом <strong>грбит</strong> .</span><span class="sxs-lookup"><span data-stu-id="1d6b7-178">Passing in a <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> structure with an invalid <strong>grbit</strong> member.</span></span> <span data-ttu-id="1d6b7-179">См. <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a>.</span><span class="sxs-lookup"><span data-stu-id="1d6b7-179">See <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a>.</span></span></p></li>
</ul>
<p><span data-ttu-id="1d6b7-180">При создании нескольких индексов одновременно (то есть если параметр <em>Циндекскреате</em> больше единицы) ни один из индексов не может содержать следующие биты:</span><span class="sxs-lookup"><span data-stu-id="1d6b7-180">When creating several indexes at once (that is, if the <em>cIndexCreate</em> parameter is greater than one), none of the indexes may contain any of the following bits:</span></span></p>
<ul>
<li><p><span data-ttu-id="1d6b7-181">JET_bitIndexPrimary</span><span class="sxs-lookup"><span data-stu-id="1d6b7-181">JET_bitIndexPrimary</span></span></p></li>
<li><p><span data-ttu-id="1d6b7-182">JET_bitIndexUnversioned</span><span class="sxs-lookup"><span data-stu-id="1d6b7-182">JET_bitIndexUnversioned</span></span></p></li>
<li><p><span data-ttu-id="1d6b7-183">JET_bitIndexEmpty</span><span class="sxs-lookup"><span data-stu-id="1d6b7-183">JET_bitIndexEmpty</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d6b7-184">JET_errInvalidLanguageId</span><span class="sxs-lookup"><span data-stu-id="1d6b7-184">JET_errInvalidLanguageId</span></span></p></td>
<td><p><span data-ttu-id="1d6b7-185">Передан недопустимый код локали (LCID) (с помощью элемента <strong>LCID</strong> в структуре <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> , которой элемент <strong>пидксуникоде</strong> в структуре <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> содержит указатель на или с помощью элемента <strong>LCID</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ).</span><span class="sxs-lookup"><span data-stu-id="1d6b7-185">An invalid Locale ID (LCID) was passed in (either through the <strong>lcid</strong> member in the <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> structure, which the <strong>pidxunicode</strong> member in the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure contains a pointer to, or through the <strong>lcid</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d6b7-186">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="1d6b7-186">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="1d6b7-187">Указано недопустимое имя индекса.</span><span class="sxs-lookup"><span data-stu-id="1d6b7-187">An invalid index name was specified.</span></span> <span data-ttu-id="1d6b7-188">Дополнительные сведения см. в разделе <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> .</span><span class="sxs-lookup"><span data-stu-id="1d6b7-188">See <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> for more details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d6b7-189">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="1d6b7-189">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="1d6b7-190">В API передан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="1d6b7-190">An invalid parameter was passed into the API.</span></span> <span data-ttu-id="1d6b7-191">Ниже приведены некоторые причины, по которым может быть возвращена эта ошибка:</span><span class="sxs-lookup"><span data-stu-id="1d6b7-191">The following are some reasons why this error may be returned:</span></span></p>
<ul>
<li><p><span data-ttu-id="1d6b7-192">Поле <strong>cbKey</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> имеет значение 0.</span><span class="sxs-lookup"><span data-stu-id="1d6b7-192">The <strong>cbKey</strong> field of a <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is set to zero.</span></span></p></li>
<li><p><span data-ttu-id="1d6b7-193">Элементу <strong>кбструкт</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> не присвоено значение sizeof ( <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ).</span><span class="sxs-lookup"><span data-stu-id="1d6b7-193">The <strong>cbStruct</strong> member of a <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is not set to sizeof( <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ).</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d6b7-194">JET_errUnicodeTranslationFail</span><span class="sxs-lookup"><span data-stu-id="1d6b7-194">JET_errUnicodeTranslationFail</span></span></p></td>
<td><p><span data-ttu-id="1d6b7-195">Произошла ошибка при попытке нормализовать столбец в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="1d6b7-195">An error occurred while trying to normalize a Unicode column.</span></span> <span data-ttu-id="1d6b7-196">Это может быть вызвано недостатком системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1d6b7-196">This can be caused by running out of system resources.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d6b7-197">JET_errSpaceHintsInvalid</span><span class="sxs-lookup"><span data-stu-id="1d6b7-197">JET_errSpaceHintsInvalid</span></span></p></td>
<td><p><span data-ttu-id="1d6b7-198">Неверное или неправильное действие элемента структуры подсказок пространства JET.</span><span class="sxs-lookup"><span data-stu-id="1d6b7-198">An element of the JET space hints structure was not correct or actionable.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="1d6b7-199">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1d6b7-199">Remarks</span></span>

<span data-ttu-id="1d6b7-200">Возвращаемое значение JET_errSuccess при успешном завершении всех указанных индексов.</span><span class="sxs-lookup"><span data-stu-id="1d6b7-200">The return value is JET_errSuccess on successful completion of all indexes specified.</span></span>

<span data-ttu-id="1d6b7-201">**JetCreateIndex3** перебирает индексы, заданные в **пиндекскреате**, и иногда прерываются при первом сбое.</span><span class="sxs-lookup"><span data-stu-id="1d6b7-201">**JetCreateIndex3** iterates through the indexes given in **pindexcreate**, and will sometimes abort on the first failure.</span></span> <span data-ttu-id="1d6b7-202">Любые индексы после первого индекса с ошибкой могут не попытаться, несмотря на то, что элемент **Err** структуры [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) содержит JET_errSuccess.</span><span class="sxs-lookup"><span data-stu-id="1d6b7-202">Any indexes after the first index with an error may not have been attempted, even though the **err** member of the [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) structure contains JET_errSuccess.</span></span>

#### <a name="requirements"></a><span data-ttu-id="1d6b7-203">Требования</span><span class="sxs-lookup"><span data-stu-id="1d6b7-203">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1d6b7-204"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="1d6b7-204"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="1d6b7-205">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="1d6b7-205">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d6b7-206"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="1d6b7-206"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="1d6b7-207">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="1d6b7-207">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d6b7-208"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="1d6b7-208"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="1d6b7-209">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="1d6b7-209">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d6b7-210"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="1d6b7-210"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="1d6b7-211">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="1d6b7-211">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d6b7-212"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="1d6b7-212"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="1d6b7-213">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="1d6b7-213">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d6b7-214"><strong>Юникод</strong></span><span class="sxs-lookup"><span data-stu-id="1d6b7-214"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="1d6b7-215">Реализуется как <strong>JetCreateIndex3W</strong> (Юникод) и <strong>JetCreateIndex3A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="1d6b7-215">Implemented as <strong>JetCreateIndex3W</strong> (Unicode) and <strong>JetCreateIndex3A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="1d6b7-216">См. также:</span><span class="sxs-lookup"><span data-stu-id="1d6b7-216">See Also</span></span>

[<span data-ttu-id="1d6b7-217">JET_CONDITIONALCOLUMN</span><span class="sxs-lookup"><span data-stu-id="1d6b7-217">JET_CONDITIONALCOLUMN</span></span>](./jet-conditionalcolumn-structure.md)  
[<span data-ttu-id="1d6b7-218">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="1d6b7-218">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="1d6b7-219">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="1d6b7-219">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="1d6b7-220">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="1d6b7-220">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="1d6b7-221">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="1d6b7-221">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="1d6b7-222">JET_INDEXCREATE2</span><span class="sxs-lookup"><span data-stu-id="1d6b7-222">JET_INDEXCREATE2</span></span>](./jet-indexcreate2-structure.md)  
[<span data-ttu-id="1d6b7-223">жеткреатеиндекс</span><span class="sxs-lookup"><span data-stu-id="1d6b7-223">JetCreateIndex</span></span>](./jetcreateindex-function.md)  
[<span data-ttu-id="1d6b7-224">жеткреатетаблеколумниндекс</span><span class="sxs-lookup"><span data-stu-id="1d6b7-224">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="1d6b7-225">JetCreateTableColumnIndex2</span><span class="sxs-lookup"><span data-stu-id="1d6b7-225">JetCreateTableColumnIndex2</span></span>](./jetcreatetablecolumnindex2-function.md)  
[<span data-ttu-id="1d6b7-226">JET_SPACEHINTS</span><span class="sxs-lookup"><span data-stu-id="1d6b7-226">JET_SPACEHINTS</span></span>](./jet-spacehints-structure.md)
