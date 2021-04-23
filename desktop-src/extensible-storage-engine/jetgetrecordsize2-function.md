---
description: Дополнительные сведения о функции JetGetRecordSize2
title: Функция JetGetRecordSize2
TOCTitle: JetGetRecordSize2 Function
ms:assetid: 803cfb4e-44f3-447a-b642-018e6f2f713f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269314(v=EXCHG.10)
ms:contentKeyID: 32765604
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetRecordSize2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5c68eafaaa53b5b88e6b003bdbafce287035cbc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105713139"
---
# <a name="jetgetrecordsize2-function"></a><span data-ttu-id="e2203-103">Функция JetGetRecordSize2</span><span class="sxs-lookup"><span data-stu-id="e2203-103">JetGetRecordSize2 Function</span></span>


<span data-ttu-id="e2203-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="e2203-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetrecordsize2-function"></a><span data-ttu-id="e2203-105">Функция JetGetRecordSize2</span><span class="sxs-lookup"><span data-stu-id="e2203-105">JetGetRecordSize2 Function</span></span>

<span data-ttu-id="e2203-106">Функция **JetGetRecordSize2** извлекает сведения о размере записи из нужного расположения.</span><span class="sxs-lookup"><span data-stu-id="e2203-106">The **JetGetRecordSize2** function retrieves record size information from the desired location.</span></span>

<span data-ttu-id="e2203-107">**Windows 7: JetGetRecordSize2** появился в операционной системе Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e2203-107">**Windows 7:  JetGetRecordSize2** is introduced in the Windows 7 operating system.</span></span>

