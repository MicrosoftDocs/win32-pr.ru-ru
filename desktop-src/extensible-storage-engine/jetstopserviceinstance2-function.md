---
description: Дополнительные сведения о функции JetStopServiceInstance2
title: Функция JetStopServiceInstance2
TOCTitle: JetStopServiceInstance2 Function
ms:assetid: ac021e13-ec83-42eb-9aef-a906d7a7ed39
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835046(v=EXCHG.10)
ms:contentKeyID: 49894668
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetStopServiceInstance2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5029e2cf45ec91d0282f32491895a24b32e6259e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810360"
---
# <a name="jetstopserviceinstance2-function"></a><span data-ttu-id="35b12-103">Функция JetStopServiceInstance2</span><span class="sxs-lookup"><span data-stu-id="35b12-103">JetStopServiceInstance2 Function</span></span>


<span data-ttu-id="35b12-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="35b12-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="35b12-105">Функция **JetStopServiceInstance2** готовит экземпляр перед приостановкой и готовит экземпляр после возобновления.</span><span class="sxs-lookup"><span data-stu-id="35b12-105">The **JetStopServiceInstance2** function prepares an instance prior to Suspend, and prepares an instance after Resume.</span></span> <span data-ttu-id="35b12-106">Приостановка и возобновление являются состояниями выполнения модели жизненного цикла приложения Магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="35b12-106">Suspend and Resume are execution states of the Windows Store App lifecycle model.</span></span>

<span data-ttu-id="35b12-107">Функция **JetStopServiceInstance2** была введена в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="35b12-107">The **JetStopServiceInstance2** function was introduced in Windows 8.</span></span>

``` c++
JET_ERR JET_API JetStopServiceInstance2(
  _In_          JET_INSTANCE       instance
  _In_          const JET_GRBIT    grbit
);
```

### <a name="parameters"></a><span data-ttu-id="35b12-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="35b12-108">Parameters</span></span>

<span data-ttu-id="35b12-109">*вхождение*</span><span class="sxs-lookup"><span data-stu-id="35b12-109">*instance*</span></span>

<span data-ttu-id="35b12-110">Целевой экземпляр.</span><span class="sxs-lookup"><span data-stu-id="35b12-110">The target instance.</span></span> <span data-ttu-id="35b12-111">Тип данных **JET_INSTANCE** является обработчиком экземпляра базы данных, который используется для вызова API Jet.</span><span class="sxs-lookup"><span data-stu-id="35b12-111">The **JET_INSTANCE** data type is a handle to the instance of the database to use for a call to the JET API.</span></span> <span data-ttu-id="35b12-112">Этот маркер получается при создании экземпляра базы данных путем вызова функций [жеткреатеинстанце](./jetcreateinstance-function.md), [JetCreateInstance2](./jetcreateinstance2-function.md), [жетинит](./jetinit-function.md)или [JetInit2](./jetinit2-function.md) .</span><span class="sxs-lookup"><span data-stu-id="35b12-112">This handle is obtained when you create an instance of the database by calling the [JetCreateInstance](./jetcreateinstance-function.md), [JetCreateInstance2](./jetcreateinstance2-function.md), [JetInit](./jetinit-function.md), or [JetInit2](./jetinit2-function.md) functions.</span></span>

<span data-ttu-id="35b12-113">*грбит*</span><span class="sxs-lookup"><span data-stu-id="35b12-113">*grbit*</span></span>

