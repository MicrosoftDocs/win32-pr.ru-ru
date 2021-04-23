---
description: Дополнительные сведения о функции Жетосснапшотпрепареинстанце
title: Функция Жетосснапшотпрепареинстанце
TOCTitle: JetOSSnapshotPrepareInstance Function
ms:assetid: b4f06342-633f-47c6-be32-64ec058920fe
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294064(v=EXCHG.10)
ms:contentKeyID: 32765679
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotPrepareInstance
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8cc5179a55aabfa3324e3caab7005f4abe437a6d
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "104424550"
---
# <a name="jetossnapshotprepareinstance-function"></a><span data-ttu-id="6511f-103">Функция Жетосснапшотпрепареинстанце</span><span class="sxs-lookup"><span data-stu-id="6511f-103">JetOSSnapshotPrepareInstance Function</span></span>


<span data-ttu-id="6511f-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="6511f-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetossnapshotprepareinstance-function"></a><span data-ttu-id="6511f-105">Функция Жетосснапшотпрепареинстанце</span><span class="sxs-lookup"><span data-stu-id="6511f-105">JetOSSnapshotPrepareInstance Function</span></span>

<span data-ttu-id="6511f-106">Функция **жетосснапшотпрепареинстанце** выбирает конкретный экземпляр, который должен быть частью сеанса моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="6511f-106">The **JetOSSnapshotPrepareInstance** function selects a specific instance to be part of the snapshot session.</span></span>

<span data-ttu-id="6511f-107">**Windows Vista:** **жетосснапшотпрепареинстанце** был впервые появился в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="6511f-107">**Windows Vista:** **JetOSSnapshotPrepareInstance** was introduced in Windows Vista.</span></span>

```cpp
JET_ERR JET_API JetOSSnapshotPrepareInstance(
  __in          JET_OSSNAPID snapId,
  __in          JET_INSTANCE instance,
  __in          const JET_GRBIT grbit
);
```

### <a name="parameters"></a><span data-ttu-id="6511f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="6511f-108">Parameters</span></span>

<span data-ttu-id="6511f-109">*снапид*</span><span class="sxs-lookup"><span data-stu-id="6511f-109">*snapId*</span></span>

<span data-ttu-id="6511f-110">Идентификатор сеанса моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="6511f-110">The identifier of the snapshot session.</span></span>

<span data-ttu-id="6511f-111">*вхождение*</span><span class="sxs-lookup"><span data-stu-id="6511f-111">*instance*</span></span>

<span data-ttu-id="6511f-112">Экземпляр, который будет использоваться для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="6511f-112">The instance that will be used for this call.</span></span>

<span data-ttu-id="6511f-113">*грбит*</span><span class="sxs-lookup"><span data-stu-id="6511f-113">*grbit*</span></span>

<span data-ttu-id="6511f-114">Параметры для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="6511f-114">The options for this call.</span></span> <span data-ttu-id="6511f-115">Этот параметр зарезервирован для использования в будущем.</span><span class="sxs-lookup"><span data-stu-id="6511f-115">This parameter is reserved for future use.</span></span> <span data-ttu-id="6511f-116">Единственное допустимое значение — 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="6511f-116">The only valid value is 0 (zero).</span></span>

### <a name="return-value"></a><span data-ttu-id="6511f-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6511f-117">Return Value</span></span>

<span data-ttu-id="6511f-118">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="6511f-118">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="6511f-119">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="6511f-119">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6511f-120">Код возврата</span><span class="sxs-lookup"><span data-stu-id="6511f-120">Return code</span></span></p></th>
<th><p><span data-ttu-id="6511f-121">Описание</span><span class="sxs-lookup"><span data-stu-id="6511f-121">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6511f-122">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="6511f-122">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="6511f-123">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="6511f-123">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6511f-124">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="6511f-124">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="6511f-125">Указатель идентификатора моментального снимка имеет <strong>значение NULL</strong> , или параметр <em>грбит</em> является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="6511f-125">The snapshot id pointer is <strong>NULL</strong> or the <em>grbit</em> parameter is invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6511f-126">JET_errOSSnapshotInvalidSequence</span><span class="sxs-lookup"><span data-stu-id="6511f-126">JET_errOSSnapshotInvalidSequence</span></span></p></td>
<td><p><span data-ttu-id="6511f-127">Сеанс моментального снимка уже выполняется.</span><span class="sxs-lookup"><span data-stu-id="6511f-127">A snapshot session is already in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6511f-128">JET_errOSSnapshotInvalidSnapId</span><span class="sxs-lookup"><span data-stu-id="6511f-128">JET_errOSSnapshotInvalidSnapId</span></span></p></td>
<td><p><span data-ttu-id="6511f-129">Недопустимый идентификатор сеанса моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="6511f-129">The identifier for the snapshot session is not valid.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6511f-130">Если эта функция выполнена, указанный экземпляр будет частью сеанса моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="6511f-130">If this function succeeds, the specified instance will be part of the snapshot session.</span></span>

<span data-ttu-id="6511f-131">Если эта функция завершается неудачно, изменение состояния модуля не происходит.</span><span class="sxs-lookup"><span data-stu-id="6511f-131">If this function fails, no change in the engine state occurs.</span></span>

