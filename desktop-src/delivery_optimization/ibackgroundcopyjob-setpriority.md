---
title: Метод использованием метода ibackgroundcopyjob SetPriority (Deliveryoptimization. h)
description: Указывает уровень приоритета задания. Уровень приоритета определяет, когда задание обрабатывается относительно других заданий в очереди обмена.
ms.assetid: DC943093-CA1D-4840-B7AC-29710764D4E5
keywords:
- Метод SetPriority
- Метод SetPriority, интерфейс использованием метода ibackgroundcopyjob
- Интерфейс использованием метода ibackgroundcopyjob, метод SetPriority
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.SetPriority
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6fb6407c5d693a2c6e75f8aaf8f7a0544d08cdec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802435"
---
# <a name="ibackgroundcopyjobsetpriority-method"></a><span data-ttu-id="13a9b-107">Метод использованием метода ibackgroundcopyjob:: SetPriority</span><span class="sxs-lookup"><span data-stu-id="13a9b-107">IBackgroundCopyJob::SetPriority method</span></span>

<span data-ttu-id="13a9b-108">Указывает уровень приоритета задания.</span><span class="sxs-lookup"><span data-stu-id="13a9b-108">Specifies the priority level of your job.</span></span> <span data-ttu-id="13a9b-109">Уровень приоритета определяет, когда задание обрабатывается относительно других заданий в очереди обмена.</span><span class="sxs-lookup"><span data-stu-id="13a9b-109">The priority level determines when your job is processed relative to other jobs in the transfer queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="13a9b-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="13a9b-110">Syntax</span></span>


```C++
HRESULT SetPriority(
  [in] BG_JOB_PRIORITY Priority
);
```



## <a name="parameters"></a><span data-ttu-id="13a9b-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="13a9b-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13a9b-112">*Приоритет* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="13a9b-112">*Priority* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13a9b-113">Указывает уровень приоритета задания относительно других заданий в очереди обмена.</span><span class="sxs-lookup"><span data-stu-id="13a9b-113">Specifies the priority level of your job relative to other jobs in the transfer queue.</span></span> <span data-ttu-id="13a9b-114">Значение по умолчанию — BG_JOB_PRIORITY_NORMAL.</span><span class="sxs-lookup"><span data-stu-id="13a9b-114">The default is BG_JOB_PRIORITY_NORMAL.</span></span> <span data-ttu-id="13a9b-115">Список уровней приоритета см. в разделе Перечисление [**BG_JOB_PRIORITY**](bg-job-priority-.md) .</span><span class="sxs-lookup"><span data-stu-id="13a9b-115">For a list of priority levels, see the [**BG_JOB_PRIORITY**](bg-job-priority-.md) enumeration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13a9b-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="13a9b-116">Return value</span></span>

<span data-ttu-id="13a9b-117">Этот метод возвращает следующие значения **HRESULT** , а также другие.</span><span class="sxs-lookup"><span data-stu-id="13a9b-117">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="13a9b-118">Код возврата</span><span class="sxs-lookup"><span data-stu-id="13a9b-118">Return code</span></span>                                                                              | <span data-ttu-id="13a9b-119">Описание</span><span class="sxs-lookup"><span data-stu-id="13a9b-119">Description</span></span>                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="13a9b-120"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="13a9b-120"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="13a9b-121">Приоритет задания успешно установлен.</span><span class="sxs-lookup"><span data-stu-id="13a9b-121">Job priority was successfully set.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="13a9b-122">Требования</span><span class="sxs-lookup"><span data-stu-id="13a9b-122">Requirements</span></span>



| <span data-ttu-id="13a9b-123">Требование</span><span class="sxs-lookup"><span data-stu-id="13a9b-123">Requirement</span></span> | <span data-ttu-id="13a9b-124">Значение</span><span class="sxs-lookup"><span data-stu-id="13a9b-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13a9b-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="13a9b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="13a9b-126">\[Только для настольных приложений Windows 10 версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="13a9b-126">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="13a9b-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="13a9b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="13a9b-128">\[Только для настольных приложений Windows Server версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="13a9b-128">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="13a9b-129">Header</span><span class="sxs-lookup"><span data-stu-id="13a9b-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="13a9b-130"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="13a9b-130"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="13a9b-131">IDL</span><span class="sxs-lookup"><span data-stu-id="13a9b-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="13a9b-132"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="13a9b-132"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="13a9b-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="13a9b-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="13a9b-134"><dt>Досвк. lib</dt></span><span class="sxs-lookup"><span data-stu-id="13a9b-134"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="13a9b-135">DLL</span><span class="sxs-lookup"><span data-stu-id="13a9b-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13a9b-136"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="13a9b-136"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="13a9b-137">IID</span><span class="sxs-lookup"><span data-stu-id="13a9b-137">IID</span></span><br/>                      | <span data-ttu-id="13a9b-138">IID_IBackgroundCopyJob определен как 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="13a9b-138">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="13a9b-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="13a9b-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13a9b-140">**Использованием метода ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="13a9b-140">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="13a9b-141">**BG_JOB_PRIORITY**</span><span class="sxs-lookup"><span data-stu-id="13a9b-141">**BG_JOB_PRIORITY**</span></span>](bg-job-priority-.md)
</dt> <dt>

[<span data-ttu-id="13a9b-142">**Использованием метода ibackgroundcopyjob:: предшествовал**</span><span class="sxs-lookup"><span data-stu-id="13a9b-142">**IBackgroundCopyJob::GetPriority**</span></span>](ibackgroundcopyjob-getpriority.md)
</dt> </dl>

 

 





