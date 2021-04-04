---
description: Дополнительные сведения о функции Жетсетколумндефаултвалуе
title: Функция Жетсетколумндефаултвалуе
TOCTitle: JetSetColumnDefaultValue Function
ms:assetid: 74bfaf50-6c2e-4907-b931-d50ad314b552
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269295(v=EXCHG.10)
ms:contentKeyID: 32765587
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetColumnDefaultValue
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9f50d30b2edeca716895d8dd2339d659f0e1382f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896965"
---
# <a name="jetsetcolumndefaultvalue-function"></a><span data-ttu-id="9bc7b-103">Функция Жетсетколумндефаултвалуе</span><span class="sxs-lookup"><span data-stu-id="9bc7b-103">JetSetColumnDefaultValue Function</span></span>


<span data-ttu-id="9bc7b-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="9bc7b-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetsetcolumndefaultvalue-function"></a><span data-ttu-id="9bc7b-105">Функция Жетсетколумндефаултвалуе</span><span class="sxs-lookup"><span data-stu-id="9bc7b-105">JetSetColumnDefaultValue Function</span></span>

<span data-ttu-id="9bc7b-106">Функцию **жетсетколумндефаултвалуе** можно использовать для изменения значения существующего столбца по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9bc7b-106">The **JetSetColumnDefaultValue** function can be used to change the default value of an existing column.</span></span>

