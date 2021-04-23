---
description: Дополнительные сведения о функции Жетосснапшотжетфризеинфо
title: Функция Жетосснапшотжетфризеинфо
TOCTitle: JetOSSnapshotGetFreezeInfo Function
ms:assetid: b94eaf91-7407-4c62-ab1e-3249ad076c1a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294070(v=EXCHG.10)
ms:contentKeyID: 32765685
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotGetFreezeInfo
- JetOSSnapshotGetFreezeInfoA
- JetOSSnapshotGetFreezeInfoW
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2fbfd3fb31567ea73b8266b5aeba506d62be7714
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712507"
---
# <a name="jetossnapshotgetfreezeinfo-function"></a><span data-ttu-id="d5f7d-103">Функция Жетосснапшотжетфризеинфо</span><span class="sxs-lookup"><span data-stu-id="d5f7d-103">JetOSSnapshotGetFreezeInfo Function</span></span>


<span data-ttu-id="d5f7d-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="d5f7d-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetossnapshotgetfreezeinfo-function"></a><span data-ttu-id="d5f7d-105">Функция Жетосснапшотжетфризеинфо</span><span class="sxs-lookup"><span data-stu-id="d5f7d-105">JetOSSnapshotGetFreezeInfo Function</span></span>

<span data-ttu-id="d5f7d-106">Функция **жетосснапшотжетфризеинфо** извлекает список экземпляров и баз данных, которые являются частью сеанса моментального снимка, в любой момент времени.</span><span class="sxs-lookup"><span data-stu-id="d5f7d-106">The **JetOSSnapshotGetFreezeInfo** function retrieves the list of instances and databases that are part of the snapshot session at any given moment.</span></span>

<span data-ttu-id="d5f7d-107">**Windows Vista:**  **Жетосснапшотжетфризеинфо** появился в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d5f7d-107">**Windows Vista:**  **JetOSSnapshotGetFreezeInfo** is introduced in Windows Vista.</span></span>

