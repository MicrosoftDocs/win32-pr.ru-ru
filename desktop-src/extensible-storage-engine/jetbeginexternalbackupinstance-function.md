---
description: Дополнительные сведения о функции Жетбегинекстерналбаккупинстанце
title: Функция Жетбегинекстерналбаккупинстанце
TOCTitle: JetBeginExternalBackupInstance Function
ms:assetid: f1c5a73d-b1cc-4ee4-942b-b5e4ef51bc2f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294132(v=EXCHG.10)
ms:contentKeyID: 32765746
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBeginExternalBackupInstance
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bab2fa3d9faa7f81abea278e3d9fcf4a4022c24c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496935"
---
# <a name="jetbeginexternalbackupinstance-function"></a><span data-ttu-id="0b4bf-103">Функция Жетбегинекстерналбаккупинстанце</span><span class="sxs-lookup"><span data-stu-id="0b4bf-103">JetBeginExternalBackupInstance Function</span></span>


<span data-ttu-id="0b4bf-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="0b4bf-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetbeginexternalbackupinstance-function"></a><span data-ttu-id="0b4bf-105">Функция Жетбегинекстерналбаккупинстанце</span><span class="sxs-lookup"><span data-stu-id="0b4bf-105">JetBeginExternalBackupInstance Function</span></span>

<span data-ttu-id="0b4bf-106">Функция **жетбегинекстерналбаккупинстанце** инициирует внешнюю архивацию, пока ядро и база данных находятся в сети и активны.</span><span class="sxs-lookup"><span data-stu-id="0b4bf-106">The **JetBeginExternalBackupInstance** function initiates an external backup while the engine and database are online and active.</span></span>

<span data-ttu-id="0b4bf-107">**Windows XP: жетбегинекстерналбаккупинстанце** появился в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0b4bf-107">**Windows XP:  JetBeginExternalBackupInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetBeginExternalBackupInstance(
      __in          JET_INSTANCE instance,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="0b4bf-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="0b4bf-108">Parameters</span></span>

<span data-ttu-id="0b4bf-109">*вхождение*</span><span class="sxs-lookup"><span data-stu-id="0b4bf-109">*instance*</span></span>

<span data-ttu-id="0b4bf-110">Экземпляр базы данных, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="0b4bf-110">The database instance to use for this call.</span></span>

<span data-ttu-id="0b4bf-111">Для Windows 2000 вариант API, который принимает этот параметр, недоступен, так как поддерживается только один экземпляр.</span><span class="sxs-lookup"><span data-stu-id="0b4bf-111">For Windows 2000, the API variant that accepts this parameter is not available because only one instance is supported.</span></span> <span data-ttu-id="0b4bf-112">В этом случае подразумевается использование этого одного глобального экземпляра.</span><span class="sxs-lookup"><span data-stu-id="0b4bf-112">The use of this one global instance is implied in this case.</span></span>

<span data-ttu-id="0b4bf-113">Для Windows XP и более поздних версий вариант API, который не принимает этот параметр, может вызываться только в том случае, если ядро находится в режиме совместимости с Windows 2000, где поддерживается только один экземпляр.</span><span class="sxs-lookup"><span data-stu-id="0b4bf-113">For Windows XP and later releases, the API variant that does not accept this parameter may only be called when the engine is in legacy mode (Windows 2000 compatibility mode) where only one instance is supported.</span></span> <span data-ttu-id="0b4bf-114">В противном случае операция завершится ошибкой с JET_errRunningInMultiInstanceMode.</span><span class="sxs-lookup"><span data-stu-id="0b4bf-114">Otherwise, the operation will fail with JET_errRunningInMultiInstanceMode.</span></span>

<span data-ttu-id="0b4bf-115">*грбит*</span><span class="sxs-lookup"><span data-stu-id="0b4bf-115">*grbit*</span></span>

