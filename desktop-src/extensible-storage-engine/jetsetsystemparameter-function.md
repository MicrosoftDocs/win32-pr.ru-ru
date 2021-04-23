---
description: Дополнительные сведения о функции Жетсетсистемпараметер
title: Функция Жетсетсистемпараметер
TOCTitle: JetSetSystemParameter Function
ms:assetid: a244b5c9-6f6e-49d1-a6f7-9248feb9b92d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294044(v=EXCHG.10)
ms:contentKeyID: 32765643
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetSystemParameterA
- JetSetSystemParameterW
- JetSetSystemParameter
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bbb57a1b50f3ad39525b894932f7111b56c3a076
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263233"
---
# <a name="jetsetsystemparameter-function"></a><span data-ttu-id="7a2bc-103">Функция Жетсетсистемпараметер</span><span class="sxs-lookup"><span data-stu-id="7a2bc-103">JetSetSystemParameter Function</span></span>


<span data-ttu-id="7a2bc-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="7a2bc-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetsetsystemparameter-function"></a><span data-ttu-id="7a2bc-105">Функция Жетсетсистемпараметер</span><span class="sxs-lookup"><span data-stu-id="7a2bc-105">JetSetSystemParameter Function</span></span>

<span data-ttu-id="7a2bc-106">Функция **жетсетсистемпараметер** используется для установки множества параметров конфигурации ядра СУБД.</span><span class="sxs-lookup"><span data-stu-id="7a2bc-106">The **JetSetSystemParameter** function is used to set the numerous configuration settings of the database engine.</span></span>

```cpp
    JET_ERR JET_API JetSetSystemParameter(
      __in_out_opt  JET_INSTANCE* pinstance,
      __in          JET_SESID sesid,
      __in          unsigned long paramid,
      __in          JET_API_PTR lParam,
      __in_opt      JET_PCSTR szParam
    );
```

### <a name="parameters"></a><span data-ttu-id="7a2bc-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="7a2bc-107">Parameters</span></span>

<span data-ttu-id="7a2bc-108">*пинстанце*</span><span class="sxs-lookup"><span data-stu-id="7a2bc-108">*pinstance*</span></span>

<span data-ttu-id="7a2bc-109">Указывает экземпляр, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="7a2bc-109">Specifies the instance to use for this call.</span></span>

<span data-ttu-id="7a2bc-110">**Windows 2000:**  Для Windows 2000 этот параметр игнорируется и всегда должен иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="7a2bc-110">**Windows 2000:**  For Windows 2000, this parameter is ignored and should always be **NULL**.</span></span>