#### <a name="remarks"></a><span data-ttu-id="6511f-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6511f-132">Remarks</span></span>

<span data-ttu-id="6511f-133">Стандартный вызов последовательности API: [жетосснапшотпрепаре](./jetossnapshotprepare-function.md), при необходимости за одним или несколькими вызовами **жетосснапшотпрепареинстанце**, после которого следует [жетосснапшотфризе](./jetossnapshotfreeze-function.md).</span><span class="sxs-lookup"><span data-stu-id="6511f-133">The normal API sequence call is: [JetOSSnapshotPrepare](./jetossnapshotprepare-function.md), optionally followed by one or more calls to **JetOSSnapshotPrepareInstance**, then followed by [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md).</span></span> <span data-ttu-id="6511f-134">После запуска замораживания его можно завершить с помощью [жетосснапшотсав](./jetossnapshotthaw-function.md).</span><span class="sxs-lookup"><span data-stu-id="6511f-134">Once the freeze is started, it can be terminated using [JetOSSnapshotThaw](./jetossnapshotthaw-function.md).</span></span> <span data-ttu-id="6511f-135">В любое время после подготовки сеанс моментального снимка может внезапно завершиться с помощью [жетосснапшотаборт](./jetossnapshotabort-function.md).</span><span class="sxs-lookup"><span data-stu-id="6511f-135">At any time after the prepare, the snapshot session can be abruptly terminated with [JetOSSnapshotAbort](./jetossnapshotabort-function.md).</span></span> <span data-ttu-id="6511f-136">Записи журнала событий будут созданы для различных этапов создания моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="6511f-136">Event log entries will be generated for the different steps of the snapshot.</span></span>

<span data-ttu-id="6511f-137">Если **жетосснапшотпрепареинстанце** не вызывается между началом сеанса ([жетосснапшотпрепаре](./jetossnapshotprepare-function.md)) и закреплением ([жетосснапшотфризе](./jetossnapshotfreeze-function.md)), все запущенные экземпляры в ядре будут закрепляться и становиться частью сеанса моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="6511f-137">If **JetOSSnapshotPrepareInstance** is not called between the start of the session ([JetOSSnapshotPrepare](./jetossnapshotprepare-function.md)) and the freeze moment ([JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)), all the running instances in the engine will freeze and become part of the snapshot session.</span></span> <span data-ttu-id="6511f-138">Это происходит по двум причинам.</span><span class="sxs-lookup"><span data-stu-id="6511f-138">This occurs for two reasons:</span></span>

  - <span data-ttu-id="6511f-139">Он упрощает код для пользователей, которым требуются все экземпляры.</span><span class="sxs-lookup"><span data-stu-id="6511f-139">It simplifies the code for users who want all instances.</span></span>

  - <span data-ttu-id="6511f-140">Он обеспечивает обратную совместимость для вызывающих объектов API моментальных снимков.</span><span class="sxs-lookup"><span data-stu-id="6511f-140">It allows backward compatibility for the callers of the snapshot APIs.</span></span>

#### <a name="requirements"></a><span data-ttu-id="6511f-141">Требования</span><span class="sxs-lookup"><span data-stu-id="6511f-141">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6511f-142"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="6511f-142"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="6511f-143">Требуется Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="6511f-143">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6511f-144"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="6511f-144"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="6511f-145">Требуется Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="6511f-145">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6511f-146"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="6511f-146"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="6511f-147">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="6511f-147">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6511f-148"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="6511f-148"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="6511f-149">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="6511f-149">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6511f-150"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="6511f-150"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="6511f-151">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="6511f-151">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="6511f-152">См. также:</span><span class="sxs-lookup"><span data-stu-id="6511f-152">See Also</span></span>

[<span data-ttu-id="6511f-153">Параметры обработки ошибок</span><span class="sxs-lookup"><span data-stu-id="6511f-153">Error Handling Parameters</span></span>](./error-handling-parameters.md)  
[<span data-ttu-id="6511f-154">Ошибки расширяемого подсистемы хранилища</span><span class="sxs-lookup"><span data-stu-id="6511f-154">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="6511f-155">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="6511f-155">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="6511f-156">жетосснапшотаборт</span><span class="sxs-lookup"><span data-stu-id="6511f-156">JetOSSnapshotAbort</span></span>](./jetossnapshotabort-function.md)  
[<span data-ttu-id="6511f-157">жетосснапшотенд</span><span class="sxs-lookup"><span data-stu-id="6511f-157">JetOSSnapshotEnd</span></span>](./jetossnapshotend-function.md)  
[<span data-ttu-id="6511f-158">жетосснапшотфризе</span><span class="sxs-lookup"><span data-stu-id="6511f-158">JetOSSnapshotFreeze</span></span>](./jetossnapshotfreeze-function.md)  
[<span data-ttu-id="6511f-159">жетосснапшотпрепаре</span><span class="sxs-lookup"><span data-stu-id="6511f-159">JetOSSnapshotPrepare</span></span>](./jetossnapshotprepare-function.md)  
[<span data-ttu-id="6511f-160">жетосснапшотсав</span><span class="sxs-lookup"><span data-stu-id="6511f-160">JetOSSnapshotThaw</span></span>](./jetossnapshotthaw-function.md)
