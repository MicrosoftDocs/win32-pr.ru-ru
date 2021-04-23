---
description: Дополнительные сведения о функции Жетсетсессионпараметер
title: Функция Жетсетсессионпараметер
TOCTitle: JetSetSessionParameter Function
ms:assetid: 11aecf42-22ef-4bea-a3d7-961a7bdc85aa
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835038(v=EXCHG.10)
ms:contentKeyID: 49894660
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetSetSessionParameter
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 926ae0db2e47ce571f441ab5836c4ddbe6f8bcc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990980"
---
# <a name="jetsetsessionparameter-function"></a><span data-ttu-id="4af6d-103">Функция Жетсетсессионпараметер</span><span class="sxs-lookup"><span data-stu-id="4af6d-103">JetSetSessionParameter Function</span></span>


<span data-ttu-id="4af6d-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="4af6d-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="4af6d-105">Функция **жетсетсессионпараметер** настраивает ядро СУБД.</span><span class="sxs-lookup"><span data-stu-id="4af6d-105">The **JetSetSessionParameter** function configures the database engine.</span></span>

``` c++
JET_ERR JET_API JetSetSessionParameter (
  __in_opt      JET_SESID sesid,
  __in          unsigned long sesparamid,
  __in_read_bytes_opt_(cbParam)  void* pvParam,
  __in          unsigned long cbParam
);
```

### <a name="parameters"></a><span data-ttu-id="4af6d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4af6d-106">Parameters</span></span>

<span data-ttu-id="4af6d-107">*сесид*</span><span class="sxs-lookup"><span data-stu-id="4af6d-107">*sesid*</span></span>

<span data-ttu-id="4af6d-108">Указывает сеанс, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="4af6d-108">Specifies the session to use for this call.</span></span>

<span data-ttu-id="4af6d-109">Если этот параметр указан, то указанный экземпляр игнорируется, и будет использоваться экземпляр, связанный с сеансом.</span><span class="sxs-lookup"><span data-stu-id="4af6d-109">When specified, the specified instance is ignored and the instance associated with the session will be used.</span></span>

<span data-ttu-id="4af6d-110">*сеспарамид*</span><span class="sxs-lookup"><span data-stu-id="4af6d-110">*sesparamid*</span></span>

<span data-ttu-id="4af6d-111">ИДЕНТИФИКАТОР устанавливаемого параметра сеанса.</span><span class="sxs-lookup"><span data-stu-id="4af6d-111">The ID of the session parameter to set.</span></span>

<span data-ttu-id="4af6d-112">*пвпарам*</span><span class="sxs-lookup"><span data-stu-id="4af6d-112">*pvParam*</span></span>

<span data-ttu-id="4af6d-113">Данные, которые необходимо задать в этом параметре сеанса.</span><span class="sxs-lookup"><span data-stu-id="4af6d-113">The data to set in this session parameter.</span></span>

<span data-ttu-id="4af6d-114">*кбпарам*</span><span class="sxs-lookup"><span data-stu-id="4af6d-114">*cbParam*</span></span>

<span data-ttu-id="4af6d-115">Размер предоставленных данных.</span><span class="sxs-lookup"><span data-stu-id="4af6d-115">The size of the data provided.</span></span>

### <a name="return-value"></a><span data-ttu-id="4af6d-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4af6d-116">Return value</span></span>

