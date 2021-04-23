---
description: Дополнительные сведения о функции Жетстопсервице
title: Функция JetStopService
TOCTitle: JetStopService Function
ms:assetid: 46aeb9ed-ee72-49cc-99e3-791a51a55b02
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269240(v=EXCHG.10)
ms:contentKeyID: 32765542
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetStopService
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1e66b4e5242710c89ca7e7964ecd0a72774b719d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711201"
---
# <a name="jetstopservice-function"></a><span data-ttu-id="a5f95-103">Функция JetStopService</span><span class="sxs-lookup"><span data-stu-id="a5f95-103">JetStopService Function</span></span>


<span data-ttu-id="a5f95-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="a5f95-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetstopservice-function"></a><span data-ttu-id="a5f95-105">Функция JetStopService</span><span class="sxs-lookup"><span data-stu-id="a5f95-105">JetStopService Function</span></span>

<span data-ttu-id="a5f95-106">Функция **жетстопсервице** готовит экземпляр к завершению.</span><span class="sxs-lookup"><span data-stu-id="a5f95-106">The **JetStopService** function prepares an instance for termination.</span></span>

<span data-ttu-id="a5f95-107">**Жетстопсервице** — это устаревший вызов, если разрешен только один экземпляр.</span><span class="sxs-lookup"><span data-stu-id="a5f95-107">**JetStopService** is the legacy call when only one instance is allowed.</span></span> <span data-ttu-id="a5f95-108">В этом случае единственным активным экземпляром является тот, который подготавливается к завершению.</span><span class="sxs-lookup"><span data-stu-id="a5f95-108">In this case, the only active instance is the one being prepared for termination.</span></span>

```cpp
    JET_ERR JET_API JetStopService(void);
```

### <a name="parameters"></a><span data-ttu-id="a5f95-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="a5f95-109">Parameters</span></span>

<span data-ttu-id="a5f95-110">У этой функции нет параметров.</span><span class="sxs-lookup"><span data-stu-id="a5f95-110">This function has no parameters.</span></span>

### <a name="return-value"></a><span data-ttu-id="a5f95-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a5f95-111">Return Value</span></span>

<span data-ttu-id="a5f95-112">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="a5f95-112">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="a5f95-113">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="a5f95-113">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a5f95-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="a5f95-114">Return code</span></span></p></th>
<th><p><span data-ttu-id="a5f95-115">Описание</span><span class="sxs-lookup"><span data-stu-id="a5f95-115">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a5f95-116">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="a5f95-116">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="a5f95-117">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="a5f95-117">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a5f95-118">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="a5f95-118">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="a5f95-119">Не ясно, какой экземпляр подготавливается к завершению при использовании <strong>жетстопсервице</strong> в режиме с несколькими экземплярами.</span><span class="sxs-lookup"><span data-stu-id="a5f95-119">It is not clear which instance to prepare for termination when using <strong>JetStopService</strong> with multiple instance mode.</span></span></p>
<p><span data-ttu-id="a5f95-120"><strong>Windows XP:</strong>  Это возвращаемое значение введено в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a5f95-120"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a5f95-121">Если эта функция выполнена, она подготавливается к будущему завершению.</span><span class="sxs-lookup"><span data-stu-id="a5f95-121">If this function succeeds, it prepares for a future termination.</span></span> <span data-ttu-id="a5f95-122">Ниже приведены шаги, предпринимаемые для подготовки к завершению работы.</span><span class="sxs-lookup"><span data-stu-id="a5f95-122">The steps taken to prepare for a termination include the following:</span></span>

  - <span data-ttu-id="a5f95-123">Останавливает оперативную дефрагментацию, если она запущена.</span><span class="sxs-lookup"><span data-stu-id="a5f95-123">Stop online defragmentation if it is running.</span></span>

  - <span data-ttu-id="a5f95-124">Запуск очистки хранилища версий.</span><span class="sxs-lookup"><span data-stu-id="a5f95-124">Start a version store clean-up.</span></span>

  - <span data-ttu-id="a5f95-125">Уменьшите глубину контрольной точки, начав с очистки «грязных» страниц в диспетчере буферов.</span><span class="sxs-lookup"><span data-stu-id="a5f95-125">Reduce the checkpoint depth by starting to flush dirty pages in the buffer manager.</span></span>

  - <span data-ttu-id="a5f95-126">Предотвращение будущих вызовов большинства функций для этого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="a5f95-126">Prevent future calls to most functions for that instance.</span></span>

