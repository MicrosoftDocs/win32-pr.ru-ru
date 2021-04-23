---
title: Метод использованием метода ibackgroundcopyjob Сетнотифифлагс (Deliveryoptimization. h)
description: Указывает тип уведомления о событии, которое требуется получить, например события, переданные для задания.
ms.assetid: 19E626A5-6B6E-44E0-BD6F-43F132F32890
keywords:
- Метод Сетнотифифлагс
- Метод Сетнотифифлагс, интерфейс использованием метода ibackgroundcopyjob
- Интерфейс использованием метода ibackgroundcopyjob, метод Сетнотифифлагс
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.SetNotifyFlags
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ea754eeafca8f0efdcad5545cfc3a462c8b508cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534235"
---
# <a name="ibackgroundcopyjobsetnotifyflags-method"></a><span data-ttu-id="9aad1-106">Метод использованием метода ibackgroundcopyjob:: Сетнотифифлагс</span><span class="sxs-lookup"><span data-stu-id="9aad1-106">IBackgroundCopyJob::SetNotifyFlags method</span></span>

<span data-ttu-id="9aad1-107">Указывает тип уведомления о событии, которое требуется получить, например события, переданные для задания.</span><span class="sxs-lookup"><span data-stu-id="9aad1-107">Specifies the type of event notification you want to receive, such as job transferred events.</span></span>

## <a name="syntax"></a><span data-ttu-id="9aad1-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9aad1-108">Syntax</span></span>


```C++
HRESULT SetNotifyFlags(
  [in] ULONG NotifyFlags
);
```



## <a name="parameters"></a><span data-ttu-id="9aad1-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="9aad1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9aad1-110">*Нотифифлагс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9aad1-110">*NotifyFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9aad1-111">Установите один или несколько следующих флагов, чтобы определить события, которые требуется получить.</span><span class="sxs-lookup"><span data-stu-id="9aad1-111">Set one or more of the following flags to identify the events that you want to receive.</span></span>



| <span data-ttu-id="9aad1-112">Значение</span><span class="sxs-lookup"><span data-stu-id="9aad1-112">Value</span></span>                                                                                                                                                                                                                                                                                    | <span data-ttu-id="9aad1-113">Значение</span><span class="sxs-lookup"><span data-stu-id="9aad1-113">Meaning</span></span>                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BG_NOTIFY_JOB_TRANSFERRED"></span><span id="bg_notify_job_transferred"></span><dl> <span data-ttu-id="9aad1-114"><dt>**BG_NOTIFY_JOB_TRANSFERRED**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="9aad1-114"><dt>**BG_NOTIFY_JOB_TRANSFERRED**</dt> <dt>0x0001</dt></span></span> </dl>                          | <span data-ttu-id="9aad1-115">Все файлы в задании были переданы.</span><span class="sxs-lookup"><span data-stu-id="9aad1-115">All of the files in the job have been transferred.</span></span><br/>                                                                                                                                                          |
| <span id="BG_NOTIFY_JOB_ERROR"></span><span id="bg_notify_job_error"></span><dl> <span data-ttu-id="9aad1-116"><dt>**BG_NOTIFY_JOB_ERROR**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="9aad1-116"><dt>**BG_NOTIFY_JOB_ERROR**</dt> <dt>0x0002</dt></span></span> </dl>                                            | <span data-ttu-id="9aad1-117">Произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="9aad1-117">An error has occurred.</span></span><br/>                                                                                                                                                                                      |
| <span id="BG_NOTIFY_DISABLE"></span><span id="bg_notify_disable"></span><dl> <span data-ttu-id="9aad1-118"><dt>**BG_NOTIFY_DISABLE**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="9aad1-118"><dt>**BG_NOTIFY_DISABLE**</dt> <dt>0x0004</dt></span></span> </dl>                                                   | <span data-ttu-id="9aad1-119">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="9aad1-119">Not supported.</span></span><br/>                                                                                                                                                                                              |
| <span id="BG_NOTIFY_JOB_MODIFICATION"></span><span id="bg_notify_job_modification"></span><dl> <span data-ttu-id="9aad1-120"><dt>**BG_NOTIFY_JOB_MODIFICATION**</dt> <dt>0x0008</dt></span><span class="sxs-lookup"><span data-stu-id="9aad1-120"><dt>**BG_NOTIFY_JOB_MODIFICATION**</dt> <dt>0x0008</dt></span></span> </dl>                       | <span data-ttu-id="9aad1-121">Задание было изменено.</span><span class="sxs-lookup"><span data-stu-id="9aad1-121">The job has been modified.</span></span> <span data-ttu-id="9aad1-122">Например, изменено значение свойства, изменено состояние задания или выполняется передача файлов.</span><span class="sxs-lookup"><span data-stu-id="9aad1-122">For example, a property value changed, the state of the job changed, or progress is made transferring the files.</span></span> <span data-ttu-id="9aad1-123">Этот флаг пропускается, если указано уведомление командной строки.</span><span class="sxs-lookup"><span data-stu-id="9aad1-123">This flag is ignored if command line notification is specified.</span></span><br/> |
| <span id="BG_NOTIFY_FILE_TRANSFERRED"></span><span id="bg_notify_file_transferred"></span><dl> <span data-ttu-id="9aad1-124"><dt>**BG_NOTIFY_FILE_TRANSFERRED**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="9aad1-124"><dt>**BG_NOTIFY_FILE_TRANSFERRED**</dt> <dt>0x0010</dt></span></span> </dl>                       | <span data-ttu-id="9aad1-125">Файл в задании передан.</span><span class="sxs-lookup"><span data-stu-id="9aad1-125">A file in the job has been transferred.</span></span> <span data-ttu-id="9aad1-126">Этот флаг пропускается, если указано уведомление командной строки.</span><span class="sxs-lookup"><span data-stu-id="9aad1-126">This flag is ignored if command line notification is specified.</span></span><br/>                                                                                                     |
| <span id="BG_NOTIFY_FILE_RANGES_TRANSFERRED"></span><span id="bg_notify_file_ranges_transferred"></span><dl> <span data-ttu-id="9aad1-127"><dt>**BG_NOTIFY_FILE_RANGES_TRANSFERRED**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="9aad1-127"><dt>**BG_NOTIFY_FILE_RANGES_TRANSFERRED**</dt> <dt>0x0020</dt></span></span> </dl> | <span data-ttu-id="9aad1-128">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="9aad1-128">Not supported.</span></span><br/>                                                                                                                                                                                              |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9aad1-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9aad1-129">Return value</span></span>

