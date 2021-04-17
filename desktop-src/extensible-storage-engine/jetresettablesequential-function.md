---
description: Дополнительные сведения о функции Жетресеттаблесекуентиал
title: Функция Жетресеттаблесекуентиал
TOCTitle: JetResetTableSequential Function
ms:assetid: 5fe9daf2-5ef1-46d6-b0c3-ef92fb57d8bb
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269261(v=EXCHG.10)
ms:contentKeyID: 32765563
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetResetTableSequential
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 86de80ac935af81fd2b4e8fdfef8b20dbb8d27d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702349"
---
# <a name="jetresettablesequential-function"></a><span data-ttu-id="e9a9b-103">Функция Жетресеттаблесекуентиал</span><span class="sxs-lookup"><span data-stu-id="e9a9b-103">JetResetTableSequential Function</span></span>


<span data-ttu-id="e9a9b-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="e9a9b-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetresettablesequential-function"></a><span data-ttu-id="e9a9b-105">Функция Жетресеттаблесекуентиал</span><span class="sxs-lookup"><span data-stu-id="e9a9b-105">JetResetTableSequential Function</span></span>

<span data-ttu-id="e9a9b-106">Функция **жетресеттаблесекуентиал** уведомляет ядро СУБД о том, что приложение больше не сканирует весь текущий индекс, содержащий данный курсор.</span><span class="sxs-lookup"><span data-stu-id="e9a9b-106">The **JetResetTableSequential** function notifies the database engine that the application is no longer scanning the entire current index containing a given cursor.</span></span> <span data-ttu-id="e9a9b-107">Этот вызов обращается к отправке уведомления, отправленного [жетсеттаблесекуентиал](./jetsettablesequential-function.md).</span><span class="sxs-lookup"><span data-stu-id="e9a9b-107">This call reverses a notification sent by [JetSetTableSequential](./jetsettablesequential-function.md).</span></span>

<span data-ttu-id="e9a9b-108">**Windows XP:**   **Жетресеттаблесекуентиал** появился в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e9a9b-108">**Windows XP:**   **JetResetTableSequential** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetResetTableSequential(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="e9a9b-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="e9a9b-109">Parameters</span></span>

<span data-ttu-id="e9a9b-110">*сесид*</span><span class="sxs-lookup"><span data-stu-id="e9a9b-110">*sesid*</span></span>

<span data-ttu-id="e9a9b-111">Сеанс, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="e9a9b-111">The session to use for this call.</span></span>

<span data-ttu-id="e9a9b-112">*TableID*</span><span class="sxs-lookup"><span data-stu-id="e9a9b-112">*tableid*</span></span>

<span data-ttu-id="e9a9b-113">Курсор, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="e9a9b-113">The cursor to use for this call.</span></span>

<span data-ttu-id="e9a9b-114">*грбит*</span><span class="sxs-lookup"><span data-stu-id="e9a9b-114">*grbit*</span></span>

<span data-ttu-id="e9a9b-115">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="e9a9b-115">Reserved for future use.</span></span>

### <a name="return-value"></a><span data-ttu-id="e9a9b-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e9a9b-116">Return Value</span></span>

<span data-ttu-id="e9a9b-117">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="e9a9b-117">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="e9a9b-118">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="e9a9b-118">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e9a9b-119">Код возврата</span><span class="sxs-lookup"><span data-stu-id="e9a9b-119">Return code</span></span></p></th>
<th><p><span data-ttu-id="e9a9b-120">Описание</span><span class="sxs-lookup"><span data-stu-id="e9a9b-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e9a9b-121">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="e9a9b-121">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="e9a9b-122">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="e9a9b-122">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9a9b-123">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="e9a9b-123">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="e9a9b-124">Невозможно выполнить операцию, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</span><span class="sxs-lookup"><span data-stu-id="e9a9b-124">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9a9b-125">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="e9a9b-125">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="e9a9b-126">Невозможно выполнить операцию, поскольку экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</span><span class="sxs-lookup"><span data-stu-id="e9a9b-126">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="e9a9b-127">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="e9a9b-127">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9a9b-128">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="e9a9b-128">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="e9a9b-129">Невозможно выполнить операцию, так как экземпляр, связанный с сеансом, еще не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="e9a9b-129">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9a9b-130">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="e9a9b-130">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="e9a9b-131">Невозможно выполнить операцию, так как в экземпляре, связанном с сеансом, выполняется операция восстановления.</span><span class="sxs-lookup"><span data-stu-id="e9a9b-131">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9a9b-132">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="e9a9b-132">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="e9a9b-133">Невозможно выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</span><span class="sxs-lookup"><span data-stu-id="e9a9b-133">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e9a9b-134">При успешном выполнении текущий индекс курсора больше не будет оптимизирован для последовательного просмотра всего индекса.</span><span class="sxs-lookup"><span data-stu-id="e9a9b-134">On success, the current index of the cursor is no longer optimized for a sequential scan of the entire index.</span></span> <span data-ttu-id="e9a9b-135">Изменение состояния базы данных не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e9a9b-135">No change to the database state will occur.</span></span>

<span data-ttu-id="e9a9b-136">В случае сбоя не произойдет никаких изменений в конфигурации курсора.</span><span class="sxs-lookup"><span data-stu-id="e9a9b-136">On failure, no change to the configuration of the cursor will occur.</span></span> <span data-ttu-id="e9a9b-137">Изменение состояния базы данных не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e9a9b-137">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="e9a9b-138">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e9a9b-138">Remarks</span></span>

<span data-ttu-id="e9a9b-139">Этот вызов можно использовать для курсора, который ранее не был настроен с помощью вызова [жетсеттаблесекуентиал](./jetsettablesequential-function.md).</span><span class="sxs-lookup"><span data-stu-id="e9a9b-139">It is safe to make this call against a cursor that has not been previously configured by a call to [JetSetTableSequential](./jetsettablesequential-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="e9a9b-140">Требования</span><span class="sxs-lookup"><span data-stu-id="e9a9b-140">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e9a9b-141"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="e9a9b-141"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="e9a9b-142">Требуется Windows Vista или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e9a9b-142">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9a9b-143"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="e9a9b-143"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="e9a9b-144">Требуется Windows Server 2008 или Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="e9a9b-144">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9a9b-145"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="e9a9b-145"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="e9a9b-146">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="e9a9b-146">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9a9b-147"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="e9a9b-147"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="e9a9b-148">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="e9a9b-148">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9a9b-149"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="e9a9b-149"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="e9a9b-150">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="e9a9b-150">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="e9a9b-151">См. также:</span><span class="sxs-lookup"><span data-stu-id="e9a9b-151">See Also</span></span>

[<span data-ttu-id="e9a9b-152">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="e9a9b-152">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="e9a9b-153">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="e9a9b-153">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="e9a9b-154">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="e9a9b-154">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="e9a9b-155">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="e9a9b-155">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="e9a9b-156">жетсеттаблесекуентиал</span><span class="sxs-lookup"><span data-stu-id="e9a9b-156">JetSetTableSequential</span></span>](./jetsettablesequential-function.md)  
[<span data-ttu-id="e9a9b-157">жетстопсервице</span><span class="sxs-lookup"><span data-stu-id="e9a9b-157">JetStopService</span></span>](./jetstopservice-function.md)
