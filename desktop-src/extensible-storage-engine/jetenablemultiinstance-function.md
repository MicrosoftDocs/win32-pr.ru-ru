---
description: Дополнительные сведения о функции Жетенаблемултиинстанце
title: Функция Жетенаблемултиинстанце
TOCTitle: JetEnableMultiInstance Function
ms:assetid: d88a7b2a-c0d1-47de-9239-3631150d92da
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294107(v=EXCHG.10)
ms:contentKeyID: 32765722
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetEnableMultiInstanceW
- JetEnableMultiInstanceA
- JetEnableMultiInstance
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 61fb058b14d9a8abeb282d4227b110ba50304a7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693779"
---
# <a name="jetenablemultiinstance-function"></a><span data-ttu-id="78511-103">Функция Жетенаблемултиинстанце</span><span class="sxs-lookup"><span data-stu-id="78511-103">JetEnableMultiInstance Function</span></span>


<span data-ttu-id="78511-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="78511-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetenablemultiinstance-function"></a><span data-ttu-id="78511-105">Функция Жетенаблемултиинстанце</span><span class="sxs-lookup"><span data-stu-id="78511-105">JetEnableMultiInstance Function</span></span>

<span data-ttu-id="78511-106">Функция **жетенаблемултиинстанце** настраивает ядро СУБД для использования с несколькими экземплярами в одном процессе.</span><span class="sxs-lookup"><span data-stu-id="78511-106">The **JetEnableMultiInstance** function configures the database engine for use with multiple instances in the same process.</span></span> <span data-ttu-id="78511-107">Необязательный массив глобальных системных параметров доступен для первого вызывающего объекта, что позволяет изменять режим с несколькими экземплярами.</span><span class="sxs-lookup"><span data-stu-id="78511-107">An optional array of global system parameters is available to the first caller allowing for the change to multi-instance mode.</span></span>

<span data-ttu-id="78511-108">**Windows XP: жетенаблемултиинстанце** появился в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="78511-108">**Windows XP:  JetEnableMultiInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetEnableMultiInstance(
      __in_opt      JET_SETSYSPARAM* psetsysparam,
      __in_opt      unsigned long csetsysparam,
      __out_opt     unsigned long* pcsetsucceed
    );