<span data-ttu-id="35b12-114">Группа битов, задающая одно или несколько значений, перечисленных и определенных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="35b12-114">A group of bits that specifies one or more of the values listed and defined in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="35b12-115">Значение</span><span class="sxs-lookup"><span data-stu-id="35b12-115">Value</span></span></p></th>
<th><p><span data-ttu-id="35b12-116">Описание</span><span class="sxs-lookup"><span data-stu-id="35b12-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="35b12-117">JET_bitStopServiceAll</span><span class="sxs-lookup"><span data-stu-id="35b12-117">JET_bitStopServiceAll</span></span></p></td>
<td><p><span data-ttu-id="35b12-118">Останавливает все службы расширенного подсистемы хранилища (ESE) для указанного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="35b12-118">Stops all Extensible Storage Engine (ESE) services for the specified instance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35b12-119">JET_bitStopServiceBackgroundUserTasks</span><span class="sxs-lookup"><span data-stu-id="35b12-119">JET_bitStopServiceBackgroundUserTasks</span></span></p></td>
<td><p><span data-ttu-id="35b12-120">Останавливает Перезапускаемые клиентские задачи фонового обслуживания (например, дефрагментацию дерева B +).</span><span class="sxs-lookup"><span data-stu-id="35b12-120">Stops restartable client-specified background maintenance tasks (B+ Tree Defrag, for example).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35b12-121">JET_bitStopServiceQuiesceCaches</span><span class="sxs-lookup"><span data-stu-id="35b12-121">JET_bitStopServiceQuiesceCaches</span></span></p></td>
<td><p><span data-ttu-id="35b12-122">Куиесцес все "грязные" кэши на диск.</span><span class="sxs-lookup"><span data-stu-id="35b12-122">Quiesces all dirty caches to disk.</span></span> <span data-ttu-id="35b12-123">Это значение является асинхронным и может быть отменено.</span><span class="sxs-lookup"><span data-stu-id="35b12-123">This value is asynchronous and can be canceled.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35b12-124">JET_bitStopServiceResume</span><span class="sxs-lookup"><span data-stu-id="35b12-124">JET_bitStopServiceResume</span></span></p></td>
<td><p><span data-ttu-id="35b12-125">Возобновляет ранее выданные операции выхода из эксплуатации; то есть он перезапускает службу.</span><span class="sxs-lookup"><span data-stu-id="35b12-125">Resumes previously issued StopService operations; that is, it restarts the service.</span></span> <span data-ttu-id="35b12-126">Это значение можно сочетать с параметром <em>грбитс</em> , чтобы возобновить работу конкретных служб, или с JET_bitStopServiceAll, чтобы возобновить работу всех ранее остановленных служб.</span><span class="sxs-lookup"><span data-stu-id="35b12-126">This value can be combined with the <em>grbits</em> parameter to resume specific services, or with JET_bitStopServiceAll to Resume all previously stopped services.</span></span> <span data-ttu-id="35b12-127">Этот бит можно использовать только для возобновления Стопсервицебаккграундусертаскс и JET_bitStopServiceQuiesceCaches.</span><span class="sxs-lookup"><span data-stu-id="35b12-127">This bit can only be used to resume StopServiceBackgroundUserTasks and JET_bitStopServiceQuiesceCaches.</span></span> <span data-ttu-id="35b12-128">Если ранее было вызвано с JET_bitStopServiceAll, попытка использовать JET_bitStopServiceResume завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="35b12-128">If you previously called with JET_bitStopServiceAll, an attempt to use JET_bitStopServiceResume will fail.</span></span> <span data-ttu-id="35b12-129">Если второй шаг возобновления не вызывается, это приведет к снижению производительности приложения.</span><span class="sxs-lookup"><span data-stu-id="35b12-129">If the second resume step does not get called, the application will have degraded performance.</span></span> <span data-ttu-id="35b12-130">В этом случае контрольная точка остается в нулевом виде.</span><span class="sxs-lookup"><span data-stu-id="35b12-130">In this situation the checkpoint is kept at zero.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="35b12-131">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="35b12-131">Return value</span></span>

