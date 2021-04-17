---
description: Дополнительные сведения о функции Жеткреатеинстанце
title: Функция JetCreateInstance
TOCTitle: JetCreateInstance Function
ms:assetid: 9d6c8c9f-3d3b-4308-87d3-84b1ef270262
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269354(v=EXCHG.10)
ms:contentKeyID: 32765641
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateInstanceW
- JetCreateInstance
- JetCreateInstanceA
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: aa64c9aadd9402ee8356a8f4db81f878022b838b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105713074"
---
# <a name="jetcreateinstance-function"></a><span data-ttu-id="91764-103">Функция JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="91764-103">JetCreateInstance Function</span></span>


<span data-ttu-id="91764-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="91764-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetcreateinstance-function"></a><span data-ttu-id="91764-105">Функция JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="91764-105">JetCreateInstance Function</span></span>

<span data-ttu-id="91764-106">Функция **жеткреатеинстанце** выделяет новый экземпляр ядра СУБД для использования в одном процессе.</span><span class="sxs-lookup"><span data-stu-id="91764-106">The **JetCreateInstance** function allocates a new instance of the database engine for use in a single process.</span></span>

<span data-ttu-id="91764-107">**Windows XP: жеткреатеинстанце** появился в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="91764-107">**Windows XP:  JetCreateInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetCreateInstance(
      __out         JET_INSTANCE* pinstance,
      __in_opt      const tchar* szInstanceName
    );
