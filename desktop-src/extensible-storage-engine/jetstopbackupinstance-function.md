---
description: Дополнительные сведения о функции Жетстопбаккупинстанце
title: Функция Жетстопбаккупинстанце
TOCTitle: JetStopBackupInstance Function
ms:assetid: 7d008eac-2a32-402b-91ef-965ed3c3b0de
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269309(v=EXCHG.10)
ms:contentKeyID: 32765599
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetStopBackupInstance
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c1813658ed1fb569795bdfa65ccada3ef8ee629c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144224"
---
# <a name="jetstopbackupinstance-function"></a><span data-ttu-id="9c96e-103">Функция Жетстопбаккупинстанце</span><span class="sxs-lookup"><span data-stu-id="9c96e-103">JetStopBackupInstance Function</span></span>


<span data-ttu-id="9c96e-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="9c96e-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetstopbackupinstance-function"></a><span data-ttu-id="9c96e-105">Функция Жетстопбаккупинстанце</span><span class="sxs-lookup"><span data-stu-id="9c96e-105">JetStopBackupInstance Function</span></span>

<span data-ttu-id="9c96e-106">Функция **жетстопбаккупинстанце** предотвращает продолжение потоковой операции резервного копирования на определенном работающем экземпляре, тем самым завершая потоковую архивацию предсказуемым образом.</span><span class="sxs-lookup"><span data-stu-id="9c96e-106">The **JetStopBackupInstance** function prevents streaming backup-related activity from continuing on a specific running instance, thus ending the streaming backup in a predictable way.</span></span>

<span data-ttu-id="9c96e-107">**Windows XP:**  **Жетстопбаккупинстанце** появился в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="9c96e-107">**Windows XP:**  **JetStopBackupInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetStopBackupInstance(
      __in          JET_INSTANCE instance
    );
```

### <a name="parameters"></a><span data-ttu-id="9c96e-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9c96e-108">Parameters</span></span>

<span data-ttu-id="9c96e-109">*вхождение*</span><span class="sxs-lookup"><span data-stu-id="9c96e-109">*instance*</span></span>

<span data-ttu-id="9c96e-110">Определяет выполняющийся экземпляр, используемый для вызова API.</span><span class="sxs-lookup"><span data-stu-id="9c96e-110">Identifies the running instance to use for the API call.</span></span>

### <a name="return-value"></a><span data-ttu-id="9c96e-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9c96e-111">Return Value</span></span>

<span data-ttu-id="9c96e-112">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="9c96e-112">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="9c96e-113">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="9c96e-113">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9c96e-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="9c96e-114">Return code</span></span></p></th>
<th><p><span data-ttu-id="9c96e-115">Описание</span><span class="sxs-lookup"><span data-stu-id="9c96e-115">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9c96e-116">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="9c96e-116">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="9c96e-117">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="9c96e-117">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c96e-118">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="9c96e-118">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="9c96e-119">Указанный параметр экземпляра имеет недопустимое значение (а не экземпляр, который сейчас выполняется).</span><span class="sxs-lookup"><span data-stu-id="9c96e-119">The specified instance parameter has an invalid value (not an instance that is currently running).</span></span></p>
<p><span data-ttu-id="9c96e-120"><strong>Windows XP:</strong>  Это возвращаемое значение введено в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="9c96e-120"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9c96e-121">Если эта функция завершается успешно, указанный экземпляр будет запускать любые новые API-интерфейсы потоковой архивации.</span><span class="sxs-lookup"><span data-stu-id="9c96e-121">If this function succeeds, the instance that was specified will start failing any new streaming backup APIs.</span></span>

<span data-ttu-id="9c96e-122">Если эта функция завершается ошибкой, то не будет выполнено никаких действий для подготовки к завершению резервного копирования на экземпляре, и изменение состояния экземпляра не будет выполнено.</span><span class="sxs-lookup"><span data-stu-id="9c96e-122">If this function fails, no steps to prepare for the backup termination on the instance will be taken and no change to the instance state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="9c96e-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9c96e-123">Remarks</span></span>

<span data-ttu-id="9c96e-124">Резервное копирование обычно запускается событием за пределами механизма обработки и с помощью этого API, а само приложение ESENT делает все последующие вызовы интерфейсов API потоковой архивации неудачными.</span><span class="sxs-lookup"><span data-stu-id="9c96e-124">Backup is usually triggered by an event outside the process mechanism and by using this API, the ESENT application itself will make any further calls to the streaming backup APIs to fail.</span></span> <span data-ttu-id="9c96e-125">Большинство API-интерфейсов потоковой архивации начнут завершаться сбоем с JET_errBackupAbortByServer.</span><span class="sxs-lookup"><span data-stu-id="9c96e-125">The majority of streaming backup APIs will start failing with JET_errBackupAbortByServer.</span></span> <span data-ttu-id="9c96e-126">Таким образом, любое выполнение потоковой архивации (например, [жетреадфилеинстанце](./jetreadfileinstance-function.md)) вернет ошибку.</span><span class="sxs-lookup"><span data-stu-id="9c96e-126">As such, any streaming backup progress (such as [JetReadFileInstance](./jetreadfileinstance-function.md)) will return an error.</span></span> <span data-ttu-id="9c96e-127">Операции резервного копирования, которые являются частью завершения резервного копирования (например, [жетендекстерналбаккупинстанце](./jetendexternalbackupinstance-function.md)), будут по-прежнему разрешены.</span><span class="sxs-lookup"><span data-stu-id="9c96e-127">Backup operations which are part of the backup termination (like [JetEndExternalBackupInstance](./jetendexternalbackupinstance-function.md)) will still be allowed.</span></span>

#### <a name="requirements"></a><span data-ttu-id="9c96e-128">Требования</span><span class="sxs-lookup"><span data-stu-id="9c96e-128">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9c96e-129"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="9c96e-129"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="9c96e-130">Требуется Windows Vista или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="9c96e-130">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c96e-131"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="9c96e-131"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="9c96e-132">Требуется Windows Server 2008 или Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="9c96e-132">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c96e-133"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="9c96e-133"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="9c96e-134">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="9c96e-134">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c96e-135"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="9c96e-135"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="9c96e-136">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="9c96e-136">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c96e-137"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="9c96e-137"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="9c96e-138">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="9c96e-138">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="9c96e-139">См. также:</span><span class="sxs-lookup"><span data-stu-id="9c96e-139">See Also</span></span>

[<span data-ttu-id="9c96e-140">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="9c96e-140">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="9c96e-141">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="9c96e-141">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="9c96e-142">жетендекстерналбаккупинстанце</span><span class="sxs-lookup"><span data-stu-id="9c96e-142">JetEndExternalBackupInstance</span></span>](./jetendexternalbackupinstance-function.md)  
[<span data-ttu-id="9c96e-143">жетреадфилеинстанце</span><span class="sxs-lookup"><span data-stu-id="9c96e-143">JetReadFileInstance</span></span>](./jetreadfileinstance-function.md)  
[<span data-ttu-id="9c96e-144">жетстопсервице</span><span class="sxs-lookup"><span data-stu-id="9c96e-144">JetStopService</span></span>](./jetstopservice-function.md)