<span data-ttu-id="35b12-132">Эта функция возвращает [JET_ERR](./jet-err.md) тип данных с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="35b12-132">This function returns the [JET_ERR](./jet-err.md) data type with one of the following return codes.</span></span> <span data-ttu-id="35b12-133">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="35b12-133">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="35b12-134">Код возврата</span><span class="sxs-lookup"><span data-stu-id="35b12-134">Return code</span></span></p></th>
<th><p><span data-ttu-id="35b12-135">Описание</span><span class="sxs-lookup"><span data-stu-id="35b12-135">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="35b12-136">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="35b12-136">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="35b12-137">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="35b12-137">The operation completed successfully.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="35b12-138">Комментарии</span><span class="sxs-lookup"><span data-stu-id="35b12-138">Remarks</span></span>

<span data-ttu-id="35b12-139">Эта функция позволяет приложению JET перевести кэш базы данных в состояние чистого или почти чистого состояния (при простом вводе-выпуске операционной системы), например, если приложение должно быть завершено, восстановление было бы быстрым.</span><span class="sxs-lookup"><span data-stu-id="35b12-139">This function allows a JET application to move the database cache to a clean or nearly clean state (with the operating system I/O idle), such that if the application were to be terminated, recovery would be quick.</span></span> <span data-ttu-id="35b12-140">Этот подход предпочтительнее, чем завершение работы с JET, путем вызова функций [жеттерм](./jetterm-function.md) или [жетдетачдатабасе](./jetdetachdatabase-function.md) , чтобы в более распространенном сценарии приложение было просто неприостановленным, а позднее приложение получило весь кэш и готово к работе как можно скорее.</span><span class="sxs-lookup"><span data-stu-id="35b12-140">This approach is preferred over terminating JET by calling the [JetTerm](./jetterm-function.md) or [JetDetachDatabase](./jetdetachdatabase-function.md) functions, so that in the more common scenario, the application is just unsuspended, and later the application has the whole cache and is ready to go as soon as possible.</span></span>

<span data-ttu-id="35b12-141">Если эта функция выполнена, она подготавливает кэш базы данных для приближающейся приостановки.</span><span class="sxs-lookup"><span data-stu-id="35b12-141">If this function succeeds, it prepares the database cache for an imminent suspension.</span></span> <span data-ttu-id="35b12-142">Эта функция очереди работает в фоновом рабочем потоке и немедленно возвращает вызывающему объекту.</span><span class="sxs-lookup"><span data-stu-id="35b12-142">This function queues work to a background worker thread and returns to the caller immediately.</span></span> <span data-ttu-id="35b12-143">Функция должна вызываться на основе PLM Висибилитинотице, а не вызывать из обработчика событий приостановки приложения, чтобы гарантировать, что у JET есть время на очистку грязных буферов перед тем, как PLM приостанавливает работу или завершает процесс.</span><span class="sxs-lookup"><span data-stu-id="35b12-143">The function should be called based on the PLM VisibilityNotice as opposed to calling from the application's suspension event handler to ensure that JET has time to flush dirty buffers before PLM suspends/terminates the process.</span></span> <span data-ttu-id="35b12-144">На внутреннем уровне JET запускает немедленную отправку обслуживания контрольных точек при изменении конфигурации (обновление контрольной точки или новый бит замораживания кэша).</span><span class="sxs-lookup"><span data-stu-id="35b12-144">Internally, JET triggers an immediate dispatch of checkpoint maintenance upon configuration change (either checkpoint update or this new quiesce caches bit).</span></span> <span data-ttu-id="35b12-145">Дополнительные сведения о событиях Висибилитинотице см. в разделе [класс висибилитичанжедевентаргс](/uwp/api/windows.ui.core.visibilitychangedeventargs).</span><span class="sxs-lookup"><span data-stu-id="35b12-145">For more information about VisibilityNotice events, see [VisibilityChangedEventArgs class](/uwp/api/windows.ui.core.visibilitychangedeventargs).</span></span>

