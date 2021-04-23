---
description: Дополнительные сведения о функции JetCreateInstance2
title: Функция JetCreateInstance2
TOCTitle: JetCreateInstance2 Function
ms:assetid: 1f894b19-fa15-4d89-a3d1-ee13b346f545
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269202(v=EXCHG.10)
ms:contentKeyID: 32765505
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateInstance2
- JetCreateInstance2W
- JetCreateInstance2A
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: af31e7e66d92cf7ebbc238ac54a9b331e6dc5362
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105719615"
---
# <a name="jetcreateinstance2-function"></a><span data-ttu-id="825af-103">Функция JetCreateInstance2</span><span class="sxs-lookup"><span data-stu-id="825af-103">JetCreateInstance2 Function</span></span>


<span data-ttu-id="825af-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="825af-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetcreateinstance2-function"></a><span data-ttu-id="825af-105">Функция JetCreateInstance2</span><span class="sxs-lookup"><span data-stu-id="825af-105">JetCreateInstance2 Function</span></span>

<span data-ttu-id="825af-106">Функция **JetCreateInstance2** используется для выделения нового экземпляра ядра СУБД для использования в одном процессе с указанным отображаемым именем.</span><span class="sxs-lookup"><span data-stu-id="825af-106">The **JetCreateInstance2** function is used to allocate a new instance of the database engine for use in a single process, with a display name specified.</span></span>

