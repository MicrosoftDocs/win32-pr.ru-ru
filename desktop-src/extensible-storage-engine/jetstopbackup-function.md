---
description: Дополнительные сведения о функции Жетстопбаккуп
title: Функция Жетстопбаккуп
TOCTitle: JetStopBackup Function
ms:assetid: b7545284-2fdb-4470-8466-fc2109ad63c5
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294067(v=EXCHG.10)
ms:contentKeyID: 32765682
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetStopBackup
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c47a1454e5846fae510a7b91c197d4b180fd14a7
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "105714063"
---
# <a name="jetstopbackup-function"></a><span data-ttu-id="a0f2e-103">Функция Жетстопбаккуп</span><span class="sxs-lookup"><span data-stu-id="a0f2e-103">JetStopBackup Function</span></span>


<span data-ttu-id="a0f2e-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="a0f2e-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetstopbackup-function"></a><span data-ttu-id="a0f2e-105">Функция Жетстопбаккуп</span><span class="sxs-lookup"><span data-stu-id="a0f2e-105">JetStopBackup Function</span></span>

<span data-ttu-id="a0f2e-106">Функция **жетстопбаккуп** предотвращает продолжение любых операций потоковой архивации на определенном работающем экземпляре, тем самым завершая потоковую архивацию предсказуемым образом.</span><span class="sxs-lookup"><span data-stu-id="a0f2e-106">The **JetStopBackup** function prevents any streaming backup-related activity from continuing on a specific running instance, thus ending the streaming backup in a predictable way.</span></span>

<span data-ttu-id="a0f2e-107">**Windows XP:**  Эта функция появилась в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a0f2e-107">**Windows XP:**  This function is introduced in Windows XP.</span></span>

<span data-ttu-id="a0f2e-108">[Жетстопсервице](./jetstopservice-function.md) — это устаревший вызов, если разрешен только один экземпляр.</span><span class="sxs-lookup"><span data-stu-id="a0f2e-108">[JetStopService](./jetstopservice-function.md) is the legacy call when only one instance is allowed.</span></span> <span data-ttu-id="a0f2e-109">В этом случае единственным активным экземпляром является тот, который подготавливается к завершению.</span><span class="sxs-lookup"><span data-stu-id="a0f2e-109">In this case, the only active instance is the one being prepared for termination.</span></span>

```cpp
JET_ERR JET_API JetStopBackup(void);
```

### <a name="parameters"></a><span data-ttu-id="a0f2e-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="a0f2e-110">Parameters</span></span>

<span data-ttu-id="a0f2e-111">У этой функции нет параметров.</span><span class="sxs-lookup"><span data-stu-id="a0f2e-111">This function has no parameters.</span></span>

### <a name="return-value"></a><span data-ttu-id="a0f2e-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a0f2e-112">Return Value</span></span>

<span data-ttu-id="a0f2e-113">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="a0f2e-113">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="a0f2e-114">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="a0f2e-114">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a0f2e-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="a0f2e-115">Return code</span></span></p></th>
<th><p><span data-ttu-id="a0f2e-116">Описание</span><span class="sxs-lookup"><span data-stu-id="a0f2e-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a0f2e-117">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="a0f2e-117">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="a0f2e-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="a0f2e-118">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0f2e-119">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="a0f2e-119">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="a0f2e-120">Не ясно, какой экземпляр подготавливается к завершению при использовании <a href="gg269240(v=exchg.10).md">жетстопсервице</a> в режиме с несколькими экземплярами.</span><span class="sxs-lookup"><span data-stu-id="a0f2e-120">It is not clear which instance to prepare for termination when using <a href="gg269240(v=exchg.10).md">JetStopService</a> with multiple instance mode.</span></span></p>
<p><span data-ttu-id="a0f2e-121"><strong>Windows XP:</strong>  Это возвращаемое значение введено в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a0f2e-121"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a0f2e-122">Если эта функция завершается успешно, экземпляр начнет работать с ошибками новых интерфейсов API потоковой архивации.</span><span class="sxs-lookup"><span data-stu-id="a0f2e-122">If this function succeeds, the instance will start failing any new streaming backup APIs.</span></span>

