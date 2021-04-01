---
description: Дополнительные сведения о функции Жетосснапшотенд
title: Функция Жетосснапшотенд
TOCTitle: JetOSSnapshotEnd Function
ms:assetid: f7f4db8b-8e40-48d7-bc7b-0c80d0d0f77f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294136(v=EXCHG.10)
ms:contentKeyID: 32765750
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotEnd
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: de1237de9af0b1b75f645346fc30a128a1b8e907
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143531"
---
# <a name="jetossnapshotend-function"></a><span data-ttu-id="2f595-103">Функция Жетосснапшотенд</span><span class="sxs-lookup"><span data-stu-id="2f595-103">JetOSSnapshotEnd Function</span></span>


<span data-ttu-id="2f595-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="2f595-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetossnapshotend-function"></a><span data-ttu-id="2f595-105">Функция Жетосснапшотенд</span><span class="sxs-lookup"><span data-stu-id="2f595-105">JetOSSnapshotEnd Function</span></span>

<span data-ttu-id="2f595-106">Функция **жетосснапшотенд** уведомляет модуль о завершении сеанса моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="2f595-106">The **JetOSSnapshotEnd** function notifies the engine that the snapshot session finished.</span></span>

<span data-ttu-id="2f595-107">**Windows Vista:**  **Жетосснапшотенд** появился в Windows Vista:.</span><span class="sxs-lookup"><span data-stu-id="2f595-107">**Windows Vista:**  **JetOSSnapshotEnd** is introduced in Windows Vista:.</span></span>

