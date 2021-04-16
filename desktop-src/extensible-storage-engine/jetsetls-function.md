---
description: Дополнительные сведения о функции Жетсетлс
title: Функция JetSetLS
TOCTitle: JetSetLS Function
ms:assetid: 4fc77e09-7173-42e8-9dfd-9a8d8de2fb9b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269243(v=EXCHG.10)
ms:contentKeyID: 32765545
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetLS
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7ae1c68a039c11cd8a3f9b1299494c5057513caa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540767"
---
# <a name="jetsetls-function"></a><span data-ttu-id="f4acf-103">Функция JetSetLS</span><span class="sxs-lookup"><span data-stu-id="f4acf-103">JetSetLS Function</span></span>


<span data-ttu-id="f4acf-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="f4acf-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetsetls-function"></a><span data-ttu-id="f4acf-105">Функция JetSetLS</span><span class="sxs-lookup"><span data-stu-id="f4acf-105">JetSetLS Function</span></span>

<span data-ttu-id="f4acf-106">Функция **жетсетлс** позволяет приложению связать описатель контекста, известный как локальное хранилище, с курсором или с таблицей, связанной с этим курсором.</span><span class="sxs-lookup"><span data-stu-id="f4acf-106">The **JetSetLS** function enables the application to associate a context handle known as Local Storage with a cursor or the table associated with that cursor.</span></span> <span data-ttu-id="f4acf-107">Этот обработчик контекста может использоваться приложением для хранения вспомогательных данных, связанных с курсором или таблицей.</span><span class="sxs-lookup"><span data-stu-id="f4acf-107">This context handle can be used by the application to store auxiliary data that is associated with a cursor or table.</span></span> <span data-ttu-id="f4acf-108">После этого приложение будет уведомлено с помощью обратного вызова времени выполнения, когда должен быть освобожден обработчик контекста.</span><span class="sxs-lookup"><span data-stu-id="f4acf-108">The application is later notified using a runtime callback when the context handle must be released.</span></span> <span data-ttu-id="f4acf-109">Это дает возможность связать динамически выделенное состояние с курсором или таблицей.</span><span class="sxs-lookup"><span data-stu-id="f4acf-109">This makes it possible to associate dynamically allocated state with a cursor or table.</span></span>

<span data-ttu-id="f4acf-110">**Windows XP:**  **Жетсетлс** появился в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f4acf-110">**Windows XP:**  **JetSetLS** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetSetLS(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_LS ls,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="f4acf-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="f4acf-111">Parameters</span></span>

<span data-ttu-id="f4acf-112">*сесид*</span><span class="sxs-lookup"><span data-stu-id="f4acf-112">*sesid*</span></span>

<span data-ttu-id="f4acf-113">Сеанс, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="f4acf-113">The session to use for this call.</span></span>

<span data-ttu-id="f4acf-114">*TableID*</span><span class="sxs-lookup"><span data-stu-id="f4acf-114">*tableid*</span></span>

<span data-ttu-id="f4acf-115">Курсор, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="f4acf-115">The cursor to use for this call.</span></span>

<span data-ttu-id="f4acf-116">*ls*</span><span class="sxs-lookup"><span data-stu-id="f4acf-116">*ls*</span></span>

<span data-ttu-id="f4acf-117">Контекстный обработчик, связываемый с курсором или таблицей.</span><span class="sxs-lookup"><span data-stu-id="f4acf-117">The context handle to be associated with the cursor or table.</span></span>

<span data-ttu-id="f4acf-118">Если указано JET_bitLSReset, фактическое значение этого параметра игнорируется, и используется JET_LSNil.</span><span class="sxs-lookup"><span data-stu-id="f4acf-118">When JET_bitLSReset is specified then the actual value of this parameter is ignored and JET_LSNil is used.</span></span>

<span data-ttu-id="f4acf-119">*грбит*</span><span class="sxs-lookup"><span data-stu-id="f4acf-119">*grbit*</span></span>