<span data-ttu-id="a0f2e-123">Если эта функция завершается ошибкой, то не будет выполнено никаких действий для подготовки к завершению резервного копирования на экземпляре, и изменение состояния экземпляра не будет выполнено.</span><span class="sxs-lookup"><span data-stu-id="a0f2e-123">If this function fails, no steps to prepare for the backup termination on the instance will be taken and no change to the instance state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="a0f2e-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a0f2e-124">Remarks</span></span>

<span data-ttu-id="a0f2e-125">Резервное копирование обычно запускается событием за пределами механизма обработки и с помощью этого API, а само приложение ESENT делает все последующие вызовы интерфейсов API потоковой архивации неудачными.</span><span class="sxs-lookup"><span data-stu-id="a0f2e-125">Backup is usually triggered by an event outside the process mechanism and by using this API, the ESENT application itself will make any further calls to the streaming backup APIs to fail.</span></span> <span data-ttu-id="a0f2e-126">Большинство API-интерфейсов потоковой архивации начнут завершаться сбоем с JET_errBackupAbortByServer.</span><span class="sxs-lookup"><span data-stu-id="a0f2e-126">The majority of streaming backup APIs will start failing with JET_errBackupAbortByServer.</span></span> <span data-ttu-id="a0f2e-127">Таким образом, любое выполнение потоковой архивации (например, [жетреадфилеинстанце](./jetreadfileinstance-function.md)) вернет ошибку.</span><span class="sxs-lookup"><span data-stu-id="a0f2e-127">As such, any streaming backup progress (like [JetReadFileInstance](./jetreadfileinstance-function.md)) will return an error.</span></span> <span data-ttu-id="a0f2e-128">Операции резервного копирования, которые являются частью завершения резервного копирования (например, [жетендекстерналбаккупинстанце](./jetendexternalbackupinstance-function.md)), по-прежнему будут разрешены.</span><span class="sxs-lookup"><span data-stu-id="a0f2e-128">Backup operations which are part of the backup termination (such as [JetEndExternalBackupInstance](./jetendexternalbackupinstance-function.md)) will still be allowed.</span></span>

#### <a name="requirements"></a><span data-ttu-id="a0f2e-129">Требования</span><span class="sxs-lookup"><span data-stu-id="a0f2e-129">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a0f2e-130"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="a0f2e-130"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="a0f2e-131">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="a0f2e-131">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0f2e-132"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="a0f2e-132"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="a0f2e-133">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="a0f2e-133">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0f2e-134"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="a0f2e-134"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="a0f2e-135">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="a0f2e-135">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0f2e-136"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="a0f2e-136"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="a0f2e-137">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="a0f2e-137">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0f2e-138"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="a0f2e-138"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="a0f2e-139">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="a0f2e-139">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="a0f2e-140">См. также:</span><span class="sxs-lookup"><span data-stu-id="a0f2e-140">See Also</span></span>

[<span data-ttu-id="a0f2e-141">жетендекстерналбаккупинстанце</span><span class="sxs-lookup"><span data-stu-id="a0f2e-141">JetEndExternalBackupInstance</span></span>](./jetendexternalbackupinstance-function.md)  
[<span data-ttu-id="a0f2e-142">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="a0f2e-142">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="a0f2e-143">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="a0f2e-143">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="a0f2e-144">жетреадфилеинстанце</span><span class="sxs-lookup"><span data-stu-id="a0f2e-144">JetReadFileInstance</span></span>](./jetreadfileinstance-function.md)  
[<span data-ttu-id="a0f2e-145">жетстопсервице</span><span class="sxs-lookup"><span data-stu-id="a0f2e-145">JetStopService</span></span>](./jetstopservice-function.md)