```cpp
    JET_ERR JET_API JetGetRecordSize2(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         JET_RECSIZE2* precsize,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="e2203-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e2203-108">Parameters</span></span>

<span data-ttu-id="e2203-109">*сесид*</span><span class="sxs-lookup"><span data-stu-id="e2203-109">*sesid*</span></span>

<span data-ttu-id="e2203-110">Определяет контекст сеанса базы данных, который будет использоваться для вызова API.</span><span class="sxs-lookup"><span data-stu-id="e2203-110">Identifies the database session context that will be used for the API call.</span></span>

<span data-ttu-id="e2203-111">*TableID*</span><span class="sxs-lookup"><span data-stu-id="e2203-111">*tableid*</span></span>

<span data-ttu-id="e2203-112">Определяет таблицу или курсор, которые будут использоваться для вызова API.</span><span class="sxs-lookup"><span data-stu-id="e2203-112">Identifies the table or cursor that will be used for the API call.</span></span> <span data-ttu-id="e2203-113">Курсор должен быть размещен в записи или иметь подготовленное обновление.</span><span class="sxs-lookup"><span data-stu-id="e2203-113">The cursor must be positioned on a record, or have an update prepared.</span></span>

<span data-ttu-id="e2203-114">*прексизе*</span><span class="sxs-lookup"><span data-stu-id="e2203-114">*precsize*</span></span>

<span data-ttu-id="e2203-115">Указатель на выходной буфер для структуры [JET_RECSIZE2](./jet-recsize2-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="e2203-115">A pointer to an output buffer for the [JET_RECSIZE2](./jet-recsize2-structure.md) structure.</span></span>

<span data-ttu-id="e2203-116">*грбит*</span><span class="sxs-lookup"><span data-stu-id="e2203-116">*grbit*</span></span>

<span data-ttu-id="e2203-117">Это одно или несколько из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="e2203-117">This is one or more of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e2203-118">Значение</span><span class="sxs-lookup"><span data-stu-id="e2203-118">Value</span></span></p></th>
<th><p><span data-ttu-id="e2203-119">Значение</span><span class="sxs-lookup"><span data-stu-id="e2203-119">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e2203-120">JET_bitRecordSizeInCopyBuffer</span><span class="sxs-lookup"><span data-stu-id="e2203-120">JET_bitRecordSizeInCopyBuffer</span></span></p></td>
<td><p><span data-ttu-id="e2203-121">Это Извлекает размер записи, которая находится в буфере копирования, подготовленном для обновления.</span><span class="sxs-lookup"><span data-stu-id="e2203-121">This retrieves the size of the record that is in the copy buffer prepared for update.</span></span> <span data-ttu-id="e2203-122">В противном случае <em>tableid</em> или курсор должны быть расположены в записи, и эта запись будет использоваться.</span><span class="sxs-lookup"><span data-stu-id="e2203-122">Otherwise, the <em>tableid</em> or cursor must be positioned on a record, and that record will be used.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2203-123">JET_bitRecordSizeRunningTotal</span><span class="sxs-lookup"><span data-stu-id="e2203-123">JET_bitRecordSizeRunningTotal</span></span></p></td>
<td><p><span data-ttu-id="e2203-124">Если этот бит указан, то перед заполнением содержимого <a href="gg269174(v=exchg.10).md">JET_RECSIZE2</a> не обнуляются, эффективно выполняя сбор статистики по нескольким просмотренным или обновленным записям.</span><span class="sxs-lookup"><span data-stu-id="e2203-124">When this bit is specified, the <a href="gg269174(v=exchg.10).md">JET_RECSIZE2</a> is not zeroed before filling the contents, effectively acting as an accumulation of the statistics for multiple records visited or updated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2203-125">JET_bitRecordSizeLocal</span><span class="sxs-lookup"><span data-stu-id="e2203-125">JET_bitRecordSizeLocal</span></span></p></td>
<td><p><span data-ttu-id="e2203-126">Это приводит к тому, что API пропускает не внутренние значения long.</span><span class="sxs-lookup"><span data-stu-id="e2203-126">This causes the API to ignore non-intrinsic Long Values.</span></span> <span data-ttu-id="e2203-127">Например, будет использоваться только локальная запись на странице.</span><span class="sxs-lookup"><span data-stu-id="e2203-127">For example, only the local record on the page will be used.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="e2203-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e2203-128">Return Value</span></span>

<span data-ttu-id="e2203-129">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="e2203-129">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="e2203-130">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="e2203-130">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e2203-131">Код возврата</span><span class="sxs-lookup"><span data-stu-id="e2203-131">Return code</span></span></p></th>
<th><p><span data-ttu-id="e2203-132">Описание</span><span class="sxs-lookup"><span data-stu-id="e2203-132">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e2203-133">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="e2203-133">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="e2203-134">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="e2203-134">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2203-135">JET_errInvalidGrbit</span><span class="sxs-lookup"><span data-stu-id="e2203-135">JET_errInvalidGrbit</span></span></p></td>
<td><p><span data-ttu-id="e2203-136">Один из запрошенных параметров недопустим или не реализован.</span><span class="sxs-lookup"><span data-stu-id="e2203-136">One of the requested options was invalid or not implemented.</span></span> <span data-ttu-id="e2203-137">Эта ошибка будет возвращена функцией <strong>JetGetRecordSize2</strong> при указании недопустимого <em>грбит</em> .</span><span class="sxs-lookup"><span data-stu-id="e2203-137">This error will be returned by the <strong>JetGetRecordSize2</strong> function when an illegal <em>grbit</em> is specified.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2203-138">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="e2203-138">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="e2203-139">Невозможно выполнить операцию, так как экземпляр, связанный с сеансом, не был инициализирован.</span><span class="sxs-lookup"><span data-stu-id="e2203-139">It is not possible to complete the operation because the instance associated with the session has not been initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2203-140">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="e2203-140">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="e2203-141">Невозможно выполнить операцию, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</span><span class="sxs-lookup"><span data-stu-id="e2203-141">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2203-142">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="e2203-142">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="e2203-143">Невозможно выполнить операцию, поскольку экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</span><span class="sxs-lookup"><span data-stu-id="e2203-143">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="e2203-144"><strong>Windows XP:  </strong> JET_errInstanceUnavailable будут возвращаться только операционной системой Windows XP и более поздними версиями Windows.</span><span class="sxs-lookup"><span data-stu-id="e2203-144"><strong>Windows XP:  </strong>JET_errInstanceUnavailable will only be returned by the Windows XP operating system and later versions of Windows.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2203-145">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="e2203-145">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="e2203-146">Невозможно выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</span><span class="sxs-lookup"><span data-stu-id="e2203-146">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2203-147">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="e2203-147">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="e2203-148">Невозможно выполнить операцию, так как в экземпляре, связанном с сеансом, выполняется операция восстановления.</span><span class="sxs-lookup"><span data-stu-id="e2203-148">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2203-149">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="e2203-149">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="e2203-150">Нельзя использовать один сеанс для нескольких потоков одновременно.</span><span class="sxs-lookup"><span data-stu-id="e2203-150">It is illegal to use the same session for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="e2203-151"><strong>Windows XP:  </strong> JET_errInstanceUnavailable будут возвращаться только Windows XP и более поздними версиями Windows.</span><span class="sxs-lookup"><span data-stu-id="e2203-151"><strong>Windows XP:  </strong>JET_errInstanceUnavailable will only be returned by Windows XP and later versions of Windows.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2203-152">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="e2203-152">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="e2203-153">Это может произойти, если курсор был размещен неправильно.</span><span class="sxs-lookup"><span data-stu-id="e2203-153">This can happen if the cursor was positioned incorrectly.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2203-154">JET_errRecordDeleted</span><span class="sxs-lookup"><span data-stu-id="e2203-154">JET_errRecordDeleted</span></span></p></td>
<td><p><span data-ttu-id="e2203-155">Если курсор не был помещен в транзакцию, это может произойти, если другой поток удаляет запись из этого сеанса.</span><span class="sxs-lookup"><span data-stu-id="e2203-155">If the cursor was not positioned in a transaction, this can happen if another thread deletes the record out from under this session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2203-156">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="e2203-156">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="e2203-157">Это может быть возвращено, если передано <strong>значение NULL</strong><em>прексизе</em> .</span><span class="sxs-lookup"><span data-stu-id="e2203-157">This can be returned if a <strong>NULL</strong><em>precsize</em> was passed.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="e2203-158">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e2203-158">Remarks</span></span>

<span data-ttu-id="e2203-159">Размер ключа, накопленного в поле **кбоверхеад** [JET_RECSIZE2](./jet-recsize2-structure.md), зависит от JET_bitRecordSizeInCopyBuffer.</span><span class="sxs-lookup"><span data-stu-id="e2203-159">The size of the key accumulated in the **cbOverhead** field of [JET_RECSIZE2](./jet-recsize2-structure.md), is affected by JET_bitRecordSizeInCopyBuffer.</span></span> <span data-ttu-id="e2203-160">Если этот бит указан, размер ключа, накопленный в поле **кбоверхеад** , является полным размером ключа.</span><span class="sxs-lookup"><span data-stu-id="e2203-160">If this bit is specified, the key size accumulated in the **cbOverhead** field is the full key size.</span></span> <span data-ttu-id="e2203-161">Если этот бит не используется, размер ключа, накопленный, не будет включать размер, сохраненный из-за сжатия префикса ключа.</span><span class="sxs-lookup"><span data-stu-id="e2203-161">If this bit is not used, the key size accumulated will not include any size saved due to key prefix compression.</span></span>

#### <a name="requirements"></a><span data-ttu-id="e2203-162">Требования</span><span class="sxs-lookup"><span data-stu-id="e2203-162">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e2203-163"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="e2203-163"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="e2203-164">Требуется Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e2203-164">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2203-165"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="e2203-165"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="e2203-166">Требуется Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="e2203-166">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2203-167"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="e2203-167"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="e2203-168">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="e2203-168">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2203-169"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="e2203-169"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="e2203-170">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="e2203-170">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2203-171"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="e2203-171"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="e2203-172">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="e2203-172">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="e2203-173">См. также:</span><span class="sxs-lookup"><span data-stu-id="e2203-173">See Also</span></span>

[<span data-ttu-id="e2203-174">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="e2203-174">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="e2203-175">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="e2203-175">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="e2203-176">JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="e2203-176">JET_RECSIZE</span></span>](./jet-recsize-structure.md)  
[<span data-ttu-id="e2203-177">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="e2203-177">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="e2203-178">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="e2203-178">JET_TABLEID</span></span>](./jet-tableid.md)
