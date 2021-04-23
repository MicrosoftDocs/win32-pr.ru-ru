---
title: Метод использованием метода ibackgroundcopyjob Complete (Deliveryoptimization. h)
description: Завершает задание и сохраняет перенесенные файлы на клиенте.
ms.assetid: A3706DBA-C44E-4F7A-A787-62FB436706FC
keywords:
- Метод Complete
- Метод Complete, интерфейс использованием метода ibackgroundcopyjob
- Интерфейс использованием метода ibackgroundcopyjob, метод Complete
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.Complete
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 72383bb235d31043f781998324891b6df134e6ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135883"
---
# <a name="ibackgroundcopyjobcomplete-method"></a><span data-ttu-id="a7714-106">Метод использованием метода ibackgroundcopyjob:: Complete</span><span class="sxs-lookup"><span data-stu-id="a7714-106">IBackgroundCopyJob::Complete method</span></span>

<span data-ttu-id="a7714-107">Завершает задание и сохраняет перенесенные файлы на клиенте.</span><span class="sxs-lookup"><span data-stu-id="a7714-107">Ends the job and saves the transferred files on the client.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7714-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a7714-108">Syntax</span></span>


```C++
HRESULT Complete();
```



## <a name="parameters"></a><span data-ttu-id="a7714-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="a7714-109">Parameters</span></span>

<span data-ttu-id="a7714-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="a7714-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a7714-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a7714-111">Return value</span></span>

<span data-ttu-id="a7714-112">Этот метод возвращает следующие значения **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a7714-112">This method returns the following **HRESULT** values.</span></span> <span data-ttu-id="a7714-113">Метод также может возвращать ошибки, связанные с переименованием временных копий переданных файлов по заданным именам.</span><span class="sxs-lookup"><span data-stu-id="a7714-113">The method can also return errors related to renaming the temporary copies of the transferred files to their given names.</span></span>



| <span data-ttu-id="a7714-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="a7714-114">Return code</span></span>                                                                                          | <span data-ttu-id="a7714-115">Описание</span><span class="sxs-lookup"><span data-stu-id="a7714-115">Description</span></span>                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a7714-116"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="a7714-116"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl>             | <span data-ttu-id="a7714-117">Все файлы успешно переданы.</span><span class="sxs-lookup"><span data-stu-id="a7714-117">All files transferred successfully.</span></span><br/>                                                                                                                                                         |
| <dl> <span data-ttu-id="a7714-118"><dt>**DO_E_INVALID_STATE**</dt></span><span class="sxs-lookup"><span data-stu-id="a7714-118"><dt>**DO_E_INVALID_STATE**</dt></span></span> </dl> | <span data-ttu-id="a7714-119">Для загрузки состояние задания не может быть BG_JOB_STATE_CANCELLED или BG_JOB_STATE_ACKNOWLEDGED.</span><span class="sxs-lookup"><span data-stu-id="a7714-119">For downloads, the state of the job cannot be BG_JOB_STATE_CANCELLED or BG_JOB_STATE_ACKNOWLEDGED.</span></span> <br/> <span data-ttu-id="a7714-120">Для отправки состояние задания должно быть BG_JOB_STATE_TRANSFERRED.</span><span class="sxs-lookup"><span data-stu-id="a7714-120">For uploads, the state of the job must be BG_JOB_STATE_TRANSFERRED.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a7714-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a7714-121">Remarks</span></span>

<span data-ttu-id="a7714-122">Все файлы были успешно переданы, если состояние задания — **BG_JOB_STATE_TRANSFERRED**.</span><span class="sxs-lookup"><span data-stu-id="a7714-122">All of the files have been successfully transferred if the job's state is **BG_JOB_STATE_TRANSFERRED**.</span></span> <span data-ttu-id="a7714-123">Чтобы проверить состояние задания, вызовите метод [**использованием метода ibackgroundcopyjob:: with State**](ibackgroundcopyjob-getstate.md) .</span><span class="sxs-lookup"><span data-stu-id="a7714-123">To check the state of the job, call the [**IBackgroundCopyJob::GetState**](ibackgroundcopyjob-getstate.md) method.</span></span> <span data-ttu-id="a7714-124">Можно также реализовать интерфейс [**ибаккграундкопикаллбакк**](ibackgroundcopycallback.md) для получения уведомлений о том, что все файлы были переданы клиенту.</span><span class="sxs-lookup"><span data-stu-id="a7714-124">You can also implement the [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) interface to receive notification when all of the files have been transferred to the client.</span></span>