<span data-ttu-id="f4acf-120">Группа битов, содержащая параметры, которые должны использоваться для этого вызова, включая ноль или более следующих значений.</span><span class="sxs-lookup"><span data-stu-id="f4acf-120">A group of bits that contain the options to be used for this call, which include zero or more of the following.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f4acf-121">Значение</span><span class="sxs-lookup"><span data-stu-id="f4acf-121">Value</span></span></p></th>
<th><p><span data-ttu-id="f4acf-122">Значение</span><span class="sxs-lookup"><span data-stu-id="f4acf-122">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f4acf-123">JET_bitLSCursor</span><span class="sxs-lookup"><span data-stu-id="f4acf-123">JET_bitLSCursor</span></span></p></td>
<td><p><span data-ttu-id="f4acf-124">Этот параметр указывает, что маркер контекста должен быть связан с данным курсором.</span><span class="sxs-lookup"><span data-stu-id="f4acf-124">This option indicates that the context handle should be associated with the given cursor.</span></span></p>
<p><span data-ttu-id="f4acf-125">Если не указано ни JET_bitLSCursor, ни JET_bitLSTable, предполагается JET_bitLSCursor.</span><span class="sxs-lookup"><span data-stu-id="f4acf-125">If neither JET_bitLSCursor nor JET_bitLSTable is specified then JET_bitLSCursor is presumed.</span></span></p>
<p><span data-ttu-id="f4acf-126">Использование этого параметра с JET_bitLSTable недопустимо.</span><span class="sxs-lookup"><span data-stu-id="f4acf-126">It is illegal to use this option with JET_bitLSTable.</span></span> <span data-ttu-id="f4acf-127">Операция завершится ошибкой с JET_errInvalidgrbit при попытке.</span><span class="sxs-lookup"><span data-stu-id="f4acf-127">The operation will fail with JET_errInvalidgrbit if this is attempted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4acf-128">JET_bitLSReset</span><span class="sxs-lookup"><span data-stu-id="f4acf-128">JET_bitLSReset</span></span></p></td>
<td><p><span data-ttu-id="f4acf-129">Этот параметр указывает, что указанный обработчик контекста должен игнорироваться, а контекстный маркер для выбранного объекта должен быть сброшен в JET_LSNil.</span><span class="sxs-lookup"><span data-stu-id="f4acf-129">This option indicates that the specified context handle should be ignored and that the context handle for the chosen object should be reset to JET_LSNil.</span></span></p>
<p><span data-ttu-id="f4acf-130">Важно отметить, что это действие не приведет к обратному вызову для очистки предыдущего значения маркера контекста для выбранного объекта.</span><span class="sxs-lookup"><span data-stu-id="f4acf-130">It is important to note that this action will not result in a callback to cleanup the previous value of the context handle for the chosen object.</span></span> <span data-ttu-id="f4acf-131">Правильная очистка предыдущего маркера контекста может быть достигнута с помощью <a href="gg269234(v=exchg.10).md">жетжетлс</a> с JET_bitLSReset.</span><span class="sxs-lookup"><span data-stu-id="f4acf-131">Proper cleanup of the previous context handle can be achieved using <a href="gg269234(v=exchg.10).md">JetGetLS</a> with JET_bitLSReset.</span></span> <span data-ttu-id="f4acf-132">Дополнительные сведения см. в разделе <a href="gg269234(v=exchg.10).md">жетжетлс</a> .</span><span class="sxs-lookup"><span data-stu-id="f4acf-132">See <a href="gg269234(v=exchg.10).md">JetGetLS</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f4acf-133">JET_bitLSTable</span><span class="sxs-lookup"><span data-stu-id="f4acf-133">JET_bitLSTable</span></span></p></td>
<td><p><span data-ttu-id="f4acf-134">Этот параметр указывает, что маркер контекста должен быть связан с таблицей, связанной с данным курсором.</span><span class="sxs-lookup"><span data-stu-id="f4acf-134">This option indicates that the context handle should be associated with the table associated with the given cursor.</span></span></p>
<p><span data-ttu-id="f4acf-135">Использование этого параметра с JET_bitLSCursor недопустимо.</span><span class="sxs-lookup"><span data-stu-id="f4acf-135">It is illegal to use this option with JET_bitLSCursor.</span></span> <span data-ttu-id="f4acf-136">Операция завершится ошибкой с JET_errInvalidgrbit при попытке.</span><span class="sxs-lookup"><span data-stu-id="f4acf-136">The operation will fail with JET_errInvalidgrbit if this is attempted.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="f4acf-137">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f4acf-137">Return Value</span></span>

