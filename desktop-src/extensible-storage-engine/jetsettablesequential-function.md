---
description: Дополнительные сведения о функции Жетсеттаблесекуентиал
title: Функция Жетсеттаблесекуентиал
TOCTitle: JetSetTableSequential Function
ms:assetid: 874ddd3c-0d69-4d48-b61a-e9e0457426ef
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269323(v=EXCHG.10)
ms:contentKeyID: 32765613
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetTableSequential
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b633b348b712e446535054c5a39d2768236b7705
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710932"
---
# <a name="jetsettablesequential-function"></a><span data-ttu-id="5d22c-103">Функция Жетсеттаблесекуентиал</span><span class="sxs-lookup"><span data-stu-id="5d22c-103">JetSetTableSequential Function</span></span>


<span data-ttu-id="5d22c-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="5d22c-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetsettablesequential-function"></a><span data-ttu-id="5d22c-105">Функция Жетсеттаблесекуентиал</span><span class="sxs-lookup"><span data-stu-id="5d22c-105">JetSetTableSequential Function</span></span>

<span data-ttu-id="5d22c-106">Функция **жетсеттаблесекуентиал** уведомляет ядро СУБД о том, что приложение сканирует весь текущий индекс, содержащий данный курсор.</span><span class="sxs-lookup"><span data-stu-id="5d22c-106">The **JetSetTableSequential** function notifies the database engine that the application is scanning the entire current index that contains a given cursor.</span></span> <span data-ttu-id="5d22c-107">Следовательно, методы, используемые для доступа к данным индекса, будут настроены таким образом, чтобы сделать этот сценарий максимально быстрым.</span><span class="sxs-lookup"><span data-stu-id="5d22c-107">Consequently, the methods that are used to access the index data will be tuned to make this scenario as fast as possible.</span></span>