<span data-ttu-id="35b12-146">Эта функция должна вызываться дважды.</span><span class="sxs-lookup"><span data-stu-id="35b12-146">This function must be called twice.</span></span> <span data-ttu-id="35b12-147">Он вызывается после того, как приложение получает уведомление о приостановке от операционной системы, но до того, как приложение будет приостановлено.</span><span class="sxs-lookup"><span data-stu-id="35b12-147">It is called after the application receives the suspension notice from the operating system, but before the application has been suspended.</span></span> <span data-ttu-id="35b12-148">Затем он вызывается снова после того, как операционная система возобновит работу приложения.</span><span class="sxs-lookup"><span data-stu-id="35b12-148">Then it is called again after the operating system resumes the application.</span></span> <span data-ttu-id="35b12-149">Пример:</span><span class="sxs-lookup"><span data-stu-id="35b12-149">For example:</span></span>

<span data-ttu-id="35b12-150">При вызове для приостановки: JET_ERR JET_API JetStopServiceInstance2 (экземпляр, JET_bitStopServiceQuiesceCaches);</span><span class="sxs-lookup"><span data-stu-id="35b12-150">When called to Suspend: JET_ERR JET_API JetStopServiceInstance2( instance, JET_bitStopServiceQuiesceCaches);</span></span>

<span data-ttu-id="35b12-151">При возобновлении: JET_ERR JET_API JetStopServiceInstance2 (экземпляр, JET_bitStopServiceQuiesceCaches | JET_bitStopServiceResume);</span><span class="sxs-lookup"><span data-stu-id="35b12-151">When Resumed: JET_ERR JET_API JetStopServiceInstance2( instance, JET_bitStopServiceQuiesceCaches|JET_bitStopServiceResume );</span></span>

#### <a name="requirements"></a><span data-ttu-id="35b12-152">Требования</span><span class="sxs-lookup"><span data-stu-id="35b12-152">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="35b12-153"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="35b12-153"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="35b12-154">Требуется Windows 8.</span><span class="sxs-lookup"><span data-stu-id="35b12-154">Requires Windows 8.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35b12-155"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="35b12-155"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="35b12-156">Требуется Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="35b12-156">Requires Windows Server 2012.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35b12-157"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="35b12-157"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="35b12-158">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="35b12-158">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35b12-159"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="35b12-159"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="35b12-160">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="35b12-160">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35b12-161"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="35b12-161"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="35b12-162">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="35b12-162">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="35b12-163">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="35b12-163">See also</span></span>

[<span data-ttu-id="35b12-164">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="35b12-164">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="35b12-165">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="35b12-165">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="35b12-166">жетклоседатабасе</span><span class="sxs-lookup"><span data-stu-id="35b12-166">JetCloseDatabase</span></span>](./jetclosedatabase-function.md)  
[<span data-ttu-id="35b12-167">жетклосетабле</span><span class="sxs-lookup"><span data-stu-id="35b12-167">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="35b12-168">жетдетачдатабасе</span><span class="sxs-lookup"><span data-stu-id="35b12-168">JetDetachDatabase</span></span>](./jetdetachdatabase-function.md)  
[<span data-ttu-id="35b12-169">жетендсессион</span><span class="sxs-lookup"><span data-stu-id="35b12-169">JetEndSession</span></span>](./jetendsession-function.md)  
[<span data-ttu-id="35b12-170">жетресетсессионконтекст</span><span class="sxs-lookup"><span data-stu-id="35b12-170">JetResetSessionContext</span></span>](./jetresetsessioncontext-function.md)  
[<span data-ttu-id="35b12-171">жетроллбакк</span><span class="sxs-lookup"><span data-stu-id="35b12-171">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="35b12-172">жеттерм</span><span class="sxs-lookup"><span data-stu-id="35b12-172">JetTerm</span></span>](./jetterm-function.md)  
[<span data-ttu-id="35b12-173">JetTerm2</span><span class="sxs-lookup"><span data-stu-id="35b12-173">JetTerm2</span></span>](./jetterm2-function.md)
