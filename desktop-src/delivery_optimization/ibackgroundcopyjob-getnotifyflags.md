---
title: Метод использованием метода ibackgroundcopyjob Жетнотифифлагс (Deliveryoptimization. h)
description: Получает флаги уведомления о событии для задания.
ms.assetid: 95ADC97F-63DC-4EB6-B85C-7BCC79238C12
keywords:
- Метод Жетнотифифлагс
- Метод Жетнотифифлагс, интерфейс использованием метода ibackgroundcopyjob
- Интерфейс использованием метода ibackgroundcopyjob, метод Жетнотифифлагс
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetNotifyFlags
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e104857725849dfeb899b449ea055bc3cdb046bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340675"
---
# <a name="ibackgroundcopyjobgetnotifyflags-method"></a><span data-ttu-id="201ec-106">Метод использованием метода ibackgroundcopyjob:: Жетнотифифлагс</span><span class="sxs-lookup"><span data-stu-id="201ec-106">IBackgroundCopyJob::GetNotifyFlags method</span></span>

<span data-ttu-id="201ec-107">Получает флаги уведомления о событии для задания.</span><span class="sxs-lookup"><span data-stu-id="201ec-107">Retrieves the event notification flags for the job.</span></span>

## <a name="syntax"></a><span data-ttu-id="201ec-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="201ec-108">Syntax</span></span>


```C++
HRESULT GetNotifyFlags(
  [out] ULONG *pNotifyFlags
);
```



## <a name="parameters"></a><span data-ttu-id="201ec-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="201ec-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="201ec-110">*пнотифифлагс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="201ec-110">*pNotifyFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="201ec-111">Определяет события, получаемые приложением.</span><span class="sxs-lookup"><span data-stu-id="201ec-111">Identifies the events that your application receives.</span></span> <span data-ttu-id="201ec-112">В следующей таблице перечислены значения флагов уведомлений о событиях.</span><span class="sxs-lookup"><span data-stu-id="201ec-112">The following table lists the event notification flag values.</span></span>



| <span data-ttu-id="201ec-113">Значение</span><span class="sxs-lookup"><span data-stu-id="201ec-113">Value</span></span>                                                                                                                                                                                                  | <span data-ttu-id="201ec-114">Значение</span><span class="sxs-lookup"><span data-stu-id="201ec-114">Meaning</span></span>                                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <span id="BG_NOTIFY_JOB_TRANSFERRED"></span><span id="bg_notify_job_transferred"></span><dl> <span data-ttu-id="201ec-115"><dt>**BG_NOTIFY_JOB_TRANSFERRED**</dt></span><span class="sxs-lookup"><span data-stu-id="201ec-115"><dt>**BG_NOTIFY_JOB_TRANSFERRED**</dt></span></span> </dl>    | <span data-ttu-id="201ec-116">Все файлы в задании были переданы.</span><span class="sxs-lookup"><span data-stu-id="201ec-116">All of the files in the job have been transferred.</span></span><br/>                  |
| <span id="BG_NOTIFY_JOB_ERROR"></span><span id="bg_notify_job_error"></span><dl> <span data-ttu-id="201ec-117"><dt>**BG_NOTIFY_JOB_ERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="201ec-117"><dt>**BG_NOTIFY_JOB_ERROR**</dt></span></span> </dl>                      | <span data-ttu-id="201ec-118">Произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="201ec-118">An error has occurred.</span></span><br/>                                              |
| <span id="BG_NOTIFY_DISABLE"></span><span id="bg_notify_disable"></span><dl> <span data-ttu-id="201ec-119"><dt>**BG_NOTIFY_DISABLE**</dt></span><span class="sxs-lookup"><span data-stu-id="201ec-119"><dt>**BG_NOTIFY_DISABLE**</dt></span></span> </dl>                             | <span data-ttu-id="201ec-120">Уведомление о событии отключено.</span><span class="sxs-lookup"><span data-stu-id="201ec-120">Event notification is disabled.</span></span> <span data-ttu-id="201ec-121">Если этот параметр задан, другие флаги не учитываются.</span><span class="sxs-lookup"><span data-stu-id="201ec-121">If set, DO ignores the other flags.</span></span><br/> |
| <span id="BG_NOTIFY_JOB_MODIFICATION"></span><span id="bg_notify_job_modification"></span><dl> <span data-ttu-id="201ec-122"><dt>**BG_NOTIFY_JOB_MODIFICATION**</dt></span><span class="sxs-lookup"><span data-stu-id="201ec-122"><dt>**BG_NOTIFY_JOB_MODIFICATION**</dt></span></span> </dl> | <span data-ttu-id="201ec-123">Задание было изменено.</span><span class="sxs-lookup"><span data-stu-id="201ec-123">The job has been modified.</span></span><br/>                                          |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="201ec-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="201ec-124">Return value</span></span>

