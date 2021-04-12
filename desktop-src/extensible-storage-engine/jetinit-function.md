---
description: Дополнительные сведения о функции Жетинит
title: Функция JetInit
TOCTitle: JetInit Function
ms:assetid: b7f78cca-7268-4045-bda2-20746b1d6370
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294068(v=EXCHG.10)
ms:contentKeyID: 32765683
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetInit
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 308c012bc5eb144e0ac0d608c64d63ccf39aeca1
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "104356213"
---
# <a name="jetinit-function"></a><span data-ttu-id="a2e19-103">Функция JetInit</span><span class="sxs-lookup"><span data-stu-id="a2e19-103">JetInit Function</span></span>


<span data-ttu-id="a2e19-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="a2e19-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetinit-function"></a><span data-ttu-id="a2e19-105">Функция JetInit</span><span class="sxs-lookup"><span data-stu-id="a2e19-105">JetInit Function</span></span>

<span data-ttu-id="a2e19-106">Функция **жетинит** помещает ядро СУБД в состояние, где оно может поддерживать использование файлов базы данных приложением.</span><span class="sxs-lookup"><span data-stu-id="a2e19-106">The **JetInit** function puts the database engine into a state where it can support application use of database files.</span></span> <span data-ttu-id="a2e19-107">Подсистема уже должна быть правильно настроена для инициализации с помощью [жетсетсистемпараметер](./jetsetsystemparameter-function.md).</span><span class="sxs-lookup"><span data-stu-id="a2e19-107">The engine must already be properly configured for initialization using [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span></span> <span data-ttu-id="a2e19-108">Восстановление после сбоя базы данных выполняется автоматически в рамках процесса инициализации.</span><span class="sxs-lookup"><span data-stu-id="a2e19-108">Database crash recovery is performed automatically as a part of the initialization process.</span></span>

```cpp
JET_ERR JET_API JetInit(
  __in_out_opt  JET_INSTANCE* pinstance
);
```

### <a name="parameters"></a><span data-ttu-id="a2e19-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="a2e19-109">Parameters</span></span>

<span data-ttu-id="a2e19-110">*пинстанце*</span><span class="sxs-lookup"><span data-stu-id="a2e19-110">*pinstance*</span></span>

<span data-ttu-id="a2e19-111">Экземпляр, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="a2e19-111">The instance to use for this call.</span></span>

<span data-ttu-id="a2e19-112">Для Windows 2000 этот параметр игнорируется и всегда должен иметь значение NULL.</span><span class="sxs-lookup"><span data-stu-id="a2e19-112">For Windows 2000, this parameter is ignored and should always be NULL.</span></span>

<span data-ttu-id="a2e19-113">Для Windows XP и более поздних версий использование этого параметра зависит от режима работы ядра.</span><span class="sxs-lookup"><span data-stu-id="a2e19-113">For Windows XP and later releases, the use of this parameter depends on the operating mode of the engine.</span></span> <span data-ttu-id="a2e19-114">Если ядро работает в устаревшем режиме (режим совместимости Windows 2000), где поддерживается только один экземпляр, то этот параметр может иметь значение NULL или быть установлен в допустимый выходной буфер, который будет возвращать глобальный экземпляр, созданный в качестве побочного результата инициализации.</span><span class="sxs-lookup"><span data-stu-id="a2e19-114">If the engine is operating in legacy mode (Windows 2000 compatibility mode) where only one instance is supported then this parameter may either be NULL or it may be set to a valid output buffer that will return the global instance handle created as a side effect of the initialization.</span></span> <span data-ttu-id="a2e19-115">Для этого выходного буфера необходимо задать значение NULL или JET_instanceNil.</span><span class="sxs-lookup"><span data-stu-id="a2e19-115">This output buffer must be set to NULL or JET_instanceNil.</span></span> <span data-ttu-id="a2e19-116">Этот экземпляр можно передать в любую другую функцию, использующую экземпляр.</span><span class="sxs-lookup"><span data-stu-id="a2e19-116">This instance handle can then be passed to any other function that uses an instance.</span></span> <span data-ttu-id="a2e19-117">Если ядро работает в режиме с несколькими экземплярами, этот параметр должен быть установлен в допустимый входной буфер, содержащий экземпляр, возвращенный экземпляром функции [жеткреатеинстанце](./jetcreateinstance-function.md) , который инициализируется.</span><span class="sxs-lookup"><span data-stu-id="a2e19-117">If the engine is operating in multi-instance mode then this parameter must be set to a valid input buffer that contains the instance handle returned by the [JetCreateInstance](./jetcreateinstance-function.md) function instance that is being initialized.</span></span>


#### <a name="remarks"></a><span data-ttu-id="a2e19-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a2e19-118">Remarks</span></span>

<span data-ttu-id="a2e19-119">Экземпляр должен быть инициализирован с помощью вызова **жетинит** , прежде чем он сможет использоваться любым другим, кроме [жетсетсистемпараметер](./jetsetsystemparameter-function.md).</span><span class="sxs-lookup"><span data-stu-id="a2e19-119">An instance must be initialized with a call to **JetInit** before it can be used by anything other than [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span></span>

<span data-ttu-id="a2e19-120">Экземпляр уничтожается вызовом функции [жеттерм](./jetterm-function.md) , даже если этот экземпляр никогда не был инициализирован с помощью **жетинит**.</span><span class="sxs-lookup"><span data-stu-id="a2e19-120">An instance is destroyed by a call to the [JetTerm](./jetterm-function.md) function, even if that instance was never initialized using **JetInit**.</span></span> <span data-ttu-id="a2e19-121">Экземпляр — это единица восстановления для ядра СУБД.</span><span class="sxs-lookup"><span data-stu-id="a2e19-121">An instance is the unit of recoverability for the database engine.</span></span> <span data-ttu-id="a2e19-122">Он управляет жизненным циклом всех файлов, используемых для защиты целостности данных в наборе файлов базы данных.</span><span class="sxs-lookup"><span data-stu-id="a2e19-122">It controls the life cycle of all the files used to protect the integrity of the data in a set of database files.</span></span> <span data-ttu-id="a2e19-123">Эти файлы включают файл контрольных точек и файлы журнала транзакций.</span><span class="sxs-lookup"><span data-stu-id="a2e19-123">These files include the checkpoint file and the transaction log files.</span></span>

<span data-ttu-id="a2e19-124">Максимальное число экземпляров, которые могут быть созданы за один раз, контролируется [JET_paramMaxInstances](./resource-parameters.md), который можно настроить с помощью вызова [жетсетсистемпараметер](./jetsetsystemparameter-function.md).</span><span class="sxs-lookup"><span data-stu-id="a2e19-124">The maximum number of instances that can be created at any one time is controlled by [JET_paramMaxInstances](./resource-parameters.md), which can be configured by a call to [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span></span> <span data-ttu-id="a2e19-125">Когда ядро СУБД инициализируется в первый раз, **жетинит** создаст начальный набор файлов для поддержки этого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="a2e19-125">When the database engine is initialized for the first time, **JetInit** will create an initial set of files to support that instance.</span></span> <span data-ttu-id="a2e19-126">Эти файлы содержат файл контрольных точек (с именем \<[JET_paramBaseName](./transaction-log-parameters.md)\> . CHK) — набор зарезервированных файлов журнала транзакций (с именем RES1. LOG и RES2. LOG) — исходный файл журнала транзакций (с именем \<[JET_paramBaseName](./transaction-log-parameters.md)\> . LOG) и временный файл базы данных (с именем в соответствии с [JET_paramTempPath](./temporary-database-parameters.md)).</span><span class="sxs-lookup"><span data-stu-id="a2e19-126">These files include a checkpoint file (named \<[JET_paramBaseName](./transaction-log-parameters.md)\>.CHK), a set of reserved transaction log files (named RES1.LOG and RES2.LOG), an initial transaction log file (named \<[JET_paramBaseName](./transaction-log-parameters.md)\>.LOG), and a temporary database file (named according to [JET_paramTempPath](./temporary-database-parameters.md)).</span></span> <span data-ttu-id="a2e19-127">Если [JET_paramRecovery](./transaction-log-parameters.md) имеет значение OFF, файл контрольных точек и файлы журнала создаваться не будут.</span><span class="sxs-lookup"><span data-stu-id="a2e19-127">If [JET_paramRecovery](./transaction-log-parameters.md) is set to "Off" then the checkpoint file and log files will not be created.</span></span> <span data-ttu-id="a2e19-128">Если [JET_paramMaxTemporaryTables](./temporary-database-parameters.md) имеет значение 0, то временный файл базы данных не будет создан.</span><span class="sxs-lookup"><span data-stu-id="a2e19-128">If [JET_paramMaxTemporaryTables](./temporary-database-parameters.md) is set to zero then the temporary database file will not be created.</span></span> <span data-ttu-id="a2e19-129">Эти файлы представляют место на диске экземпляра, и управление им должно осуществляться с осторожностью.</span><span class="sxs-lookup"><span data-stu-id="a2e19-129">These files represent the on disk footprint of an instance and must be managed with care.</span></span> <span data-ttu-id="a2e19-130">Если эти файлы повреждены по отдельности или по отношению друг к другу, то данные, хранящиеся в базах данных, связанных с экземпляром, могут быть потеряны.</span><span class="sxs-lookup"><span data-stu-id="a2e19-130">If these files are corrupted individually or with respect to one another then the data stored in the databases associated with the instance may be lost.</span></span>

<span data-ttu-id="a2e19-131">Когда ядро СУБД инициализируется с помощью существующего набора файлов журнала транзакций, эти файлы будут проверены, чтобы узнать, не завершилось ли предыдущее воплощение экземпляра со сбоями.</span><span class="sxs-lookup"><span data-stu-id="a2e19-131">When the database engine is initialized with an existing set of transaction log files then those files will be inspected to see if the previous incarnation of the instance suffered from a crash.</span></span> <span data-ttu-id="a2e19-132">При обнаружении сбоя будет автоматически выполнено восстановление после сбоя.</span><span class="sxs-lookup"><span data-stu-id="a2e19-132">If a crash is detected then crash recovery will automatically be performed.</span></span> <span data-ttu-id="a2e19-133">Этот процесс приведет к восстановлению баз данных, присоединенных к экземпляру, во время предыдущего создания подсистемы и сохранения изменений в файлах базы данных.</span><span class="sxs-lookup"><span data-stu-id="a2e19-133">This process will reconstruct the databases attached to the instance during the previous incarnation of the engine and save the changes back to the database files.</span></span> <span data-ttu-id="a2e19-134">Результатом будут базы данных с одинаковыми транзакциями.</span><span class="sxs-lookup"><span data-stu-id="a2e19-134">The result will be databases that are transaction consistent.</span></span> <span data-ttu-id="a2e19-135">Этот процесс может занять довольно много времени, если количество файлов журнала транзакций, воспроизводимых с базами данных, велико.</span><span class="sxs-lookup"><span data-stu-id="a2e19-135">It is possible for this process to take quite some time if the number of transaction log files to replay against the databases is large.</span></span>

<span data-ttu-id="a2e19-136">Из-за того, что **жетинит** выполняет восстановление после сбоя, в случае сбоя может возвращаться почти любая ошибка ядра СУБД.</span><span class="sxs-lookup"><span data-stu-id="a2e19-136">Due to the fact that **JetInit** performs crash recovery, it is possible for almost any database engine error to be returned in the event of a failure.</span></span> <span data-ttu-id="a2e19-137">На практике большинство ошибок, возникающих при развертывании, делятся на две категории: повреждение данных и неудачное Управление файлами.</span><span class="sxs-lookup"><span data-stu-id="a2e19-137">In practice, most of the errors seen in deployment fall into two categories: data corruption and file mismanagement.</span></span> <span data-ttu-id="a2e19-138">Повреждение данных будет очень часто переявляться в следующих или похожих ошибках:</span><span class="sxs-lookup"><span data-stu-id="a2e19-138">Data corruption will manifest itself most often in the following or similar errors:</span></span>

  - <span data-ttu-id="a2e19-139">JET_errReadVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="a2e19-139">JET_errReadVerifyFailure</span></span>

  - <span data-ttu-id="a2e19-140">JET_errLogFileCorrupt</span><span class="sxs-lookup"><span data-stu-id="a2e19-140">JET_errLogFileCorrupt</span></span>

  - <span data-ttu-id="a2e19-141">JET_errCheckpointCorrupt</span><span class="sxs-lookup"><span data-stu-id="a2e19-141">JET_errCheckpointCorrupt</span></span>

<span data-ttu-id="a2e19-142">Эти ошибки почти всегда вызываются аппаратными проблемами, поэтому их нельзя избежать.</span><span class="sxs-lookup"><span data-stu-id="a2e19-142">These errors are almost always caused by hardware problems and thus cannot be avoided.</span></span> <span data-ttu-id="a2e19-143">Необычное Управление файлами сама по себе будет переявляться в следующих или похожих ошибках:</span><span class="sxs-lookup"><span data-stu-id="a2e19-143">File mismanagement will manifest itself most often in the following or similar errors:</span></span>

  - <span data-ttu-id="a2e19-144">JET_errMissingLogFile</span><span class="sxs-lookup"><span data-stu-id="a2e19-144">JET_errMissingLogFile</span></span>

  - <span data-ttu-id="a2e19-145">JET_errAttachedDatabaseMismatch</span><span class="sxs-lookup"><span data-stu-id="a2e19-145">JET_errAttachedDatabaseMismatch</span></span>

  - <span data-ttu-id="a2e19-146">JET_errDatabaseSharingViolation</span><span class="sxs-lookup"><span data-stu-id="a2e19-146">JET_errDatabaseSharingViolation</span></span>

  - <span data-ttu-id="a2e19-147">JET_errInvalidLogSequence</span><span class="sxs-lookup"><span data-stu-id="a2e19-147">JET_errInvalidLogSequence</span></span>

<span data-ttu-id="a2e19-148">Если восстановление выполняется на наборе журналов, для которых не все базы данных (возвращающие ошибку JET_errAttachedDatabaseMismatch при нормальных обстоятельствах), и клиент желает восстановиться, несмотря на отсутствующие базы данных, можно использовать JET_ Битреплайигноремиссингдб для продолжения восстановления доступных баз данных.</span><span class="sxs-lookup"><span data-stu-id="a2e19-148">If recovery is running on a set of logs, for which not all databases is present (which will return the error JET_errAttachedDatabaseMismatch under normal circumstances), and the client wishes recovery to continue despite missing databases, the JET_ bitReplayIgnoreMissingDB can be used to continue recovery for the available databases.</span></span> <span data-ttu-id="a2e19-149">Эти ошибки предотвращаются приложением.</span><span class="sxs-lookup"><span data-stu-id="a2e19-149">These errors are preventable by the application.</span></span> <span data-ttu-id="a2e19-150">Приложение должно быть аккуратным, чтобы защитить репозиторий этих файлов от манипуляции извне, такими как пользователь или другие приложения.</span><span class="sxs-lookup"><span data-stu-id="a2e19-150">The application must be careful to protect the repository of these files from manipulation by outside forces such as the user or other applications.</span></span> <span data-ttu-id="a2e19-151">Если приложение должно полностью уничтожить экземпляр, необходимо удалить все файлы, связанные с этим экземпляром.</span><span class="sxs-lookup"><span data-stu-id="a2e19-151">If the application desires to destroy an instance entirely then all the files associated with the instance must be deleted.</span></span> <span data-ttu-id="a2e19-152">К ним относятся файл контрольных точек, файлы журнала транзакций и все файлы базы данных, присоединенные к экземпляру.</span><span class="sxs-lookup"><span data-stu-id="a2e19-152">These include the checkpoint file, the transaction log files, and any database files attached to the instance.</span></span>

<span data-ttu-id="a2e19-153">Функция **жетинит** ведет себя по-разному, в отношении файлов базы данных, присоединенных к экземпляру, между Windows 2000 и более поздними версиями.</span><span class="sxs-lookup"><span data-stu-id="a2e19-153">The **JetInit** function behaves differently, with respect to database files attached to the instance, between Windows 2000 and later releases.</span></span>

<span data-ttu-id="a2e19-154">**Windows 2000:**  В Windows 2000 любая база данных, присоединенная к экземпляру во время предыдущего создания этого экземпляра, остается прикрепленной к экземпляру после успешного завершения **жетинит** .</span><span class="sxs-lookup"><span data-stu-id="a2e19-154">**Windows 2000:**  In Windows 2000, any database attached to the instance during a previous incarnation of that instance remains attached to the instance after **JetInit** completes successfully.</span></span> <span data-ttu-id="a2e19-155">Необязательно вызывать [жетаттачдатабасе](./jetattachdatabase-function.md) после **жетинит** , чтобы получить доступ к базе данных в дальнейшем.</span><span class="sxs-lookup"><span data-stu-id="a2e19-155">It is not necessary to call [JetAttachDatabase](./jetattachdatabase-function.md) after **JetInit** to insure later database access.</span></span> <span data-ttu-id="a2e19-156">Если функция [жетаттачдатабасе](./jetattachdatabase-function.md) вызывается после функции **жетинит** , будет возвращено предупреждение JET_wrnDatabaseAttached.</span><span class="sxs-lookup"><span data-stu-id="a2e19-156">If the [JetAttachDatabase](./jetattachdatabase-function.md) function is called after the **JetInit** function, the JET_wrnDatabaseAttached warning will be returned.</span></span> <span data-ttu-id="a2e19-157">Это предупреждение означает, что вложение базы данных сохранено и может быть проигнорировано.</span><span class="sxs-lookup"><span data-stu-id="a2e19-157">This warning indicates that the database attachment was preserved and can be ignored.</span></span>

<span data-ttu-id="a2e19-158">**Windows XP:**  В Windows XP и более поздних версиях все базы данных автоматически отсоединяются от экземпляра с помощью **жетинит**.</span><span class="sxs-lookup"><span data-stu-id="a2e19-158">**Windows XP:**  In Windows XP and later releases, all databases are automatically detached from the instance by **JetInit**.</span></span> <span data-ttu-id="a2e19-159">Это означает, что в данном случае [жетаттачдатабасе](./jetattachdatabase-function.md) всегда должен вызываться после **жетинит** .</span><span class="sxs-lookup"><span data-stu-id="a2e19-159">This means that [JetAttachDatabase](./jetattachdatabase-function.md) must always be called after **JetInit** in this case.</span></span>

<span data-ttu-id="a2e19-160">Любое приложение, написанное для запуска в Windows 2000 и последующих выпусках, должно всегда вызывать [жетаттачдатабасе](./jetattachdatabase-function.md) после **жетинит**.</span><span class="sxs-lookup"><span data-stu-id="a2e19-160">Any application written to run on Windows 2000 and on later releases must always call [JetAttachDatabase](./jetattachdatabase-function.md) after **JetInit**.</span></span> <span data-ttu-id="a2e19-161">Если приложение выполняется в Windows 2000, в некоторых случаях должно появиться JET_wrnDatabaseAttached.</span><span class="sxs-lookup"><span data-stu-id="a2e19-161">If the application runs on Windows 2000 then it must expect to see JET_wrnDatabaseAttached in some cases.</span></span> <span data-ttu-id="a2e19-162">Дополнительные сведения см. в разделе [жетаттачдатабасе](./jetattachdatabase-function.md) .</span><span class="sxs-lookup"><span data-stu-id="a2e19-162">See [JetAttachDatabase](./jetattachdatabase-function.md) for more information.</span></span>

#### <a name="requirements"></a><span data-ttu-id="a2e19-163">Требования</span><span class="sxs-lookup"><span data-stu-id="a2e19-163">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a2e19-164"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="a2e19-164"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="a2e19-165">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="a2e19-165">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a2e19-166"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="a2e19-166"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="a2e19-167">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="a2e19-167">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a2e19-168"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="a2e19-168"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="a2e19-169">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="a2e19-169">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a2e19-170"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="a2e19-170"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="a2e19-171">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="a2e19-171">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a2e19-172"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="a2e19-172"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="a2e19-173">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="a2e19-173">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="a2e19-174">См. также:</span><span class="sxs-lookup"><span data-stu-id="a2e19-174">See Also</span></span>

[<span data-ttu-id="a2e19-175">Расширяемые файлы подсистемы хранилища</span><span class="sxs-lookup"><span data-stu-id="a2e19-175">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="a2e19-176">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="a2e19-176">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="a2e19-177">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="a2e19-177">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="a2e19-178">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="a2e19-178">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="a2e19-179">JET_paramMaxTemporaryTables</span><span class="sxs-lookup"><span data-stu-id="a2e19-179">JET_paramMaxTemporaryTables</span></span>](./temporary-database-parameters.md)  
[<span data-ttu-id="a2e19-180">JET_paramRecovery</span><span class="sxs-lookup"><span data-stu-id="a2e19-180">JET_paramRecovery</span></span>](./transaction-log-parameters.md)  
[<span data-ttu-id="a2e19-181">жетаттачдатабасе</span><span class="sxs-lookup"><span data-stu-id="a2e19-181">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="a2e19-182">жеткреатеинстанце</span><span class="sxs-lookup"><span data-stu-id="a2e19-182">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="a2e19-183">JetInit3</span><span class="sxs-lookup"><span data-stu-id="a2e19-183">JetInit3</span></span>](./jetinit3-function.md)  
[<span data-ttu-id="a2e19-184">жетсетсистемпараметер</span><span class="sxs-lookup"><span data-stu-id="a2e19-184">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)