<span data-ttu-id="825af-107">**Windows XP:**  **JetCreateInstance2** появился в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="825af-107">**Windows XP:**  **JetCreateInstance2** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetCreateInstance2(
      __out         JET_INSTANCE* pinstance,
      __in_opt      const tchar* szInstanceName,
      __in_opt      const tchar* szDisplayName,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="825af-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="825af-108">Parameters</span></span>

<span data-ttu-id="825af-109">*пинстанце*</span><span class="sxs-lookup"><span data-stu-id="825af-109">*pinstance*</span></span>

<span data-ttu-id="825af-110">Выходной буфер, который будет принимать только что созданный экземпляр.</span><span class="sxs-lookup"><span data-stu-id="825af-110">The output buffer that will receive the newly created instance.</span></span>

<span data-ttu-id="825af-111">*сзинстанценаме*</span><span class="sxs-lookup"><span data-stu-id="825af-111">*szInstanceName*</span></span>

<span data-ttu-id="825af-112">Задает уникальный идентификатор строки для создаваемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="825af-112">Specifies a unique string identifier for the instance to be created.</span></span> <span data-ttu-id="825af-113">Эта строка должна быть уникальной в пределах данного процесса, в котором размещается ядро СУБД.</span><span class="sxs-lookup"><span data-stu-id="825af-113">This string must be unique within a given process hosting the database engine.</span></span>

<span data-ttu-id="825af-114">**Примечание** . Значение NULL обрабатывается как допустимый строковый идентификатор для экземпляра.</span><span class="sxs-lookup"><span data-stu-id="825af-114">**Note** A NULL value is treated as a valid string identifier for an instance.</span></span> <span data-ttu-id="825af-115">Только один экземпляр может иметь строковый идентификатор NULL.</span><span class="sxs-lookup"><span data-stu-id="825af-115">Only one instance may have a NULL string identifier.</span></span>

<span data-ttu-id="825af-116">*сздисплайнаме*</span><span class="sxs-lookup"><span data-stu-id="825af-116">*szDisplayName*</span></span>

<span data-ttu-id="825af-117">Отображаемое имя создаваемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="825af-117">A display name for the instance to be created.</span></span> <span data-ttu-id="825af-118">Если этот параметр отсутствует, предполагается, что его значение равно NULL.</span><span class="sxs-lookup"><span data-stu-id="825af-118">When this parameter is not present, its value is presumed to be NULL.</span></span>

<span data-ttu-id="825af-119">*грбит*</span><span class="sxs-lookup"><span data-stu-id="825af-119">*grbit*</span></span>

<span data-ttu-id="825af-120">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="825af-120">Reserved for future use.</span></span> <span data-ttu-id="825af-121">Если этот параметр отсутствует, предполагается, что его значение равно нулю.</span><span class="sxs-lookup"><span data-stu-id="825af-121">When this parameter is not present, its value is presumed to be zero.</span></span>

### <a name="return-value"></a><span data-ttu-id="825af-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="825af-122">Return Value</span></span>

<span data-ttu-id="825af-123">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="825af-123">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="825af-124">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="825af-124">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="825af-125">Код возврата</span><span class="sxs-lookup"><span data-stu-id="825af-125">Return code</span></span></p></th>
<th><p><span data-ttu-id="825af-126">Описание</span><span class="sxs-lookup"><span data-stu-id="825af-126">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="825af-127">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="825af-127">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="825af-128">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="825af-128">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="825af-129">JET_errInstanceNameInUse</span><span class="sxs-lookup"><span data-stu-id="825af-129">JET_errInstanceNameInUse</span></span></p></td>
<td><p><span data-ttu-id="825af-130">Указанное имя экземпляра уже используется для этого процесса.</span><span class="sxs-lookup"><span data-stu-id="825af-130">The specified instance name is already in use for this process.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="825af-131">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="825af-131">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="825af-132">Один из указанных параметров содержит непредвиденное значение или содержит значение, которое не имеет смысла при объединении со значением другого параметра.</span><span class="sxs-lookup"><span data-stu-id="825af-132">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="825af-133">Это может произойти для <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a> , когда <em>пинстанце</em> имеет значение null.</span><span class="sxs-lookup"><span data-stu-id="825af-133">This can happen for <a href="gg269354(v=exchg.10).md">JetCreateInstance</a> when <em>pinstance</em> is NULL.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="825af-134">JET_errRunningInOneInstanceMode</span><span class="sxs-lookup"><span data-stu-id="825af-134">JET_errRunningInOneInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="825af-135">Операция завершилась ошибкой, так как ее нельзя использовать, если ядро СУБД работает в режиме одиночного экземпляра (режим совместимости с Windows 2000).</span><span class="sxs-lookup"><span data-stu-id="825af-135">The operation failed because it cannot be used when the database engine is operating in single instance mode (Windows 2000 compatibility mode).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="825af-136">JET_errTooManyInstances</span><span class="sxs-lookup"><span data-stu-id="825af-136">JET_errTooManyInstances</span></span></p></td>
<td><p><span data-ttu-id="825af-137">Не удалось создать новый экземпляр, так как достигнуто максимальное число экземпляров.</span><span class="sxs-lookup"><span data-stu-id="825af-137">A new instance could not be created because the maximum number of instances has been reached.</span></span> <span data-ttu-id="825af-138">Максимальное число поддерживаемых экземпляров настраивается с помощью <a href="gg294044(v=exchg.10).md">жетсетсистемпараметер</a> с помощью <em>JET_paramMaxInstances</em>.</span><span class="sxs-lookup"><span data-stu-id="825af-138">The maximum number of supported instances is configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> using <em>JET_paramMaxInstances</em>.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="825af-139">При успешном выполнении будет выделена новая копия, и будет возвращен идентификатор для него.</span><span class="sxs-lookup"><span data-stu-id="825af-139">On success, a new instance will be allocated and the identifier for it will be returned.</span></span> <span data-ttu-id="825af-140">На этом этапе все системные параметры экземпляра будут иметь значения глобальных системных параметров по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="825af-140">At this point, all system parameters for the instance will have the values of the global default system parameters.</span></span> <span data-ttu-id="825af-141">После того как экземпляр будет выделен, он должен быть завершен и/или освобожден позже.</span><span class="sxs-lookup"><span data-stu-id="825af-141">Once an instance will be allocated, it needs to be terminated and/or freed later on.</span></span>

<span data-ttu-id="825af-142">В случае сбоя будет возвращена ошибка, представляющая причину сбоя, и ни один экземпляр не будет выделен.</span><span class="sxs-lookup"><span data-stu-id="825af-142">On failure, an error representing the cause of failure will be returned and no instance will be allocated.</span></span>

#### <a name="remarks"></a><span data-ttu-id="825af-143">Комментарии</span><span class="sxs-lookup"><span data-stu-id="825af-143">Remarks</span></span>

<span data-ttu-id="825af-144">Экземпляр должен быть инициализирован с помощью вызова [жетинит](./jetinit-function.md) , прежде чем он сможет использоваться любым другим, кроме [жетсетсистемпараметер](./jetsetsystemparameter-function.md).</span><span class="sxs-lookup"><span data-stu-id="825af-144">An instance must be initialized with a call to [JetInit](./jetinit-function.md) before it can be used by anything other than [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span></span>

<span data-ttu-id="825af-145">Экземпляр уничтожается вызовом функции [жеттерм](./jetterm-function.md) , даже если этот экземпляр никогда не был инициализирован с помощью [жетинит](./jetinit-function.md).</span><span class="sxs-lookup"><span data-stu-id="825af-145">An instance is destroyed by a call to the [JetTerm](./jetterm-function.md) function, even if that instance was never initialized using [JetInit](./jetinit-function.md).</span></span> <span data-ttu-id="825af-146">Максимальное число экземпляров, которые могут быть созданы за один раз, управляется *JET_paramMaxInstances*, которые можно настроить с помощью вызова [жетсетсистемпараметер](./jetsetsystemparameter-function.md).</span><span class="sxs-lookup"><span data-stu-id="825af-146">The maximum number of instances that may be created at any one time is controlled by *JET_paramMaxInstances*, which can be configured by a call to [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span></span> <span data-ttu-id="825af-147">Экземпляр — это единица восстановления для ядра СУБД.</span><span class="sxs-lookup"><span data-stu-id="825af-147">An instance is the unit of recoverability for the database engine.</span></span> <span data-ttu-id="825af-148">Он управляет жизненным циклом всех файлов, используемых для защиты целостности данных в наборе файлов базы данных.</span><span class="sxs-lookup"><span data-stu-id="825af-148">It controls the life cycle of all the files used to protect the integrity of the data in a set of database files.</span></span> <span data-ttu-id="825af-149">Эти файлы включают файл контрольных точек и файлы журнала транзакций.</span><span class="sxs-lookup"><span data-stu-id="825af-149">These files include the checkpoint file and the transaction log files.</span></span>

<span data-ttu-id="825af-150">Если функция выполнена, ядро СУБД автоматически перейдет в режим с несколькими экземплярами как побочный результат этого вызова.</span><span class="sxs-lookup"><span data-stu-id="825af-150">If the function succeeds, the database engine will automatically be changed to multi-instance mode as a side effect of this call.</span></span> <span data-ttu-id="825af-151">Если приложению нужно разрешить только один экземпляр в процессе, то для запуска ядра СУБД в режиме совместимости Windows 2000 следует использовать [жетинит](./jetinit-function.md) .</span><span class="sxs-lookup"><span data-stu-id="825af-151">If the application desires to allow only one instance in the process then [JetInit](./jetinit-function.md) should be used to start the database engine in Windows 2000 compatibility mode.</span></span>

<span data-ttu-id="825af-152">При наличии параметра *сздисплайнаме* будет использоваться для указания экземпляра в таких местах, как журнал событий, или для других вызывающих объектов, таких как приложения резервного копирования (с помощью таких функций, как [жетжетинстанцеинфо](./jetgetinstanceinfo-function.md) или [жетосснапшотфризе](./jetossnapshotfreeze-function.md)).</span><span class="sxs-lookup"><span data-stu-id="825af-152">If present, the *szDisplayName* parameter will be used to identify the instance in places like Event Log or towards other callers like backup applications (through functions like [JetGetInstanceInfo](./jetgetinstanceinfo-function.md) or [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)).</span></span> <span data-ttu-id="825af-153">Если отображаемое имя не указано, вместо него будет использоваться уникальный параметр *сзинстанценаме* , если он есть, в противном случае возвращается пустая строка.</span><span class="sxs-lookup"><span data-stu-id="825af-153">If the display name is not provided, the unique *szInstanceName* parameter will be used instead, if present, otherwise an empty string will be returned.</span></span> <span data-ttu-id="825af-154">Если в обработчике не установлен режим выполнения, после этого вызова он будет установлен в режим с несколькими экземплярами.</span><span class="sxs-lookup"><span data-stu-id="825af-154">If the engine did not have the running mode set, after this call, it will be set to multi-instance mode.</span></span>

<span data-ttu-id="825af-155">Типичная последовательность запуска для процесса, потенциально выполняющего несколько экземпляров Jet, будет выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="825af-155">The typical start-up sequence for a process potentially running multiple Jet instances would be:</span></span>

  - <span data-ttu-id="825af-156">Вызов **JetCreateInstance2** , который выделит и назначит имя экземпляра.</span><span class="sxs-lookup"><span data-stu-id="825af-156">A call to **JetCreateInstance2** which will allocate and name the instance.</span></span>

  - <span data-ttu-id="825af-157">Несколько вызовов [жетсетсистемпараметер](./jetsetsystemparameter-function.md) для этого экземпляра, чтобы задать различные системные параметры.</span><span class="sxs-lookup"><span data-stu-id="825af-157">Multiple calls to [JetSetSystemParameter](./jetsetsystemparameter-function.md) for that instance in order to set different system parameters.</span></span> <span data-ttu-id="825af-158">Обратите внимание, что некоторые системные параметры должны быть уникальными для каждого экземпляра (например, *JET_paramSystemPath* или *JET_paramLogFilePath*), поэтому, скорее всего, потребуется задать каждый из них.</span><span class="sxs-lookup"><span data-stu-id="825af-158">Note that some system parameters need to be unique for each instance (like *JET_paramSystemPath* or *JET_paramLogFilePath*) so most likely, each of these will need to be set.</span></span>

  - <span data-ttu-id="825af-159">Запустите экземпляр с помощью [жетинит](./jetinit-function.md) или [JetInit2](./jetinit2-function.md).</span><span class="sxs-lookup"><span data-stu-id="825af-159">Start the instance using [JetInit](./jetinit-function.md) or [JetInit2](./jetinit2-function.md).</span></span> <span data-ttu-id="825af-160">Чтобы завершить и/или освободить экземпляр, используйте [жеттерм](./jetterm-function.md) или [JetTerm2](./jetterm2-function.md).</span><span class="sxs-lookup"><span data-stu-id="825af-160">In order to terminate and/or free an instance, use [JetTerm](./jetterm-function.md) or [JetTerm2](./jetterm2-function.md).</span></span>

<span data-ttu-id="825af-161">Если это первый экземпляр для запуска, существует ряд дополнительных шагов, которые будут выполнены во время этого вызова для выполнения базовой инициализации и настройки системы.</span><span class="sxs-lookup"><span data-stu-id="825af-161">If this is the first instance to be started, there are a number of additional steps which will be executed during this call in order to make basic system initialization and configuration.</span></span> <span data-ttu-id="825af-162">Некоторые из этих шагов могут привести к возникновению конкретных ошибок, начинающихся с JET_errOutOfMemory, а также других (см. Дополнительные сведения о возвращаемых значениях).</span><span class="sxs-lookup"><span data-stu-id="825af-162">A number of those steps might result in specific errors starting with JET_errOutOfMemory but others as well (see Return Values for more information).</span></span>

#### <a name="requirements"></a><span data-ttu-id="825af-163">Требования</span><span class="sxs-lookup"><span data-stu-id="825af-163">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="825af-164"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="825af-164"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="825af-165">Требуется Windows Vista или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="825af-165">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="825af-166"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="825af-166"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="825af-167">Требуется Windows Server 2008 или Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="825af-167">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="825af-168"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="825af-168"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="825af-169">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="825af-169">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="825af-170"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="825af-170"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="825af-171">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="825af-171">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="825af-172"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="825af-172"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="825af-173">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="825af-173">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="825af-174"><strong>Юникод</strong></span><span class="sxs-lookup"><span data-stu-id="825af-174"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="825af-175">Реализуется как <strong>JetCreateInstance2W</strong> (Юникод) и <strong>JetCreateInstance2A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="825af-175">Implemented as <strong>JetCreateInstance2W</strong> (Unicode) and <strong>JetCreateInstance2A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="825af-176">См. также:</span><span class="sxs-lookup"><span data-stu-id="825af-176">See Also</span></span>

[<span data-ttu-id="825af-177">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="825af-177">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="825af-178">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="825af-178">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="825af-179">жеткреатеинстанце</span><span class="sxs-lookup"><span data-stu-id="825af-179">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="825af-180">жетенаблемултиинстанце</span><span class="sxs-lookup"><span data-stu-id="825af-180">JetEnableMultiInstance</span></span>](./jetenablemultiinstance-function.md)  
[<span data-ttu-id="825af-181">жетжетинстанцеинфо</span><span class="sxs-lookup"><span data-stu-id="825af-181">JetGetInstanceInfo</span></span>](./jetgetinstanceinfo-function.md)  
[<span data-ttu-id="825af-182">жетинит</span><span class="sxs-lookup"><span data-stu-id="825af-182">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="825af-183">JetInit2</span><span class="sxs-lookup"><span data-stu-id="825af-183">JetInit2</span></span>](./jetinit2-function.md)  
[<span data-ttu-id="825af-184">жетосснапшотфризе</span><span class="sxs-lookup"><span data-stu-id="825af-184">JetOSSnapshotFreeze</span></span>](./jetossnapshotfreeze-function.md)  
[<span data-ttu-id="825af-185">жетсетсистемпараметер</span><span class="sxs-lookup"><span data-stu-id="825af-185">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="825af-186">жеттерм</span><span class="sxs-lookup"><span data-stu-id="825af-186">JetTerm</span></span>](./jetterm-function.md)  
[<span data-ttu-id="825af-187">JetTerm2</span><span class="sxs-lookup"><span data-stu-id="825af-187">JetTerm2</span></span>](./jetterm2-function.md)
