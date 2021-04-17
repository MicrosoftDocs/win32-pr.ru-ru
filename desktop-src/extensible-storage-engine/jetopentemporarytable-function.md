---
description: Дополнительные сведения о функции Жетопентемпораритабле
title: Функция Жетопентемпораритабле
TOCTitle: JetOpenTemporaryTable Function
ms:assetid: feacd0b8-2298-4ec6-aa59-0fede08474bc
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294144(v=EXCHG.10)
ms:contentKeyID: 32765758
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenTemporaryTable
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2335f6d6426b321d5db55b4ed005c6220484d509
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693349"
---
# <a name="jetopentemporarytable-function"></a><span data-ttu-id="a7ddd-103">Функция Жетопентемпораритабле</span><span class="sxs-lookup"><span data-stu-id="a7ddd-103">JetOpenTemporaryTable Function</span></span>


<span data-ttu-id="a7ddd-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="a7ddd-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetopentemporarytable-function"></a><span data-ttu-id="a7ddd-105">Функция Жетопентемпораритабле</span><span class="sxs-lookup"><span data-stu-id="a7ddd-105">JetOpenTemporaryTable Function</span></span>

<span data-ttu-id="a7ddd-106">Функция **жетопентемпораритабле** создает переменную таблицы с одним индексом, который может использоваться для хранения и извлечения записей, как и обычная таблица, созданная с помощью [жеткреатетаблеколумниндекс](./jetcreatetablecolumnindex-function.md).</span><span class="sxs-lookup"><span data-stu-id="a7ddd-106">The **JetOpenTemporaryTable** function creates a volatile table with a single index that can be used to store and retrieve records, just like an ordinary table that is created via [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md).</span></span>

<span data-ttu-id="a7ddd-107">**Windows Vista:**  **Жетопентемпораритабле** появился в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-107">**Windows Vista:**  **JetOpenTemporaryTable** is introduced in Windows Vista.</span></span>

<span data-ttu-id="a7ddd-108">Временные таблицы работают быстрее обычных таблиц из-за их временной природы.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-108">Temporary tables are faster than ordinary tables due to their volatile nature.</span></span> <span data-ttu-id="a7ddd-109">Они могут быстро отсортировать и выполнить удаление дубликатов наборов записей, если доступ к ним осуществляется исключительно последовательно.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-109">They can quickly sort and perform duplicate removal on record sets when they are accessed in a purely sequential manner.</span></span>

```cpp
    JET_ERR JET_API JetOpenTemporaryTable(
      __in          JET_SESID sesid,
      __in          JET_OPENTEMPORARYTABLE* popentemporarytable
    );
```

### <a name="parameters"></a><span data-ttu-id="a7ddd-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="a7ddd-110">Parameters</span></span>

<span data-ttu-id="a7ddd-111">*сесид*</span><span class="sxs-lookup"><span data-stu-id="a7ddd-111">*sesid*</span></span>

<span data-ttu-id="a7ddd-112">Сеанс, который будет использоваться для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-112">The session that will be used for this call.</span></span>

<span data-ttu-id="a7ddd-113">*попентемпораритабле*</span><span class="sxs-lookup"><span data-stu-id="a7ddd-113">*popentemporarytable*</span></span>

<span data-ttu-id="a7ddd-114">Указатель на структуру [JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-structure.md) , содержащую описание временной таблицы, создаваемой на входе.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-114">A pointer to a [JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-structure.md) structure that contains the description of the temporary table to create on input.</span></span> <span data-ttu-id="a7ddd-115">После успешного вызова структура содержит описатель для временной таблицы и идентификаторов столбцов.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-115">After a successful call, the structure contains the handle to the temporary table and column identifications.</span></span>

### <a name="return-value"></a><span data-ttu-id="a7ddd-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a7ddd-116">Return Value</span></span>

