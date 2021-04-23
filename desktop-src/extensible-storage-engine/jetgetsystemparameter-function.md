---
description: Дополнительные сведения о функции Жетжетсистемпараметер
title: Функция Жетжетсистемпараметер
TOCTitle: JetGetSystemParameter Function
ms:assetid: 6e6ddb49-702c-4c45-ac9f-35ae817696dd
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269291(v=EXCHG.10)
ms:contentKeyID: 32765583
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetSystemParameter
- JetGetSystemParameterA
- JetGetSystemParameterW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 80005be47037bade1f22e8125d4633c5dac45f8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272116"
---
# <a name="jetgetsystemparameter-function"></a><span data-ttu-id="c621b-103">Функция Жетжетсистемпараметер</span><span class="sxs-lookup"><span data-stu-id="c621b-103">JetGetSystemParameter Function</span></span>


<span data-ttu-id="c621b-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="c621b-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetsystemparameter-function"></a><span data-ttu-id="c621b-105">Функция Жетжетсистемпараметер</span><span class="sxs-lookup"><span data-stu-id="c621b-105">JetGetSystemParameter Function</span></span>

<span data-ttu-id="c621b-106">Функция **жетжетсистемпараметер** считывает многочисленные параметры конфигурации ядра СУБД.</span><span class="sxs-lookup"><span data-stu-id="c621b-106">The **JetGetSystemParameter** function reads the numerous configuration settings of the database engine.</span></span>

```cpp
    JET_ERR JET_API JetGetSystemParameter(
      __in          JET_INSTANCE instance,
      __in          JET_SESID sesid,
      __in          unsigned long paramid,
      __in_out_opt  JET_API_PTR* plParam,
      __out_opt     JET_PSTR szParam,
      __in          unsigned long cbMax
    );
```

### <a name="parameters"></a><span data-ttu-id="c621b-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="c621b-107">Parameters</span></span>

<span data-ttu-id="c621b-108">*вхождение*</span><span class="sxs-lookup"><span data-stu-id="c621b-108">*instance*</span></span>

<span data-ttu-id="c621b-109">Экземпляр, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="c621b-109">The instance to use for this call.</span></span>

<span data-ttu-id="c621b-110">Для Windows 2000 этот параметр игнорируется и всегда должен иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="c621b-110">For Windows 2000, this parameter is ignored and should always be **NULL**.</span></span>