<span data-ttu-id="0b4bf-116">Группа битов, задающая ноль или более следующих параметров.</span><span class="sxs-lookup"><span data-stu-id="0b4bf-116">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0b4bf-117">Значение</span><span class="sxs-lookup"><span data-stu-id="0b4bf-117">Value</span></span></p></th>
<th><p><span data-ttu-id="0b4bf-118">Значение</span><span class="sxs-lookup"><span data-stu-id="0b4bf-118">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0b4bf-119">JET_bitBackupAtomic</span><span class="sxs-lookup"><span data-stu-id="0b4bf-119">JET_bitBackupAtomic</span></span></p></td>
<td><p><span data-ttu-id="0b4bf-120">Этот флаг является устаревшим.</span><span class="sxs-lookup"><span data-stu-id="0b4bf-120">This flag is deprecated.</span></span> <span data-ttu-id="0b4bf-121">Использование этого бита приведет к возвращению JET_errInvalidgrbit.</span><span class="sxs-lookup"><span data-stu-id="0b4bf-121">Usage of this bit will result in JET_errInvalidgrbit being returned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0b4bf-122">JET_bitBackupIncremental</span><span class="sxs-lookup"><span data-stu-id="0b4bf-122">JET_bitBackupIncremental</span></span></p></td>
<td><p><span data-ttu-id="0b4bf-123">Создает добавочное резервное копирование, а не полное резервное копирование.</span><span class="sxs-lookup"><span data-stu-id="0b4bf-123">Creates an incremental backup as opposed to a full backup.</span></span> <span data-ttu-id="0b4bf-124">Это означает, что резервное копирование выполняется только для файлов журнала с момента последнего полного или добавочного резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="0b4bf-124">This means that only the log files since the last full or incremental backup will be backed up.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0b4bf-125">JET_bitBackupSnapshot</span><span class="sxs-lookup"><span data-stu-id="0b4bf-125">JET_bitBackupSnapshot</span></span></p></td>
<td><p><span data-ttu-id="0b4bf-126">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="0b4bf-126">Reserved for future use.</span></span> <span data-ttu-id="0b4bf-127">Определено для Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0b4bf-127">Defined for Windows XP.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="0b4bf-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0b4bf-128">Return Value</span></span>

