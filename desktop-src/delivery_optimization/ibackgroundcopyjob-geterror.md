---
title: Метод использованием метода ibackgroundcopyjob-Error (Deliveryoptimization. h)
description: Возвращает интерфейс ошибки после возникновения ошибки.
ms.assetid: 66891557-C118-4C66-AEFC-D8FD70976B9A
keywords:
- Метод метода с ошибками
- Метод использованием метода ibackgroundcopyjob, интерфейс
- Интерфейс использованием метода ibackgroundcopyjob, метод method
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetError
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1f2da994da83a786b89adb5ae63104dbaa6e2ef9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415533"
---
# <a name="ibackgroundcopyjobgeterror-method"></a><span data-ttu-id="8075f-106">Метод использованием метода ibackgroundcopyjob:: Error</span><span class="sxs-lookup"><span data-stu-id="8075f-106">IBackgroundCopyJob::GetError method</span></span>

<span data-ttu-id="8075f-107">Возвращает интерфейс ошибки после возникновения ошибки.</span><span class="sxs-lookup"><span data-stu-id="8075f-107">Retrieves the error interface after an error occurs.</span></span>

<span data-ttu-id="8075f-108">Оптимизация доставки (DO) создает объект Error, если состояние задания — BG_JOB_STATE_ERROR или BG_JOB_STATE_TRANSIENT_ERROR.</span><span class="sxs-lookup"><span data-stu-id="8075f-108">Delivery Optimization (DO) generates an error object when the state of the job is BG_JOB_STATE_ERROR or BG_JOB_STATE_TRANSIENT_ERROR.</span></span> <span data-ttu-id="8075f-109">Служба не создает объект Error при сбое вызова метода интерфейса **ибаккграундкопикскскскс** .</span><span class="sxs-lookup"><span data-stu-id="8075f-109">The service does not create an error object when a call to an **IBackgroundCopyXXXX** interface method fails.</span></span> <span data-ttu-id="8075f-110">Объект Error доступен до тех пор, пока не начнется передача данных (состояние задания меняется на BG_JOB_STATE_TRANSFERRING) для задания или до выхода из приложения.</span><span class="sxs-lookup"><span data-stu-id="8075f-110">The error object is available until DO begins transferring data (the state of the job changes to BG_JOB_STATE_TRANSFERRING) for the job or until your application exits.</span></span>

## <a name="syntax"></a><span data-ttu-id="8075f-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8075f-111">Syntax</span></span>


```C++
HRESULT GetError(
  [out] IBackgroundCopyError **ppError
);
```



## <a name="parameters"></a><span data-ttu-id="8075f-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="8075f-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8075f-113">*пперрор* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="8075f-113">*ppError* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8075f-114">Интерфейс ошибки, который предоставляет код ошибки, описание ошибки и контекст, в котором произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="8075f-114">Error interface that provides the error code, a description of the error, and the context in which the error occurred.</span></span> <span data-ttu-id="8075f-115">Этот параметр также определяет файл, который передается в момент возникновения ошибки.</span><span class="sxs-lookup"><span data-stu-id="8075f-115">This parameter also identifies the file being transferred at the time the error occurred.</span></span> <span data-ttu-id="8075f-116">Выпустите *пперрор* по завершении.</span><span class="sxs-lookup"><span data-stu-id="8075f-116">Release *ppError* when done.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8075f-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8075f-117">Return value</span></span>