<span data-ttu-id="a7ddd-117">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-117">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="a7ddd-118">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="a7ddd-118">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a7ddd-119">Код возврата</span><span class="sxs-lookup"><span data-stu-id="a7ddd-119">Return code</span></span></p></th>
<th><p><span data-ttu-id="a7ddd-120">Описание</span><span class="sxs-lookup"><span data-stu-id="a7ddd-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a7ddd-121">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="a7ddd-121">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="a7ddd-122">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-122">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a7ddd-123">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="a7ddd-123">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="a7ddd-124">Не удалось выполнить операцию из-за нехватки памяти, выделенной для ее завершения.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-124">The operation failed because not enough memory could be allocated to complete it.</span></span></p>
<p><span data-ttu-id="a7ddd-125"><strong>Жетопентемпораритабле</strong> может возвращать JET_errOutOfMemory, если адресное пространство хост-процесса оказывается слишком фрагментированным.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-125"><strong>JetOpenTemporaryTable</strong> can return JET_errOutOfMemory if the address space of the host process becomes too fragmented.</span></span> <span data-ttu-id="a7ddd-126">Временный диспетчер таблиц выделит блок адресного пространства размером 1 МБ для каждой создаваемой временной таблицы независимо от объема хранимых данных.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-126">The temporary table manager will allocates a 1 MB chunk of address space for every temporary table created regardless of the amount of data is stored.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a7ddd-127">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="a7ddd-127">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="a7ddd-128">Один из указанных параметров содержал непредвиденное значение или сочетание нескольких значений параметров привело к непредвиденному результату.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-128">One of the provided parameters contained an unexpected value or the combination of several parameter values resulted in an unexpected result.</span></span></p>
<p><span data-ttu-id="a7ddd-129">Эта ошибка возвращается функцией <strong>жетопентемпораритабле</strong> при выполнении следующих условий:</span><span class="sxs-lookup"><span data-stu-id="a7ddd-129">This error is returned by <strong>JetOpenTemporaryTable</strong> under the following conditions:</span></span></p>
<ul>
<li><p><span data-ttu-id="a7ddd-130">Элемент <strong>кбструкт</strong> структуры <a href="gg269206(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a> не соответствует версии этой структуры, которая поддерживается этой версией ядра СУБД.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-130">The <strong>cbStruct</strong> member of the <a href="gg269206(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a> structure does not correspond to a version of this structure that is supported by that version of the database engine</span></span></p></li>
<li><p><span data-ttu-id="a7ddd-131">Элемент <strong>кбкэймост</strong> структуры <a href="gg269206(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a> меньше JET_cbKeyMostMin.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-131">The <strong>cbKeyMost</strong> member of the <a href="gg269206(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a> structure is less than JET_cbKeyMostMin.</span></span></p></li>
<li><p><span data-ttu-id="a7ddd-132">Элемент <strong>кбкэймост</strong> структуры <a href="gg269206(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a> больше, чем наибольшее поддерживаемое значение размера страницы базы данных для экземпляра (JET_paramDatabasePageSize).</span><span class="sxs-lookup"><span data-stu-id="a7ddd-132">The <strong>cbKeyMost</strong> member of the <a href="gg269206(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a> structure is larger than the largest supported value for the database page size for the instance (JET_paramDatabasePageSize).</span></span> <span data-ttu-id="a7ddd-133">Дополнительные сведения см. в описании параметра JET_paramKeyMost в списке <a href="gg269241(v=exchg.10).md">информационных параметров</a> .</span><span class="sxs-lookup"><span data-stu-id="a7ddd-133">See the JET_paramKeyMost parameter in the list of <a href="gg269241(v=exchg.10).md">Informational Parameters</a> for more information.</span></span></p></li>
<li><p><span data-ttu-id="a7ddd-134">Элемент Кбварсегмак структуры <a href="gg269206(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a> больше, чем элемент <strong>кбкэймост</strong> .</span><span class="sxs-lookup"><span data-stu-id="a7ddd-134">The cbVarSegMac member of the <a href="gg269206(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a> structure is larger than The <strong>cbKeyMost</strong> member.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a7ddd-135">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="a7ddd-135">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="a7ddd-136">Операция не может быть завершена, так как экземпляр, связанный с сеансом, еще не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-136">The operation cannot complete because the instance that was associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a7ddd-137">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="a7ddd-137">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="a7ddd-138">Операция не может быть завершена, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-138">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a7ddd-139">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="a7ddd-139">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="a7ddd-140">Операция не может быть завершена, поскольку в экземпляре, связанном с сеансом, произошла неустранимая ошибка, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-140">The operation cannot complete because the instance that is associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="a7ddd-141"><strong>Windows XP:</strong>  Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-141"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a7ddd-142">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="a7ddd-142">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="a7ddd-143">Не удается выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-143">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a7ddd-144">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="a7ddd-144">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="a7ddd-145">Операция не может быть завершена, так как выполняется операция восстановления на экземпляре, связанном с сеансом.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-145">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a7ddd-146">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="a7ddd-146">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="a7ddd-147">Один и тот же сеанс нельзя использовать одновременно для нескольких потоков.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-147">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="a7ddd-148"><strong>Windows XP:</strong>  Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-148"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a7ddd-149">JET_errInvalidSesid</span><span class="sxs-lookup"><span data-stu-id="a7ddd-149">JET_errInvalidSesid</span></span></p></td>
<td><p><span data-ttu-id="a7ddd-150">Недопустимый обработчик сеанса или ссылается на закрытый сеанс.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-150">The session handle is invalid or refers to a closed session.</span></span></p>
<p><span data-ttu-id="a7ddd-151"><strong>Примечание</strong>  .  Эта ошибка не возвращается при всех обстоятельствах.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-151"><strong>Note</strong>  This error is not returned under all circumstances.</span></span> <span data-ttu-id="a7ddd-152">Дескрипторы проверяются только на основе наилучшей силы.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-152">Handles are validated on a best effort basis only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a7ddd-153">JET_errOutOfCursors</span><span class="sxs-lookup"><span data-stu-id="a7ddd-153">JET_errOutOfCursors</span></span></p></td>
<td><p><span data-ttu-id="a7ddd-154">Не удалось выполнить операцию, так как подсистема не может выделить ресурсы, необходимые для открытия нового курсора.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-154">The operation failed because the engine cannot allocate the resources that are required to open a new cursor.</span></span> <span data-ttu-id="a7ddd-155">Ресурсы курсора настраиваются с помощью <a href="gg294044(v=exchg.10).md">жетсетсистемпараметер</a> с <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-155">Cursor resources are configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a7ddd-156">JET_errTooManySorts</span><span class="sxs-lookup"><span data-stu-id="a7ddd-156">JET_errTooManySorts</span></span></p></td>
<td><p><span data-ttu-id="a7ddd-157">Не удалось выполнить операцию, так как подсистема не может выделить ресурсы, необходимые для создания временной таблицы.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-157">The operation failed because the engine cannot allocate the resources that are required to create a temporary table.</span></span> <span data-ttu-id="a7ddd-158">Временные ресурсы таблицы настраиваются с помощью <a href="gg294044(v=exchg.10).md">жетсетсистемпараметер</a> с <a href="gg294140(v=exchg.10).md">JET_paramMaxTemporaryTables</a>.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-158">Temporary table resources are configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg294140(v=exchg.10).md">JET_paramMaxTemporaryTables</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a7ddd-159">JET_errCannotMaterializeForwardOnlySort</span><span class="sxs-lookup"><span data-stu-id="a7ddd-159">JET_errCannotMaterializeForwardOnlySort</span></span></p></td>
<td><p><span data-ttu-id="a7ddd-160">Произошел сбой <strong>жетопентемпораритабле</strong> , так как указана JET_bitTTForwardOnly, и не удалось создать временную таблицу с использованием оптимизации "только вперед".</span><span class="sxs-lookup"><span data-stu-id="a7ddd-160"><strong>JetOpenTemporaryTable</strong> failed because JET_bitTTForwardOnly was specified and the temporary table that was specified could not be created using the forward-only optimization.</span></span></p>
<p><span data-ttu-id="a7ddd-161"><strong>Windows Server 2003:</strong>  Эта ошибка будет возвращена только в Windows Server 2003 и более поздних выпусках.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-161"><strong>Windows Server 2003:</strong>  This error will only be returned by Windows Server 2003 and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a7ddd-162">JET_errTooManyColumns</span><span class="sxs-lookup"><span data-stu-id="a7ddd-162">JET_errTooManyColumns</span></span></p></td>
<td><p><span data-ttu-id="a7ddd-163">Предпринята попытка добавить в таблицу слишком много столбцов.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-163">An attempt was made to add too many columns to the table.</span></span> <span data-ttu-id="a7ddd-164">Таблица может содержать не более JET_ccolFixedMost фиксированных столбцов, не более JET_ccolVarMost столбцов переменной длины и не более JET_ccolTaggedMost столбцов с тегами.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-164">A table can have no more than JET_ccolFixedMost fixed columns, no more than JET_ccolVarMost variable-length columns, and no more than JET_ccolTaggedMost tagged columns.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a7ddd-165">JET_errTooManyOpenTables</span><span class="sxs-lookup"><span data-stu-id="a7ddd-165">JET_errTooManyOpenTables</span></span></p></td>
<td><p><span data-ttu-id="a7ddd-166">Не удалось выполнить операцию, так как подсистема не может выделить ресурсы, необходимые для кэширования схемы таблицы.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-166">The operation failed because the engine cannot allocate the resources that are required to cache the schema of the table.</span></span> <span data-ttu-id="a7ddd-167">Чтобы настроить число таблиц со схемами, которые могут быть кэшированы, используйте <a href="gg294044(v=exchg.10).md">жетсетсистемпараметер</a> с <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-167">To configure the number of tables that have schemas that can be cached, use <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a7ddd-168">JET_errInvalidCodePage</span><span class="sxs-lookup"><span data-stu-id="a7ddd-168">JET_errInvalidCodePage</span></span></p></td>
<td><p><span data-ttu-id="a7ddd-169">Элементу <strong>CP</strong> структуры <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> не задана допустимая кодовая страница.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-169">The <strong>cp</strong> member of the <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> structure was not set to a valid code page.</span></span> <span data-ttu-id="a7ddd-170">Единственными допустимыми значениями для текстовых столбцов являются английский (1252) и Unicode (1200).</span><span class="sxs-lookup"><span data-stu-id="a7ddd-170">The only valid values for text columns are English (1252) and Unicode (1200).</span></span> <span data-ttu-id="a7ddd-171">Значение 0 означает, что будет использоваться по умолчанию (английский, 1252).</span><span class="sxs-lookup"><span data-stu-id="a7ddd-171">A value of 0 means the default will be used (English, 1252).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a7ddd-172">JET_errInvalidColumnType</span><span class="sxs-lookup"><span data-stu-id="a7ddd-172">JET_errInvalidColumnType</span></span></p></td>
<td><p><span data-ttu-id="a7ddd-173">Для элемента <strong>колтип</strong> <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> не был задан допустимый тип столбца.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-173">The <strong>coltyp</strong> member of the <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> was not set to a valid column type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a7ddd-174">JET_errInvalidLanguageId</span><span class="sxs-lookup"><span data-stu-id="a7ddd-174">JET_errInvalidLanguageId</span></span></p></td>
<td><p><span data-ttu-id="a7ddd-175">Не удалось создать индекс, поскольку была предпринята попытка использовать недопустимый код локали.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-175">The index could not be created because an attempt was made to use an invalid locale ID.</span></span> <span data-ttu-id="a7ddd-176">КОД локали может быть либо полностью недопустимым, либо связанный с ним языковой пакет не может быть установлен.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-176">The locale ID might be either completely invalid or the associated language pack might not be installed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a7ddd-177">JET_errInvalidLCMapStringFlags</span><span class="sxs-lookup"><span data-stu-id="a7ddd-177">JET_errInvalidLCMapStringFlags</span></span></p></td>
<td><p><span data-ttu-id="a7ddd-178">Не удалось создать индекс, поскольку предпринята попытка использовать недопустимый набор флагов нормализации.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-178">The index could not be created because an attempt was made to use an invalid set of normalization flags.</span></span></p>
<p><span data-ttu-id="a7ddd-179"><strong>Windows XP:</strong>  Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-179"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p>
<p><span data-ttu-id="a7ddd-180"><strong>Windows 2000:</strong>  В Windows 2000 недопустимые флаги нормализации приводят к JET_errIndexInvalidDef.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-180"><strong>Windows 2000:</strong>  On Windows 2000, invalid normalization flags will result in JET_errIndexInvalidDef.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a7ddd-181">JET_errIndexInvalidDef</span><span class="sxs-lookup"><span data-stu-id="a7ddd-181">JET_errIndexInvalidDef</span></span></p></td>
<td><p><span data-ttu-id="a7ddd-182">Не удалось создать индекс, так как было указано недопустимое определение индекса.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-182">The index could not be created because an invalid index definition was specified.</span></span> <span data-ttu-id="a7ddd-183"><strong>Жетопентемпораритабле</strong> будет возвращать эту ошибку при следующих условиях:</span><span class="sxs-lookup"><span data-stu-id="a7ddd-183"><strong>JetOpenTemporaryTable</strong> will return this error under the following conditions:</span></span></p>
<ul>
<li><p><span data-ttu-id="a7ddd-184">Указан языковой стандарт, не зависящий от языка.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-184">The Language Neutral locale is specified.</span></span></p></li>
<li><p><span data-ttu-id="a7ddd-185">Указан недопустимый набор флагов нормализации.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-185">An invalid set of normalization flags is specified.</span></span></p></li>
</ul>
<p><span data-ttu-id="a7ddd-186"><strong>Windows 2000:</strong>  Эта ошибка будет возвращена только Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-186"><strong>Windows 2000:</strong>  This error will only be returned by Windows 2000.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a7ddd-187">JET_errTooManyOpenIndexes</span><span class="sxs-lookup"><span data-stu-id="a7ddd-187">JET_errTooManyOpenIndexes</span></span></p></td>
<td><p><span data-ttu-id="a7ddd-188">Не удалось выполнить операцию, так как подсистема не может выделить ресурсы, необходимые для кэширования индексов таблицы.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-188">The operation failed because the engine cannot allocate the resources that are required to cache the indexes of the table.</span></span> <span data-ttu-id="a7ddd-189">Чтобы настроить количество индексов, имеющих схемы, которые могут быть кэшированы, используйте <a href="gg294044(v=exchg.10).md">жетсетсистемпараметер</a> с <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-189">To configure the number of indexes that have schemas that can be cached, use <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a7ddd-190">При успешном выполнении будет возвращен курсор, Открытый во вновь созданной временной таблице.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-190">On success, a cursor opened on the newly created temporary table will be returned.</span></span> <span data-ttu-id="a7ddd-191">Состояние временной базы данных будет подготовлено для размещения новой временной таблицы.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-191">The state of the temporary database will be prepared to contain the new temporary table.</span></span> <span data-ttu-id="a7ddd-192">Состояние всех обычных баз данных, используемых ядром СУБД, останется неизменным.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-192">The state of any ordinary databases in use by the database engine will remain unchanged.</span></span>

<span data-ttu-id="a7ddd-193">При сбое временная таблица не будет создана и курсор не будет возвращен.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-193">On failure, the temporary table will not be created and a cursor will not be returned.</span></span> <span data-ttu-id="a7ddd-194">Состояние временной базы данных можно изменить.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-194">The state of the temporary database can be changed.</span></span> <span data-ttu-id="a7ddd-195">Состояние всех обычных баз данных, используемых ядром СУБД, останется неизменным.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-195">The state of any ordinary databases in use by the database engine will remain unchanged.</span></span>

#### <a name="remarks"></a><span data-ttu-id="a7ddd-196">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a7ddd-196">Remarks</span></span>

<span data-ttu-id="a7ddd-197">Временные таблицы не поддерживают полное дополнение параметров определения столбца, которые обычно поддерживаются ядром СУБД.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-197">Temporary tables do not support the full complement of column definition options that are ordinarily supported by the database engine.</span></span> <span data-ttu-id="a7ddd-198">На самом деле поддерживаются только JET_bitColumnFixed и JET_bitColumnTagged.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-198">In fact, only JET_bitColumnFixed and JET_bitColumnTagged are supported.</span></span> <span data-ttu-id="a7ddd-199">Это означает, что невозможно создать столбец с автоматическим приращением, версией или многозначным столбцом во временной таблице.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-199">This means that it is not possible to create an auto-increment, version, or multi-valued column in a temporary table.</span></span> <span data-ttu-id="a7ddd-200">Наконец, столбцы депонированного обновления не поддерживаются, так как они могут использоваться только одним сеансом за раз.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-200">Finally, escrow update columns are not supported because they can only be used by one session at a time.</span></span> <span data-ttu-id="a7ddd-201">При запросе любого из этих параметров они будут проигнорированы.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-201">If any of these options are requested then they will be ignored.</span></span>

<span data-ttu-id="a7ddd-202">Временные таблицы не поддерживают значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-202">Temporary tables do not support default values.</span></span> <span data-ttu-id="a7ddd-203">Если указано определение столбца, содержащее спецификацию значения по умолчанию, то эта спецификация будет пропущена.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-203">If a column definition is provided that contains a default value specification then that specification will be ignored.</span></span>

<span data-ttu-id="a7ddd-204">Временные таблицы возвращаются вызывающему объекту в результате многих различных функций ESE.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-204">Temporary tables are returned to the caller as a result of many different ESE functions.</span></span> <span data-ttu-id="a7ddd-205">Например, [жетжетиндексинфо](./jetgetindexinfo-function.md) с набором параметров JET_IdxInfo вернет временную таблицу, содержащую список всех ключевых столбцов в заданном индексе.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-205">For example, [JetGetIndexInfo](./jetgetindexinfo-function.md) with the JET_IdxInfo option set will return a temporary table containing a list of all the key columns in a given index.</span></span> <span data-ttu-id="a7ddd-206">Временные таблицы следуют тем же правилам жизненного цикла, что и обычные временные таблицы, как описано здесь.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-206">The temporary tables follow the same lifecycle rules as ordinary temporary tables as described here.</span></span>

<span data-ttu-id="a7ddd-207">Временные таблицы также используются внутренне ядром СУБД для многих задач.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-207">Temporary tables are also used internally by the database engine for many tasks.</span></span> <span data-ttu-id="a7ddd-208">Наиболее важной из этих задач является создание индекса для существующей таблицы.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-208">The most important of these tasks is the creation of an index over an existing table.</span></span> <span data-ttu-id="a7ddd-209">Для сортировки ключей индекса, используемых для построения этого индекса, будет использоваться временная таблица.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-209">A temporary table will be used to sort the index keys that are used to construct that index.</span></span>

<span data-ttu-id="a7ddd-210">Все временные таблицы хранятся во временной базе данных.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-210">All temporary tables are stored in the temporary database.</span></span> <span data-ttu-id="a7ddd-211">Временная база данных — это специальный файл базы данных, который сохраняется в течение времени существования экземпляра ESE и удаляется при завершении работы или перезапуске этого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-211">The temporary database is a special database file that is maintained during the lifetime of an ESE instance and is deleted when that instance is shut down or restarted.</span></span> <span data-ttu-id="a7ddd-212">Расположение временной базы данных можно настроить с помощью [жетсетсистемпараметер](./jetsetsystemparameter-function.md) с [JET_paramTempPath](./temporary-database-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="a7ddd-212">The location of the temporary database can be configured using [JetSetSystemParameter](./jetsetsystemparameter-function.md) with [JET_paramTempPath](./temporary-database-parameters.md).</span></span> <span data-ttu-id="a7ddd-213">Размещение временной базы данных на диске относительно файлов журнала транзакций и файлов базы данных может быть важным, если приложение активно использует временные таблицы или часто создает индексы.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-213">Placement of the temporary database on disk relative to your transaction log files and database files may be important if your application makes heavy use of temporary tables or creates indexes frequently.</span></span>

<span data-ttu-id="a7ddd-214">Жизненный цикл временной таблицы привязан к курсорам, ссылающимся на нее.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-214">The lifecycle of a temporary table is tied to the cursors that reference it.</span></span> <span data-ttu-id="a7ddd-215">Если все курсоры, ссылающиеся на временную таблицу, закрыты, либо неявно, либо явно, то временная таблица будет удалена.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-215">If all the cursors that reference a temporary table are closed, either implicitly or explicitly, then the temporary table will be deleted.</span></span> <span data-ttu-id="a7ddd-216">Если во время транзакции создается временная таблица и эта транзакция затем откатывается назад, то временная таблица будет удалена, так как все курсоры, на которые она ссылается, будут неявно закрыты.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-216">If a temporary table is created inside a transaction and that transaction is subsequently rolled back then the temporary table will be deleted because any cursors that referenced it at this time will be implicitly closed.</span></span> <span data-ttu-id="a7ddd-217">Новые курсоры могут ссылаться на временную таблицу только с помощью [жетдупкурсор](./jetdupcursor-function.md).</span><span class="sxs-lookup"><span data-stu-id="a7ddd-217">New cursors can reference a temporary table only through the use of [JetDupCursor](./jetdupcursor-function.md).</span></span> <span data-ttu-id="a7ddd-218">В этом случае новые курсоры будут размещены на первой записи индекса временной таблицы.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-218">In this case, the new cursors will be positioned on the first index entry of the temporary table.</span></span> <span data-ttu-id="a7ddd-219">[Жетдупкурсор](./jetdupcursor-function.md) будет работать только на определенных этапах использования временной таблицы.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-219">[JetDupCursor](./jetdupcursor-function.md) will only work during certain phases of use for the temporary table.</span></span> <span data-ttu-id="a7ddd-220">Дополнительные сведения см. в разделе Примечания о возможностях курсора временной таблицы.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-220">See the remarks concerning temporary table cursor capabilities for more information.</span></span> <span data-ttu-id="a7ddd-221">Нельзя ссылаться на временную таблицу более чем за один сеанс за раз.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-221">It is not possible to reference a temporary table from more than one session at a time.</span></span>

<span data-ttu-id="a7ddd-222">**Внимание!**  В [жетдупкурсор](./jetdupcursor-function.md) есть важная проблема, влияющая на временные таблицы.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-222">**Caution**  There is an important problem in [JetDupCursor](./jetdupcursor-function.md) that affects temporary tables.</span></span> <span data-ttu-id="a7ddd-223">При попытке скопировать временную таблицу, которая находится в однонаправленном режиме, полученный курсор не будет правильно создан и будет работать неправильно.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-223">If an attempt is made to duplicate a temporary table that is in forward-only mode then the resulting cursor will not be created properly and will malfunction.</span></span> <span data-ttu-id="a7ddd-224">По-прежнему можно дублировать курсор по материализованным временным таблицам.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-224">It is still safe to duplicate a cursor over a materialized temporary table.</span></span>

<span data-ttu-id="a7ddd-225">Временный диспетчер таблиц может реализовать временную таблицу тремя способами.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-225">The temporary table manager can implement a temporary table in three ways.</span></span> <span data-ttu-id="a7ddd-226">Первый способ — сохранить таблицу в памяти.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-226">The first method is to maintain an in-memory table.</span></span> <span data-ttu-id="a7ddd-227">Эта стратегия самая высокая, но может использоваться только для небольших, простых и временных таблиц.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-227">This strategy is the fastest but can only be used for small, simple, temporary tables.</span></span> <span data-ttu-id="a7ddd-228">Второй способ — создать дисковую сортировку, которую можно использовать с помощью однонаправленного итератора.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-228">The second method is to create a disk-based sort that can be driven using a forward-only iterator.</span></span> <span data-ttu-id="a7ddd-229">Эта стратегия может использоваться только в определенных обстоятельствах и является самым быстрым способом сортировки и удаления дубликатов из очень большого набора данных.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-229">This strategy can only be used under certain circumstances and is the fastest way to sort and remove duplicates from a very large data set.</span></span> <span data-ttu-id="a7ddd-230">Третий способ — создать дерево B + во временной базе данных для хранения временной таблицы.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-230">The third method is to create a B+ Tree in the temporary database to hold the temporary table.</span></span> <span data-ttu-id="a7ddd-231">Эта стратегия является самой медленной, но наиболее универсальной и называется материализованным временным таблицей.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-231">This strategy is the slowest, but the most versatile, and is referred to as a materialized temporary table.</span></span> <span data-ttu-id="a7ddd-232">Эти стратегии можно использовать в сочетании с целью обеспечения функциональности, запрашиваемой во временной таблице.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-232">These strategies can be used in combination to ultimately achieve the functionality that is requested of the temporary table.</span></span>

<span data-ttu-id="a7ddd-233">Если временная таблица не соматериализованны, она используется главным образом в двух основных этапах.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-233">When the temporary table is not materialized then it is used primarily in two major phases.</span></span> <span data-ttu-id="a7ddd-234">Первый этап — это фаза вставки, в которой таблица заполняется начальным набором данных.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-234">The first phase is the insertion phase where the table is populated with its initial data set.</span></span> <span data-ttu-id="a7ddd-235">На этом этапе допускается только вставка данных.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-235">During this phase, only data insertion is allowed.</span></span> <span data-ttu-id="a7ddd-236">Этот этап завершается, когда выполняется попытка переместить курсор с помощью [жетмове](./jetmove-function.md) или [жетсик](./jetseek-function.md).</span><span class="sxs-lookup"><span data-stu-id="a7ddd-236">This phase ends when an attempt is made to move the cursor using [JetMove](./jetmove-function.md) or [JetSeek](./jetseek-function.md).</span></span> <span data-ttu-id="a7ddd-237">Второй этап — этап извлечения данных.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-237">The second phase is the data extraction phase.</span></span> <span data-ttu-id="a7ddd-238">На этом этапе данные, хранящиеся во временной таблице, можно извлечь в соответствии с возможностями, которые были запрошены при создании временной таблицы.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-238">During this phase, the data that is stored in the temporary table can be extracted according to the capabilities that were requested when the temporary table was created.</span></span>

<span data-ttu-id="a7ddd-239">**Возможности курсора временной таблицы**</span><span class="sxs-lookup"><span data-stu-id="a7ddd-239">**Temporary Table Cursor Capabilities**</span></span>

<span data-ttu-id="a7ddd-240">При материализации временной таблицы курсор имеет следующие возможности, но может быть дополнительно ограничен запрашиваемыми параметрами:</span><span class="sxs-lookup"><span data-stu-id="a7ddd-240">When the temporary table is materialized, the cursor has the following capabilities but might be further limited by the options that are requested:</span></span>

  - [<span data-ttu-id="a7ddd-241">жетклосетабле</span><span class="sxs-lookup"><span data-stu-id="a7ddd-241">JetCloseTable</span></span>](./jetclosetable-function.md)

  - [<span data-ttu-id="a7ddd-242">жетделете</span><span class="sxs-lookup"><span data-stu-id="a7ddd-242">JetDelete</span></span>](./jetdelete-function.md)

  - [<span data-ttu-id="a7ddd-243">жетдупкурсор</span><span class="sxs-lookup"><span data-stu-id="a7ddd-243">JetDupCursor</span></span>](./jetdupcursor-function.md)

  - [<span data-ttu-id="a7ddd-244">жетенумератеколумнс</span><span class="sxs-lookup"><span data-stu-id="a7ddd-244">JetEnumerateColumns</span></span>](./jetenumeratecolumns-function.md)

  - [<span data-ttu-id="a7ddd-245">жетескровупдате</span><span class="sxs-lookup"><span data-stu-id="a7ddd-245">JetEscrowUpdate</span></span>](./jetescrowupdate-function.md)

  - [<span data-ttu-id="a7ddd-246">жетжетбукмарк</span><span class="sxs-lookup"><span data-stu-id="a7ddd-246">JetGetBookmark</span></span>](./jetgetbookmark-function.md)

  - [<span data-ttu-id="a7ddd-247">жетжеткурсоринфо</span><span class="sxs-lookup"><span data-stu-id="a7ddd-247">JetGetCursorInfo</span></span>](./jetgetcursorinfo-function.md)

  - [<span data-ttu-id="a7ddd-248">жетжетлс</span><span class="sxs-lookup"><span data-stu-id="a7ddd-248">JetGetLS</span></span>](./jetgetls-function.md)

  - [<span data-ttu-id="a7ddd-249">жетжетрекордсизе</span><span class="sxs-lookup"><span data-stu-id="a7ddd-249">JetGetRecordSize</span></span>](./jetgetrecordsize-function.md)

  - [<span data-ttu-id="a7ddd-250">жетжеттаблеинфо</span><span class="sxs-lookup"><span data-stu-id="a7ddd-250">JetGetTableInfo</span></span>](./jetgettableinfo-function.md)

  - [<span data-ttu-id="a7ddd-251">жетготобукмарк</span><span class="sxs-lookup"><span data-stu-id="a7ddd-251">JetGotoBookmark</span></span>](./jetgotobookmark-function.md)

  - [<span data-ttu-id="a7ddd-252">жетмакекэй</span><span class="sxs-lookup"><span data-stu-id="a7ddd-252">JetMakeKey</span></span>](./jetmakekey-function.md)

  - [<span data-ttu-id="a7ddd-253">жетмове</span><span class="sxs-lookup"><span data-stu-id="a7ddd-253">JetMove</span></span>](./jetmove-function.md)

  - [<span data-ttu-id="a7ddd-254">жетпрепареупдате</span><span class="sxs-lookup"><span data-stu-id="a7ddd-254">JetPrepareUpdate</span></span>](./jetprepareupdate-function.md)

  - [<span data-ttu-id="a7ddd-255">жетретриевеколумн</span><span class="sxs-lookup"><span data-stu-id="a7ddd-255">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)

  - [<span data-ttu-id="a7ddd-256">жетретриевеколумнс</span><span class="sxs-lookup"><span data-stu-id="a7ddd-256">JetRetrieveColumns</span></span>](./jetretrievecolumns-function.md)

  - [<span data-ttu-id="a7ddd-257">жетретриевекэй</span><span class="sxs-lookup"><span data-stu-id="a7ddd-257">JetRetrieveKey</span></span>](./jetretrievekey-function.md)

  - [<span data-ttu-id="a7ddd-258">жетсик</span><span class="sxs-lookup"><span data-stu-id="a7ddd-258">JetSeek</span></span>](./jetseek-function.md)

  - [<span data-ttu-id="a7ddd-259">жетсетколумн</span><span class="sxs-lookup"><span data-stu-id="a7ddd-259">JetSetColumn</span></span>](./jetsetcolumn-function.md)

  - [<span data-ttu-id="a7ddd-260">жетсетколумнс</span><span class="sxs-lookup"><span data-stu-id="a7ddd-260">JetSetColumns</span></span>](./jetsetcolumns-function.md)

  - [<span data-ttu-id="a7ddd-261">жетсетиндексранже</span><span class="sxs-lookup"><span data-stu-id="a7ddd-261">JetSetIndexRange</span></span>](./jetsetindexrange-function.md)

  - [<span data-ttu-id="a7ddd-262">жетсетлс</span><span class="sxs-lookup"><span data-stu-id="a7ddd-262">JetSetLS</span></span>](./jetsetls-function.md)

  - [<span data-ttu-id="a7ddd-263">жетупдате</span><span class="sxs-lookup"><span data-stu-id="a7ddd-263">JetUpdate</span></span>](./jetupdate-function.md)

<span data-ttu-id="a7ddd-264">Если временная таблица не материализованный и находится на фазе вставки, то курсор имеет следующие возможности, но может быть дополнительно ограничен запрашиваемыми параметрами:</span><span class="sxs-lookup"><span data-stu-id="a7ddd-264">When the temporary table is not materialized and is in the insert phase, the cursor has the following capabilities but might be further limited by the options that are requested:</span></span>

  - [<span data-ttu-id="a7ddd-265">жетклосетабле</span><span class="sxs-lookup"><span data-stu-id="a7ddd-265">JetCloseTable</span></span>](./jetclosetable-function.md)

  - [<span data-ttu-id="a7ddd-266">жетескровупдате</span><span class="sxs-lookup"><span data-stu-id="a7ddd-266">JetEscrowUpdate</span></span>](./jetescrowupdate-function.md)

  - [<span data-ttu-id="a7ddd-267">жетмакекэй</span><span class="sxs-lookup"><span data-stu-id="a7ddd-267">JetMakeKey</span></span>](./jetmakekey-function.md)

  - [<span data-ttu-id="a7ddd-268">жетмове</span><span class="sxs-lookup"><span data-stu-id="a7ddd-268">JetMove</span></span>](./jetmove-function.md)
    
    <span data-ttu-id="a7ddd-269">**Примечание**  .  Вызывает переход на фазу извлечения.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-269">**Note**  Causes transition to the extract phase.</span></span>

  - [<span data-ttu-id="a7ddd-270">жетпрепареупдате</span><span class="sxs-lookup"><span data-stu-id="a7ddd-270">JetPrepareUpdate</span></span>](./jetprepareupdate-function.md)

  - [<span data-ttu-id="a7ddd-271">жетретриевекэй</span><span class="sxs-lookup"><span data-stu-id="a7ddd-271">JetRetrieveKey</span></span>](./jetretrievekey-function.md)

  - [<span data-ttu-id="a7ddd-272">жетсик</span><span class="sxs-lookup"><span data-stu-id="a7ddd-272">JetSeek</span></span>](./jetseek-function.md)
    
    <span data-ttu-id="a7ddd-273">**Примечание**  .  Вызывает переход на фазу извлечения.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-273">**Note**  Causes transition to the extract phase.</span></span>

  - [<span data-ttu-id="a7ddd-274">жетсетколумн</span><span class="sxs-lookup"><span data-stu-id="a7ddd-274">JetSetColumn</span></span>](./jetsetcolumn-function.md)

  - [<span data-ttu-id="a7ddd-275">жетсетколумнс</span><span class="sxs-lookup"><span data-stu-id="a7ddd-275">JetSetColumns</span></span>](./jetsetcolumns-function.md)

  - [<span data-ttu-id="a7ddd-276">жетупдате</span><span class="sxs-lookup"><span data-stu-id="a7ddd-276">JetUpdate</span></span>](./jetupdate-function.md)

<span data-ttu-id="a7ddd-277">Если временная таблица не соблюдается и находится на этапе извлечения, курсор имеет следующие возможности, но может быть дополнительно ограничен запрашиваемыми параметрами:</span><span class="sxs-lookup"><span data-stu-id="a7ddd-277">When the temporary table is not materialized and is in the extract phase, the cursor has the following capabilities but may be further limited by the options that are requested:</span></span>

  - [<span data-ttu-id="a7ddd-278">жетклосетабле</span><span class="sxs-lookup"><span data-stu-id="a7ddd-278">JetCloseTable</span></span>](./jetclosetable-function.md)

  - [<span data-ttu-id="a7ddd-279">жетдупкурсор</span><span class="sxs-lookup"><span data-stu-id="a7ddd-279">JetDupCursor</span></span>](./jetdupcursor-function.md)
    
    <span data-ttu-id="a7ddd-280">**Примечание**  .  При попытке скопировать временную таблицу, которая находится в однонаправленном режиме, полученный курсор не будет правильно создан и будет работать неправильно.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-280">**Note**  If an attempt is made to duplicate a temporary table that is in forward-only mode then the resulting cursor will not be created properly and will malfunction.</span></span> <span data-ttu-id="a7ddd-281">По-прежнему можно дублировать курсор по материализованным временным таблицам.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-281">It is still safe to duplicate a cursor over a materialized temporary table.</span></span>

  - [<span data-ttu-id="a7ddd-282">жетенумератеколумнс</span><span class="sxs-lookup"><span data-stu-id="a7ddd-282">JetEnumerateColumns</span></span>](./jetenumeratecolumns-function.md)

  - [<span data-ttu-id="a7ddd-283">жетжетбукмарк</span><span class="sxs-lookup"><span data-stu-id="a7ddd-283">JetGetBookmark</span></span>](./jetgetbookmark-function.md)

  - [<span data-ttu-id="a7ddd-284">жетжетлс</span><span class="sxs-lookup"><span data-stu-id="a7ddd-284">JetGetLS</span></span>](./jetgetls-function.md)

  - [<span data-ttu-id="a7ddd-285">жетжетрекордсизе</span><span class="sxs-lookup"><span data-stu-id="a7ddd-285">JetGetRecordSize</span></span>](./jetgetrecordsize-function.md)

  - [<span data-ttu-id="a7ddd-286">жетжеттаблеинфо</span><span class="sxs-lookup"><span data-stu-id="a7ddd-286">JetGetTableInfo</span></span>](./jetgettableinfo-function.md)

  - [<span data-ttu-id="a7ddd-287">жетготобукмарк</span><span class="sxs-lookup"><span data-stu-id="a7ddd-287">JetGotoBookmark</span></span>](./jetgotobookmark-function.md)

  - [<span data-ttu-id="a7ddd-288">жетмакекэй</span><span class="sxs-lookup"><span data-stu-id="a7ddd-288">JetMakeKey</span></span>](./jetmakekey-function.md)

  - [<span data-ttu-id="a7ddd-289">жетмове</span><span class="sxs-lookup"><span data-stu-id="a7ddd-289">JetMove</span></span>](./jetmove-function.md)

  - [<span data-ttu-id="a7ddd-290">жетретриевеколумн</span><span class="sxs-lookup"><span data-stu-id="a7ddd-290">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)

  - [<span data-ttu-id="a7ddd-291">жетретриевеколумнс</span><span class="sxs-lookup"><span data-stu-id="a7ddd-291">JetRetrieveColumns</span></span>](./jetretrievecolumns-function.md)

  - [<span data-ttu-id="a7ddd-292">жетретриевекэй</span><span class="sxs-lookup"><span data-stu-id="a7ddd-292">JetRetrieveKey</span></span>](./jetretrievekey-function.md)

  - [<span data-ttu-id="a7ddd-293">жетсик</span><span class="sxs-lookup"><span data-stu-id="a7ddd-293">JetSeek</span></span>](./jetseek-function.md)

  - [<span data-ttu-id="a7ddd-294">жетсетиндексранже</span><span class="sxs-lookup"><span data-stu-id="a7ddd-294">JetSetIndexRange</span></span>](./jetsetindexrange-function.md)

  - [<span data-ttu-id="a7ddd-295">жетсетлс</span><span class="sxs-lookup"><span data-stu-id="a7ddd-295">JetSetLS</span></span>](./jetsetls-function.md)

#### <a name="requirements"></a><span data-ttu-id="a7ddd-296">Требования</span><span class="sxs-lookup"><span data-stu-id="a7ddd-296">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a7ddd-297"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="a7ddd-297"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="a7ddd-298">Требуется Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-298">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a7ddd-299"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="a7ddd-299"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="a7ddd-300">Требуется Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-300">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a7ddd-301"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="a7ddd-301"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="a7ddd-302">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-302">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a7ddd-303"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="a7ddd-303"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="a7ddd-304">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-304">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a7ddd-305"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="a7ddd-305"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="a7ddd-306">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="a7ddd-306">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="a7ddd-307">См. также:</span><span class="sxs-lookup"><span data-stu-id="a7ddd-307">See Also</span></span>

[<span data-ttu-id="a7ddd-308">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="a7ddd-308">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="a7ddd-309">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="a7ddd-309">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="a7ddd-310">JET_OPENTEMPORARYTABLE</span><span class="sxs-lookup"><span data-stu-id="a7ddd-310">JET_OPENTEMPORARYTABLE</span></span>](./jet-opentemporarytable-structure.md)  
[<span data-ttu-id="a7ddd-311">жетклосетабле</span><span class="sxs-lookup"><span data-stu-id="a7ddd-311">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="a7ddd-312">жеткреатетаблеколумниндекс</span><span class="sxs-lookup"><span data-stu-id="a7ddd-312">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="a7ddd-313">жетдупкурсор</span><span class="sxs-lookup"><span data-stu-id="a7ddd-313">JetDupCursor</span></span>](./jetdupcursor-function.md)  
[<span data-ttu-id="a7ddd-314">жетмове</span><span class="sxs-lookup"><span data-stu-id="a7ddd-314">JetMove</span></span>](./jetmove-function.md)  
[<span data-ttu-id="a7ddd-315">жетроллбакк</span><span class="sxs-lookup"><span data-stu-id="a7ddd-315">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="a7ddd-316">жетсик</span><span class="sxs-lookup"><span data-stu-id="a7ddd-316">JetSeek</span></span>](./jetseek-function.md)  
[<span data-ttu-id="a7ddd-317">жетсетсистемпараметер</span><span class="sxs-lookup"><span data-stu-id="a7ddd-317">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="a7ddd-318">Информационные параметры</span><span class="sxs-lookup"><span data-stu-id="a7ddd-318">Informational Parameters</span></span>](./informational-parameters.md)  
[<span data-ttu-id="a7ddd-319">Параметры временной базы данных</span><span class="sxs-lookup"><span data-stu-id="a7ddd-319">Temporary Database Parameters</span></span>](./temporary-database-parameters.md)