<span data-ttu-id="0b4bf-129">Система может создать коды успеха или сбоя в результате вызова этой функции.</span><span class="sxs-lookup"><span data-stu-id="0b4bf-129">The system may generate success or failure codes as a result of a call to this function.</span></span> <span data-ttu-id="0b4bf-130">Полный список ошибок для этого API см. в разделе [расширенные коды ошибок подсистемы хранилища](./extensible-storage-engine-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="0b4bf-130">For a complete list of errors for this API, see [Extensible Storage Engine Error Codes](./extensible-storage-engine-error-codes.md).</span></span>

<span data-ttu-id="0b4bf-131">См. [жетбегинекстерналбаккуп](./jetbeginexternalbackup-function.md).</span><span class="sxs-lookup"><span data-stu-id="0b4bf-131">See [JetBeginExternalBackup](./jetbeginexternalbackup-function.md).</span></span>

#### <a name="remarks"></a><span data-ttu-id="0b4bf-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0b4bf-132">Remarks</span></span>

<span data-ttu-id="0b4bf-133">**Жетбегинекстерналбаккупинстанце** — это первая функция в серии функций, которая должна вызываться для успешного выполнения резервного копирования (не на основе VSS).</span><span class="sxs-lookup"><span data-stu-id="0b4bf-133">**JetBeginExternalBackupInstance** is the first function in a series of functions that must be called to execute a successful online (non-VSS based) backup.</span></span> <span data-ttu-id="0b4bf-134">См. также [жетбегинекстерналбаккуп](./jetbeginexternalbackup-function.md) и [жетстопбаккупинстанце](./jetstopbackupinstance-function.md).</span><span class="sxs-lookup"><span data-stu-id="0b4bf-134">See also [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) and [JetStopBackupInstance](./jetstopbackupinstance-function.md).</span></span>

<span data-ttu-id="0b4bf-135">Внешнюю резервную копию можно использовать для реализации полных, добавочных или разностных резервных копий.</span><span class="sxs-lookup"><span data-stu-id="0b4bf-135">An external backup can be used to implement full, incremental, or differential backups.</span></span>

<span data-ttu-id="0b4bf-136">Резервное копирование будет нечетким, в то время как резервная копия будет соответствовать одному моменту времени в журнале транзакций, но в данный момент нельзя будет контролировать конкретный момент времени.</span><span class="sxs-lookup"><span data-stu-id="0b4bf-136">The backup will be fuzzy, in that the backup will be consistent to a single point in time in the transaction history, but controlling the exact point in time is not possible at this time.</span></span>

#### <a name="requirements"></a><span data-ttu-id="0b4bf-137">Требования</span><span class="sxs-lookup"><span data-stu-id="0b4bf-137">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0b4bf-138"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="0b4bf-138"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="0b4bf-139">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="0b4bf-139">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0b4bf-140"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="0b4bf-140"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="0b4bf-141">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="0b4bf-141">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0b4bf-142"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="0b4bf-142"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="0b4bf-143">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="0b4bf-143">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0b4bf-144"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="0b4bf-144"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="0b4bf-145">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="0b4bf-145">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0b4bf-146"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="0b4bf-146"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="0b4bf-147">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="0b4bf-147">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="0b4bf-148">См. также:</span><span class="sxs-lookup"><span data-stu-id="0b4bf-148">See Also</span></span>

[<span data-ttu-id="0b4bf-149">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="0b4bf-149">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="0b4bf-150">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="0b4bf-150">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="0b4bf-151">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="0b4bf-151">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="0b4bf-152">жетаттачдатабасе</span><span class="sxs-lookup"><span data-stu-id="0b4bf-152">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="0b4bf-153">жетбегинекстерналбаккуп</span><span class="sxs-lookup"><span data-stu-id="0b4bf-153">JetBeginExternalBackup</span></span>](./jetbeginexternalbackup-function.md)  
[<span data-ttu-id="0b4bf-154">жетклосефиле</span><span class="sxs-lookup"><span data-stu-id="0b4bf-154">JetCloseFile</span></span>](./jetclosefile-function.md)  
[<span data-ttu-id="0b4bf-155">жетендекстерналбаккуп</span><span class="sxs-lookup"><span data-stu-id="0b4bf-155">JetEndExternalBackup</span></span>](./jetendexternalbackup-function.md)  
[<span data-ttu-id="0b4bf-156">JetEndExternalBackupInstance2</span><span class="sxs-lookup"><span data-stu-id="0b4bf-156">JetEndExternalBackupInstance2</span></span>](./jetendexternalbackupinstance2-function.md)  
[<span data-ttu-id="0b4bf-157">жетжетаттачинфо</span><span class="sxs-lookup"><span data-stu-id="0b4bf-157">JetGetAttachInfo</span></span>](./jetgetattachinfo-function.md)  
[<span data-ttu-id="0b4bf-158">жетжетлогинфо</span><span class="sxs-lookup"><span data-stu-id="0b4bf-158">JetGetLogInfo</span></span>](./jetgetloginfo-function.md)  
[<span data-ttu-id="0b4bf-159">жетопенфиле</span><span class="sxs-lookup"><span data-stu-id="0b4bf-159">JetOpenFile</span></span>](./jetopenfile-function.md)  
[<span data-ttu-id="0b4bf-160">жетреадфиле</span><span class="sxs-lookup"><span data-stu-id="0b4bf-160">JetReadFile</span></span>](./jetreadfile-function.md)  
[<span data-ttu-id="0b4bf-161">жетстопбаккуп</span><span class="sxs-lookup"><span data-stu-id="0b4bf-161">JetStopBackup</span></span>](./jetstopbackup-function.md)  
[<span data-ttu-id="0b4bf-162">жеттрункателог</span><span class="sxs-lookup"><span data-stu-id="0b4bf-162">JetTruncateLog</span></span>](./jettruncatelog-function.md)