<span data-ttu-id="8075f-118">Этот метод возвращает следующие значения **HRESULT** , а также другие.</span><span class="sxs-lookup"><span data-stu-id="8075f-118">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="8075f-119">Код возврата</span><span class="sxs-lookup"><span data-stu-id="8075f-119">Return code</span></span>                                                                                                           | <span data-ttu-id="8075f-120">Описание</span><span class="sxs-lookup"><span data-stu-id="8075f-120">Description</span></span>                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8075f-121"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="8075f-121"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl>                              | <span data-ttu-id="8075f-122">Объект ошибки успешно создан.</span><span class="sxs-lookup"><span data-stu-id="8075f-122">Successfully generated the error object.</span></span><br/>                                                                                                                                                       |
| <dl> <span data-ttu-id="8075f-123"><dt>**DO_E_ERROR_INFORMATION_UNAVAILABLE**</dt></span><span class="sxs-lookup"><span data-stu-id="8075f-123"><dt>**DO_E_ERROR_INFORMATION_UNAVAILABLE**</dt></span></span> </dl> | <span data-ttu-id="8075f-124">Интерфейс Error доступен только после возникновения ошибки (BG_JOB_STATE_ERROR или BG_JOB_STATE_TRANSIENT_ERROR) и перед началом передачи данных (BG_JOB_STATE_TRANSFERRING).</span><span class="sxs-lookup"><span data-stu-id="8075f-124">The error interface is available only after an error occurs (BG_JOB_STATE_ERROR or BG_JOB_STATE_TRANSIENT_ERROR) and before DO begins transferring data (BG_JOB_STATE_TRANSFERRING).</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8075f-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8075f-125">Remarks</span></span>

<span data-ttu-id="8075f-126">Задание помещается в состояние ошибки при неустранимых ошибках.</span><span class="sxs-lookup"><span data-stu-id="8075f-126">The job is placed in an error state on fatal errors.</span></span> <span data-ttu-id="8075f-127">Чтобы определить, является ли задание ошибкой, используйте один из следующих параметров:</span><span class="sxs-lookup"><span data-stu-id="8075f-127">Use one of the following options to determine if the job is in error:</span></span>

