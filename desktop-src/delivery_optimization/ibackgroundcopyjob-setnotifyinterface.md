---
title: Метод использованием метода ibackgroundcopyjob Сетнотифинтерфаце (Deliveryoptimization. h)
description: Определяет вашу реализацию интерфейса Ибаккграундкопикаллбакк. Используйте интерфейс Ибаккграундкопикаллбакк для получения уведомлений о событиях, связанных с заданием.
ms.assetid: 792211FC-440E-4D2C-A6C7-CE9EFB86571C
keywords:
- Метод Сетнотифинтерфаце
- Метод Сетнотифинтерфаце, интерфейс использованием метода ibackgroundcopyjob
- Интерфейс использованием метода ibackgroundcopyjob, метод Сетнотифинтерфаце
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.SetNotifyInterface
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f3b6e8205eb60cbd2ca645cd484e41f8f242619d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340620"
---
# <a name="ibackgroundcopyjobsetnotifyinterface-method"></a><span data-ttu-id="e5a8a-107">Метод использованием метода ibackgroundcopyjob:: Сетнотифинтерфаце</span><span class="sxs-lookup"><span data-stu-id="e5a8a-107">IBackgroundCopyJob::SetNotifyInterface method</span></span>

<span data-ttu-id="e5a8a-108">Определяет вашу реализацию интерфейса [**ибаккграундкопикаллбакк**](ibackgroundcopycallback.md) .</span><span class="sxs-lookup"><span data-stu-id="e5a8a-108">Identifies your implementation of the [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) interface to DO.</span></span> <span data-ttu-id="e5a8a-109">Используйте интерфейс **ибаккграундкопикаллбакк** для получения уведомлений о событиях, связанных с заданием.</span><span class="sxs-lookup"><span data-stu-id="e5a8a-109">Use the **IBackgroundCopyCallback** interface to receive notification of job-related events.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5a8a-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e5a8a-110">Syntax</span></span>


```C++
HRESULT SetNotifyInterface(
   IUnknown *pNotifyInterface
);
```



## <a name="parameters"></a><span data-ttu-id="e5a8a-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="e5a8a-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5a8a-112">*пнотифинтерфаце*</span><span class="sxs-lookup"><span data-stu-id="e5a8a-112">*pNotifyInterface*</span></span> 
</dt> <dd>

<span data-ttu-id="e5a8a-113">Указатель интерфейса [**ибаккграундкопикаллбакк**](ibackgroundcopycallback.md) .</span><span class="sxs-lookup"><span data-stu-id="e5a8a-113">An [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) interface pointer.</span></span> <span data-ttu-id="e5a8a-114">Чтобы удалить текущий указатель интерфейса обратного вызова, присвойте этому параметру **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="e5a8a-114">To remove the current callback interface pointer, set this parameter to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5a8a-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e5a8a-115">Return value</span></span>

<span data-ttu-id="e5a8a-116">Этот метод возвращает следующие значения **HRESULT** , а также другие.</span><span class="sxs-lookup"><span data-stu-id="e5a8a-116">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="e5a8a-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="e5a8a-117">Return code</span></span>                                                                              | <span data-ttu-id="e5a8a-118">Описание</span><span class="sxs-lookup"><span data-stu-id="e5a8a-118">Description</span></span>                                                     |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="e5a8a-119"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="e5a8a-119"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="e5a8a-120">Указатель интерфейса уведомления успешно установлен.</span><span class="sxs-lookup"><span data-stu-id="e5a8a-120">Notification interface pointer was successfully set.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e5a8a-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e5a8a-121">Remarks</span></span>

<span data-ttu-id="e5a8a-122">Этот метод следует вызывать только при реализации интерфейса [**ибаккграундкопикаллбакк**](ibackgroundcopycallback.md) .</span><span class="sxs-lookup"><span data-stu-id="e5a8a-122">Call this method only if you implement the [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) interface.</span></span> <span data-ttu-id="e5a8a-123">Используйте метод **сетнотифинтерфаце** в сочетании с методом [**сетнотифифлагс**](ibackgroundcopyjob-setnotifyflags.md) , чтобы указать тип уведомления, которое требуется получить.</span><span class="sxs-lookup"><span data-stu-id="e5a8a-123">Use the **SetNotifyInterface** method in conjunction with the [**SetNotifyFlags**](ibackgroundcopyjob-setnotifyflags.md) method to specify the type of notification that you want to receive.</span></span>