<span data-ttu-id="5d22c-108">**Windows XP:**  **Жетсеттаблесекуентиал** появился в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="5d22c-108">**Windows XP:**  **JetSetTableSequential** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetSetTableSequential(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="5d22c-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="5d22c-109">Parameters</span></span>

<span data-ttu-id="5d22c-110">*сесид*</span><span class="sxs-lookup"><span data-stu-id="5d22c-110">*sesid*</span></span>

<span data-ttu-id="5d22c-111">Сеанс, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="5d22c-111">The session to use for this call.</span></span>

<span data-ttu-id="5d22c-112">*TableID*</span><span class="sxs-lookup"><span data-stu-id="5d22c-112">*tableid*</span></span>

<span data-ttu-id="5d22c-113">Курсор, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="5d22c-113">The cursor to use for this call.</span></span>

<span data-ttu-id="5d22c-114">*грбит*</span><span class="sxs-lookup"><span data-stu-id="5d22c-114">*grbit*</span></span>

<span data-ttu-id="5d22c-115">Группа битов, задающих ноль или более следующих параметров.</span><span class="sxs-lookup"><span data-stu-id="5d22c-115">A group of bits that specify zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5d22c-116">Значение</span><span class="sxs-lookup"><span data-stu-id="5d22c-116">Value</span></span></p></th>
<th><p><span data-ttu-id="5d22c-117">Значение</span><span class="sxs-lookup"><span data-stu-id="5d22c-117">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5d22c-118">JET_bitPrereadForward</span><span class="sxs-lookup"><span data-stu-id="5d22c-118">JET_bitPrereadForward</span></span></p></td>
<td><p><span data-ttu-id="5d22c-119">Этот параметр используется для индексирования в прямом направлении.</span><span class="sxs-lookup"><span data-stu-id="5d22c-119">This option is used to index in the forward direction.</span></span></p>
<p><span data-ttu-id="5d22c-120"><strong>Windows 7:</strong>  <strong>JET_bitPrereadForward</strong> введен в Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5d22c-120"><strong>Windows 7:</strong>  <strong>JET_bitPrereadForward</strong> is introduced in Windows 7.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d22c-121">JET_bitPrereadBackward</span><span class="sxs-lookup"><span data-stu-id="5d22c-121">JET_bitPrereadBackward</span></span></p></td>
<td><p><span data-ttu-id="5d22c-122">Этот параметр используется для индексации в обратном направлении.</span><span class="sxs-lookup"><span data-stu-id="5d22c-122">This option is used to index in the backward direction.</span></span></p>
<p><span data-ttu-id="5d22c-123"><strong>Windows 7:</strong>  <strong>JET_bitPrereadBackward</strong> введен в Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5d22c-123"><strong>Windows 7:</strong>  <strong>JET_bitPrereadBackward</strong> is introduced in Windows 7.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="5d22c-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5d22c-124">Return Value</span></span>

<span data-ttu-id="5d22c-125">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="5d22c-125">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="5d22c-126">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="5d22c-126">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5d22c-127">Код возврата</span><span class="sxs-lookup"><span data-stu-id="5d22c-127">Return code</span></span></p></th>
<th><p><span data-ttu-id="5d22c-128">Описание</span><span class="sxs-lookup"><span data-stu-id="5d22c-128">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5d22c-129">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="5d22c-129">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="5d22c-130">Операция не может быть завершена, так как все действия в экземпляре, связанном с сеансом, были заморожены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</span><span class="sxs-lookup"><span data-stu-id="5d22c-130">The operation cannot complete because all activity on the instance that is associated with the session has been quiesced as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d22c-131">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="5d22c-131">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="5d22c-132">Операция не может быть завершена, так как экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</span><span class="sxs-lookup"><span data-stu-id="5d22c-132">The operation cannot complete because the instance that is associated with the session encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="5d22c-133"><strong>Windows XP:</strong>  Это возвращаемое значение введено в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="5d22c-133"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5d22c-134">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="5d22c-134">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="5d22c-135">Операция не может быть завершена, так как экземпляр, связанный с сеансом, еще не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="5d22c-135">The operation cannot complete because the instance that is associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d22c-136">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="5d22c-136">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="5d22c-137">Операция не может быть завершена, так как выполняется операция восстановления на экземпляре, связанном с сеансом.</span><span class="sxs-lookup"><span data-stu-id="5d22c-137">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5d22c-138">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="5d22c-138">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="5d22c-139">Не удается выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</span><span class="sxs-lookup"><span data-stu-id="5d22c-139">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5d22c-140">Если эта функция выполнена, текущий индекс курсора оптимизирован для последовательного просмотра всего индекса.</span><span class="sxs-lookup"><span data-stu-id="5d22c-140">If this function succeeds, the current index of the cursor is optimized for a sequential scan of the entire index.</span></span> <span data-ttu-id="5d22c-141">Изменение состояния базы данных не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5d22c-141">No change to the database state will occur.</span></span>

<span data-ttu-id="5d22c-142">Если эта функция завершается неудачно, не выполняется никаких изменений в конфигурации курсора.</span><span class="sxs-lookup"><span data-stu-id="5d22c-142">If this function fails, no change to the configuration of the cursor will occur.</span></span> <span data-ttu-id="5d22c-143">Изменение состояния базы данных не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5d22c-143">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="5d22c-144">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5d22c-144">Remarks</span></span>

<span data-ttu-id="5d22c-145">Если приложению требуется эффективно сканировать известное подмножество индекса, подобная оптимизация также выполняется при каждом создании диапазона индексов с помощью [жетсетиндексранже](./jetsetindexrange-function.md).</span><span class="sxs-lookup"><span data-stu-id="5d22c-145">If the application needs to efficiently scan a known subset of an index, a similar optimization is also performed whenever an index range is established by using [JetSetIndexRange](./jetsetindexrange-function.md).</span></span> <span data-ttu-id="5d22c-146">Эта оптимизация доступна только в Windows XP и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="5d22c-146">This optimization is only available on Windows XP and later releases.</span></span>

<span data-ttu-id="5d22c-147">Если приложению нужно эффективно сканировать неизвестное подмножество индекса, никакие действия не выполняются.</span><span class="sxs-lookup"><span data-stu-id="5d22c-147">If the application needs to efficiently scan an unknown subset of an index, no action should be taken.</span></span> <span data-ttu-id="5d22c-148">Подсистема может автоматически обнаружить поведение при сканировании и будет получать данные заранее.</span><span class="sxs-lookup"><span data-stu-id="5d22c-148">The engine can automatically detect scanning behavior and will fetch data ahead of time.</span></span> <span data-ttu-id="5d22c-149">Однако это поведение не так агрессивно.</span><span class="sxs-lookup"><span data-stu-id="5d22c-149">This behavior is not as aggressive, however.</span></span>

<span data-ttu-id="5d22c-150">Эта оптимизация обеспечит эффективную проверку первичного индекса и сделает проверку данных записи индекса вторичным индексом эффективной.</span><span class="sxs-lookup"><span data-stu-id="5d22c-150">This optimization will make scanning the primary index efficient and will make scanning just the index entry data in a secondary index efficient.</span></span> <span data-ttu-id="5d22c-151">При этом не выполняется проверка вторичного индекса при получении данных о неэффективном доступе к записям.</span><span class="sxs-lookup"><span data-stu-id="5d22c-151">It will not make scanning a secondary index while retrieving record data efficient.</span></span> <span data-ttu-id="5d22c-152">Это обусловлено тем, что модуль не выполняет упреждающее чтение данных записи.</span><span class="sxs-lookup"><span data-stu-id="5d22c-152">This is because the engine does not perform a read-ahead on the record data.</span></span>

#### <a name="requirements"></a><span data-ttu-id="5d22c-153">Требования</span><span class="sxs-lookup"><span data-stu-id="5d22c-153">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5d22c-154"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="5d22c-154"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="5d22c-155">Требуется Windows Vista или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="5d22c-155">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d22c-156"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="5d22c-156"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="5d22c-157">Требуется Windows Server 2008 или Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="5d22c-157">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5d22c-158"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="5d22c-158"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="5d22c-159">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="5d22c-159">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d22c-160"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="5d22c-160"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="5d22c-161">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="5d22c-161">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5d22c-162"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="5d22c-162"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="5d22c-163">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="5d22c-163">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="5d22c-164">См. также:</span><span class="sxs-lookup"><span data-stu-id="5d22c-164">See Also</span></span>

[<span data-ttu-id="5d22c-165">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="5d22c-165">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="5d22c-166">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="5d22c-166">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="5d22c-167">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="5d22c-167">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="5d22c-168">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="5d22c-168">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="5d22c-169">жетсетиндексранже</span><span class="sxs-lookup"><span data-stu-id="5d22c-169">JetSetIndexRange</span></span>](./jetsetindexrange-function.md)  
[<span data-ttu-id="5d22c-170">жетстопсервице</span><span class="sxs-lookup"><span data-stu-id="5d22c-170">JetStopService</span></span>](./jetstopservice-function.md)