```cpp
    JET_ERR JET_API JetSetColumnDefaultValue(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          JET_PCSTR szTableName,
      __in          JET_PCSTR szColumnName,
      __in          const void* pvData,
      __in          const unsigned long cbData,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="9bc7b-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="9bc7b-107">Parameters</span></span>

<span data-ttu-id="9bc7b-108">*сесид*</span><span class="sxs-lookup"><span data-stu-id="9bc7b-108">*sesid*</span></span>

<span data-ttu-id="9bc7b-109">Сеанс, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="9bc7b-109">The session to use for this call.</span></span>

<span data-ttu-id="9bc7b-110">*DBID*</span><span class="sxs-lookup"><span data-stu-id="9bc7b-110">*dbid*</span></span>

<span data-ttu-id="9bc7b-111">База данных, используемая для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="9bc7b-111">The database to use for this call.</span></span>

<span data-ttu-id="9bc7b-112">*сзтабленаме*</span><span class="sxs-lookup"><span data-stu-id="9bc7b-112">*szTableName*</span></span>

<span data-ttu-id="9bc7b-113">Имя таблицы, содержащей столбец, который будет затронут.</span><span class="sxs-lookup"><span data-stu-id="9bc7b-113">The name of the table containing the column that will be affected.</span></span>

<span data-ttu-id="9bc7b-114">*сзколумннаме*</span><span class="sxs-lookup"><span data-stu-id="9bc7b-114">*szColumnName*</span></span>

<span data-ttu-id="9bc7b-115">Имя столбца, значение по умолчанию которого будет изменено.</span><span class="sxs-lookup"><span data-stu-id="9bc7b-115">The name of the column whose default value will be changed.</span></span>

<span data-ttu-id="9bc7b-116">*пвдата*</span><span class="sxs-lookup"><span data-stu-id="9bc7b-116">*pvData*</span></span>

<span data-ttu-id="9bc7b-117">Входной буфер, содержащий новое значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9bc7b-117">The input buffer containing the new default value.</span></span>

<span data-ttu-id="9bc7b-118">*cbData*</span><span class="sxs-lookup"><span data-stu-id="9bc7b-118">*cbData*</span></span>

<span data-ttu-id="9bc7b-119">Размер входного буфера, содержащего новое значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9bc7b-119">The size of the input buffer containing the new default value.</span></span>

<span data-ttu-id="9bc7b-120">*грбит*</span><span class="sxs-lookup"><span data-stu-id="9bc7b-120">*grbit*</span></span>

<span data-ttu-id="9bc7b-121">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="9bc7b-121">Reserved for future use.</span></span>

### <a name="return-value"></a><span data-ttu-id="9bc7b-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9bc7b-122">Return Value</span></span>

<span data-ttu-id="9bc7b-123">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="9bc7b-123">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="9bc7b-124">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="9bc7b-124">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9bc7b-125">Код возврата</span><span class="sxs-lookup"><span data-stu-id="9bc7b-125">Return code</span></span></p></th>
<th><p><span data-ttu-id="9bc7b-126">Описание</span><span class="sxs-lookup"><span data-stu-id="9bc7b-126">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9bc7b-127">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="9bc7b-127">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="9bc7b-128">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="9bc7b-128">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9bc7b-129">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="9bc7b-129">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="9bc7b-130">Невозможно выполнить операцию, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</span><span class="sxs-lookup"><span data-stu-id="9bc7b-130">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9bc7b-131">JET_errColumnIllegalNull</span><span class="sxs-lookup"><span data-stu-id="9bc7b-131">JET_errColumnIllegalNull</span></span></p></td>
<td><p><span data-ttu-id="9bc7b-132">То же, что и JET_errNullInvalid.</span><span class="sxs-lookup"><span data-stu-id="9bc7b-132">Same as JET_errNullInvalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9bc7b-133">JET_errColumnInUse</span><span class="sxs-lookup"><span data-stu-id="9bc7b-133">JET_errColumnInUse</span></span></p></td>
<td><p><span data-ttu-id="9bc7b-134">Этот указанный столбец в настоящее время используется индексом.</span><span class="sxs-lookup"><span data-stu-id="9bc7b-134">This specified column is currently in use by an index.</span></span></p>
<p><span data-ttu-id="9bc7b-135"><strong>Жетсетколумндефаултвалуе</strong> не может изменить значение по умолчанию для столбца, на который указывает ссылка в определении индекса.</span><span class="sxs-lookup"><span data-stu-id="9bc7b-135"><strong>JetSetColumnDefaultValue</strong> cannot change the default value of a column that is referenced in the definition of an index.</span></span> <span data-ttu-id="9bc7b-136">Это связано с тем, что это может привести к изменению содержимого индекса.</span><span class="sxs-lookup"><span data-stu-id="9bc7b-136">This is because doing so could change the contents of the index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9bc7b-137">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="9bc7b-137">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="9bc7b-138">Указанный столбец не существует для этой таблицы.</span><span class="sxs-lookup"><span data-stu-id="9bc7b-138">This specified column does not exist for this table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9bc7b-139">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="9bc7b-139">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="9bc7b-140">Невозможно выполнить операцию, поскольку экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</span><span class="sxs-lookup"><span data-stu-id="9bc7b-140">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="9bc7b-141">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="9bc7b-141">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9bc7b-142">JET_errInvalidDatabaseId</span><span class="sxs-lookup"><span data-stu-id="9bc7b-142">JET_errInvalidDatabaseId</span></span></p></td>
<td><p><span data-ttu-id="9bc7b-143">Указан недопустимый идентификатор базы данных.</span><span class="sxs-lookup"><span data-stu-id="9bc7b-143">The specified database ID was invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9bc7b-144">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="9bc7b-144">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="9bc7b-145">Одно из указанных имен объектов недопустимо.</span><span class="sxs-lookup"><span data-stu-id="9bc7b-145">One of the specified object names was invalid.</span></span> <span data-ttu-id="9bc7b-146">Все имена объектов должны соответствовать одному и тому же набору правил.</span><span class="sxs-lookup"><span data-stu-id="9bc7b-146">All object names must conform to the same set of rules.</span></span> <span data-ttu-id="9bc7b-147">Ниже приведены эти правила.</span><span class="sxs-lookup"><span data-stu-id="9bc7b-147">These rules are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="9bc7b-148">Имена объектов должны состоять из символов ASCII.</span><span class="sxs-lookup"><span data-stu-id="9bc7b-148">Object names must be composed of ASCII characters.</span></span></p></li>
<li><p><span data-ttu-id="9bc7b-149">Имена объектов должны иметь длину по крайней мере один символ.</span><span class="sxs-lookup"><span data-stu-id="9bc7b-149">Object names must be at least one character in length.</span></span></p></li>
<li><p><span data-ttu-id="9bc7b-150">Длина имен объектов не может превышать JET_cbNameMost (64) символов.</span><span class="sxs-lookup"><span data-stu-id="9bc7b-150">Object names may not exceed JET_cbNameMost (64) characters in length.</span></span></p></li>
<li><p><span data-ttu-id="9bc7b-151">Имена объектов не могут начинаться с пробела.</span><span class="sxs-lookup"><span data-stu-id="9bc7b-151">Object names may not begin with a space.</span></span></p></li>
<li><p><span data-ttu-id="9bc7b-152">Имена объектов не могут содержать управляющие символы ASCII (0x00 – 0x1F).</span><span class="sxs-lookup"><span data-stu-id="9bc7b-152">Object names may not contain ASCII control characters (0x00 through 0x1F).</span></span></p></li>
<li><p><span data-ttu-id="9bc7b-153">Имена объектов не могут содержать восклицательный знак (!), точку (.), открывающую квадратную скобку ([) или правую квадратную скобку (]).</span><span class="sxs-lookup"><span data-stu-id="9bc7b-153">Object names may not contain an exclamation point (!), period (.), left bracket ([), or right bracket (]) character.</span></span></p></li>
<li><p><span data-ttu-id="9bc7b-154">После проверки для имени объекта будет использоваться только часть строки вплоть до первого пробела (если таковая имеется).</span><span class="sxs-lookup"><span data-stu-id="9bc7b-154">Once validated, only the portion of the string up to the first space (if any) will be used for the object name.</span></span> <span data-ttu-id="9bc7b-155">Это означает, что имена объектов не могут содержать пробелы.</span><span class="sxs-lookup"><span data-stu-id="9bc7b-155">This means that object names may not contain a space either.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9bc7b-156">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="9bc7b-156">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="9bc7b-157">Невозможно выполнить операцию, так как экземпляр, связанный с сеансом, еще не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="9bc7b-157">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9bc7b-158">JET_errNullInvalid</span><span class="sxs-lookup"><span data-stu-id="9bc7b-158">JET_errNullInvalid</span></span></p></td>
<td><p><span data-ttu-id="9bc7b-159">Не удалось установить значение NULL для этого столбца.</span><span class="sxs-lookup"><span data-stu-id="9bc7b-159">The column could not be set to NULL.</span></span> <span data-ttu-id="9bc7b-160">Это происходит для <strong>жетсетколумндефаултвалуе</strong> в следующих случаях:</span><span class="sxs-lookup"><span data-stu-id="9bc7b-160">This happens for <strong>JetSetColumnDefaultValue</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="9bc7b-161"><em>cbData</em> имеет нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="9bc7b-161"><em>cbData</em> is zero.</span></span></p></li>
<li><p><span data-ttu-id="9bc7b-162"><strong>пвдата</strong> имеет значение null.</span><span class="sxs-lookup"><span data-stu-id="9bc7b-162"><strong>pvData</strong> is NULL.</span></span></p></li>
</ul>
<p><span data-ttu-id="9bc7b-163">Поэтому невозможно установить значение по умолчанию для столбца (Back) в NULL или значение нулевой длины.</span><span class="sxs-lookup"><span data-stu-id="9bc7b-163">Therefore, it is not possible to set the default value of a column (back) to NULL or to a zero length value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9bc7b-164">JET_errObjectNotFound</span><span class="sxs-lookup"><span data-stu-id="9bc7b-164">JET_errObjectNotFound</span></span></p></td>
<td><p><span data-ttu-id="9bc7b-165">Указанная таблица не существует для этой базы данных.</span><span class="sxs-lookup"><span data-stu-id="9bc7b-165">This specified table does not exist for this database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9bc7b-166">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="9bc7b-166">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="9bc7b-167">Невозможно выполнить операцию, так как в экземпляре, связанном с сеансом, выполняется операция восстановления.</span><span class="sxs-lookup"><span data-stu-id="9bc7b-167">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9bc7b-168">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="9bc7b-168">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="9bc7b-169">Один и тот же сеанс нельзя использовать одновременно для нескольких потоков.</span><span class="sxs-lookup"><span data-stu-id="9bc7b-169">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="9bc7b-170">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="9bc7b-170">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9bc7b-171">JET_errTableInUse</span><span class="sxs-lookup"><span data-stu-id="9bc7b-171">JET_errTableInUse</span></span></p></td>
<td><p><span data-ttu-id="9bc7b-172">Указанная таблица используется другим сеансом.</span><span class="sxs-lookup"><span data-stu-id="9bc7b-172">This specified table is in use by another session.</span></span></p>
<p><span data-ttu-id="9bc7b-173"><strong>Жетсетколумндефаултвалуе</strong> требует монопольного доступа к таблице, чтобы изменить значение столбца по умолчанию для выпусков до Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="9bc7b-173"><strong>JetSetColumnDefaultValue</strong> requires exclusive access to a table in order to change the default value of the column for releases prior to Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9bc7b-174">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="9bc7b-174">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="9bc7b-175">Невозможно выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</span><span class="sxs-lookup"><span data-stu-id="9bc7b-175">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9bc7b-176">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="9bc7b-176">JET_errTransReadOnly</span></span></p></td>
<td><p><span data-ttu-id="9bc7b-177">Попытка обновления недействительна в пределах транзакции, доступной только для чтения.</span><span class="sxs-lookup"><span data-stu-id="9bc7b-177">It is illegal to attempt an update when inside the scope of a read only transaction.</span></span> <span data-ttu-id="9bc7b-178">Транзакция только для чтения — это транзакция, которая была запущена с помощью вызова <a href="gg269268(v=exchg.10).md">JetBeginTransaction2</a> с JET_bitTransactionReadOnly.</span><span class="sxs-lookup"><span data-stu-id="9bc7b-178">A read only transaction is a transaction that has been started using a call to <a href="gg269268(v=exchg.10).md">JetBeginTransaction2</a> with JET_bitTransactionReadOnly.</span></span> <span data-ttu-id="9bc7b-179">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="9bc7b-179">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9bc7b-180">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="9bc7b-180">JET_errWriteConflict</span></span></p></td>
<td><p><span data-ttu-id="9bc7b-181">Другой сеанс ранее заблокировал запись для обновления.</span><span class="sxs-lookup"><span data-stu-id="9bc7b-181">Another session has previously locked the record for update.</span></span> <span data-ttu-id="9bc7b-182">Обновление, которое попыталось этот сеанс, завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="9bc7b-182">The update attempted by this session will fail.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9bc7b-183">При успешном выполнении значение по умолчанию указанного столбца в данной таблице в заданной базе данных постоянно меняется на новое значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9bc7b-183">On success, the default value of the specified column in the given table in the given database is permanently changed to the new default value.</span></span>

<span data-ttu-id="9bc7b-184">В случае сбоя не произойдет никаких изменений в состоянии базы данных.</span><span class="sxs-lookup"><span data-stu-id="9bc7b-184">On failure, no change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="9bc7b-185">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9bc7b-185">Remarks</span></span>

<span data-ttu-id="9bc7b-186">Невозможно изменить значение по умолчанию для столбца в таблице шаблона.</span><span class="sxs-lookup"><span data-stu-id="9bc7b-186">It is not possible to change the default value of a column in a template table.</span></span>

<span data-ttu-id="9bc7b-187">Ядро СУБД автоматически усекает значение столбца по умолчанию до 255 байт для длинных текстовых и длинных двоичных столбцов.</span><span class="sxs-lookup"><span data-stu-id="9bc7b-187">The database engine will silently truncate the default value of a column to 255 bytes for long text and long binary columns.</span></span>

#### <a name="requirements"></a><span data-ttu-id="9bc7b-188">Требования</span><span class="sxs-lookup"><span data-stu-id="9bc7b-188">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9bc7b-189"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="9bc7b-189"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="9bc7b-190">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="9bc7b-190">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9bc7b-191"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="9bc7b-191"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="9bc7b-192">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="9bc7b-192">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9bc7b-193"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="9bc7b-193"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="9bc7b-194">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="9bc7b-194">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9bc7b-195"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="9bc7b-195"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="9bc7b-196">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="9bc7b-196">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9bc7b-197"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="9bc7b-197"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="9bc7b-198">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="9bc7b-198">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9bc7b-199"><strong>Юникод</strong></span><span class="sxs-lookup"><span data-stu-id="9bc7b-199"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="9bc7b-200">Реализуется как <strong>жетсетколумндефаултвалуев</strong> (Юникод) и <strong>жетсетколумндефаултвалуеа</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="9bc7b-200">Implemented as <strong>JetSetColumnDefaultValueW</strong> (Unicode) and <strong>JetSetColumnDefaultValueA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="9bc7b-201">См. также:</span><span class="sxs-lookup"><span data-stu-id="9bc7b-201">See Also</span></span>

[<span data-ttu-id="9bc7b-202">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="9bc7b-202">JET_DBID</span></span>](./jet-dbid.md)  
[<span data-ttu-id="9bc7b-203">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="9bc7b-203">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="9bc7b-204">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="9bc7b-204">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="9bc7b-205">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="9bc7b-205">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="9bc7b-206">JetBeginTransaction2</span><span class="sxs-lookup"><span data-stu-id="9bc7b-206">JetBeginTransaction2</span></span>](./jetbegintransaction2-function.md)  
[<span data-ttu-id="9bc7b-207">жетстопсервице</span><span class="sxs-lookup"><span data-stu-id="9bc7b-207">JetStopService</span></span>](./jetstopservice-function.md)