<span data-ttu-id="c621b-111">Для Windows XP и более поздних версий этот параметр несколько перегружен.</span><span class="sxs-lookup"><span data-stu-id="c621b-111">For Windows XP and later releases, this parameter is somewhat overloaded.</span></span> <span data-ttu-id="c621b-112">Если ядро работает в устаревшем режиме (режим совместимости Windows 2000), где поддерживается только один экземпляр, этот параметр может иметь **значение NULL** или содержать фактический экземпляр, возвращаемый функцией [жетинит](./jetinit-function.md).</span><span class="sxs-lookup"><span data-stu-id="c621b-112">If the engine is operating in legacy mode (Windows 2000 compatibility mode) where only one instance is supported, this parameter may be **NULL** or may contain the actual instance returned by [JetInit](./jetinit-function.md).</span></span> <span data-ttu-id="c621b-113">В любом случае все параметры системного параметра считываются из одного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="c621b-113">In either case, all system parameter settings are read from that one instance.</span></span> <span data-ttu-id="c621b-114">Если ядро работает в режиме с несколькими экземплярами, этот параметр может иметь **значение NULL** или указатель на экземпляр, созданный с помощью [жетинит](./jetinit-function.md) или [жеткреатеинстанце](./jetcreateinstance-function.md).</span><span class="sxs-lookup"><span data-stu-id="c621b-114">If the engine is operating in multi-instance mode, this parameter may be **NULL** or a pointer to an instance created using [JetInit](./jetinit-function.md) or [JetCreateInstance](./jetcreateinstance-function.md).</span></span> <span data-ttu-id="c621b-115">Если этот параметр имеет **значение NULL** , то считывается параметр глобального системного параметра (или значение по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="c621b-115">When this parameter is **NULL** then the global system parameter setting (or default) is read.</span></span> <span data-ttu-id="c621b-116">Если этот параметр является экземпляром, то параметр системного параметра для этого экземпляра считывается.</span><span class="sxs-lookup"><span data-stu-id="c621b-116">When this parameter is an instance then the system parameter setting for that instance is read.</span></span>

<span data-ttu-id="c621b-117">*сесид*</span><span class="sxs-lookup"><span data-stu-id="c621b-117">*sesid*</span></span>

<span data-ttu-id="c621b-118">Сеанс, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="c621b-118">The session to use for this call.</span></span>

<span data-ttu-id="c621b-119">Если этот параметр указан, то указанный экземпляр игнорируется, и будет использоваться экземпляр, связанный с сеансом.</span><span class="sxs-lookup"><span data-stu-id="c621b-119">When specified, the specified instance is ignored and the instance associated with the session will be used.</span></span>

<span data-ttu-id="c621b-120">*paramid*</span><span class="sxs-lookup"><span data-stu-id="c621b-120">*paramid*</span></span>

<span data-ttu-id="c621b-121">Идентификатор системного параметра, который будет считаться.</span><span class="sxs-lookup"><span data-stu-id="c621b-121">The ID of the system parameter that will be read.</span></span>

<span data-ttu-id="c621b-122">Полный список системных параметров и их свойств см. в разделе [Параметры системы](./extensible-storage-engine-system-parameters.md) .</span><span class="sxs-lookup"><span data-stu-id="c621b-122">See [System Parameters](./extensible-storage-engine-system-parameters.md) for a complete list of system parameters and their properties.</span></span>

<span data-ttu-id="c621b-123">*плпарам*</span><span class="sxs-lookup"><span data-stu-id="c621b-123">*plParam*</span></span>

<span data-ttu-id="c621b-124">Выходной буфер, который получает значение выбранного системного параметра, если этот системный параметр имеет целочисленный тип.</span><span class="sxs-lookup"><span data-stu-id="c621b-124">The output buffer that receives the value of the selected system parameter if that system parameter is of an integer type.</span></span>

<span data-ttu-id="c621b-125">*сзпарам*</span><span class="sxs-lookup"><span data-stu-id="c621b-125">*szParam*</span></span>

<span data-ttu-id="c621b-126">Выходной буфер, который получает значение выбранного системного параметра, если этот системный параметр имеет строковый тип.</span><span class="sxs-lookup"><span data-stu-id="c621b-126">The output buffer that receives the value of the selected system parameter if that system parameter is of a string type.</span></span>

<span data-ttu-id="c621b-127">*кбмакс*</span><span class="sxs-lookup"><span data-stu-id="c621b-127">*cbMax*</span></span>

<span data-ttu-id="c621b-128">Максимальный размер строкового выходного буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="c621b-128">The maximum size in bytes of the string output buffer.</span></span>

### <a name="return-value"></a><span data-ttu-id="c621b-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c621b-129">Return Value</span></span>

<span data-ttu-id="c621b-130">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="c621b-130">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="c621b-131">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="c621b-131">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c621b-132">Код возврата</span><span class="sxs-lookup"><span data-stu-id="c621b-132">Return code</span></span></p></th>
<th><p><span data-ttu-id="c621b-133">Описание</span><span class="sxs-lookup"><span data-stu-id="c621b-133">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c621b-134">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="c621b-134">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="c621b-135">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="c621b-135">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c621b-136">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="c621b-136">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="c621b-137">Невозможно выполнить операцию, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</span><span class="sxs-lookup"><span data-stu-id="c621b-137">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c621b-138">JET_errInitInProgress</span><span class="sxs-lookup"><span data-stu-id="c621b-138">JET_errInitInProgress</span></span></p></td>
<td><p><span data-ttu-id="c621b-139">Невозможно выполнить операцию, так как инициализируется экземпляр, связанный с сеансом.</span><span class="sxs-lookup"><span data-stu-id="c621b-139">It is not possible to complete the operation because the instance associated with the session is being initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c621b-140">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="c621b-140">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="c621b-141">Невозможно выполнить операцию, поскольку экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</span><span class="sxs-lookup"><span data-stu-id="c621b-141">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="c621b-142">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="c621b-142">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c621b-143">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="c621b-143">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="c621b-144">Один из указанных параметров содержит непредвиденное значение или содержит значение, которое не имеет смысла при объединении со значением другого параметра.</span><span class="sxs-lookup"><span data-stu-id="c621b-144">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span></p>
<p><span data-ttu-id="c621b-145">Это может произойти для <strong>жетжетсистемпараметер</strong> в следующих случаях:</span><span class="sxs-lookup"><span data-stu-id="c621b-145">This can happen for <strong>JetGetSystemParameter</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="c621b-146">Указанный идентификатор системного параметра является недопустимым или не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="c621b-146">The specified system parameter ID is invalid or unsupported.</span></span></p></li>
<li><p><span data-ttu-id="c621b-147">Для указанного системного параметра требуется предоставить целочисленный выходной буфер, а указатель выходного буфера имел <strong>значение NULL</strong>.</span><span class="sxs-lookup"><span data-stu-id="c621b-147">The specified system parameter requires the integer output buffer to be provided and that output buffer pointer was <strong>NULL</strong>.</span></span></p></li>
<li><p><span data-ttu-id="c621b-148">Для указанного системного параметра требуется предоставить строковый выходной буфер, а указатель выходного буфера имел <strong>значение NULL</strong>.</span><span class="sxs-lookup"><span data-stu-id="c621b-148">The specified system parameter requires a string output buffer to be provided and that output buffer pointer was <strong>NULL</strong>.</span></span></p>
<p><span data-ttu-id="c621b-149"><strong>Windows Vista:  </strong> Это может произойти только в Windows Vista и более поздних выпусках.</span><span class="sxs-lookup"><span data-stu-id="c621b-149"><strong>Windows Vista:  </strong>This can only happen on Windows Vista and later releases.</span></span></p></li>
<li><p><span data-ttu-id="c621b-150">Указанный системный параметр требует наличия строкового выходного буфера, и размер этого выходного буфера слишком мал для приема строки, завершающейся нулем.</span><span class="sxs-lookup"><span data-stu-id="c621b-150">The specified system parameter requires a string output buffer to be provided and the size of that output buffer is too small to accept a null terminated string.</span></span></p>
<p><span data-ttu-id="c621b-151"><strong>Windows Vista:  </strong> Это может произойти только в Windows Vista и более поздних выпусках.</span><span class="sxs-lookup"><span data-stu-id="c621b-151"><strong>Windows Vista:  </strong>This can only happen on Windows Vista and later releases.</span></span></p></li>
<li><p><span data-ttu-id="c621b-152">Не удается прочитать указанный системный параметр, так как он доступен только для записи.</span><span class="sxs-lookup"><span data-stu-id="c621b-152">The specified system parameter cannot be read because it is write-only.</span></span></p></li>
<li><p><span data-ttu-id="c621b-153">Указанный системный параметр является глобальным, и предпринята попытка чтения конкретного значения этого системного параметра.</span><span class="sxs-lookup"><span data-stu-id="c621b-153">The specified system parameter is global only and an attempt was made to read an instance specific value for that system parameter.</span></span> <span data-ttu-id="c621b-154">Это может происходить только в Windows XP и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="c621b-154">This can only happen on Windows XP and later releases.</span></span></p></li>
<li><p><span data-ttu-id="c621b-155">Указанный системный параметр доступен только для одного экземпляра, и предпринята попытка чтения глобального значения для этого системного параметра.</span><span class="sxs-lookup"><span data-stu-id="c621b-155">The specified system parameter is per-instance only and an attempt was made to read the global value for that system parameter.</span></span> <span data-ttu-id="c621b-156">Это может происходить только в Windows XP и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="c621b-156">This can only happen on Windows XP and later releases.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c621b-157">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="c621b-157">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="c621b-158">Невозможно выполнить операцию, так как экземпляр, связанный с сеансом, еще не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="c621b-158">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c621b-159">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="c621b-159">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="c621b-160">Невозможно выполнить операцию, так как в экземпляре, связанном с сеансом, выполняется операция восстановления.</span><span class="sxs-lookup"><span data-stu-id="c621b-160">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c621b-161">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="c621b-161">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="c621b-162">Невозможно выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</span><span class="sxs-lookup"><span data-stu-id="c621b-162">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c621b-163">JET_errInvalidSesid</span><span class="sxs-lookup"><span data-stu-id="c621b-163">JET_errInvalidSesid</span></span></p></td>
<td><p><span data-ttu-id="c621b-164">Недопустимый обработчик сеанса или ссылается на закрытый сеанс.</span><span class="sxs-lookup"><span data-stu-id="c621b-164">The session handle is invalid or refers to a closed session.</span></span> <span data-ttu-id="c621b-165">Эта ошибка не возвращается при всех обстоятельствах.</span><span class="sxs-lookup"><span data-stu-id="c621b-165">This error is not returned under all circumstances.</span></span> <span data-ttu-id="c621b-166">Дескрипторы проверяются только на основе наилучшей силы.</span><span class="sxs-lookup"><span data-stu-id="c621b-166">Handles are validated on a best effort basis only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c621b-167">JET_errInvalidInstance</span><span class="sxs-lookup"><span data-stu-id="c621b-167">JET_errInvalidInstance</span></span></p></td>
<td><p><span data-ttu-id="c621b-168">Недопустимый указатель экземпляра или ссылка на экземпляр, который был завершен.</span><span class="sxs-lookup"><span data-stu-id="c621b-168">The instance handle is invalid or refers to an instance that has been shutdown.</span></span> <span data-ttu-id="c621b-169">Эта ошибка не возвращается при всех обстоятельствах.</span><span class="sxs-lookup"><span data-stu-id="c621b-169">This error is not returned under all circumstances.</span></span> <span data-ttu-id="c621b-170">Дескрипторы проверяются только на основе наилучшей силы.</span><span class="sxs-lookup"><span data-stu-id="c621b-170">Handles are validated on a best effort basis only.</span></span></p>
<p><span data-ttu-id="c621b-171"><strong>Windows Vista:  </strong> Эта ошибка будет возвращаться только в Windows Vista и более поздних выпусках.</span><span class="sxs-lookup"><span data-stu-id="c621b-171"><strong>Windows Vista:  </strong>This error will only be returned by Windows Vista and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c621b-172">JET_wrnBufferTruncated</span><span class="sxs-lookup"><span data-stu-id="c621b-172">JET_wrnBufferTruncated</span></span></p></td>
<td><p><span data-ttu-id="c621b-173">Операция успешно завершена, но выходной буфер слишком мал, чтобы получить весь параметр системного параметра.</span><span class="sxs-lookup"><span data-stu-id="c621b-173">The operation completed successfully, but the output buffer was too small to receive the entire system parameter setting.</span></span></p>
<p><span data-ttu-id="c621b-174">Выходной буфер был заполнен как часть параметра системного параметра, которая будет соответствовать.</span><span class="sxs-lookup"><span data-stu-id="c621b-174">The output buffer has been filled with as much of the system parameter setting as would fit.</span></span> <span data-ttu-id="c621b-175">Если выходной буфер имеет длину по крайней мере один символ, то строка в этом выходном буфере будет завершаться нулем.</span><span class="sxs-lookup"><span data-stu-id="c621b-175">If the output buffer is at least one character in length then the string in that output buffer will be null terminated.</span></span></p>
<p><span data-ttu-id="c621b-176"><strong>Примечание  </strong> . Эта ошибка не возвращается во всех выпусках.</span><span class="sxs-lookup"><span data-stu-id="c621b-176"><strong>Note  </strong>This error is not returned by all releases.</span></span> <span data-ttu-id="c621b-177">Дополнительные сведения см. в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="c621b-177">Please see the Remarks section for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c621b-178">JET_errBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="c621b-178">JET_errBufferTooSmall</span></span></p></td>
<td><p><span data-ttu-id="c621b-179">Не удалось выполнить операцию, так как выходной буфер слишком мал для получения всего параметра системного параметра.</span><span class="sxs-lookup"><span data-stu-id="c621b-179">The operation failed because the output buffer was too small to receive the entire system parameter setting.</span></span></p>
<p><span data-ttu-id="c621b-180"><strong>Примечание  </strong> . Эта ошибка не возвращается в некоторых случаях для сохранения совместимости приложений.</span><span class="sxs-lookup"><span data-stu-id="c621b-180"><strong>Note  </strong>This error is not returned in some cases to preserve application compatibility.</span></span> <span data-ttu-id="c621b-181">Дополнительные сведения см. в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="c621b-181">Please see the Remarks section for more information.</span></span></p>
<p><span data-ttu-id="c621b-182"><strong>Windows Vista:  </strong> Эта ошибка будет возвращаться только в Windows Vista и более поздних выпусках.</span><span class="sxs-lookup"><span data-stu-id="c621b-182"><strong>Windows Vista:  </strong>This error will only be returned by Windows Vista and later releases.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c621b-183">В случае успеха выходной буфер, соответствующий запрошенному системному параметру, будет установлен в значение этого системного параметра.</span><span class="sxs-lookup"><span data-stu-id="c621b-183">On success, the output buffer appropriate for the requested system parameter will be set to the value of that system parameter.</span></span>

<span data-ttu-id="c621b-184">В случае сбоя состояние выходных буферов будет не определено.</span><span class="sxs-lookup"><span data-stu-id="c621b-184">On failure, the state of the output buffers will be undefined.</span></span>

#### <a name="remarks"></a><span data-ttu-id="c621b-185">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c621b-185">Remarks</span></span>

<span data-ttu-id="c621b-186">В этом API есть важная проблема, которая присутствует во всех выпусках.</span><span class="sxs-lookup"><span data-stu-id="c621b-186">There is an important problem in this API that is present in all releases.</span></span> <span data-ttu-id="c621b-187">Если системный параметр с строковым значением запрашивается и выходной буфер слишком мал для получения всего параметра системного параметра, JET_wrnBufferTruncated не будет возвращен.</span><span class="sxs-lookup"><span data-stu-id="c621b-187">If a system parameter with a string value is requested and the output buffer is too small to receive the entire system parameter setting, JET_wrnBufferTruncated will NOT be returned.</span></span> <span data-ttu-id="c621b-188">Вместо этого возвращается JET_errSuccess.</span><span class="sxs-lookup"><span data-stu-id="c621b-188">JET_errSuccess is returned instead.</span></span> <span data-ttu-id="c621b-189">Если длина возвращаемой строки равна размеру выходного буфера, меньшего терминатора **null** , вызывающий объект должен реагировать так, как будто были возвращены JET_wrnBufferTruncated.</span><span class="sxs-lookup"><span data-stu-id="c621b-189">If the length of the returned string is equal to the size of the output buffer less the **NULL** terminator, the caller should react as if JET_wrnBufferTruncated were returned.</span></span> <span data-ttu-id="c621b-190">Если указан строковый выходной буфер нулевого размера, вызывающий объект должен реагировать так, как будто были возвращены JET_errInvalidParameter.</span><span class="sxs-lookup"><span data-stu-id="c621b-190">If a zero-sized string output buffer is specified, the caller should react as if JET_errInvalidParameter were returned.</span></span>

#### <a name="requirements"></a><span data-ttu-id="c621b-191">Требования</span><span class="sxs-lookup"><span data-stu-id="c621b-191">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c621b-192"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="c621b-192"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="c621b-193">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="c621b-193">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c621b-194"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="c621b-194"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="c621b-195">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="c621b-195">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c621b-196"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="c621b-196"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="c621b-197">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="c621b-197">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c621b-198"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="c621b-198"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="c621b-199">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="c621b-199">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c621b-200"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="c621b-200"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="c621b-201">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="c621b-201">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c621b-202"><strong>Юникод</strong></span><span class="sxs-lookup"><span data-stu-id="c621b-202"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="c621b-203">Реализуется как <strong>жетжетсистемпараметерв</strong> (Юникод) и <strong>жетжетсистемпараметера</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="c621b-203">Implemented as <strong>JetGetSystemParameterW</strong> (Unicode) and <strong>JetGetSystemParameterA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="c621b-204">См. также:</span><span class="sxs-lookup"><span data-stu-id="c621b-204">See Also</span></span>

[<span data-ttu-id="c621b-205">JET_API_PTR</span><span class="sxs-lookup"><span data-stu-id="c621b-205">JET_API_PTR</span></span>](./jet-api-ptr.md)  
[<span data-ttu-id="c621b-206">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="c621b-206">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="c621b-207">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="c621b-207">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="c621b-208">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="c621b-208">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="c621b-209">жеткреатеинстанце</span><span class="sxs-lookup"><span data-stu-id="c621b-209">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="c621b-210">жетинит</span><span class="sxs-lookup"><span data-stu-id="c621b-210">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="c621b-211">жетсетсистемпараметер</span><span class="sxs-lookup"><span data-stu-id="c621b-211">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="c621b-212">жетстопсервице</span><span class="sxs-lookup"><span data-stu-id="c621b-212">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="c621b-213">Системные параметры</span><span class="sxs-lookup"><span data-stu-id="c621b-213">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