```

### <a name="parameters"></a><span data-ttu-id="78511-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="78511-109">Parameters</span></span>

<span data-ttu-id="78511-110">*псетсиспарам*</span><span class="sxs-lookup"><span data-stu-id="78511-110">*psetsysparam*</span></span>

<span data-ttu-id="78511-111">Массив глобальных системных параметров, который задается только в том случае, если обработчик переходит в режим с несколькими экземплярами в результате этого вызова.</span><span class="sxs-lookup"><span data-stu-id="78511-111">An array of global system parameters to set if and only if the engine enters multi-instance mode as a result of this call.</span></span> <span data-ttu-id="78511-112">Если *ксетсиспарам* равен нулю, *псетсиспарам* игнорируется.</span><span class="sxs-lookup"><span data-stu-id="78511-112">If *csetsysparam* is zero then *psetsysparam* is ignored.</span></span>

<span data-ttu-id="78511-113">*ксетсиспарам*</span><span class="sxs-lookup"><span data-stu-id="78511-113">*csetsysparam*</span></span>

<span data-ttu-id="78511-114">Число элементов для массива глобальных параметров, которые задаются только в том случае, если обработчик переходит в режим с несколькими экземплярами в результате этого вызова.</span><span class="sxs-lookup"><span data-stu-id="78511-114">The count of elements for the array of global parameters to set if and only if the engine enters multi-instance mode as a result of this call.</span></span> <span data-ttu-id="78511-115">Если *ксетсиспарам* равен нулю, *псетсиспарам* игнорируется.</span><span class="sxs-lookup"><span data-stu-id="78511-115">If *csetsysparam* is zero then *psetsysparam* is ignored.</span></span>

<span data-ttu-id="78511-116">*пксетсукцеед*</span><span class="sxs-lookup"><span data-stu-id="78511-116">*pcsetsucceed*</span></span>

<span data-ttu-id="78511-117">Указатель на число глобальных системных параметров, которые были успешно настроены в результате этого вызова.</span><span class="sxs-lookup"><span data-stu-id="78511-117">A pointer to the count of global system parameters that were successfully configured as a result of this call.</span></span>

### <a name="return-value"></a><span data-ttu-id="78511-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="78511-118">Return Value</span></span>

<span data-ttu-id="78511-119">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="78511-119">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="78511-120">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="78511-120">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="78511-121">Код возврата</span><span class="sxs-lookup"><span data-stu-id="78511-121">Return code</span></span></p></th>
<th><p><span data-ttu-id="78511-122">Описание</span><span class="sxs-lookup"><span data-stu-id="78511-122">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="78511-123">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="78511-123">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="78511-124">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="78511-124">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78511-125">JET_errIndexTuplesInvalidLimits</span><span class="sxs-lookup"><span data-stu-id="78511-125">JET_errIndexTuplesInvalidLimits</span></span></p></td>
<td><p><span data-ttu-id="78511-126">Указанные параметры индекса кортежа не допускаются.</span><span class="sxs-lookup"><span data-stu-id="78511-126">The specified tuple index parameters were not allowed.</span></span> <span data-ttu-id="78511-127">Эта ошибка может возвращаться <strong>жетенаблемултиинстанце</strong> только при задании недопустимых значений <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMin</a>, <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMax</a>или <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesToIndexMax</a> .</span><span class="sxs-lookup"><span data-stu-id="78511-127">This error can be returned by <strong>JetEnableMultiInstance</strong> only when setting <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMin</a>, <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMax</a>, or <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesToIndexMax</a> to an illegal value.</span></span></p>
<p><span data-ttu-id="78511-128"><strong>Windows XP:</strong>  Это возвращаемое значение введено в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="78511-128"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78511-129">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="78511-129">JET_errInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="78511-130">Указан недопустимый путь к файловой системе.</span><span class="sxs-lookup"><span data-stu-id="78511-130">The specified file system path was invalid.</span></span> <span data-ttu-id="78511-131">Эта ошибка может возвращаться <strong>жетенаблемултиинстанце</strong> только при задании системных параметров, представляющих пути файловой системы.</span><span class="sxs-lookup"><span data-stu-id="78511-131">This error can be returned by <strong>JetEnableMultiInstance</strong> only when setting system parameters that represent file system paths.</span></span> <span data-ttu-id="78511-132">Например, <a href="gg269235(v=exchg.10).md">JET_paramSystemPath</a> может возвращать эту ошибку.</span><span class="sxs-lookup"><span data-stu-id="78511-132">For example, <a href="gg269235(v=exchg.10).md">JET_paramSystemPath</a> can return this error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78511-133">JET_errRunningInOneInstanceMode</span><span class="sxs-lookup"><span data-stu-id="78511-133">JET_errRunningInOneInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="78511-134">Операция завершилась ошибкой, так как она недопустима, если ядро СУБД работает в режиме одиночного экземпляра (режим совместимости с Windows 2000).</span><span class="sxs-lookup"><span data-stu-id="78511-134">The operation failed because it is illegal when the database engine is operating in single instance mode (Windows 2000 compatibility mode).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78511-135">JET_errSystemParamsAlreadySet</span><span class="sxs-lookup"><span data-stu-id="78511-135">JET_errSystemParamsAlreadySet</span></span></p></td>
<td><p><span data-ttu-id="78511-136">Сбой <strong>жетенаблемултиинстанце</strong> , так как модуль уже находится в режиме с несколькими экземплярами.</span><span class="sxs-lookup"><span data-stu-id="78511-136"><strong>JetEnableMultiInstance</strong> failed because the engine is already in multi-instance mode.</span></span></p>
<p><span data-ttu-id="78511-137"><strong>Примечание  </strong> . Это произойдет, даже если системные параметры не указаны.</span><span class="sxs-lookup"><span data-stu-id="78511-137"><strong>Note  </strong>This will happen even if no system parameters are specified.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="78511-138">Если эта функция завершится с ошибкой, ядро СУБД будет настроено для работы в режиме с несколькими экземплярами.</span><span class="sxs-lookup"><span data-stu-id="78511-138">If this function succeeds, the database engine will be configured to run in multi-instance mode.</span></span> <span data-ttu-id="78511-139">Для этого механизма также успешно настроен необязательный список глобальных параметров системы.</span><span class="sxs-lookup"><span data-stu-id="78511-139">The engine was also successfully configured with the optional list of global system parameters.</span></span>

<span data-ttu-id="78511-140">Если эта функция завершается ошибкой, ядро СУБД остается в текущем режиме.</span><span class="sxs-lookup"><span data-stu-id="78511-140">If this function fails, the database engine will remain in the current mode.</span></span> <span data-ttu-id="78511-141">Если *пксетсукцеед* не равно нулю, то это число системных параметров останется установленным.</span><span class="sxs-lookup"><span data-stu-id="78511-141">If *pcsetsucceed* is non-zero, that number of system parameters will remain set.</span></span>

#### <a name="remarks"></a><span data-ttu-id="78511-142">Комментарии</span><span class="sxs-lookup"><span data-stu-id="78511-142">Remarks</span></span>

<span data-ttu-id="78511-143">Эта функция должна использоваться, только если приложение должно настроить заданный набор системных параметров атомарно при настройке ядра СУБД для использования в сценарии с несколькими пользователями в одном процессе.</span><span class="sxs-lookup"><span data-stu-id="78511-143">This function should only be used if the application must configure a given set of system parameters atomically when setting up the database engine for use in a multi-user scenario in the same process.</span></span> <span data-ttu-id="78511-144">Если доступен другой метод синхронизации, предпочтительнее вызывать [жеткреатеинстанце](./jetcreateinstance-function.md) и [жетсетсистемпараметер](./jetsetsystemparameter-function.md) отдельно.</span><span class="sxs-lookup"><span data-stu-id="78511-144">If another method of synchronization is available, it is preferable to call [JetCreateInstance](./jetcreateinstance-function.md) and [JetSetSystemParameter](./jetsetsystemparameter-function.md) separately.</span></span>

#### <a name="requirements"></a><span data-ttu-id="78511-145">Требования</span><span class="sxs-lookup"><span data-stu-id="78511-145">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="78511-146"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="78511-146"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="78511-147">Требуется Windows Vista или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="78511-147">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78511-148"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="78511-148"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="78511-149">Требуется Windows Server 2008 или Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="78511-149">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78511-150"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="78511-150"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="78511-151">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="78511-151">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78511-152"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="78511-152"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="78511-153">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="78511-153">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78511-154"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="78511-154"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="78511-155">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="78511-155">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78511-156"><strong>Юникод</strong></span><span class="sxs-lookup"><span data-stu-id="78511-156"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="78511-157">Реализуется как <strong>жетенаблемултиинстанцев</strong> (Юникод) и <strong>жетенаблемултиинстанцеа</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="78511-157">Implemented as <strong>JetEnableMultiInstanceW</strong> (Unicode) and <strong>JetEnableMultiInstanceA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="78511-158">См. также:</span><span class="sxs-lookup"><span data-stu-id="78511-158">See Also</span></span>

[<span data-ttu-id="78511-159">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="78511-159">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="78511-160">JET_SETSYSPARAM</span><span class="sxs-lookup"><span data-stu-id="78511-160">JET_SETSYSPARAM</span></span>](./jet-setsysparam-structure.md)  
[<span data-ttu-id="78511-161">жеткреатеинстанце</span><span class="sxs-lookup"><span data-stu-id="78511-161">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="78511-162">жетинит</span><span class="sxs-lookup"><span data-stu-id="78511-162">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="78511-163">жетсетсистемпараметер</span><span class="sxs-lookup"><span data-stu-id="78511-163">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)