-   <span data-ttu-id="8075f-128">Чтобы опросить состояние задания, вызовите метод [**использованием метода ibackgroundcopyjob:: with State**](ibackgroundcopyjob-getstate.md) .</span><span class="sxs-lookup"><span data-stu-id="8075f-128">To poll for the state of the job, call the [**IBackgroundCopyJob::GetState**](ibackgroundcopyjob-getstate.md) method.</span></span> <span data-ttu-id="8075f-129">Задание находится в ошибке, если состояние BG_JOB_STATE_ERROR.</span><span class="sxs-lookup"><span data-stu-id="8075f-129">The job is in error if the state is BG_JOB_STATE_ERROR.</span></span>
-   <span data-ttu-id="8075f-130">Чтобы получить уведомление при возникновении ошибки, реализуйте интерфейс [**ибаккграундкопикаллбакк**](ibackgroundcopycallback.md) (в частности, метод [**жоберрор**](https://www.bing.com/search?q=**JobError**) ).</span><span class="sxs-lookup"><span data-stu-id="8075f-130">To receive notification when an error occurs, implement the [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) interface (specifically, the [**JobError**](https://www.bing.com/search?q=**JobError**) method).</span></span> <span data-ttu-id="8075f-131">Затем вызовите метод [**использованием метода ibackgroundcopyjob:: сетнотифинтерфаце**](ibackgroundcopyjob-setnotifyinterface.md) , чтобы зарегистрировать обратный вызов и метод [**использованием метода ibackgroundcopyjob:: сетнотифифлагс**](ibackgroundcopyjob-setnotifyflags.md) для установки флага BG_NOTIFY_JOB_ERROR.</span><span class="sxs-lookup"><span data-stu-id="8075f-131">Then, call the [**IBackgroundCopyJob::SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md) method to register the callback and the [**IBackgroundCopyJob::SetNotifyFlags**](ibackgroundcopyjob-setnotifyflags.md) method to set the BG_NOTIFY_JOB_ERROR flag.</span></span>

<span data-ttu-id="8075f-132">Интерфейс [**ибаккграундкоперрор**](ibackgroundcopyerror.md) содержит сведения, которые используются для определения причины ошибки, а также в случае, если процесс перемещения может быть продолжен.</span><span class="sxs-lookup"><span data-stu-id="8075f-132">The [**IBackgroundCopyError**](ibackgroundcopyerror.md) interface contains information that you use to determine the cause of the error and if the transfer process can proceed.</span></span> <span data-ttu-id="8075f-133">Определив причину ошибки, выполните одно из следующих действий.</span><span class="sxs-lookup"><span data-stu-id="8075f-133">After you determine the cause of the error, perform one of the following options:</span></span>

-   <span data-ttu-id="8075f-134">Чтобы отменить задание, вызовите метод [**использованием метода ibackgroundcopyjob:: Cancel**](ibackgroundcopyjob-cancel.md) .</span><span class="sxs-lookup"><span data-stu-id="8075f-134">To cancel the job, call the [**IBackgroundCopyJob::Cancel**](ibackgroundcopyjob-cancel.md) method.</span></span>
-   <span data-ttu-id="8075f-135">Чтобы сохранить файлы, которые были успешно переданы до возникновения ошибки, вызовите метод [**использованием метода ibackgroundcopyjob:: Complete**](ibackgroundcopyjob-complete.md) .</span><span class="sxs-lookup"><span data-stu-id="8075f-135">To save those files that transferred successfully before the error occurred, call the [**IBackgroundCopyJob::Complete**](ibackgroundcopyjob-complete.md) method.</span></span>
-   <span data-ttu-id="8075f-136">Чтобы завершить обработку задания, устраните проблему, а затем вызовите метод [**использованием метода ibackgroundcopyjob:: Resume**](ibackgroundcopyjob-resume.md) .</span><span class="sxs-lookup"><span data-stu-id="8075f-136">To finish processing the job, fix the problem, and then call the [**IBackgroundCopyJob::Resume**](ibackgroundcopyjob-resume.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="8075f-137">Требования</span><span class="sxs-lookup"><span data-stu-id="8075f-137">Requirements</span></span>



| <span data-ttu-id="8075f-138">Требование</span><span class="sxs-lookup"><span data-stu-id="8075f-138">Requirement</span></span> | <span data-ttu-id="8075f-139">Значение</span><span class="sxs-lookup"><span data-stu-id="8075f-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8075f-140">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8075f-140">Minimum supported client</span></span><br/> | <span data-ttu-id="8075f-141">\[Только для настольных приложений Windows 10 версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="8075f-141">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="8075f-142">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8075f-142">Minimum supported server</span></span><br/> | <span data-ttu-id="8075f-143">\[Только для настольных приложений Windows Server версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="8075f-143">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="8075f-144">Header</span><span class="sxs-lookup"><span data-stu-id="8075f-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="8075f-145"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="8075f-145"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="8075f-146">IDL</span><span class="sxs-lookup"><span data-stu-id="8075f-146">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8075f-147"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8075f-147"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="8075f-148">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8075f-148">Library</span></span><br/>                  | <dl> <span data-ttu-id="8075f-149"><dt>Досвк. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8075f-149"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="8075f-150">DLL</span><span class="sxs-lookup"><span data-stu-id="8075f-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8075f-151"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8075f-151"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="8075f-152">IID</span><span class="sxs-lookup"><span data-stu-id="8075f-152">IID</span></span><br/>                      | <span data-ttu-id="8075f-153">IID_IBackgroundCopyJob определен как 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="8075f-153">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="8075f-154">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8075f-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8075f-155">**Использованием метода ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="8075f-155">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="8075f-156">**Ибаккграундкопикаллбакк:: Жоберрор**</span><span class="sxs-lookup"><span data-stu-id="8075f-156">**IBackgroundCopyCallback::JobError**</span></span>](ibackgroundcopycallback-joberror-method.md)
</dt> <dt>

[<span data-ttu-id="8075f-157">**ибаккграундкоперрор**</span><span class="sxs-lookup"><span data-stu-id="8075f-157">**IBackgroundCopyError**</span></span>](ibackgroundcopyerror.md)
</dt> <dt>

[<span data-ttu-id="8075f-158">**Использованием метода ibackgroundcopyjob:: State**</span><span class="sxs-lookup"><span data-stu-id="8075f-158">**IBackgroundCopyJob::GetState**</span></span>](ibackgroundcopyjob-getstate.md)
</dt> </dl>

 

 