<span data-ttu-id="f4acf-138">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="f4acf-138">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="f4acf-139">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="f4acf-139">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f4acf-140">Код возврата</span><span class="sxs-lookup"><span data-stu-id="f4acf-140">Return code</span></span></p></th>
<th><p><span data-ttu-id="f4acf-141">Описание</span><span class="sxs-lookup"><span data-stu-id="f4acf-141">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f4acf-142">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="f4acf-142">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="f4acf-143">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="f4acf-143">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4acf-144">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="f4acf-144">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="f4acf-145">Невозможно выполнить операцию, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</span><span class="sxs-lookup"><span data-stu-id="f4acf-145">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f4acf-146">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="f4acf-146">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="f4acf-147">Один из запрошенных параметров недопустим, используется неправильно или не реализован.</span><span class="sxs-lookup"><span data-stu-id="f4acf-147">One of the options requested was invalid, used incorrectly, or not implemented.</span></span> <span data-ttu-id="f4acf-148">Это может произойти для <strong>жетсетлс</strong> , если одновременно указаны значения JET_bitLSCursor и JET_bitLSTable.</span><span class="sxs-lookup"><span data-stu-id="f4acf-148">This can happen for <strong>JetSetLS</strong> when JET_bitLSCursor and JET_bitLSTable are both specified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4acf-149">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="f4acf-149">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="f4acf-150">Невозможно выполнить операцию, поскольку экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</span><span class="sxs-lookup"><span data-stu-id="f4acf-150">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="f4acf-151">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="f4acf-151">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f4acf-152">JET_errLSAlreadySet</span><span class="sxs-lookup"><span data-stu-id="f4acf-152">JET_errLSAlreadySet</span></span></p></td>
<td><p><span data-ttu-id="f4acf-153">Данный обработчик контекста не может быть связан с запрошенным объектом, так как с ним уже связан обработчик контекста.</span><span class="sxs-lookup"><span data-stu-id="f4acf-153">The given context handle could not be associated with the requested object because it already had a context handle associated with it.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4acf-154">JET_errLSCallbackNotSpecified</span><span class="sxs-lookup"><span data-stu-id="f4acf-154">JET_errLSCallbackNotSpecified</span></span></p></td>
<td><p><span data-ttu-id="f4acf-155">Данный обработчик контекста не может быть связан с запрошенным объектом, так как обратный вызов времени выполнения не был настроен для экземпляра, связанного с сеансом.</span><span class="sxs-lookup"><span data-stu-id="f4acf-155">The given context handle could not be associated with the requested object because the runtime callback has not been configured for the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f4acf-156">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="f4acf-156">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="f4acf-157">Невозможно выполнить операцию, так как экземпляр, связанный с сеансом, еще не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="f4acf-157">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4acf-158">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="f4acf-158">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="f4acf-159">Невозможно выполнить операцию, так как в экземпляре, связанном с сеансом, выполняется операция восстановления.</span><span class="sxs-lookup"><span data-stu-id="f4acf-159">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f4acf-160">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="f4acf-160">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="f4acf-161">Невозможно выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</span><span class="sxs-lookup"><span data-stu-id="f4acf-161">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f4acf-162">При успешном выполнении указанный обработчик контекста успешно связан с запрошенным объектом.</span><span class="sxs-lookup"><span data-stu-id="f4acf-162">On success, the given context handle was successfully associated with the requested object.</span></span> <span data-ttu-id="f4acf-163">Изменение состояния базы данных не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f4acf-163">No change to the database state will occur.</span></span>

<span data-ttu-id="f4acf-164">В случае сбоя не произошло изменение состояния запрошенного объекта.</span><span class="sxs-lookup"><span data-stu-id="f4acf-164">On failure, no change to the state of the requested object has occurred.</span></span> <span data-ttu-id="f4acf-165">Изменение состояния базы данных не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f4acf-165">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="f4acf-166">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f4acf-166">Remarks</span></span>

