---
description: Дополнительные сведения о функции Жетосснапшотаборт
title: Функция Жетосснапшотаборт
TOCTitle: JetOSSnapshotAbort Function
ms:assetid: 629455af-b526-4366-9b9a-112757f72c32
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269265(v=EXCHG.10)
ms:contentKeyID: 32765567
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotAbort
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d976f027a940bcf0199016d0e617d515273183ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712509"
---
# <a name="jetossnapshotabort-function"></a><span data-ttu-id="81105-103">Функция Жетосснапшотаборт</span><span class="sxs-lookup"><span data-stu-id="81105-103">JetOSSnapshotAbort Function</span></span>


<span data-ttu-id="81105-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="81105-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetossnapshotabort-function"></a><span data-ttu-id="81105-105">Функция Жетосснапшотаборт</span><span class="sxs-lookup"><span data-stu-id="81105-105">JetOSSnapshotAbort Function</span></span>

<span data-ttu-id="81105-106">Функция **жетосснапшотаборт** уведомляет модуль о том, что он может возобновить нормальные операции ввода-вывода после завершения периода фиксации с неудачным снимком.</span><span class="sxs-lookup"><span data-stu-id="81105-106">The **JetOSSnapshotAbort** function notifies the engine that it can resume normal IO operations after a freeze period ended with a failed snapshot.</span></span>

<span data-ttu-id="81105-107">**Windows server 2003:**  **Жетосснапшотаборт** появился в Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="81105-107">**Windows Server 2003:**  **JetOSSnapshotAbort** is introduced in Windows Server 2003.</span></span>

```cpp
    JET_ERR JET_API JetOSSnapshotAbort(
      __in          const JET_OSSNAPID snapId,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="81105-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="81105-108">Parameters</span></span>

<span data-ttu-id="81105-109">*снапид*</span><span class="sxs-lookup"><span data-stu-id="81105-109">*snapId*</span></span>

<span data-ttu-id="81105-110">Идентификатор сеанса моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="81105-110">The identifier of the snapshot session.</span></span>

<span data-ttu-id="81105-111">*грбит*</span><span class="sxs-lookup"><span data-stu-id="81105-111">*grbit*</span></span>

<span data-ttu-id="81105-112">Параметры для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="81105-112">The options for this call.</span></span> <span data-ttu-id="81105-113">Этот параметр зарезервирован для будущего использования, и поддерживается только допустимое значение 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="81105-113">This parameter is reserved for future use and the only valid value supported is 0 (zero).</span></span>

### <a name="return-value"></a><span data-ttu-id="81105-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="81105-114">Return Value</span></span>

<span data-ttu-id="81105-115">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="81105-115">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="81105-116">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="81105-116">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="81105-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="81105-117">Return code</span></span></p></th>
<th><p><span data-ttu-id="81105-118">Описание</span><span class="sxs-lookup"><span data-stu-id="81105-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="81105-119">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="81105-119">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="81105-120">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="81105-120">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="81105-121">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="81105-121">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="81105-122">Недопустимый сеанс моментального снимка, или параметр грбит недопустим.</span><span class="sxs-lookup"><span data-stu-id="81105-122">The snapshot session is invalid or the grbit parameter is invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="81105-123">JET_errOSSnapshotInvalidSnapId</span><span class="sxs-lookup"><span data-stu-id="81105-123">JET_errOSSnapshotInvalidSnapId</span></span></p></td>
<td><p><span data-ttu-id="81105-124">Недопустимый идентификатор сеанса моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="81105-124">The identifier for the snapshot session is not valid.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="81105-125">Если эта функция завершается, то сеанс моментального снимка завершится, и поведение нормального обработчика будет возобновлено.</span><span class="sxs-lookup"><span data-stu-id="81105-125">If this function succeeds, the snapshot session will end and the normal engine behavior will resume.</span></span> <span data-ttu-id="81105-126">Новый сеанс моментального снимка можно запустить позже.</span><span class="sxs-lookup"><span data-stu-id="81105-126">A new snapshot session can be started at a later point.</span></span>

<span data-ttu-id="81105-127">Если эта функция завершается ошибкой, сеанс моментального снимка не будет прерван.</span><span class="sxs-lookup"><span data-stu-id="81105-127">If this function fails, the snapshot session will not be aborted.</span></span>

#### <a name="remarks"></a><span data-ttu-id="81105-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="81105-128">Remarks</span></span>

<span data-ttu-id="81105-129">Эта функция должна вызываться вместо [жетосснапшотсав](./jetossnapshotthaw-function.md) , чтобы информировать механизм о том, что моментальный снимок был прерван по причинам, не связанным с ядром.</span><span class="sxs-lookup"><span data-stu-id="81105-129">This function should be called instead of [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) to inform the engine that the snapshot was aborted for reasons that don't relate to the engine.</span></span> <span data-ttu-id="81105-130">Эти сведения можно использовать позже для выведения сообщений журнала событий о сеансе моментальных снимков или для определения других соответствующих действий.</span><span class="sxs-lookup"><span data-stu-id="81105-130">This information can be used later to help issue event log messages about the snapshot session or to help determine other appropriate actions.</span></span>

#### <a name="requirements"></a><span data-ttu-id="81105-131">Требования</span><span class="sxs-lookup"><span data-stu-id="81105-131">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="81105-132"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="81105-132"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="81105-133">Требуется Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="81105-133">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="81105-134"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="81105-134"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="81105-135">Требуется Windows Server 2008 или Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="81105-135">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="81105-136"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="81105-136"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="81105-137">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="81105-137">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="81105-138"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="81105-138"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="81105-139">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="81105-139">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="81105-140"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="81105-140"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="81105-141">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="81105-141">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="81105-142">См. также:</span><span class="sxs-lookup"><span data-stu-id="81105-142">See Also</span></span>

[<span data-ttu-id="81105-143">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="81105-143">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="81105-144">JET_OSSNAPID</span><span class="sxs-lookup"><span data-stu-id="81105-144">JET_OSSNAPID</span></span>](./jet-ossnapid.md)  
[<span data-ttu-id="81105-145">жетосснапшотфризе</span><span class="sxs-lookup"><span data-stu-id="81105-145">JetOSSnapshotFreeze</span></span>](./jetossnapshotfreeze-function.md)  
[<span data-ttu-id="81105-146">жетосснапшотпрепаре</span><span class="sxs-lookup"><span data-stu-id="81105-146">JetOSSnapshotPrepare</span></span>](./jetossnapshotprepare-function.md)  
[<span data-ttu-id="81105-147">жетосснапшотсав</span><span class="sxs-lookup"><span data-stu-id="81105-147">JetOSSnapshotThaw</span></span>](./jetossnapshotthaw-function.md)