<span data-ttu-id="201ec-125">Этот метод возвращает следующие значения **HRESULT** , а также другие.</span><span class="sxs-lookup"><span data-stu-id="201ec-125">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="201ec-126">Код возврата</span><span class="sxs-lookup"><span data-stu-id="201ec-126">Return code</span></span>                                                                              | <span data-ttu-id="201ec-127">Описание</span><span class="sxs-lookup"><span data-stu-id="201ec-127">Description</span></span>                                                |
|------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <span data-ttu-id="201ec-128"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="201ec-128"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="201ec-129">Флаги уведомления о событии успешно получены.</span><span class="sxs-lookup"><span data-stu-id="201ec-129">Event notify flags were successfully retrieved.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="201ec-130">Требования</span><span class="sxs-lookup"><span data-stu-id="201ec-130">Requirements</span></span>



| <span data-ttu-id="201ec-131">Требование</span><span class="sxs-lookup"><span data-stu-id="201ec-131">Requirement</span></span> | <span data-ttu-id="201ec-132">Значение</span><span class="sxs-lookup"><span data-stu-id="201ec-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="201ec-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="201ec-133">Minimum supported client</span></span><br/> | <span data-ttu-id="201ec-134">\[Только для настольных приложений Windows 10 версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="201ec-134">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="201ec-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="201ec-135">Minimum supported server</span></span><br/> | <span data-ttu-id="201ec-136">\[Только для настольных приложений Windows Server версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="201ec-136">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="201ec-137">Header</span><span class="sxs-lookup"><span data-stu-id="201ec-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="201ec-138"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="201ec-138"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="201ec-139">IDL</span><span class="sxs-lookup"><span data-stu-id="201ec-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="201ec-140"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="201ec-140"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="201ec-141">Библиотека</span><span class="sxs-lookup"><span data-stu-id="201ec-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="201ec-142"><dt>Досвк. lib</dt></span><span class="sxs-lookup"><span data-stu-id="201ec-142"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="201ec-143">DLL</span><span class="sxs-lookup"><span data-stu-id="201ec-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="201ec-144"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="201ec-144"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="201ec-145">IID</span><span class="sxs-lookup"><span data-stu-id="201ec-145">IID</span></span><br/>                      | <span data-ttu-id="201ec-146">IID_IBackgroundCopyJob определен как 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="201ec-146">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="201ec-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="201ec-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="201ec-148">**Использованием метода ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="201ec-148">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="201ec-149">**ибаккграундкопикаллбакк**</span><span class="sxs-lookup"><span data-stu-id="201ec-149">**IBackgroundCopyCallback**</span></span>](ibackgroundcopycallback.md)
</dt> <dt>

[<span data-ttu-id="201ec-150">**Использованием метода ibackgroundcopyjob:: Жетнотифинтерфаце**</span><span class="sxs-lookup"><span data-stu-id="201ec-150">**IBackgroundCopyJob::GetNotifyInterface**</span></span>](ibackgroundcopyjob-getnotifyinterface.md)
</dt> <dt>

[<span data-ttu-id="201ec-151">**Использованием метода ibackgroundcopyjob:: Сетнотифифлагс**</span><span class="sxs-lookup"><span data-stu-id="201ec-151">**IBackgroundCopyJob::SetNotifyFlags**</span></span>](ibackgroundcopyjob-setnotifyflags.md)
</dt> </dl>

 

 