<span data-ttu-id="9aad1-130">Этот метод возвращает следующие значения **HRESULT** , а также другие.</span><span class="sxs-lookup"><span data-stu-id="9aad1-130">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="9aad1-131">Код возврата</span><span class="sxs-lookup"><span data-stu-id="9aad1-131">Return code</span></span>                                                                                          | <span data-ttu-id="9aad1-132">Описание</span><span class="sxs-lookup"><span data-stu-id="9aad1-132">Description</span></span>                                                                                          |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9aad1-133"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="9aad1-133"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl>             | <span data-ttu-id="9aad1-134">Тип уведомления о событии успешно задан.</span><span class="sxs-lookup"><span data-stu-id="9aad1-134">Type of event notification was successfully set.</span></span><br/>                                          |
| <dl> <span data-ttu-id="9aad1-135"><dt>**DO_E_INVALID_STATE**</dt></span><span class="sxs-lookup"><span data-stu-id="9aad1-135"><dt>**DO_E_INVALID_STATE**</dt></span></span> </dl> | <span data-ttu-id="9aad1-136">Состояние задания не может быть BG_JOB_STATE_CANCELLED или BG_JOB_STATE_ACKNOWLEDGED.</span><span class="sxs-lookup"><span data-stu-id="9aad1-136">The state of the job cannot be BG_JOB_STATE_CANCELLED or BG_JOB_STATE_ACKNOWLEDGED.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9aad1-137">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9aad1-137">Remarks</span></span>

<span data-ttu-id="9aad1-138">Используйте метод **сетнотифифлагс** в сочетании с [**использованием метода ibackgroundcopyjob:: сетнотифинтерфаце**](ibackgroundcopyjob-setnotifyinterface.md).</span><span class="sxs-lookup"><span data-stu-id="9aad1-138">Use the **SetNotifyFlags** method in conjunction with the [**IBackgroundCopyJob::SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9aad1-139">Требования</span><span class="sxs-lookup"><span data-stu-id="9aad1-139">Requirements</span></span>



| <span data-ttu-id="9aad1-140">Требование</span><span class="sxs-lookup"><span data-stu-id="9aad1-140">Requirement</span></span> | <span data-ttu-id="9aad1-141">Значение</span><span class="sxs-lookup"><span data-stu-id="9aad1-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9aad1-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9aad1-142">Minimum supported client</span></span><br/> | <span data-ttu-id="9aad1-143">\[Только для настольных приложений Windows 10 версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="9aad1-143">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="9aad1-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9aad1-144">Minimum supported server</span></span><br/> | <span data-ttu-id="9aad1-145">\[Только для настольных приложений Windows Server версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="9aad1-145">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="9aad1-146">Header</span><span class="sxs-lookup"><span data-stu-id="9aad1-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="9aad1-147"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="9aad1-147"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="9aad1-148">IDL</span><span class="sxs-lookup"><span data-stu-id="9aad1-148">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9aad1-149"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9aad1-149"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="9aad1-150">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9aad1-150">Library</span></span><br/>                  | <dl> <span data-ttu-id="9aad1-151"><dt>Досвк. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9aad1-151"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="9aad1-152">DLL</span><span class="sxs-lookup"><span data-stu-id="9aad1-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9aad1-153"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9aad1-153"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="9aad1-154">IID</span><span class="sxs-lookup"><span data-stu-id="9aad1-154">IID</span></span><br/>                      | <span data-ttu-id="9aad1-155">IID_IBackgroundCopyJob определен как 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="9aad1-155">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="9aad1-156">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9aad1-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9aad1-157">**Использованием метода ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="9aad1-157">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="9aad1-158">**ибаккграундкопикаллбакк**</span><span class="sxs-lookup"><span data-stu-id="9aad1-158">**IBackgroundCopyCallback**</span></span>](ibackgroundcopycallback.md)
</dt> <dt>

[<span data-ttu-id="9aad1-159">**Использованием метода ibackgroundcopyjob:: Жетнотифифлагс**</span><span class="sxs-lookup"><span data-stu-id="9aad1-159">**IBackgroundCopyJob::GetNotifyFlags**</span></span>](ibackgroundcopyjob-getnotifyflags.md)
</dt> <dt>

[<span data-ttu-id="9aad1-160">**Использованием метода ibackgroundcopyjob:: Сетнотифинтерфаце**</span><span class="sxs-lookup"><span data-stu-id="9aad1-160">**IBackgroundCopyJob::SetNotifyInterface**</span></span>](ibackgroundcopyjob-setnotifyinterface.md)
</dt> </dl>

 

 