<span data-ttu-id="f4acf-167">Локальное хранилище для курсора или таблицы следует просматривать как временный кэш.</span><span class="sxs-lookup"><span data-stu-id="f4acf-167">The Local Storage for a cursor or table should be viewed as a volatile cache.</span></span> <span data-ttu-id="f4acf-168">Приложение должно сначала попытаться получить маркер контекста с помощью [жетжетлс](./jetgetls-function.md).</span><span class="sxs-lookup"><span data-stu-id="f4acf-168">The application should first try to retrieve the context handle using [JetGetLS](./jetgetls-function.md).</span></span> <span data-ttu-id="f4acf-169">Если значение не задано (то есть JET_LSNil), приложение должно создать новый контекст и загрузить его в кэш с помощью **жетсетлс**.</span><span class="sxs-lookup"><span data-stu-id="f4acf-169">If the value is not set (that is it is JET_LSNil) then the application should create a new context and load it into the cache using **JetSetLS**.</span></span> <span data-ttu-id="f4acf-170">Приложение может очистить кэш с помощью вызова [жетжетлс](./jetgetls-function.md) с JET_bitLSReset.</span><span class="sxs-lookup"><span data-stu-id="f4acf-170">The application can purge the cache using a call to [JetGetLS](./jetgetls-function.md) with JET_bitLSReset.</span></span> <span data-ttu-id="f4acf-171">Если ядро СУБД удаляет кэш, будет создан обратный вызов времени выполнения, чтобы дать приложению возможность очистить этот контекст.</span><span class="sxs-lookup"><span data-stu-id="f4acf-171">If the database engine purges the cache then a runtime callback will be generated to give the application a chance to cleanup that context.</span></span> <span data-ttu-id="f4acf-172">Тип обратного вызова будет JET_cbtypFreeCursorLS для обработчика контекста, связанного с курсором, и JET_cbtypFreeTableLS для обработчика контекста, связанного с таблицей.</span><span class="sxs-lookup"><span data-stu-id="f4acf-172">The callback type will be JET_cbtypFreeCursorLS for a context handle associated with a cursor and JET_cbtypFreeTableLS for a context handle associated with a table.</span></span> <span data-ttu-id="f4acf-173">В любом случае маркер контекста будет передан как pvArg1.</span><span class="sxs-lookup"><span data-stu-id="f4acf-173">In either case, the context handle will be passed as pvArg1.</span></span> <span data-ttu-id="f4acf-174">Дополнительные сведения см. в разделе [JET_CALLBACK](./jet-callback-callback-function.md) .</span><span class="sxs-lookup"><span data-stu-id="f4acf-174">See [JET_CALLBACK](./jet-callback-callback-function.md) for more information.</span></span>

<span data-ttu-id="f4acf-175">Необходимо правильно настроить обратный вызов среды выполнения для экземпляра, связанного с данным сеансом, прежде чем можно будет использовать локальное хранилище.</span><span class="sxs-lookup"><span data-stu-id="f4acf-175">The runtime callback must be properly configured for the instance associated with the given session before Local Storage can be used.</span></span> <span data-ttu-id="f4acf-176">Этот обратный вызов можно задать с помощью [жетсетсистемпараметер](./jetsetsystemparameter-function.md) с [JET_paramRuntimeCallback](./callback-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="f4acf-176">This callback can be set using [JetSetSystemParameter](./jetsetsystemparameter-function.md) with [JET_paramRuntimeCallback](./callback-parameters.md).</span></span> <span data-ttu-id="f4acf-177">Дополнительные сведения см. в статье [жетсетсистемпараметер](./jetsetsystemparameter-function.md) и [JET_paramRuntimeCallback](./callback-parameters.md) в разделе Системные параметры.</span><span class="sxs-lookup"><span data-stu-id="f4acf-177">See [JetSetSystemParameter](./jetsetsystemparameter-function.md) and [JET_paramRuntimeCallback](./callback-parameters.md) in System Parameters for more information.</span></span>

#### <a name="requirements"></a><span data-ttu-id="f4acf-178">Требования</span><span class="sxs-lookup"><span data-stu-id="f4acf-178">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f4acf-179"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="f4acf-179"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="f4acf-180">Требуется Windows Vista или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f4acf-180">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4acf-181"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="f4acf-181"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="f4acf-182">Требуется Windows Server 2008 или Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="f4acf-182">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f4acf-183"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="f4acf-183"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="f4acf-184">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="f4acf-184">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4acf-185"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="f4acf-185"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="f4acf-186">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="f4acf-186">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f4acf-187"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="f4acf-187"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="f4acf-188">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="f4acf-188">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="f4acf-189">См. также:</span><span class="sxs-lookup"><span data-stu-id="f4acf-189">See Also</span></span>

[<span data-ttu-id="f4acf-190">JET_CALLBACK</span><span class="sxs-lookup"><span data-stu-id="f4acf-190">JET_CALLBACK</span></span>](./jet-callback-callback-function.md)  
[<span data-ttu-id="f4acf-191">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="f4acf-191">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="f4acf-192">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="f4acf-192">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="f4acf-193">JET_LS</span><span class="sxs-lookup"><span data-stu-id="f4acf-193">JET_LS</span></span>](./jet-ls.md)  
[<span data-ttu-id="f4acf-194">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="f4acf-194">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="f4acf-195">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="f4acf-195">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="f4acf-196">жетжетлс</span><span class="sxs-lookup"><span data-stu-id="f4acf-196">JetGetLS</span></span>](./jetgetls-function.md)  
[<span data-ttu-id="f4acf-197">жетсетсистемпараметер</span><span class="sxs-lookup"><span data-stu-id="f4acf-197">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="f4acf-198">Системные параметры</span><span class="sxs-lookup"><span data-stu-id="f4acf-198">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
