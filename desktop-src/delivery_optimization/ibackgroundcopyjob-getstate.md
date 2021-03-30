---
title: Метод использованием метода ibackgroundcopyjob-State (Deliveryoptimization. h)
description: Возвращает состояние задания.
ms.assetid: 975AF0FB-37AE-4CE8-9EC1-35A972E422D8
keywords:
- Метод WebMethod
- Метод WebMethod, интерфейс использованием метода ibackgroundcopyjob
- Интерфейс использованием метода ibackgroundcopyjob, метод методаического состояния
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetState
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5b195377a44cab8f336bae8090bacc5ca5624d7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802440"
---
# <a name="ibackgroundcopyjobgetstate-method"></a><span data-ttu-id="58d28-106">Метод использованием метода ibackgroundcopyjob:: with State</span><span class="sxs-lookup"><span data-stu-id="58d28-106">IBackgroundCopyJob::GetState method</span></span>

<span data-ttu-id="58d28-107">Возвращает состояние задания.</span><span class="sxs-lookup"><span data-stu-id="58d28-107">Retrieves the state of the job.</span></span>

## <a name="syntax"></a><span data-ttu-id="58d28-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="58d28-108">Syntax</span></span>


```C++
HRESULT GetState(
  [out] BG_JOB_STATE *pJobState
);
```



## <a name="parameters"></a><span data-ttu-id="58d28-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="58d28-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58d28-110">*пжобстате* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="58d28-110">*pJobState* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="58d28-111">Состояние задания.</span><span class="sxs-lookup"><span data-stu-id="58d28-111">The state of the job.</span></span> <span data-ttu-id="58d28-112">Например, состояние показывает, что задание находится в состоянии ошибки, передаче данных или приостановлено.</span><span class="sxs-lookup"><span data-stu-id="58d28-112">For example, the state reflects whether the job is in error, transferring data, or suspended.</span></span> <span data-ttu-id="58d28-113">Список состояний заданий см. в разделе Перечисление [**BG_JOB_STATE**](bg-job-state-.md) .</span><span class="sxs-lookup"><span data-stu-id="58d28-113">For a list of job states, see the [**BG_JOB_STATE**](bg-job-state-.md) enumeration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58d28-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="58d28-114">Return value</span></span>

<span data-ttu-id="58d28-115">Этот метод возвращает следующие значения **HRESULT** , а также другие.</span><span class="sxs-lookup"><span data-stu-id="58d28-115">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="58d28-116">Код возврата</span><span class="sxs-lookup"><span data-stu-id="58d28-116">Return code</span></span>                                                                              | <span data-ttu-id="58d28-117">Описание</span><span class="sxs-lookup"><span data-stu-id="58d28-117">Description</span></span>                                                 |
|------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <span data-ttu-id="58d28-118"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="58d28-118"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="58d28-119">Состояние задания успешно получено.</span><span class="sxs-lookup"><span data-stu-id="58d28-119">The state of the job was successfully retrieved.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="58d28-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="58d28-120">Remarks</span></span>

<span data-ttu-id="58d28-121">Если вы хотите узнать, когда задание находится в состоянии ошибки или передало все файлы в задании, можно использовать этот метод для опроса состояния задания или регистрации для получения уведомлений о наступлении событий.</span><span class="sxs-lookup"><span data-stu-id="58d28-121">If you want to know when a job is in error or has transferred all the files in the job, you can use this method to poll for the state of the job or you can register to receive notification when events occur.</span></span> <span data-ttu-id="58d28-122">Дополнительные сведения о регистрации для получения уведомлений о событиях см. в разделе интерфейс [**ибаккграундкопикаллбакк**](ibackgroundcopycallback.md) .</span><span class="sxs-lookup"><span data-stu-id="58d28-122">For details on registering to receive event notification, see the [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="58d28-123">Требования</span><span class="sxs-lookup"><span data-stu-id="58d28-123">Requirements</span></span>



| <span data-ttu-id="58d28-124">Требование</span><span class="sxs-lookup"><span data-stu-id="58d28-124">Requirement</span></span> | <span data-ttu-id="58d28-125">Значение</span><span class="sxs-lookup"><span data-stu-id="58d28-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58d28-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="58d28-126">Minimum supported client</span></span><br/> | <span data-ttu-id="58d28-127">\[Только для настольных приложений Windows 10 версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="58d28-127">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="58d28-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="58d28-128">Minimum supported server</span></span><br/> | <span data-ttu-id="58d28-129">\[Только для настольных приложений Windows Server версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="58d28-129">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="58d28-130">Header</span><span class="sxs-lookup"><span data-stu-id="58d28-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="58d28-131"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="58d28-131"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="58d28-132">IDL</span><span class="sxs-lookup"><span data-stu-id="58d28-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="58d28-133"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="58d28-133"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="58d28-134">Библиотека</span><span class="sxs-lookup"><span data-stu-id="58d28-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="58d28-135"><dt>Досвк. lib</dt></span><span class="sxs-lookup"><span data-stu-id="58d28-135"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="58d28-136">DLL</span><span class="sxs-lookup"><span data-stu-id="58d28-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="58d28-137"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="58d28-137"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="58d28-138">IID</span><span class="sxs-lookup"><span data-stu-id="58d28-138">IID</span></span><br/>                      | <span data-ttu-id="58d28-139">IID_IBackgroundCopyJob определен как 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="58d28-139">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="58d28-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="58d28-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58d28-141">**Использованием метода ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="58d28-141">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="58d28-142">**BG_JOB_STATE**</span><span class="sxs-lookup"><span data-stu-id="58d28-142">**BG_JOB_STATE**</span></span>](bg-job-state-.md)
</dt> <dt>

[<span data-ttu-id="58d28-143">**ибаккграундкопикаллбакк**</span><span class="sxs-lookup"><span data-stu-id="58d28-143">**IBackgroundCopyCallback**</span></span>](ibackgroundcopycallback.md)
</dt> </dl>

 

 





