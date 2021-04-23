---
title: Метод Ибаккграундкопикаллбакк Жоберрор (Deliveryoptimization. h)
description: Оптимизация доставки (DO) вызывает реализацию метода Жоберрор, когда состояние задания изменяется на BG_JOB_STATE_ERROR.
ms.assetid: 121712A5-98EB-4B2F-A004-A3BDF9C1332B
keywords:
- Метод Жоберрор
- Метод Жоберрор, интерфейс Ибаккграундкопикаллбакк
- Интерфейс Ибаккграундкопикаллбакк, метод Жоберрор
topic_type:
- apiref
api_name:
- IBackgroundCopyCallback.JobError
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0122f5777303506be5fd81d0966b00f828bf2073
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415392"
---
# <a name="ibackgroundcopycallbackjoberror-method"></a><span data-ttu-id="00ff5-106">Метод Ибаккграундкопикаллбакк:: Жоберрор</span><span class="sxs-lookup"><span data-stu-id="00ff5-106">IBackgroundCopyCallback::JobError method</span></span>

<span data-ttu-id="00ff5-107">Оптимизация доставки (DO) вызывает реализацию метода [**жоберрор**](https://www.bing.com/search?q=**JobError**) , когда состояние задания изменяется на BG_JOB_STATE_ERROR.</span><span class="sxs-lookup"><span data-stu-id="00ff5-107">Delivery Optimization (DO) calls your implementation of the [**JobError**](https://www.bing.com/search?q=**JobError**) method when the state of the job changes to BG_JOB_STATE_ERROR.</span></span>

## <a name="syntax"></a><span data-ttu-id="00ff5-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="00ff5-108">Syntax</span></span>


```C++
HRESULT JobError(
  [in] IBackgroundCopyJob   *pJob,
  [in] IBackgroundCopyError *pError
);
```



## <a name="parameters"></a><span data-ttu-id="00ff5-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="00ff5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00ff5-110">*пжоб* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="00ff5-110">*pJob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00ff5-111">Содержит сведения, связанные с заданиями, такие как число байтов и файлов, переданных до возникновения ошибки.</span><span class="sxs-lookup"><span data-stu-id="00ff5-111">Contains job-related information, such as the number of bytes and files transferred before the error occurred.</span></span> <span data-ttu-id="00ff5-112">Он также содержит методы для возобновления и отмены задания.</span><span class="sxs-lookup"><span data-stu-id="00ff5-112">It also contains the methods to resume and cancel the job.</span></span> <span data-ttu-id="00ff5-113">Не освобождайте *пжоб*; Выпускайте интерфейс, когда метод [**жоберрор**](https://www.bing.com/search?q=**JobError**) возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="00ff5-113">Do not release *pJob*; DO releases the interface when the [**JobError**](https://www.bing.com/search?q=**JobError**) method returns.</span></span>

</dd> <dt>

<span data-ttu-id="00ff5-114">*perror* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="00ff5-114">*pError* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00ff5-115">Содержит сведения об ошибке, такие как обрабатываемый файл во время возникновения неустранимой ошибки и описание ошибки.</span><span class="sxs-lookup"><span data-stu-id="00ff5-115">Contains error information, such as the file being processed at the time the fatal error occurred and a description of the error.</span></span> <span data-ttu-id="00ff5-116">Не освобождайте *perror*; Выпускайте интерфейс, когда метод [**жоберрор**](https://www.bing.com/search?q=**JobError**) возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="00ff5-116">Do not release *pError*; DO releases the interface when the [**JobError**](https://www.bing.com/search?q=**JobError**) method returns.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00ff5-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="00ff5-117">Return value</span></span>

<span data-ttu-id="00ff5-118">Этот метод должен возвращать **S_OK**; в противном случае Вызывайте этот метод до тех пор, пока не будет возвращено **S_OK** .</span><span class="sxs-lookup"><span data-stu-id="00ff5-118">This method should return **S_OK**; otherwise, DO continues to call this method until **S_OK** is returned.</span></span> <span data-ttu-id="00ff5-119">В целях повышения производительности следует ограничить количество возвращаемых значений, кроме **S_OK** , в несколько раз.</span><span class="sxs-lookup"><span data-stu-id="00ff5-119">For performance reasons, you should limit the number of times you return a value other than **S_OK** to a few times.</span></span> <span data-ttu-id="00ff5-120">В качестве альтернативы возврату кода ошибки рекомендуется всегда возвращать **S_OK** и обрабатывать ошибку внутренним образом.</span><span class="sxs-lookup"><span data-stu-id="00ff5-120">As an alternative to returning an error code, consider always returning **S_OK** and handling the error internally.</span></span> <span data-ttu-id="00ff5-121">Интервал, с которым вызывается этот метод, является произвольным.</span><span class="sxs-lookup"><span data-stu-id="00ff5-121">The interval at which this method is called is arbitrary.</span></span>

## <a name="remarks"></a><span data-ttu-id="00ff5-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="00ff5-122">Remarks</span></span>

<span data-ttu-id="00ff5-123">Определив причину ошибки, выполните одно из следующих действий.</span><span class="sxs-lookup"><span data-stu-id="00ff5-123">After you determine the cause of the error, perform one of the following options:</span></span>

-   <span data-ttu-id="00ff5-124">Чтобы отменить задание, вызовите метод [**использованием метода ibackgroundcopyjob:: Cancel**](ibackgroundcopyjob-cancel.md) .</span><span class="sxs-lookup"><span data-stu-id="00ff5-124">To cancel the job, call the [**IBackgroundCopyJob::Cancel**](ibackgroundcopyjob-cancel.md) method.</span></span>
-   <span data-ttu-id="00ff5-125">Чтобы принять часть задания, которая успешно передалася до возникновения ошибки, вызовите метод [**использованием метода ibackgroundcopyjob:: Complete**](ibackgroundcopyjob-complete.md) .</span><span class="sxs-lookup"><span data-stu-id="00ff5-125">To accept the portion of the job that transferred successfully before the error occurred, call the [**IBackgroundCopyJob::Complete**](ibackgroundcopyjob-complete.md) method.</span></span> <span data-ttu-id="00ff5-126">Этот параметр не применяется для отправки заданий. часть задания отправки выполнить нельзя.</span><span class="sxs-lookup"><span data-stu-id="00ff5-126">This option does not apply to upload jobs; you cannot complete a portion of an upload job.</span></span>
-   <span data-ttu-id="00ff5-127">Чтобы завершить обработку задания, устраните проблему, а затем вызовите метод [**использованием метода ibackgroundcopyjob:: Resume**](ibackgroundcopyjob-resume.md) .</span><span class="sxs-lookup"><span data-stu-id="00ff5-127">To finish processing the job, fix the problem, and then call the [**IBackgroundCopyJob::Resume**](ibackgroundcopyjob-resume.md) method.</span></span>

<span data-ttu-id="00ff5-128">Временные ошибки не создают вызовы метода [**жоберрор**](https://www.bing.com/search?q=**JobError**) .</span><span class="sxs-lookup"><span data-stu-id="00ff5-128">Transient errors do not generate calls to the [**JobError**](https://www.bing.com/search?q=**JobError**) method.</span></span>

<span data-ttu-id="00ff5-129">Функция возвращает BG_ERROR_CONTEXT_REMOTE_FILE, если задание вызвало ошибку HTTP 403, BG_ERROR_CONTEXT_NONE в противном случае.</span><span class="sxs-lookup"><span data-stu-id="00ff5-129">DO returns BG_ERROR_CONTEXT_REMOTE_FILE if the job hit a HTTP 403 error, BG_ERROR_CONTEXT_NONE otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="00ff5-130">Требования</span><span class="sxs-lookup"><span data-stu-id="00ff5-130">Requirements</span></span>



| <span data-ttu-id="00ff5-131">Требование</span><span class="sxs-lookup"><span data-stu-id="00ff5-131">Requirement</span></span> | <span data-ttu-id="00ff5-132">Значение</span><span class="sxs-lookup"><span data-stu-id="00ff5-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00ff5-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="00ff5-133">Minimum supported client</span></span><br/> | <span data-ttu-id="00ff5-134">\[Только для настольных приложений Windows 10 версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="00ff5-134">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="00ff5-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="00ff5-135">Minimum supported server</span></span><br/> | <span data-ttu-id="00ff5-136">\[Только для настольных приложений Windows Server версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="00ff5-136">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="00ff5-137">Header</span><span class="sxs-lookup"><span data-stu-id="00ff5-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="00ff5-138"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="00ff5-138"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="00ff5-139">IDL</span><span class="sxs-lookup"><span data-stu-id="00ff5-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="00ff5-140"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="00ff5-140"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="00ff5-141">Библиотека</span><span class="sxs-lookup"><span data-stu-id="00ff5-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="00ff5-142"><dt>Досвк. lib</dt></span><span class="sxs-lookup"><span data-stu-id="00ff5-142"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="00ff5-143">DLL</span><span class="sxs-lookup"><span data-stu-id="00ff5-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="00ff5-144"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="00ff5-144"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="00ff5-145">IID</span><span class="sxs-lookup"><span data-stu-id="00ff5-145">IID</span></span><br/>                      | <span data-ttu-id="00ff5-146">IID_IBackgroundCopyCallback определен как 97EA99C7-0186-4AD4-8DF9-C5B4E0ED6B22</span><span class="sxs-lookup"><span data-stu-id="00ff5-146">IID_IBackgroundCopyCallback is defined as 97EA99C7-0186-4AD4-8DF9-C5B4E0ED6B22</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="00ff5-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="00ff5-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00ff5-148">**ибаккграундкопикаллбакк**</span><span class="sxs-lookup"><span data-stu-id="00ff5-148">**IBackgroundCopyCallback**</span></span>](ibackgroundcopycallback.md)
</dt> <dt>

[<span data-ttu-id="00ff5-149">**ибаккграундкоперрор**</span><span class="sxs-lookup"><span data-stu-id="00ff5-149">**IBackgroundCopyError**</span></span>](ibackgroundcopyerror.md)
</dt> <dt>

[<span data-ttu-id="00ff5-150">**Использованием метода ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="00ff5-150">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="00ff5-151">**Использованием метода ibackgroundcopyjob:: Cancel**</span><span class="sxs-lookup"><span data-stu-id="00ff5-151">**IBackgroundCopyJob::Cancel**</span></span>](ibackgroundcopyjob-cancel.md)
</dt> <dt>

[<span data-ttu-id="00ff5-152">**Использованием метода ibackgroundcopyjob:: Resume**</span><span class="sxs-lookup"><span data-stu-id="00ff5-152">**IBackgroundCopyJob::Resume**</span></span>](ibackgroundcopyjob-resume.md)
</dt> </dl>

 

 