```

### <a name="parameters"></a><span data-ttu-id="91764-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="91764-108">Parameters</span></span>

<span data-ttu-id="91764-109">*пинстанце*</span><span class="sxs-lookup"><span data-stu-id="91764-109">*pinstance*</span></span>

<span data-ttu-id="91764-110">Выходной буфер, который получает только что созданный экземпляр.</span><span class="sxs-lookup"><span data-stu-id="91764-110">The output buffer that receives the newly-created instance.</span></span>

<span data-ttu-id="91764-111">*сзинстанценаме*</span><span class="sxs-lookup"><span data-stu-id="91764-111">*szInstanceName*</span></span>

<span data-ttu-id="91764-112">Уникальный идентификатор строки для создаваемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="91764-112">A unique string identifier for the instance to be created.</span></span> <span data-ttu-id="91764-113">Эта строка должна быть уникальной в пределах данного процесса, в котором размещается ядро СУБД.</span><span class="sxs-lookup"><span data-stu-id="91764-113">This string must be unique within a given process hosting the database engine.</span></span>

<span data-ttu-id="91764-114">**Примечание** . Значение NULL обрабатывается как допустимый строковый идентификатор для экземпляра.</span><span class="sxs-lookup"><span data-stu-id="91764-114">**Note** A NULL value is treated as a valid string identifier for an instance.</span></span> <span data-ttu-id="91764-115">Только один экземпляр может иметь строковый идентификатор NULL.</span><span class="sxs-lookup"><span data-stu-id="91764-115">Only one instance may have a NULL string identifier.</span></span>

### <a name="return-value"></a><span data-ttu-id="91764-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="91764-116">Return Value</span></span>

<span data-ttu-id="91764-117">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="91764-117">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="91764-118">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="91764-118">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="91764-119">Код возврата</span><span class="sxs-lookup"><span data-stu-id="91764-119">Return code</span></span></p></th>
<th><p><span data-ttu-id="91764-120">Описание</span><span class="sxs-lookup"><span data-stu-id="91764-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="91764-121">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="91764-121">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="91764-122">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="91764-122">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="91764-123">JET_errInstanceNameInUse</span><span class="sxs-lookup"><span data-stu-id="91764-123">JET_errInstanceNameInUse</span></span></p></td>
<td><p><span data-ttu-id="91764-124">Указанное имя экземпляра уже используется для этого процесса.</span><span class="sxs-lookup"><span data-stu-id="91764-124">The specified instance name is already in use for this process.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="91764-125">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="91764-125">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="91764-126">Один из указанных параметров содержит непредвиденное значение или содержит значение, которое не имеет смысла при объединении со значением другого параметра.</span><span class="sxs-lookup"><span data-stu-id="91764-126">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="91764-127">Это может произойти для <strong>жеткреатеинстанце</strong> , когда <em>Пинстанце</em> имеет <strong>значение NULL</strong>.</span><span class="sxs-lookup"><span data-stu-id="91764-127">This can happen for <strong>JetCreateInstance</strong> when <em>pinstance</em> is <strong>NULL</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="91764-128">JET_errRunningInOneInstanceMode</span><span class="sxs-lookup"><span data-stu-id="91764-128">JET_errRunningInOneInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="91764-129">Операция завершилась ошибкой, так как ее нельзя использовать, если ядро СУБД работает в режиме одиночного экземпляра (режим совместимости с Windows 2000).</span><span class="sxs-lookup"><span data-stu-id="91764-129">The operation failed because it cannot be used when the database engine is operating in single instance mode (Windows 2000 compatibility mode).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="91764-130">JET_errTooManyInstances</span><span class="sxs-lookup"><span data-stu-id="91764-130">JET_errTooManyInstances</span></span></p></td>
<td><p><span data-ttu-id="91764-131">Не удалось создать новый экземпляр, так как достигнуто максимальное число экземпляров.</span><span class="sxs-lookup"><span data-stu-id="91764-131">A new instance could not be created because the maximum number of instances has been reached.</span></span> <span data-ttu-id="91764-132">Максимальное число поддерживаемых экземпляров настраивается с помощью <a href="gg294044(v=exchg.10).md">жетсетсистемпараметер</a> с помощью <em>JET_paramMaxInstances</em>.</span><span class="sxs-lookup"><span data-stu-id="91764-132">The maximum number of supported instances is configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> using <em>JET_paramMaxInstances</em>.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="91764-133">При успешном выполнении будет выделена новая копия, и будет возвращен идентификатор для него.</span><span class="sxs-lookup"><span data-stu-id="91764-133">On success, a new instance will be allocated and the identifier for it will be returned.</span></span> <span data-ttu-id="91764-134">На этом этапе все системные параметры экземпляра будут иметь значения глобальных системных параметров по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="91764-134">At this point, all system parameters for the instance will have the values of the global default system parameters.</span></span> <span data-ttu-id="91764-135">После того как экземпляр будет выделен, он должен быть завершен и/или освобожден позже.</span><span class="sxs-lookup"><span data-stu-id="91764-135">Once an instance will be allocated, it needs to be terminated and/or freed later on.</span></span>

<span data-ttu-id="91764-136">В случае сбоя будет возвращена ошибка, представляющая причину сбоя, и ни один экземпляр не будет выделен.</span><span class="sxs-lookup"><span data-stu-id="91764-136">On failure, an error representing the cause of failure will be returned and no instance will be allocated.</span></span>

#### <a name="remarks"></a><span data-ttu-id="91764-137">Комментарии</span><span class="sxs-lookup"><span data-stu-id="91764-137">Remarks</span></span>

<span data-ttu-id="91764-138">Экземпляр должен быть инициализирован с помощью вызова [жетинит](./jetinit-function.md) , прежде чем он сможет использоваться любым другим, кроме [жетсетсистемпараметер](./jetsetsystemparameter-function.md).</span><span class="sxs-lookup"><span data-stu-id="91764-138">An instance must be initialized with a call to [JetInit](./jetinit-function.md) before it can be used by anything other than [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span></span>

<span data-ttu-id="91764-139">Экземпляр уничтожается вызовом функции [жеттерм](./jetterm-function.md) , даже если этот экземпляр никогда не был инициализирован с помощью [жетинит](./jetinit-function.md).</span><span class="sxs-lookup"><span data-stu-id="91764-139">An instance is destroyed by a call to the [JetTerm](./jetterm-function.md) function, even if that instance was never initialized using [JetInit](./jetinit-function.md).</span></span> <span data-ttu-id="91764-140">Максимальное число экземпляров, которые могут быть созданы за один раз, управляется [JET_paramMaxInstances](./resource-parameters.md), которые можно настроить с помощью вызова [жетсетсистемпараметер](./jetsetsystemparameter-function.md).</span><span class="sxs-lookup"><span data-stu-id="91764-140">The maximum number of instances that may be created at any one time is controlled by [JET_paramMaxInstances](./resource-parameters.md), which can be configured by a call to [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span></span> <span data-ttu-id="91764-141">Экземпляр — это единица восстановления для ядра СУБД.</span><span class="sxs-lookup"><span data-stu-id="91764-141">An instance is the unit of recoverability for the database engine.</span></span> <span data-ttu-id="91764-142">Он управляет жизненным циклом всех файлов, используемых для защиты целостности данных в наборе файлов базы данных.</span><span class="sxs-lookup"><span data-stu-id="91764-142">It controls the life cycle of all the files used to protect the integrity of the data in a set of database files.</span></span> <span data-ttu-id="91764-143">Эти файлы включают файл контрольных точек и файлы журнала транзакций.</span><span class="sxs-lookup"><span data-stu-id="91764-143">These files include the checkpoint file and the transaction log files.</span></span>

<span data-ttu-id="91764-144">Если функция выполнена, ядро СУБД автоматически перейдет в режим с несколькими экземплярами как побочный результат этого вызова.</span><span class="sxs-lookup"><span data-stu-id="91764-144">If the function succeeds, the database engine will automatically be changed to multi-instance mode as a side effect of this call.</span></span> <span data-ttu-id="91764-145">Если приложению нужно разрешить только один экземпляр в процессе, то для запуска ядра СУБД в режиме совместимости Windows 2000 следует использовать [жетинит](./jetinit-function.md) .</span><span class="sxs-lookup"><span data-stu-id="91764-145">If the application desires to allow only one instance in the process then [JetInit](./jetinit-function.md) should be used to start the database engine in Windows 2000 compatibility mode.</span></span>

<span data-ttu-id="91764-146">При наличии *сздисплайнаме* будет использоваться для указания экземпляра в таких местах, как журнал событий, или для других вызывающих объектов, таких как резервные приложения (с помощью таких функций, как [жетжетинстанцеинфо](./jetgetinstanceinfo-function.md) или [жетосснапшотфризе](./jetossnapshotfreeze-function.md)).</span><span class="sxs-lookup"><span data-stu-id="91764-146">If present, the *szDisplayName* will be used to identify the instance in places like Event Log or towards other callers like backup applications (through functions like [JetGetInstanceInfo](./jetgetinstanceinfo-function.md) or [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)).</span></span> <span data-ttu-id="91764-147">Если отображаемое имя не указано, вместо него будет использоваться уникальный *сзинстанценаме* , в противном случае будет возвращена пустая строка.</span><span class="sxs-lookup"><span data-stu-id="91764-147">If the display name is not provided, the unique *szInstanceName* will be used instead if present, otherwise an empty string will be returned.</span></span> <span data-ttu-id="91764-148">Если в обработчике не установлен режим выполнения, после этого вызова он будет установлен в режим с несколькими экземплярами.</span><span class="sxs-lookup"><span data-stu-id="91764-148">If the engine did not have the running mode set, after this call, it will be set to multi-instance mode.</span></span>

<span data-ttu-id="91764-149">Типичная последовательность запуска для процесса, потенциально выполняющего несколько экземпляров Jet, будет выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="91764-149">The typical start-up sequence for a process potentially running multiple Jet instances would be:</span></span>

  - <span data-ttu-id="91764-150">Вызов [JetCreateInstance2](./jetcreateinstance2-function.md) , который выделит и назначит имя экземпляра.</span><span class="sxs-lookup"><span data-stu-id="91764-150">A call to [JetCreateInstance2](./jetcreateinstance2-function.md) which will allocate and name the instance.</span></span>

  - <span data-ttu-id="91764-151">Несколько вызовов [жетсетсистемпараметер](./jetsetsystemparameter-function.md) для этого экземпляра, чтобы задать различные системные параметры.</span><span class="sxs-lookup"><span data-stu-id="91764-151">Multiple calls to [JetSetSystemParameter](./jetsetsystemparameter-function.md) for that instance in order to set different system parameters.</span></span> <span data-ttu-id="91764-152">Обратите внимание, что некоторые системные параметры должны быть уникальными для каждого экземпляра (например, [JET_paramSystemPath](./transaction-log-parameters.md) или [JET_paramLogFilePath](./transaction-log-parameters.md)), поэтому, скорее всего, потребуется установить каждый из них.</span><span class="sxs-lookup"><span data-stu-id="91764-152">Note that some system parameters need to be unique per instance (like [JET_paramSystemPath](./transaction-log-parameters.md) or [JET_paramLogFilePath](./transaction-log-parameters.md)) so most likely one will need to set each of those.</span></span>

  - <span data-ttu-id="91764-153">Запустите экземпляр с помощью [жетинит](./jetinit-function.md) или [JetInit2](./jetinit2-function.md).</span><span class="sxs-lookup"><span data-stu-id="91764-153">Start the instance using [JetInit](./jetinit-function.md) or [JetInit2](./jetinit2-function.md).</span></span> <span data-ttu-id="91764-154">Чтобы завершить и (или) освободить экземпляр, необходимо использовать [жеттерм](./jetterm-function.md), [JetTerm2](./jetterm2-function.md) .</span><span class="sxs-lookup"><span data-stu-id="91764-154">In order to terminate and/or free an instance, [JetTerm](./jetterm-function.md), [JetTerm2](./jetterm2-function.md) needs to be used.</span></span>

<span data-ttu-id="91764-155">Если это первый экземпляр для запуска, существует ряд дополнительных шагов, которые будут выполнены во время этого вызова для выполнения базовой инициализации и настройки системы.</span><span class="sxs-lookup"><span data-stu-id="91764-155">If this is the first instance to be started, there are a number of additional steps which will be executed during this call in order to make basic system initialization and configuration.</span></span> <span data-ttu-id="91764-156">Некоторые из этих шагов могут привести к возникновению конкретных ошибок, начинающихся с JET_errOutOfMemory, а также других (см. ошибки выше).</span><span class="sxs-lookup"><span data-stu-id="91764-156">A number of those steps might result in specific errors starting with JET_errOutOfMemory but others as well (see errors above).</span></span>

#### <a name="requirements"></a><span data-ttu-id="91764-157">Требования</span><span class="sxs-lookup"><span data-stu-id="91764-157">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="91764-158"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="91764-158"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="91764-159">Требуется Windows Vista или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="91764-159">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="91764-160"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="91764-160"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="91764-161">Требуется Windows Server 2008 или Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="91764-161">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="91764-162"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="91764-162"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="91764-163">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="91764-163">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="91764-164"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="91764-164"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="91764-165">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="91764-165">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="91764-166"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="91764-166"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="91764-167">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="91764-167">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="91764-168"><strong>Юникод</strong></span><span class="sxs-lookup"><span data-stu-id="91764-168"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="91764-169">Реализуется как <strong>жеткреатеинстанцев</strong> (Юникод) и <strong>жеткреатеинстанцеа</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="91764-169">Implemented as <strong>JetCreateInstanceW</strong> (Unicode) and <strong>JetCreateInstanceA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="91764-170">См. также:</span><span class="sxs-lookup"><span data-stu-id="91764-170">See Also</span></span>

[<span data-ttu-id="91764-171">Расширяемые файлы подсистемы хранилища</span><span class="sxs-lookup"><span data-stu-id="91764-171">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="91764-172">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="91764-172">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="91764-173">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="91764-173">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="91764-174">JetCreateInstance2</span><span class="sxs-lookup"><span data-stu-id="91764-174">JetCreateInstance2</span></span>](./jetcreateinstance2-function.md)  
[<span data-ttu-id="91764-175">жетенаблемултиинстанце</span><span class="sxs-lookup"><span data-stu-id="91764-175">JetEnableMultiInstance</span></span>](./jetenablemultiinstance-function.md)  
[<span data-ttu-id="91764-176">жетжетинстанцеинфо</span><span class="sxs-lookup"><span data-stu-id="91764-176">JetGetInstanceInfo</span></span>](./jetgetinstanceinfo-function.md)  
[<span data-ttu-id="91764-177">жетинит</span><span class="sxs-lookup"><span data-stu-id="91764-177">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="91764-178">JetInit2</span><span class="sxs-lookup"><span data-stu-id="91764-178">JetInit2</span></span>](./jetinit2-function.md)  
[<span data-ttu-id="91764-179">жетосснапшотфризе</span><span class="sxs-lookup"><span data-stu-id="91764-179">JetOSSnapshotFreeze</span></span>](./jetossnapshotfreeze-function.md)  
[<span data-ttu-id="91764-180">жетсетсистемпараметер</span><span class="sxs-lookup"><span data-stu-id="91764-180">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="91764-181">жеттерм</span><span class="sxs-lookup"><span data-stu-id="91764-181">JetTerm</span></span>](./jetterm-function.md)  
[<span data-ttu-id="91764-182">JetTerm2</span><span class="sxs-lookup"><span data-stu-id="91764-182">JetTerm2</span></span>](./jetterm2-function.md)
