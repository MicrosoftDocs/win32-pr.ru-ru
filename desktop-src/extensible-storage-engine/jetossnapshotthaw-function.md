---
description: Дополнительные сведения о функции Жетосснапшотсав
title: Функция Жетосснапшотсав
TOCTitle: JetOSSnapshotThaw Function
ms:assetid: 3b001113-6299-4082-ab15-461f2e33e996
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269229(v=EXCHG.10)
ms:contentKeyID: 32765531
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotThaw
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: da7d5037cfc6b9a5f001dede57581127e4de60b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913559"
---
# <a name="jetossnapshotthaw-function"></a><span data-ttu-id="d05be-103">Функция Жетосснапшотсав</span><span class="sxs-lookup"><span data-stu-id="d05be-103">JetOSSnapshotThaw Function</span></span>


<span data-ttu-id="d05be-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="d05be-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetossnapshotthaw-function"></a><span data-ttu-id="d05be-105">Функция Жетосснапшотсав</span><span class="sxs-lookup"><span data-stu-id="d05be-105">JetOSSnapshotThaw Function</span></span>

<span data-ttu-id="d05be-106">Функция **жетосснапшотсав** уведомляет модуль о том, что он может возобновить нормальную операцию ввода-вывода после точки фиксации и успешного создания моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="d05be-106">The **JetOSSnapshotThaw** function notifies the engine that it can resume normal IO operations after a freeze period and a successful snapshot.</span></span>

<span data-ttu-id="d05be-107">**Windows XP:**  **Жетосснапшотсав** появился в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d05be-107">**Windows XP:**  **JetOSSnapshotThaw** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetOSSnapshotThaw(
      __in          const JET_OSSNAPID snapId,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="d05be-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d05be-108">Parameters</span></span>

<span data-ttu-id="d05be-109">*снапид*</span><span class="sxs-lookup"><span data-stu-id="d05be-109">*snapId*</span></span>

<span data-ttu-id="d05be-110">Идентификатор сеанса моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="d05be-110">The identifier of the snapshot session.</span></span>

<span data-ttu-id="d05be-111">*грбит*</span><span class="sxs-lookup"><span data-stu-id="d05be-111">*grbit*</span></span>

<span data-ttu-id="d05be-112">Этот параметр зарезервирован для будущего использования, и поддерживается только допустимое значение 0.</span><span class="sxs-lookup"><span data-stu-id="d05be-112">This parameter is reserved for future use and the only valid value supported is 0.</span></span>

### <a name="return-value"></a><span data-ttu-id="d05be-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d05be-113">Return Value</span></span>

<span data-ttu-id="d05be-114">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="d05be-114">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="d05be-115">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="d05be-115">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d05be-116">Код возврата</span><span class="sxs-lookup"><span data-stu-id="d05be-116">Return code</span></span></p></th>
<th><p><span data-ttu-id="d05be-117">Описание</span><span class="sxs-lookup"><span data-stu-id="d05be-117">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d05be-118">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="d05be-118">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="d05be-119">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="d05be-119">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d05be-120">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="d05be-120">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="d05be-121">Недопустимый сеанс моментального снимка, или параметр <em>грбит</em> недопустим.</span><span class="sxs-lookup"><span data-stu-id="d05be-121">The snapshot session is invalid or the <em>grbit</em> parameter is invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d05be-122">JET_errOSSnapshotTimeOut</span><span class="sxs-lookup"><span data-stu-id="d05be-122">JET_errOSSnapshotTimeOut</span></span></p></td>
<td><p><span data-ttu-id="d05be-123">Время сеанса моментального снимка истекло до возникновения этого вызова.</span><span class="sxs-lookup"><span data-stu-id="d05be-123">The snapshot session had an internal timeout before this call occurred.</span></span> <span data-ttu-id="d05be-124">Следовательно, перед совершением этого вызова операции ввода-вывода возвращены в нормальный режим.</span><span class="sxs-lookup"><span data-stu-id="d05be-124">Consequently, IO operations returned to normal before this call was made.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d05be-125">JET_errOSSnapshotInvalidSnapId</span><span class="sxs-lookup"><span data-stu-id="d05be-125">JET_errOSSnapshotInvalidSnapId</span></span></p></td>
<td><p><span data-ttu-id="d05be-126">Недопустимый идентификатор сеанса моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="d05be-126">The identifier for snapshot session is not valid.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d05be-127">Если эта функция завершается, то сеанс моментального снимка завершается, а нормальное поведение ядра возобновляется.</span><span class="sxs-lookup"><span data-stu-id="d05be-127">If this function succeeds, a snapshot session ends and the normal engine behavior resumes.</span></span> <span data-ttu-id="d05be-128">Новый сеанс моментального снимка можно запустить позже.</span><span class="sxs-lookup"><span data-stu-id="d05be-128">A new snapshot session can be started later.</span></span>

<span data-ttu-id="d05be-129">Если эта функция завершается ошибкой, текущий сеанс моментального снимка завершается, но замораживание IOs в течение периода моментального снимка не учитывается внутренне.</span><span class="sxs-lookup"><span data-stu-id="d05be-129">If this function fails, the current snapshot session ends but the freeze of IOs during the snapshot period was not respected internally.</span></span>

#### <a name="remarks"></a><span data-ttu-id="d05be-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d05be-130">Remarks</span></span>

<span data-ttu-id="d05be-131">Записи журнала событий будут созданы для различных этапов создания моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="d05be-131">Event log entries will be generated for the different steps of the snapshot.</span></span>

#### <a name="requirements"></a><span data-ttu-id="d05be-132">Требования</span><span class="sxs-lookup"><span data-stu-id="d05be-132">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d05be-133"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="d05be-133"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="d05be-134">Требуется Windows Vista или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d05be-134">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d05be-135"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="d05be-135"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="d05be-136">Требуется Windows Server 2008 или Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="d05be-136">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d05be-137"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="d05be-137"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="d05be-138">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="d05be-138">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d05be-139"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="d05be-139"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="d05be-140">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="d05be-140">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d05be-141"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="d05be-141"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="d05be-142">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="d05be-142">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="d05be-143">См. также:</span><span class="sxs-lookup"><span data-stu-id="d05be-143">See Also</span></span>

[<span data-ttu-id="d05be-144">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="d05be-144">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="d05be-145">JET_OSSNAPID</span><span class="sxs-lookup"><span data-stu-id="d05be-145">JET_OSSNAPID</span></span>](./jet-ossnapid.md)  
[<span data-ttu-id="d05be-146">жетосснапшотаборт</span><span class="sxs-lookup"><span data-stu-id="d05be-146">JetOSSnapshotAbort</span></span>](./jetossnapshotabort-function.md)  
[<span data-ttu-id="d05be-147">жетосснапшотфризе</span><span class="sxs-lookup"><span data-stu-id="d05be-147">JetOSSnapshotFreeze</span></span>](./jetossnapshotfreeze-function.md)  
[<span data-ttu-id="d05be-148">жетосснапшотпрепаре</span><span class="sxs-lookup"><span data-stu-id="d05be-148">JetOSSnapshotPrepare</span></span>](./jetossnapshotprepare-function.md)