<span data-ttu-id="7a2bc-111">**Windows XP:**  Для Windows XP и более поздних версий этот параметр несколько перегружен.</span><span class="sxs-lookup"><span data-stu-id="7a2bc-111">**Windows XP:**  For Windows XP and later releases, this parameter is somewhat overloaded.</span></span> <span data-ttu-id="7a2bc-112">Если ядро работает в устаревшем режиме (режим совместимости Windows 2000), где поддерживается только один экземпляр, этот параметр может иметь **значение NULL** или содержать фактический экземпляр, возвращаемый функцией [жетинит](./jetinit-function.md).</span><span class="sxs-lookup"><span data-stu-id="7a2bc-112">If the engine is operating in legacy mode (Windows 2000 compatibility mode) where only one instance is supported, then this parameter may be **NULL** or may contain the actual instance returned by [JetInit](./jetinit-function.md).</span></span> <span data-ttu-id="7a2bc-113">В любом случае все параметры системного параметра считываются из одного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="7a2bc-113">In either case, all system parameter settings are read from that one instance.</span></span> <span data-ttu-id="7a2bc-114">Если ядро работает в режиме с несколькими экземплярами, этот параметр может иметь **значение NULL** или указатель на экземпляр, созданный с помощью [жетинит](./jetinit-function.md) или [жеткреатеиндекс](./jetcreateindex-function.md).</span><span class="sxs-lookup"><span data-stu-id="7a2bc-114">If the engine is operating in multi-instance mode, then this parameter may be **NULL** or a pointer to an instance created using [JetInit](./jetinit-function.md) or [JetCreateIndex](./jetcreateindex-function.md).</span></span> <span data-ttu-id="7a2bc-115">Если этот параметр имеет **значение NULL** , то считывается параметр глобального системного параметра (или значение по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="7a2bc-115">When this parameter is **NULL** then the global system parameter setting (or default) is read.</span></span> <span data-ttu-id="7a2bc-116">Если этот параметр является экземпляром, то параметр системного параметра для этого экземпляра считывается.</span><span class="sxs-lookup"><span data-stu-id="7a2bc-116">When this parameter is an instance then the system parameter setting for that instance is read.</span></span>

<span data-ttu-id="7a2bc-117">Несмотря на то, что это технически параметр out, этот API никогда не изменяет содержимое предоставленного буфера.</span><span class="sxs-lookup"><span data-stu-id="7a2bc-117">Even though this is technically an out parameter, this API never modifies the contents of the provided buffer.</span></span>

<span data-ttu-id="7a2bc-118">*сесид*</span><span class="sxs-lookup"><span data-stu-id="7a2bc-118">*sesid*</span></span>

<span data-ttu-id="7a2bc-119">Указывает сеанс, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="7a2bc-119">Specifies the session to use for this call.</span></span>

<span data-ttu-id="7a2bc-120">Если этот параметр указан, то указанный экземпляр игнорируется, и будет использоваться экземпляр, связанный с сеансом.</span><span class="sxs-lookup"><span data-stu-id="7a2bc-120">When specified, the specified instance is ignored and the instance associated with the session will be used.</span></span>

<span data-ttu-id="7a2bc-121">*paramid*</span><span class="sxs-lookup"><span data-stu-id="7a2bc-121">*paramid*</span></span>

<span data-ttu-id="7a2bc-122">Идентификатор системного параметра, который будет установлен.</span><span class="sxs-lookup"><span data-stu-id="7a2bc-122">The ID of the system parameter that will be set.</span></span> <span data-ttu-id="7a2bc-123">Полный список системных параметров и их свойств см. в разделе [Параметры системы](./extensible-storage-engine-system-parameters.md) .</span><span class="sxs-lookup"><span data-stu-id="7a2bc-123">See [System Parameters](./extensible-storage-engine-system-parameters.md) for a complete list of system parameters and their properties.</span></span>

<span data-ttu-id="7a2bc-124">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7a2bc-124">*lParam*</span></span>

<span data-ttu-id="7a2bc-125">Предоставляет значение, которое должно быть задано для выбранного системного параметра, если этот системный параметр имеет целочисленный тип.</span><span class="sxs-lookup"><span data-stu-id="7a2bc-125">Provides the value to be set for the selected system parameter if that system parameter is of an integer type.</span></span>

<span data-ttu-id="7a2bc-126">*сзпарам*</span><span class="sxs-lookup"><span data-stu-id="7a2bc-126">*szParam*</span></span>

<span data-ttu-id="7a2bc-127">Предоставляет значение для выбранного системного параметра, если этот системный параметр имеет строковый тип.</span><span class="sxs-lookup"><span data-stu-id="7a2bc-127">Provides the value for the selected system parameter if that system parameter is of a string type.</span></span>

### <a name="return-value"></a><span data-ttu-id="7a2bc-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7a2bc-128">Return Value</span></span>

<span data-ttu-id="7a2bc-129">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="7a2bc-129">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="7a2bc-130">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="7a2bc-130">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7a2bc-131">Код возврата</span><span class="sxs-lookup"><span data-stu-id="7a2bc-131">Return code</span></span></p></th>
<th><p><span data-ttu-id="7a2bc-132">Описание</span><span class="sxs-lookup"><span data-stu-id="7a2bc-132">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7a2bc-133">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="7a2bc-133">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="7a2bc-134">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="7a2bc-134">The operation completed successfully.</span></span></p>
<p><span data-ttu-id="7a2bc-135"><strong>Windows Vista:</strong>  В Windows Vista и более поздних выпусках успешное выполнение может быть возвращено без изменения значения системного параметра.</span><span class="sxs-lookup"><span data-stu-id="7a2bc-135"><strong>Windows Vista:</strong>  On Windows Vista and later releases, success can be returned without a change to the system parameter's value.</span></span> <span data-ttu-id="7a2bc-136">Дополнительные сведения см. в описании параметра JET_paramEnableAdvanced System в разделе " <a href="gg269346(v=exchg.10).md">Параметры meta</a> ".</span><span class="sxs-lookup"><span data-stu-id="7a2bc-136">See the JET_paramEnableAdvanced system parameter in the <a href="gg269346(v=exchg.10).md">Meta Parameters</a> topic for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a2bc-137">JET_errAlreadyInitialized</span><span class="sxs-lookup"><span data-stu-id="7a2bc-137">JET_errAlreadyInitialized</span></span></p></td>
<td><p><span data-ttu-id="7a2bc-138">Экземпляр был инициализирован с помощью вызова <a href="gg294068(v=exchg.10).md">жетинит</a> , и эта операция не может быть выполнена в результате.</span><span class="sxs-lookup"><span data-stu-id="7a2bc-138">The instance has been initialized using a call to <a href="gg294068(v=exchg.10).md">JetInit</a> and this operation cannot be performed as a result.</span></span> <span data-ttu-id="7a2bc-139">Это может произойти для <strong>жетсетсистемпараметер</strong> при попытке настроить системный параметр после того, как изменение его значения не повлияет на состояние ядра СУБД.</span><span class="sxs-lookup"><span data-stu-id="7a2bc-139">This can happen for <strong>JetSetSystemParameter</strong> when an attempt is made to configure a system parameter after a change in its value cannot affect the state of the database engine.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a2bc-140">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="7a2bc-140">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="7a2bc-141">Невозможно выполнить операцию, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</span><span class="sxs-lookup"><span data-stu-id="7a2bc-141">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a2bc-142">JET_errIndexTuplesInvalidLimits</span><span class="sxs-lookup"><span data-stu-id="7a2bc-142">JET_errIndexTuplesInvalidLimits</span></span></p></td>
<td><p><span data-ttu-id="7a2bc-143">Указаны недопустимые параметры индекса кортежа.</span><span class="sxs-lookup"><span data-stu-id="7a2bc-143">The specified tuple index parameters were illegal.</span></span> <span data-ttu-id="7a2bc-144">Эта ошибка может возвращаться <strong>жетсетсистемпараметер</strong> только при задании недопустимых значений <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMin</a>, <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMax</a>или <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesToIndexMax</a> .</span><span class="sxs-lookup"><span data-stu-id="7a2bc-144">This error may be returned by <strong>JetSetSystemParameter</strong> only when setting <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMin</a>, <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMax</a>, or <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesToIndexMax</a> to an illegal value.</span></span></p>
<p><span data-ttu-id="7a2bc-145"><strong>Windows XP и Windows Server 2003:</strong>  Это может произойти только в Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="7a2bc-145"><strong>Windows XP and Windows Server 2003:</strong>  This can only happen on Windows XP and Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a2bc-146">JET_errInitInProgress</span><span class="sxs-lookup"><span data-stu-id="7a2bc-146">JET_errInitInProgress</span></span></p></td>
<td><p><span data-ttu-id="7a2bc-147">Невозможно выполнить операцию, так как инициализируется экземпляр, связанный с сеансом.</span><span class="sxs-lookup"><span data-stu-id="7a2bc-147">It is not possible to complete the operation because the instance associated with the session is being initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a2bc-148">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="7a2bc-148">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="7a2bc-149">Невозможно выполнить операцию, поскольку экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</span><span class="sxs-lookup"><span data-stu-id="7a2bc-149">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="7a2bc-150"><strong>Windows XP:</strong>  Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="7a2bc-150"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a2bc-151">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="7a2bc-151">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="7a2bc-152">Один из указанных параметров содержит непредвиденное значение или содержит значение, которое не имеет смысла при объединении со значением другого параметра.</span><span class="sxs-lookup"><span data-stu-id="7a2bc-152">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="7a2bc-153">Это может произойти для <strong>жетсетсистемпараметер</strong> в следующих случаях:</span><span class="sxs-lookup"><span data-stu-id="7a2bc-153">This can happen for <strong>JetSetSystemParameter</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="7a2bc-154">Указанный идентификатор системного параметра является недопустимым или не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="7a2bc-154">The specified system parameter ID is invalid or unsupported.</span></span></p></li>
<li><p><span data-ttu-id="7a2bc-155">Предпринята попытка установить системный параметр с строковыми значениями, длина которого находилась вне допустимого диапазона для параметра.</span><span class="sxs-lookup"><span data-stu-id="7a2bc-155">An attempt was made to set a string-valued system parameter with a string whose length was outside the legal range for the parameter.</span></span></p></li>
<li><p><span data-ttu-id="7a2bc-156">Предпринята попытка установить системный параметр с символьным значением, где длина его абсолютного пути находилась вне допустимого диапазона для этого параметра.</span><span class="sxs-lookup"><span data-stu-id="7a2bc-156">An attempt was made to set a string-valued system parameter with a file path where the length of its absolute path representation was outside the legal range for that parameter.</span></span></p>
<p><span data-ttu-id="7a2bc-157"><strong>Windows Vista:</strong>  Это может произойти только в Windows Vista и более поздних выпусках.</span><span class="sxs-lookup"><span data-stu-id="7a2bc-157"><strong>Windows Vista:</strong>  This can only happen on Windows Vista and later releases.</span></span></p></li>
<li><p><span data-ttu-id="7a2bc-158">Предпринята попытка установить системный параметр с целочисленными значениями, который находится за пределами допустимого диапазона для параметра.</span><span class="sxs-lookup"><span data-stu-id="7a2bc-158">An attempt was made to set an integer-valued system parameter with an integer that was outside the legal range for the parameter.</span></span></p></li>
<li><p><span data-ttu-id="7a2bc-159">Предпринята попытка задать JET_paramUnicodeIndexDefault с <strong>нулевым</strong> указателем <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> , недопустимым LCID или неподдерживаемым набором флагов LCMapString завершилось ошибкой.</span><span class="sxs-lookup"><span data-stu-id="7a2bc-159">An attempt was made to set JET_paramUnicodeIndexDefault with a <strong>NULL</strong> <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> pointer, an invalid LCID, or an unsupported set of LCMapString flags.</span></span></p>
<p><span data-ttu-id="7a2bc-160"><strong>Windows Vista:</strong>  Это может произойти только в Windows Vista и более поздних выпусках.</span><span class="sxs-lookup"><span data-stu-id="7a2bc-160"><strong>Windows Vista:</strong>  This can only happen on Windows Vista and later releases.</span></span></p></li>
<li><p><span data-ttu-id="7a2bc-161">Невозможно задать указанный системный параметр, так как он доступен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="7a2bc-161">The specified system parameter cannot be set because it is read-only.</span></span></p></li>
<li><p><span data-ttu-id="7a2bc-162">Предпринята попытка установить системный параметр после вызова <a href="gg294068(v=exchg.10).md">жетинит</a> , ядро СУБД находится в режиме с одним экземпляром, а сеанс не был указан.</span><span class="sxs-lookup"><span data-stu-id="7a2bc-162">An attempt was made to set a system parameter after <a href="gg294068(v=exchg.10).md">JetInit</a> was called, the database engine is in single-instance mode, and a session was not specified.</span></span></p>
<p><span data-ttu-id="7a2bc-163"><strong>Windows XP и Windows Server 2003:</strong>  Это может произойти только в Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="7a2bc-163"><strong>Windows XP and Windows Server 2003:</strong>  This can only happen on Windows XP and Windows Server 2003.</span></span></p></li>
<li><p><span data-ttu-id="7a2bc-164">Указанный системный параметр является глобальным, и предпринята попытка установить для этого системного параметра значение конкретного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="7a2bc-164">The specified system parameter is global only and an attempt was made to set an instance specific value for that system parameter.</span></span></p>
<p><span data-ttu-id="7a2bc-165"><strong>Windows XP и Windows Server 2003:</strong>  Это может произойти только в Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="7a2bc-165"><strong>Windows XP and Windows Server 2003:</strong>  This can only happen on Windows XP and Windows Server 2003.</span></span></p></li>
<li><p><span data-ttu-id="7a2bc-166">Указанный системный параметр доступен только для одного экземпляра, и предпринята попытка установить глобальное значение для этого системного параметра.</span><span class="sxs-lookup"><span data-stu-id="7a2bc-166">The specified system parameter is per-instance only and an attempt was made to set the global value for that system parameter.</span></span></p>
<p><span data-ttu-id="7a2bc-167"><strong>Windows XP и Windows Server 2003:</strong>  Это может произойти только в Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="7a2bc-167"><strong>Windows XP and Windows Server 2003:</strong>  This can only happen on Windows XP and Windows Server 2003.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a2bc-168">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="7a2bc-168">JET_errInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="7a2bc-169">Указан недопустимый путь к файловой системе.</span><span class="sxs-lookup"><span data-stu-id="7a2bc-169">The specified file system path was invalid.</span></span> <span data-ttu-id="7a2bc-170">Эта ошибка может возвращаться <strong>жетсетсистемпараметер</strong> только при задании системных параметров, представляющих пути файловой системы.</span><span class="sxs-lookup"><span data-stu-id="7a2bc-170">This error may be returned by <strong>JetSetSystemParameter</strong> only when setting system parameters that represent file system paths.</span></span> <span data-ttu-id="7a2bc-171">Например, <a href="gg269235(v=exchg.10).md">JET_paramSystemPath</a> может вернуть эту ошибку.</span><span class="sxs-lookup"><span data-stu-id="7a2bc-171">For example, <a href="gg269235(v=exchg.10).md">JET_paramSystemPath</a> may return this error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a2bc-172">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="7a2bc-172">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="7a2bc-173">Невозможно выполнить операцию, так как экземпляр, связанный с сеансом, еще не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="7a2bc-173">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a2bc-174">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="7a2bc-174">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="7a2bc-175">Невозможно выполнить операцию, так как в экземпляре, связанном с сеансом, выполняется операция восстановления.</span><span class="sxs-lookup"><span data-stu-id="7a2bc-175">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a2bc-176">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="7a2bc-176">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="7a2bc-177">Невозможно выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</span><span class="sxs-lookup"><span data-stu-id="7a2bc-177">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a2bc-178">JET_errInvalidSesid</span><span class="sxs-lookup"><span data-stu-id="7a2bc-178">JET_errInvalidSesid</span></span></p></td>
<td><p><span data-ttu-id="7a2bc-179">Недопустимый обработчик сеанса или ссылается на закрытый сеанс.</span><span class="sxs-lookup"><span data-stu-id="7a2bc-179">The session handle is invalid or refers to a closed session.</span></span></p>
<p><span data-ttu-id="7a2bc-180">Эта ошибка не возвращается при всех обстоятельствах.</span><span class="sxs-lookup"><span data-stu-id="7a2bc-180">This error is not returned under all circumstances.</span></span> <span data-ttu-id="7a2bc-181">Дескрипторы проверяются только на основе наилучшей силы.</span><span class="sxs-lookup"><span data-stu-id="7a2bc-181">Handles are validated on a best effort basis only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a2bc-182">JET_errInvalidInstance</span><span class="sxs-lookup"><span data-stu-id="7a2bc-182">JET_errInvalidInstance</span></span></p></td>
<td><p><span data-ttu-id="7a2bc-183">Недопустимый указатель экземпляра или ссылка на экземпляр, который был завершен.</span><span class="sxs-lookup"><span data-stu-id="7a2bc-183">The instance handle is invalid or refers to an instance that has been shutdown.</span></span></p>
<p><span data-ttu-id="7a2bc-184">Эта ошибка не возвращается при всех обстоятельствах.</span><span class="sxs-lookup"><span data-stu-id="7a2bc-184">This error is not returned under all circumstances.</span></span> <span data-ttu-id="7a2bc-185">Дескрипторы проверяются только на основе наилучшей силы.</span><span class="sxs-lookup"><span data-stu-id="7a2bc-185">Handles are validated on a best effort basis only.</span></span></p>
<p><span data-ttu-id="7a2bc-186"><strong>Windows Vista:</strong>  Эта ошибка будет возвращаться только в Windows Vista и более поздних выпусках.</span><span class="sxs-lookup"><span data-stu-id="7a2bc-186"><strong>Windows Vista:</strong>  This error will only be returned by Windows Vista and later releases.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7a2bc-187">При успешном выполнении параметру System будет присвоено указанное значение.</span><span class="sxs-lookup"><span data-stu-id="7a2bc-187">On success, the setting for the system parameter will be set to the provided value.</span></span>

<span data-ttu-id="7a2bc-188">При сбое параметр системного параметра останется неизменным.</span><span class="sxs-lookup"><span data-stu-id="7a2bc-188">On failure, the setting for the system parameter will remain unchanged.</span></span>

#### <a name="remarks"></a><span data-ttu-id="7a2bc-189">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7a2bc-189">Remarks</span></span>

<span data-ttu-id="7a2bc-190">**Жетсетсистемпараметер** выполняет неплохое задание проверки выбранного параметра для каждого системного параметра.</span><span class="sxs-lookup"><span data-stu-id="7a2bc-190">**JetSetSystemParameter** does a poor job of validating the chosen setting for each system parameter.</span></span> <span data-ttu-id="7a2bc-191">Необходимо соблюдать осторожность, чтобы не полагаться на эту проверку для применения правильных параметров.</span><span class="sxs-lookup"><span data-stu-id="7a2bc-191">Care must be taken to not rely on this validation to enforce good settings.</span></span> <span data-ttu-id="7a2bc-192">Обратите особое внимание на описание каждого системного параметра и следуйте этим рекомендациям для хорошего параметра системного параметра.</span><span class="sxs-lookup"><span data-stu-id="7a2bc-192">Please pay close attention to the description of each system parameter and follow those guidelines for a good system parameter setting.</span></span>

<span data-ttu-id="7a2bc-193">Существует набор системных параметров, которые всегда должны быть установлены, чтобы гарантировать, что ядро СУБД работает правильно.</span><span class="sxs-lookup"><span data-stu-id="7a2bc-193">There are a set of system parameters that should always be set to guarantee that the database engine works as intended.</span></span> <span data-ttu-id="7a2bc-194">В частности, всегда следует устанавливать любые системные параметры, влияющие на физическую структуру файлов, используемых ядром СУБД.</span><span class="sxs-lookup"><span data-stu-id="7a2bc-194">Specifically, any system parameters that affect the physical layout of the files used by the database engine should always be set.</span></span> <span data-ttu-id="7a2bc-195">Дополнительные сведения см. в разделе [системные параметры](./extensible-storage-engine-system-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="7a2bc-195">For more information, see [System Parameters](./extensible-storage-engine-system-parameters.md).</span></span>

<span data-ttu-id="7a2bc-196">Каждый системный параметр имеет значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7a2bc-196">Every system parameter has a default value.</span></span> <span data-ttu-id="7a2bc-197">Эти значения по умолчанию были изменены со временем и являются довольно произвольными.</span><span class="sxs-lookup"><span data-stu-id="7a2bc-197">These default values have evolved over time and are quite arbitrary.</span></span> <span data-ttu-id="7a2bc-198">Настоятельно рекомендуется, чтобы приложение вычисляют все значения по умолчанию, чтобы убедиться, что они подходят.</span><span class="sxs-lookup"><span data-stu-id="7a2bc-198">It is highly recommended that an application evaluate all the default values to ensure that they are appropriate.</span></span> <span data-ttu-id="7a2bc-199">Если они не подходят, они должны быть настроены приложением.</span><span class="sxs-lookup"><span data-stu-id="7a2bc-199">If they are not appropriate, then they should be configured by the application.</span></span> <span data-ttu-id="7a2bc-200">Это важно, так как многие из этих параметров могут значительно повлиять на надежность, производительность и использование ресурсов ядром СУБД.</span><span class="sxs-lookup"><span data-stu-id="7a2bc-200">This is important as many of these parameters can greatly impact the reliability, performance, and resource utilization of the database engine.</span></span>

#### <a name="requirements"></a><span data-ttu-id="7a2bc-201">Требования</span><span class="sxs-lookup"><span data-stu-id="7a2bc-201">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7a2bc-202"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="7a2bc-202"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="7a2bc-203">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="7a2bc-203">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a2bc-204"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="7a2bc-204"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="7a2bc-205">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="7a2bc-205">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a2bc-206"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="7a2bc-206"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="7a2bc-207">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="7a2bc-207">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a2bc-208"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="7a2bc-208"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="7a2bc-209">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="7a2bc-209">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a2bc-210"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="7a2bc-210"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="7a2bc-211">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="7a2bc-211">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a2bc-212"><strong>Юникод</strong></span><span class="sxs-lookup"><span data-stu-id="7a2bc-212"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="7a2bc-213">Реализуется как <strong>жетсетсистемпараметерв</strong> (Юникод) и <strong>жетсетсистемпараметера</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="7a2bc-213">Implemented as <strong>JetSetSystemParameterW</strong> (Unicode) and <strong>JetSetSystemParameterA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="7a2bc-214">См. также:</span><span class="sxs-lookup"><span data-stu-id="7a2bc-214">See Also</span></span>

[<span data-ttu-id="7a2bc-215">JET_API_PTR</span><span class="sxs-lookup"><span data-stu-id="7a2bc-215">JET_API_PTR</span></span>](./jet-api-ptr.md)  
[<span data-ttu-id="7a2bc-216">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="7a2bc-216">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="7a2bc-217">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="7a2bc-217">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="7a2bc-218">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="7a2bc-218">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="7a2bc-219">жеткреатеинстанце</span><span class="sxs-lookup"><span data-stu-id="7a2bc-219">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="7a2bc-220">жетжетсистемпараметер</span><span class="sxs-lookup"><span data-stu-id="7a2bc-220">JetGetSystemParameter</span></span>](./jetgetsystemparameter-function.md)  
[<span data-ttu-id="7a2bc-221">жетинит</span><span class="sxs-lookup"><span data-stu-id="7a2bc-221">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="7a2bc-222">Системные параметры</span><span class="sxs-lookup"><span data-stu-id="7a2bc-222">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