```cpp
    JET_ERR JET_API JetOSSnapshotGetFreezeInfo(
      __in          const JET_OSSNAPID snapId,
      __out         unsigned long* pcInstanceInfo,
      __out         JET_INSTANCE_INFO** paInstanceInfo,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="d5f7d-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d5f7d-108">Parameters</span></span>

<span data-ttu-id="d5f7d-109">*снапид*</span><span class="sxs-lookup"><span data-stu-id="d5f7d-109">*snapId*</span></span>

<span data-ttu-id="d5f7d-110">Идентификатор сеанса моментального снимка, который необходимо запустить.</span><span class="sxs-lookup"><span data-stu-id="d5f7d-110">The identifier of the snapshot session to be started.</span></span>

<span data-ttu-id="d5f7d-111">*пЦинстанцеинфо*</span><span class="sxs-lookup"><span data-stu-id="d5f7d-111">*pcInstanceInfo*</span></span>

<span data-ttu-id="d5f7d-112">Количество выполняющихся в данный момент экземпляров, которые являются частью сеанса моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="d5f7d-112">The number of instances currently running that are part of the snapshot session.</span></span>

<span data-ttu-id="d5f7d-113">*паинстанцеинфо*</span><span class="sxs-lookup"><span data-stu-id="d5f7d-113">*paInstanceInfo*</span></span>

<span data-ttu-id="d5f7d-114">Массив структур, по одному для каждого выполняющегося экземпляра, описывающих экземпляр и базы данных, которые являются его частью.</span><span class="sxs-lookup"><span data-stu-id="d5f7d-114">An array of structures, one for each running instance, describing the instance and the databases that are part of it.</span></span>

<span data-ttu-id="d5f7d-115">*грбит*</span><span class="sxs-lookup"><span data-stu-id="d5f7d-115">*grbit*</span></span>

<span data-ttu-id="d5f7d-116">Параметры для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="d5f7d-116">The options for this call.</span></span> <span data-ttu-id="d5f7d-117">Этот параметр зарезервирован для использования в будущем.</span><span class="sxs-lookup"><span data-stu-id="d5f7d-117">This parameter is reserved for future use.</span></span> <span data-ttu-id="d5f7d-118">Единственное допустимое значение — 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="d5f7d-118">The only valid value is 0 (zero).</span></span>

### <a name="return-value"></a><span data-ttu-id="d5f7d-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d5f7d-119">Return Value</span></span>

<span data-ttu-id="d5f7d-120">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="d5f7d-120">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="d5f7d-121">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="d5f7d-121">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d5f7d-122">Код возврата</span><span class="sxs-lookup"><span data-stu-id="d5f7d-122">Return code</span></span></p></th>
<th><p><span data-ttu-id="d5f7d-123">Описание</span><span class="sxs-lookup"><span data-stu-id="d5f7d-123">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d5f7d-124">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="d5f7d-124">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="d5f7d-125">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="d5f7d-125">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d5f7d-126">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="d5f7d-126">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="d5f7d-127">Ошибка при выполнении функции из-за нехватки памяти.</span><span class="sxs-lookup"><span data-stu-id="d5f7d-127">The function failed due to an out-of-memory condition.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d5f7d-128">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="d5f7d-128">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="d5f7d-129"><em>пЦинстанцеинфо</em> или <em>Паинстанцеинфо</em> имеет <strong>значение NULL</strong>.</span><span class="sxs-lookup"><span data-stu-id="d5f7d-129"><em>pcInstanceInfo</em> or <em>paInstanceInfo</em> is <strong>NULL</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d5f7d-130">JET_errOSSnapshotInvalidSnapId</span><span class="sxs-lookup"><span data-stu-id="d5f7d-130">JET_errOSSnapshotInvalidSnapId</span></span></p></td>
<td><p><span data-ttu-id="d5f7d-131">Недопустимый идентификатор сеанса моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="d5f7d-131">The identifier for the snapshot session is not valid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d5f7d-132">JET_errOSSnapshotInvalidSequence</span><span class="sxs-lookup"><span data-stu-id="d5f7d-132">JET_errOSSnapshotInvalidSequence</span></span></p></td>
<td><p><span data-ttu-id="d5f7d-133">Сеанс моментального снимка не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d5f7d-133">A snapshot session is not in progress.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d5f7d-134">Если эта функция выполнена успешно, сведения об экземпляре должны быть заполнены правильно, и их необходимо освободить позже путем вызова [жетфрибуффер](./jetfreebuffer-function.md) с указателем на возвращаемый массив сведений об экземпляре.</span><span class="sxs-lookup"><span data-stu-id="d5f7d-134">If this function succeeds, the instance information is properly filled and it must be freed later by calling [JetFreeBuffer](./jetfreebuffer-function.md) with the pointer to the instance info array that was returned.</span></span>

<span data-ttu-id="d5f7d-135">Если эта функция завершается неудачно, изменение состояния модуля не происходит.</span><span class="sxs-lookup"><span data-stu-id="d5f7d-135">If this function fails, no change in the engine state occurs.</span></span>

#### <a name="requirements"></a><span data-ttu-id="d5f7d-136">Требования</span><span class="sxs-lookup"><span data-stu-id="d5f7d-136">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d5f7d-137"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="d5f7d-137"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="d5f7d-138">Требуется Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d5f7d-138">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d5f7d-139"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="d5f7d-139"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="d5f7d-140">Требуется Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="d5f7d-140">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d5f7d-141"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="d5f7d-141"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="d5f7d-142">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="d5f7d-142">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d5f7d-143"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="d5f7d-143"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="d5f7d-144">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="d5f7d-144">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d5f7d-145"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="d5f7d-145"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="d5f7d-146">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="d5f7d-146">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d5f7d-147"><strong>Юникод</strong></span><span class="sxs-lookup"><span data-stu-id="d5f7d-147"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="d5f7d-148">Реализуется как <strong>жетосснапшотжетфризеинфов</strong> (Юникод) и <strong>жетосснапшотжетфризеинфоа</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="d5f7d-148">Implemented as <strong>JetOSSnapshotGetFreezeInfoW</strong> (Unicode) and <strong>JetOSSnapshotGetFreezeInfoA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="d5f7d-149">См. также:</span><span class="sxs-lookup"><span data-stu-id="d5f7d-149">See Also</span></span>

[<span data-ttu-id="d5f7d-150">Параметры обработки ошибок</span><span class="sxs-lookup"><span data-stu-id="d5f7d-150">Error Handling Parameters</span></span>](./error-handling-parameters.md)  
[<span data-ttu-id="d5f7d-151">Ошибки расширяемого подсистемы хранилища</span><span class="sxs-lookup"><span data-stu-id="d5f7d-151">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="d5f7d-152">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="d5f7d-152">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="d5f7d-153">жетфрибуффер</span><span class="sxs-lookup"><span data-stu-id="d5f7d-153">JetFreeBuffer</span></span>](./jetfreebuffer-function.md)  
[<span data-ttu-id="d5f7d-154">жетосснапшотаборт</span><span class="sxs-lookup"><span data-stu-id="d5f7d-154">JetOSSnapshotAbort</span></span>](./jetossnapshotabort-function.md)  
[<span data-ttu-id="d5f7d-155">жетосснапшотфризе</span><span class="sxs-lookup"><span data-stu-id="d5f7d-155">JetOSSnapshotFreeze</span></span>](./jetossnapshotfreeze-function.md)  
[<span data-ttu-id="d5f7d-156">жетосснапшотсав</span><span class="sxs-lookup"><span data-stu-id="d5f7d-156">JetOSSnapshotThaw</span></span>](./jetossnapshotthaw-function.md)