<span data-ttu-id="4af6d-117">Эта функция возвращает [JET_ERR](./jet-err.md) тип данных с одним из кодов возврата, перечисленных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="4af6d-117">This function returns the [JET_ERR](./jet-err.md) data type with one of the return codes listed in the following table.</span></span> <span data-ttu-id="4af6d-118">Дополнительные сведения о возможных ошибках ESE см. в разделе [Расширенные ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="4af6d-118">For more information about the possible Extensible Storage Engine (ESE) errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4af6d-119">Код возврата</span><span class="sxs-lookup"><span data-stu-id="4af6d-119">Return code</span></span></p></th>
<th><p><span data-ttu-id="4af6d-120">Описание</span><span class="sxs-lookup"><span data-stu-id="4af6d-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4af6d-121">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="4af6d-121">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="4af6d-122">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="4af6d-122">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4af6d-123">JET_errAlreadyInitialized</span><span class="sxs-lookup"><span data-stu-id="4af6d-123">JET_errAlreadyInitialized</span></span></p></td>
<td><p><span data-ttu-id="4af6d-124">Экземпляр был инициализирован с помощью вызова функции <a href="gg294068(v=exchg.10).md">жетинит</a> , и эта операция не может быть выполнена в результате.</span><span class="sxs-lookup"><span data-stu-id="4af6d-124">The instance has been initialized by using a call to the <a href="gg294068(v=exchg.10).md">JetInit</a> function and this operation cannot be performed as a result.</span></span> <span data-ttu-id="4af6d-125">Это может произойти при попытке настроить системный параметр после изменения значения параметра, которое больше не может повлиять на состояние ядра СУБД.</span><span class="sxs-lookup"><span data-stu-id="4af6d-125">This can happen when an attempt is made to configure a system parameter after a change in the parameter value can no longer affect the state of the database engine.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4af6d-126">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="4af6d-126">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="4af6d-127">Невозможно выполнить операцию, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова функции <a href="gg269240(v=exchg.10).md">жетстопсервице</a> .</span><span class="sxs-lookup"><span data-stu-id="4af6d-127">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to the <a href="gg269240(v=exchg.10).md">JetStopService</a> function.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4af6d-128">JET_errIndexTuplesInvalidLimits</span><span class="sxs-lookup"><span data-stu-id="4af6d-128">JET_errIndexTuplesInvalidLimits</span></span></p></td>
<td><p><span data-ttu-id="4af6d-129">Указаны недопустимые параметры индекса кортежа.</span><span class="sxs-lookup"><span data-stu-id="4af6d-129">The specified tuple index parameters were illegal.</span></span> <span data-ttu-id="4af6d-130">Эта ошибка возвращается только в том случае, если для параметра <em>JET_paramIndexTuplesLengthMin</em>, <em>JET_paramIndexTuplesLengthMax</em>или <em>JET_paramIndexTuplesToIndexMax</em> задано недопустимое значение.</span><span class="sxs-lookup"><span data-stu-id="4af6d-130">This error is returned only when the <em>JET_paramIndexTuplesLengthMin</em>, <em>JET_paramIndexTuplesLengthMax</em>, or <em>JET_paramIndexTuplesToIndexMax</em> parameter is set to an illegal value.</span></span> <span data-ttu-id="4af6d-131">Дополнительные сведения об этих параметрах см. в разделе <a href="gg294119(v=exchg.10).md">Параметры индекса</a>.</span><span class="sxs-lookup"><span data-stu-id="4af6d-131">For information about these parameters, see <a href="gg294119(v=exchg.10).md">Index Parameters</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4af6d-132">JET_errInitInProgress</span><span class="sxs-lookup"><span data-stu-id="4af6d-132">JET_errInitInProgress</span></span></p></td>
<td><p><span data-ttu-id="4af6d-133">Невозможно выполнить операцию, так как инициализируется экземпляр, связанный с сеансом.</span><span class="sxs-lookup"><span data-stu-id="4af6d-133">It is not possible to complete the operation because the instance associated with the session is being initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4af6d-134">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="4af6d-134">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="4af6d-135">Невозможно выполнить операцию, поскольку экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</span><span class="sxs-lookup"><span data-stu-id="4af6d-135">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4af6d-136">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="4af6d-136">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="4af6d-137">Один из указанных параметров содержит непредвиденное значение или содержит значение, которое не имеет смысла при объединении со значением другого параметра.</span><span class="sxs-lookup"><span data-stu-id="4af6d-137">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="4af6d-138">Это может произойти, если происходит следующее:</span><span class="sxs-lookup"><span data-stu-id="4af6d-138">This can happen when the following occurs:</span></span></p>
<ul>
<li><p><span data-ttu-id="4af6d-139">Указанный идентификатор системного параметра является недопустимым или не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="4af6d-139">The specified system parameter ID is invalid or unsupported.</span></span></p></li>
<li><p><span data-ttu-id="4af6d-140">Предпринята попытка установить системный параметр с строковыми значениями, длина которого находилась вне допустимого диапазона для параметра.</span><span class="sxs-lookup"><span data-stu-id="4af6d-140">An attempt was made to set a string-valued system parameter with a string the length of which was outside the legal range for the parameter.</span></span></p></li>
<li><p><span data-ttu-id="4af6d-141">Предпринята попытка установить системный параметр с символьным значением, где длина его абсолютного пути находилась вне допустимого диапазона для этого параметра.</span><span class="sxs-lookup"><span data-stu-id="4af6d-141">An attempt was made to set a string-valued system parameter with a file path where the length of its absolute path representation was outside the legal range for that parameter.</span></span></p></li>
<li><p><span data-ttu-id="4af6d-142">Предпринята попытка установить системный параметр с целочисленными значениями, который находится за пределами допустимого диапазона для параметра.</span><span class="sxs-lookup"><span data-stu-id="4af6d-142">An attempt was made to set an integer-valued system parameter with an integer that was outside the legal range for the parameter.</span></span></p></li>
<li><p><span data-ttu-id="4af6d-143">Предпринята попытка задать JET_paramUnicodeIndexDefault с нулевым указателем <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> , недопустимым LCID или неподдерживаемым набором флагов <strong>LCMapString завершилось ошибкой</strong> .</span><span class="sxs-lookup"><span data-stu-id="4af6d-143">An attempt was made to set JET_paramUnicodeIndexDefault with a null <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> pointer, an invalid LCID, or an unsupported set of <strong>LCMapString</strong> flags.</span></span></p></li>
<li><p><span data-ttu-id="4af6d-144">Невозможно задать указанный системный параметр, так как он доступен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="4af6d-144">The specified system parameter cannot be set because it is read-only.</span></span></p></li>
<li><p><span data-ttu-id="4af6d-145">Предпринята попытка установить системный параметр после вызова функции <a href="gg294068(v=exchg.10).md">жетинит</a> , ядро СУБД находится в режиме с одним экземпляром, а сеанс не был указан.</span><span class="sxs-lookup"><span data-stu-id="4af6d-145">An attempt was made to set a system parameter after the <a href="gg294068(v=exchg.10).md">JetInit</a> function was called, the database engine is in single-instance mode, and a session was not specified.</span></span></p></li>
<li><p><span data-ttu-id="4af6d-146">Указанный системный параметр является глобальным, и предпринята попытка задать для этого системного параметра значение конкретного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="4af6d-146">The specified system parameter is global only and an attempt was made to set an instance-specific value for that system parameter.</span></span></p></li>
<li><p><span data-ttu-id="4af6d-147">Указанный системный параметр доступен только для одного экземпляра, и предпринята попытка установить глобальное значение для этого системного параметра.</span><span class="sxs-lookup"><span data-stu-id="4af6d-147">The specified system parameter is per-instance only and an attempt was made to set the global value for that system parameter.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4af6d-148">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="4af6d-148">JET_errInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="4af6d-149">Указан недопустимый путь к файловой системе.</span><span class="sxs-lookup"><span data-stu-id="4af6d-149">The specified file system path was invalid.</span></span> <span data-ttu-id="4af6d-150">Эта ошибка может возвращаться <strong>жетсетсессионпараметер</strong> только при задании системных параметров, представляющих пути файловой системы.</span><span class="sxs-lookup"><span data-stu-id="4af6d-150">This error may be returned by <strong>JetSetSessionParameter</strong> only when setting system parameters that represent file system paths.</span></span> <span data-ttu-id="4af6d-151">Например, параметр <em>JET_paramSystemPath</em> может возвращать эту ошибку.</span><span class="sxs-lookup"><span data-stu-id="4af6d-151">For example, the <em>JET_paramSystemPath</em> parameter may return this error.</span></span> <span data-ttu-id="4af6d-152">Дополнительные сведения об этом параметре см. в разделе <a href="gg269235(v=exchg.10).md">Параметры журнала транзакций</a>.</span><span class="sxs-lookup"><span data-stu-id="4af6d-152">For information about this parameter, see <a href="gg269235(v=exchg.10).md">Transaction Log Parameters</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4af6d-153">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="4af6d-153">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="4af6d-154">Невозможно выполнить операцию, так как экземпляр, связанный с сеансом, еще не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="4af6d-154">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4af6d-155">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="4af6d-155">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="4af6d-156">Невозможно выполнить операцию, так как в экземпляре, связанном с сеансом, выполняется операция восстановления.</span><span class="sxs-lookup"><span data-stu-id="4af6d-156">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4af6d-157">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="4af6d-157">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="4af6d-158">Невозможно выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</span><span class="sxs-lookup"><span data-stu-id="4af6d-158">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4af6d-159">JET_errInvalidSesid</span><span class="sxs-lookup"><span data-stu-id="4af6d-159">JET_errInvalidSesid</span></span></p></td>
<td><p><span data-ttu-id="4af6d-160">Недопустимый обработчик сеанса или ссылается на закрытый сеанс.</span><span class="sxs-lookup"><span data-stu-id="4af6d-160">The session handle is invalid or refers to a closed session.</span></span></p>
<p><span data-ttu-id="4af6d-161">Эта ошибка не возвращается при всех обстоятельствах.</span><span class="sxs-lookup"><span data-stu-id="4af6d-161">This error is not returned under all circumstances.</span></span> <span data-ttu-id="4af6d-162">Дескрипторы проверяются только на основе наилучшей силы.</span><span class="sxs-lookup"><span data-stu-id="4af6d-162">Handles are validated on a best effort basis only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4af6d-163">JET_errInvalidInstance</span><span class="sxs-lookup"><span data-stu-id="4af6d-163">JET_errInvalidInstance</span></span></p></td>
<td><p><span data-ttu-id="4af6d-164">Недопустимый указатель экземпляра или ссылка на экземпляр, который был закрыт.</span><span class="sxs-lookup"><span data-stu-id="4af6d-164">The instance handle is invalid or refers to an instance that has been shut down.</span></span></p>
<p><span data-ttu-id="4af6d-165">Эта ошибка не возвращается при всех обстоятельствах.</span><span class="sxs-lookup"><span data-stu-id="4af6d-165">This error is not returned under all circumstances.</span></span> <span data-ttu-id="4af6d-166">Дескрипторы проверяются только на основе наилучшей силы.</span><span class="sxs-lookup"><span data-stu-id="4af6d-166">Handles are validated on a best effort basis only.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4af6d-167">При успешном выполнении параметру System будет присвоено указанное значение.</span><span class="sxs-lookup"><span data-stu-id="4af6d-167">On success, the system parameter will be set to the provided value.</span></span>

<span data-ttu-id="4af6d-168">При сбое значение системного параметра останется неизменным.</span><span class="sxs-lookup"><span data-stu-id="4af6d-168">On failure, the system parameter value will remain unchanged.</span></span>

#### <a name="requirements"></a><span data-ttu-id="4af6d-169">Требования</span><span class="sxs-lookup"><span data-stu-id="4af6d-169">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4af6d-170"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="4af6d-170"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="4af6d-171">Требуется Windows 8.</span><span class="sxs-lookup"><span data-stu-id="4af6d-171">Requires Windows 8.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4af6d-172"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="4af6d-172"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="4af6d-173">Требуется Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="4af6d-173">Requires Windows Server 2012.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4af6d-174"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="4af6d-174"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="4af6d-175">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="4af6d-175">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4af6d-176"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="4af6d-176"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="4af6d-177">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="4af6d-177">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4af6d-178"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="4af6d-178"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="4af6d-179">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="4af6d-179">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="4af6d-180">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4af6d-180">See also</span></span>

[<span data-ttu-id="4af6d-181">JET_API_PTR</span><span class="sxs-lookup"><span data-stu-id="4af6d-181">JET_API_PTR</span></span>](./jet-api-ptr.md)  
[<span data-ttu-id="4af6d-182">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="4af6d-182">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="4af6d-183">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="4af6d-183">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="4af6d-184">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="4af6d-184">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="4af6d-185">жеткреатеинстанце</span><span class="sxs-lookup"><span data-stu-id="4af6d-185">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="4af6d-186">жетжетсистемпараметер</span><span class="sxs-lookup"><span data-stu-id="4af6d-186">JetGetSystemParameter</span></span>](./jetgetsystemparameter-function.md)  
[<span data-ttu-id="4af6d-187">жетинит</span><span class="sxs-lookup"><span data-stu-id="4af6d-187">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="4af6d-188">Системные параметры</span><span class="sxs-lookup"><span data-stu-id="4af6d-188">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