<span data-ttu-id="e5a8a-124">Интерфейс уведомления станет недействительным после завершения работы приложения. Не сохраняет интерфейс уведомления.</span><span class="sxs-lookup"><span data-stu-id="e5a8a-124">The notification interface becomes invalid when your application terminates; DO does not persist the notify interface.</span></span> <span data-ttu-id="e5a8a-125">В результате процесс инициализации приложения должен вызвать метод **сетнотифинтерфаце** для тех существующих заданий, для которых вы хотите получить уведомление.</span><span class="sxs-lookup"><span data-stu-id="e5a8a-125">As a result, your application's initialization process should call the **SetNotifyInterface** method on those existing jobs for which you want to receive notification.</span></span> <span data-ttu-id="e5a8a-126">Если необходимо собрать сведения о состоянии и ходе выполнения, произошедшие с момента последнего запуска приложения, следует опросить сведения о состоянии и ходе выполнения во время инициализации приложения.</span><span class="sxs-lookup"><span data-stu-id="e5a8a-126">If you need to capture state and progress information that occurred since the last time your application was run, poll for state and progress information during application initialization.</span></span>

<span data-ttu-id="e5a8a-127">Только владелец, создатель или администратор задания могут зарегистрироваться для получения уведомлений.</span><span class="sxs-lookup"><span data-stu-id="e5a8a-127">Only the job owner/creator or an administrator can register for notifications.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5a8a-128">Требования</span><span class="sxs-lookup"><span data-stu-id="e5a8a-128">Requirements</span></span>



| <span data-ttu-id="e5a8a-129">Требование</span><span class="sxs-lookup"><span data-stu-id="e5a8a-129">Requirement</span></span> | <span data-ttu-id="e5a8a-130">Значение</span><span class="sxs-lookup"><span data-stu-id="e5a8a-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5a8a-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e5a8a-131">Minimum supported client</span></span><br/> | <span data-ttu-id="e5a8a-132">\[Только для настольных приложений Windows 10 версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="e5a8a-132">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="e5a8a-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e5a8a-133">Minimum supported server</span></span><br/> | <span data-ttu-id="e5a8a-134">\[Только для настольных приложений Windows Server версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="e5a8a-134">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="e5a8a-135">Header</span><span class="sxs-lookup"><span data-stu-id="e5a8a-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="e5a8a-136"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5a8a-136"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="e5a8a-137">IDL</span><span class="sxs-lookup"><span data-stu-id="e5a8a-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e5a8a-138"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e5a8a-138"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="e5a8a-139">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e5a8a-139">Library</span></span><br/>                  | <dl> <span data-ttu-id="e5a8a-140"><dt>Досвк. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e5a8a-140"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="e5a8a-141">DLL</span><span class="sxs-lookup"><span data-stu-id="e5a8a-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e5a8a-142"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e5a8a-142"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="e5a8a-143">IID</span><span class="sxs-lookup"><span data-stu-id="e5a8a-143">IID</span></span><br/>                      | <span data-ttu-id="e5a8a-144">IID_IBackgroundCopyJob определен как 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="e5a8a-144">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="e5a8a-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e5a8a-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5a8a-146">**Использованием метода ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="e5a8a-146">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="e5a8a-147">**ибаккграундкопикаллбакк**</span><span class="sxs-lookup"><span data-stu-id="e5a8a-147">**IBackgroundCopyCallback**</span></span>](ibackgroundcopycallback.md)
</dt> <dt>

[<span data-ttu-id="e5a8a-148">**Использованием метода ibackgroundcopyjob:: Жетнотифинтерфаце**</span><span class="sxs-lookup"><span data-stu-id="e5a8a-148">**IBackgroundCopyJob::GetNotifyInterface**</span></span>](ibackgroundcopyjob-getnotifyinterface.md)
</dt> <dt>

[<span data-ttu-id="e5a8a-149">**Использованием метода ibackgroundcopyjob:: Сетнотифифлагс**</span><span class="sxs-lookup"><span data-stu-id="e5a8a-149">**IBackgroundCopyJob::SetNotifyFlags**</span></span>](ibackgroundcopyjob-setnotifyflags.md)
</dt> </dl>

 

 