<span data-ttu-id="a7714-125">Сохраняются только задания, срок действия которых меньше 30 дней.</span><span class="sxs-lookup"><span data-stu-id="a7714-125">DO retains jobs that are less than 30 days only.</span></span> <span data-ttu-id="a7714-126">Все более старые задания будут удалены.</span><span class="sxs-lookup"><span data-stu-id="a7714-126">All older jobs will be removed.</span></span> <span data-ttu-id="a7714-127">Не поддерживает групповая политика [жобинактивититимеаут](https://www.bing.com/search?q=JobInactivityTimeout) .</span><span class="sxs-lookup"><span data-stu-id="a7714-127">DO does not support the [JobInactivityTimeout](https://www.bing.com/search?q=JobInactivityTimeout) Group Policy.</span></span>

<span data-ttu-id="a7714-128">Для заданий загрузки можно вызвать метод **Complete** в любое время в процессе перемещения; Однако сохраняются только те файлы, которые были успешно переданы клиенту до вызова этого метода.</span><span class="sxs-lookup"><span data-stu-id="a7714-128">For download jobs, you can call the **Complete** method at anytime during the transfer process; however, only files that were successfully transferred to the client before calling this method are saved.</span></span> <span data-ttu-id="a7714-129">Например, при вызове метода **Complete** во время обработки третьей из пяти файлов сохраняются только первые два файла.</span><span class="sxs-lookup"><span data-stu-id="a7714-129">For example, if you call the **Complete** method while DO is processing the third of five files, only the first two files are saved.</span></span> <span data-ttu-id="a7714-130">Чтобы определить, какие файлы были переданы, вызовите метод [**ибаккграундкопифиле:: Progress**](ibackgroundcopyfile-getprogress-method.md) и сравните элемент **BytesTransferred** с элементом **битестотал** структуры [**BG_FILE_PROGRESS**](bg-file-progress.md) .</span><span class="sxs-lookup"><span data-stu-id="a7714-130">To determine which files have been transferred, call the [**IBackgroundCopyFile::GetProgress**](ibackgroundcopyfile-getprogress-method.md) method and compare the **BytesTransferred** member to the **BytesTotal** member of the [**BG_FILE_PROGRESS**](bg-file-progress.md) structure.</span></span>

<span data-ttu-id="a7714-131">Для заданий отправки можно вызвать метод **Complete** , только если задание находится в состоянии **BG_JOB_STATE_TRANSFERRED**.</span><span class="sxs-lookup"><span data-stu-id="a7714-131">For upload jobs, you can call the **Complete** method only when the job's state is **BG_JOB_STATE_TRANSFERRED**.</span></span>

<span data-ttu-id="a7714-132">Владельцем файла является пользователь, выполнивший вызов.</span><span class="sxs-lookup"><span data-stu-id="a7714-132">The owner of the file is the user who made the call.</span></span> <span data-ttu-id="a7714-133">Например, если администратор выполняет задание другого пользователя, он не является владельцем задания.</span><span class="sxs-lookup"><span data-stu-id="a7714-133">For example, if an administrator completes someone else's job, the administrator not the owner of the job owns the file.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7714-134">Требования</span><span class="sxs-lookup"><span data-stu-id="a7714-134">Requirements</span></span>



| <span data-ttu-id="a7714-135">Требование</span><span class="sxs-lookup"><span data-stu-id="a7714-135">Requirement</span></span> | <span data-ttu-id="a7714-136">Значение</span><span class="sxs-lookup"><span data-stu-id="a7714-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7714-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a7714-137">Minimum supported client</span></span><br/> | <span data-ttu-id="a7714-138">\[Только для настольных приложений Windows 10 версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="a7714-138">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="a7714-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a7714-139">Minimum supported server</span></span><br/> | <span data-ttu-id="a7714-140">\[Только для настольных приложений Windows Server версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="a7714-140">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="a7714-141">Header</span><span class="sxs-lookup"><span data-stu-id="a7714-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="a7714-142"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="a7714-142"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="a7714-143">IDL</span><span class="sxs-lookup"><span data-stu-id="a7714-143">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a7714-144"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a7714-144"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="a7714-145">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a7714-145">Library</span></span><br/>                  | <dl> <span data-ttu-id="a7714-146"><dt>Досвк. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a7714-146"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="a7714-147">DLL</span><span class="sxs-lookup"><span data-stu-id="a7714-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a7714-148"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a7714-148"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="a7714-149">IID</span><span class="sxs-lookup"><span data-stu-id="a7714-149">IID</span></span><br/>                      | <span data-ttu-id="a7714-150">IID_IBackgroundCopyJob определен как 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="a7714-150">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="a7714-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a7714-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7714-152">**Использованием метода ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="a7714-152">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="a7714-153">**Использованием метода ibackgroundcopyjob:: Cancel**</span><span class="sxs-lookup"><span data-stu-id="a7714-153">**IBackgroundCopyJob::Cancel**</span></span>](ibackgroundcopyjob-cancel.md)
</dt> <dt>

[<span data-ttu-id="a7714-154">**Использованием метода ibackgroundcopyjob:: State**</span><span class="sxs-lookup"><span data-stu-id="a7714-154">**IBackgroundCopyJob::GetState**</span></span>](ibackgroundcopyjob-getstate.md)
</dt> </dl>

 

 