<span data-ttu-id="a5f95-127">Если эта функция завершается ошибкой, не будет выполнен ни один из шагов подготовки к завершению работы экземпляра, поэтому изменение состояния экземпляра не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a5f95-127">If this function fails, none of the steps to prepare for an instance termination will be taken, so no change to the instance state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="a5f95-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a5f95-128">Remarks</span></span>

<span data-ttu-id="a5f95-129">Эта функция сокращает работу, которую экземпляр будет выполнять при завершении, но не будет завершать экземпляр.</span><span class="sxs-lookup"><span data-stu-id="a5f95-129">This function reduces the work the instance will have to do when terminated, but will not terminate the instance.</span></span> <span data-ttu-id="a5f95-130">В результате эта функция является просто оптимизацией и не является обязательной для использования.</span><span class="sxs-lookup"><span data-stu-id="a5f95-130">As a result, this function is just an optimization and is not mandatory to use.</span></span> <span data-ttu-id="a5f95-131">Обратите внимание, что объем работы, выполненной в процессе подготовки, был меньше в Windows 2000 и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a5f95-131">Note that the amount of work done in preparation was less in Windows 2000 and Windows XP.</span></span> <span data-ttu-id="a5f95-132">После выполнения функции вызов функций, которые больше не разрешены, возвратит JET_errClientRequestToStopJetService.</span><span class="sxs-lookup"><span data-stu-id="a5f95-132">Once the function succeeds, calling functions that are no longer allowed will return JET_errClientRequestToStopJetService.</span></span> <span data-ttu-id="a5f95-133">Функции, по-прежнему разрешенные после этого вызова: [жетроллбакк](./jetrollback-function.md), [жетклосетабле](./jetclosetable-function.md), [жетендсессион](./jetendsession-function.md), [жетклоседатабасе](./jetclosedatabase-function.md), [жетдетачдатабасе](./jetdetachdatabase-function.md) и [жетресетсессионконтекст](./jetresetsessioncontext-function.md).</span><span class="sxs-lookup"><span data-stu-id="a5f95-133">Functions that are still allowed after this call are: [JetRollback](./jetrollback-function.md), [JetCloseTable](./jetclosetable-function.md), [JetEndSession](./jetendsession-function.md), [JetCloseDatabase](./jetclosedatabase-function.md), [JetDetachDatabase](./jetdetachdatabase-function.md) and [JetResetSessionContext](./jetresetsessioncontext-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="a5f95-134">Требования</span><span class="sxs-lookup"><span data-stu-id="a5f95-134">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a5f95-135"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="a5f95-135"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="a5f95-136">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="a5f95-136">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a5f95-137"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="a5f95-137"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="a5f95-138">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="a5f95-138">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a5f95-139"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="a5f95-139"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="a5f95-140">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="a5f95-140">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a5f95-141"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="a5f95-141"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="a5f95-142">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="a5f95-142">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a5f95-143"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="a5f95-143"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="a5f95-144">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="a5f95-144">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="a5f95-145">См. также:</span><span class="sxs-lookup"><span data-stu-id="a5f95-145">See Also</span></span>

[<span data-ttu-id="a5f95-146">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="a5f95-146">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="a5f95-147">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="a5f95-147">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="a5f95-148">жетклоседатабасе</span><span class="sxs-lookup"><span data-stu-id="a5f95-148">JetCloseDatabase</span></span>](./jetclosedatabase-function.md)  
[<span data-ttu-id="a5f95-149">жетклосетабле</span><span class="sxs-lookup"><span data-stu-id="a5f95-149">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="a5f95-150">жетдетачдатабасе</span><span class="sxs-lookup"><span data-stu-id="a5f95-150">JetDetachDatabase</span></span>](./jetdetachdatabase-function.md)  
[<span data-ttu-id="a5f95-151">жетендсессион</span><span class="sxs-lookup"><span data-stu-id="a5f95-151">JetEndSession</span></span>](./jetendsession-function.md)  
[<span data-ttu-id="a5f95-152">жетресетсессионконтекст</span><span class="sxs-lookup"><span data-stu-id="a5f95-152">JetResetSessionContext</span></span>](./jetresetsessioncontext-function.md)  
[<span data-ttu-id="a5f95-153">жетроллбакк</span><span class="sxs-lookup"><span data-stu-id="a5f95-153">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="a5f95-154">жеттерм</span><span class="sxs-lookup"><span data-stu-id="a5f95-154">JetTerm</span></span>](./jetterm-function.md)  
[<span data-ttu-id="a5f95-155">JetTerm2</span><span class="sxs-lookup"><span data-stu-id="a5f95-155">JetTerm2</span></span>](./jetterm2-function.md)