```cpp
    JET_ERR JET_API JetOSSnapshotEnd(
      __in          const JET_OSSNAPID snapId,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="2f595-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="2f595-108">Parameters</span></span>

<span data-ttu-id="2f595-109">*снапид*</span><span class="sxs-lookup"><span data-stu-id="2f595-109">*snapId*</span></span>

<span data-ttu-id="2f595-110">Идентификатор сеанса моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="2f595-110">The identifier of the snapshot session.</span></span>

<span data-ttu-id="2f595-111">*грбит*</span><span class="sxs-lookup"><span data-stu-id="2f595-111">*grbit*</span></span>

<span data-ttu-id="2f595-112">Параметры для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="2f595-112">The options for this call.</span></span> <span data-ttu-id="2f595-113">Этот параметр может иметь сочетание следующих значений.</span><span class="sxs-lookup"><span data-stu-id="2f595-113">This parameter can have a combination of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2f595-114">Значение</span><span class="sxs-lookup"><span data-stu-id="2f595-114">Value</span></span></p></th>
<th><p><span data-ttu-id="2f595-115">Значение</span><span class="sxs-lookup"><span data-stu-id="2f595-115">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2f595-116">0</span><span class="sxs-lookup"><span data-stu-id="2f595-116">0</span></span></p></td>
<td><p><span data-ttu-id="2f595-117">Успешное завершение сеанса моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="2f595-117">The successful end of the snapshot session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f595-118">JET_bitAbortSnapshot</span><span class="sxs-lookup"><span data-stu-id="2f595-118">JET_bitAbortSnapshot</span></span></p></td>
<td><p><span data-ttu-id="2f595-119">Сеанс моментального снимка прерван.</span><span class="sxs-lookup"><span data-stu-id="2f595-119">The snapshot session aborted.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="2f595-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2f595-120">Return Value</span></span>

<span data-ttu-id="2f595-121">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="2f595-121">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="2f595-122">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="2f595-122">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2f595-123">Код возврата</span><span class="sxs-lookup"><span data-stu-id="2f595-123">Return code</span></span></p></th>
<th><p><span data-ttu-id="2f595-124">Описание</span><span class="sxs-lookup"><span data-stu-id="2f595-124">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2f595-125">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="2f595-125">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="2f595-126">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="2f595-126">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f595-127">JET_errInvalidGrbit</span><span class="sxs-lookup"><span data-stu-id="2f595-127">JET_errInvalidGrbit</span></span></p></td>
<td><p><span data-ttu-id="2f595-128">Один из запрошенных параметров недопустим, используется неправильно или не реализован.</span><span class="sxs-lookup"><span data-stu-id="2f595-128">One of the options requested is invalid, used incorrectly, or not implemented.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f595-129">JET_errOSSnapshotInvalidSequence</span><span class="sxs-lookup"><span data-stu-id="2f595-129">JET_errOSSnapshotInvalidSequence</span></span></p></td>
<td><p><span data-ttu-id="2f595-130">Сеанс моментального снимка уже выполняется.</span><span class="sxs-lookup"><span data-stu-id="2f595-130">A snapshot session is already in progress.</span></span> <span data-ttu-id="2f595-131">Это не допускается.</span><span class="sxs-lookup"><span data-stu-id="2f595-131">This is not allowed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f595-132">JET_errOSSnapshotInvalidSnapId</span><span class="sxs-lookup"><span data-stu-id="2f595-132">JET_errOSSnapshotInvalidSnapId</span></span></p></td>
<td><p><span data-ttu-id="2f595-133">Недопустимый идентификатор сеанса моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="2f595-133">The identifier for the snapshot session is not valid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f595-134">JET_errOSSnapshotTimeOut</span><span class="sxs-lookup"><span data-stu-id="2f595-134">JET_errOSSnapshotTimeOut</span></span></p></td>
<td><p><span data-ttu-id="2f595-135">Время сеанса моментального снимка истекло до возникновения этого вызова.</span><span class="sxs-lookup"><span data-stu-id="2f595-135">The snapshot session had an internal timeout before this call occurred.</span></span> <span data-ttu-id="2f595-136">В результате операции ввода-вывода, возвращенные в нормальный режим до того, как был выполнен этот вызов.</span><span class="sxs-lookup"><span data-stu-id="2f595-136">As a result, the IO operations returned to normal before this call was made.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2f595-137">Если эта функция завершается, то сеанс моментального снимка будет завершен и будет возобновлено нормальное поведение ядра.</span><span class="sxs-lookup"><span data-stu-id="2f595-137">If this function succeeds, a snapshot session will complete and the normal engine behavior will resume.</span></span> <span data-ttu-id="2f595-138">Новый сеанс моментального снимка можно запустить позже.</span><span class="sxs-lookup"><span data-stu-id="2f595-138">A new snapshot session can be started later.</span></span>

<span data-ttu-id="2f595-139">Если эта функция завершается ошибкой, возвращается код возврата JET_errOSSnapshotTimeOut и текущий сеанс моментального снимка завершается, но замораживание IOs в течение периода моментального снимка не учитывается внутренне.</span><span class="sxs-lookup"><span data-stu-id="2f595-139">If this function fails, the JET_errOSSnapshotTimeOut return code returns and the current snapshot session ends but the freeze of IOs during the snapshot period was not respected internally.</span></span> <span data-ttu-id="2f595-140">Для всех остальных ошибок состояние сеанса моментального снимка не изменится.</span><span class="sxs-lookup"><span data-stu-id="2f595-140">For all other errors, the snapshot session state will not be changed.</span></span>

#### <a name="remarks"></a><span data-ttu-id="2f595-141">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2f595-141">Remarks</span></span>

<span data-ttu-id="2f595-142">Эта функция вызывается, только если [жетосснапшотсав](./jetossnapshotthaw-function.md) был вызван с JET_bitContinueAfterThaw.</span><span class="sxs-lookup"><span data-stu-id="2f595-142">This function is called only if [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) was called with JET_bitContinueAfterThaw.</span></span>

<span data-ttu-id="2f595-143">Сеанс моментального снимка должен быть завершен для проверки моментальных снимков и усечения журнала.</span><span class="sxs-lookup"><span data-stu-id="2f595-143">The snapshot session must complete for the snapshot verification and log truncation to take place.</span></span> <span data-ttu-id="2f595-144">Записи журнала событий будут созданы для различных этапов создания моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="2f595-144">Event log entries will be generated for the different steps of the snapshot.</span></span>

#### <a name="requirements"></a><span data-ttu-id="2f595-145">Требования</span><span class="sxs-lookup"><span data-stu-id="2f595-145">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2f595-146"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="2f595-146"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="2f595-147">Требуется Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="2f595-147">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f595-148"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="2f595-148"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="2f595-149">Требуется Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="2f595-149">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f595-150"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="2f595-150"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="2f595-151">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="2f595-151">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f595-152"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="2f595-152"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="2f595-153">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="2f595-153">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f595-154"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="2f595-154"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="2f595-155">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="2f595-155">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="2f595-156">См. также:</span><span class="sxs-lookup"><span data-stu-id="2f595-156">See Also</span></span>

[<span data-ttu-id="2f595-157">Параметры обработки ошибок</span><span class="sxs-lookup"><span data-stu-id="2f595-157">Error Handling Parameters</span></span>](./error-handling-parameters.md)  
[<span data-ttu-id="2f595-158">Ошибки расширяемого подсистемы хранилища</span><span class="sxs-lookup"><span data-stu-id="2f595-158">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="2f595-159">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="2f595-159">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="2f595-160">жетосснапшотсав</span><span class="sxs-lookup"><span data-stu-id="2f595-160">JetOSSnapshotThaw</span></span>](./jetossnapshotthaw-function.md)
