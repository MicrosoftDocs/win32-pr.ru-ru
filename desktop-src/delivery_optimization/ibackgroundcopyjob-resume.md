---
title: Метод Resume использованием метода ibackgroundcopyjob (Deliveryoptimization. h)
description: Активирует новое задание или перезапускает приостановленное задание.
ms.assetid: B745BDA6-36B9-41FD-9737-61D14150A9E4
keywords:
- Метод Resume
- Метод Resume, интерфейс использованием метода ibackgroundcopyjob
- Интерфейс использованием метода ibackgroundcopyjob, метод Resume
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.Resume
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f87f5b5347785810d84331ce56f240cd1f016383
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135475"
---
# <a name="ibackgroundcopyjobresume-method"></a><span data-ttu-id="22202-106">Метод использованием метода ibackgroundcopyjob:: Resume</span><span class="sxs-lookup"><span data-stu-id="22202-106">IBackgroundCopyJob::Resume method</span></span>

<span data-ttu-id="22202-107">Активирует новое задание или перезапускает приостановленное задание.</span><span class="sxs-lookup"><span data-stu-id="22202-107">Activates a new job or restarts a job that has been suspended.</span></span>

## <a name="syntax"></a><span data-ttu-id="22202-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="22202-108">Syntax</span></span>


```C++
HRESULT Resume();
```



## <a name="parameters"></a><span data-ttu-id="22202-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="22202-109">Parameters</span></span>

<span data-ttu-id="22202-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="22202-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="22202-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="22202-111">Return value</span></span>

<span data-ttu-id="22202-112">Этот метод возвращает следующие значения **HRESULT** , а также другие.</span><span class="sxs-lookup"><span data-stu-id="22202-112">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="22202-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="22202-113">Return code</span></span>                                                                                          | <span data-ttu-id="22202-114">Описание</span><span class="sxs-lookup"><span data-stu-id="22202-114">Description</span></span>                                                                                          |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="22202-115"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="22202-115"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl>             | <span data-ttu-id="22202-116">Задание успешно перезапущено.</span><span class="sxs-lookup"><span data-stu-id="22202-116">Job was successfully restarted.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="22202-117"><dt>**DO_E_EMPTY**</dt></span><span class="sxs-lookup"><span data-stu-id="22202-117"><dt>**DO_E_EMPTY**</dt></span></span> </dl>          | <span data-ttu-id="22202-118">Нет файлов для передачи.</span><span class="sxs-lookup"><span data-stu-id="22202-118">There are no files to transfer.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="22202-119"><dt>**DO_E_INVALID_STATE**</dt></span><span class="sxs-lookup"><span data-stu-id="22202-119"><dt>**DO_E_INVALID_STATE**</dt></span></span> </dl> | <span data-ttu-id="22202-120">Состояние задания не может быть BG_JOB_STATE_CANCELLED или BG_JOB_STATE_ACKNOWLEDGED.</span><span class="sxs-lookup"><span data-stu-id="22202-120">The state of the job cannot be BG_JOB_STATE_CANCELLED or BG_JOB_STATE_ACKNOWLEDGED.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="22202-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="22202-121">Remarks</span></span>

<span data-ttu-id="22202-122">При создании задания изначально его работа приостанавливается.</span><span class="sxs-lookup"><span data-stu-id="22202-122">When you create a job, the job is initially suspended.</span></span> <span data-ttu-id="22202-123">Вызов **Resume** перемещает задание в состояние передачи.</span><span class="sxs-lookup"><span data-stu-id="22202-123">Calling **Resume** moves the job to the Transferring state.</span></span> <span data-ttu-id="22202-124">Обратите внимание, что задание должно содержать один или несколько файлов перед вызовом этого метода.</span><span class="sxs-lookup"><span data-stu-id="22202-124">Note that the job must contain one or more files before calling this method.</span></span>

<span data-ttu-id="22202-125">Если задание находится в состоянии BG_JOB_STATE_TRANSIENT_ERROR или BG_JOB_STATE_ERROR, вызовите метод **Resume** , чтобы перезапустить задание после устранения ошибки.</span><span class="sxs-lookup"><span data-stu-id="22202-125">If a job that is in the BG_JOB_STATE_TRANSIENT_ERROR or BG_JOB_STATE_ERROR state, call the **Resume** method to restart the job after you fix the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="22202-126">Требования</span><span class="sxs-lookup"><span data-stu-id="22202-126">Requirements</span></span>



| <span data-ttu-id="22202-127">Требование</span><span class="sxs-lookup"><span data-stu-id="22202-127">Requirement</span></span> | <span data-ttu-id="22202-128">Значение</span><span class="sxs-lookup"><span data-stu-id="22202-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22202-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="22202-129">Minimum supported client</span></span><br/> | <span data-ttu-id="22202-130">\[Только для настольных приложений Windows 10 версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="22202-130">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="22202-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="22202-131">Minimum supported server</span></span><br/> | <span data-ttu-id="22202-132">\[Только для настольных приложений Windows Server версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="22202-132">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="22202-133">Header</span><span class="sxs-lookup"><span data-stu-id="22202-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="22202-134"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="22202-134"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="22202-135">IDL</span><span class="sxs-lookup"><span data-stu-id="22202-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="22202-136"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="22202-136"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="22202-137">Библиотека</span><span class="sxs-lookup"><span data-stu-id="22202-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="22202-138"><dt>Досвк. lib</dt></span><span class="sxs-lookup"><span data-stu-id="22202-138"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="22202-139">DLL</span><span class="sxs-lookup"><span data-stu-id="22202-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="22202-140"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="22202-140"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="22202-141">IID</span><span class="sxs-lookup"><span data-stu-id="22202-141">IID</span></span><br/>                      | <span data-ttu-id="22202-142">IID_IBackgroundCopyJob определен как 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="22202-142">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="22202-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="22202-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22202-144">**Использованием метода ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="22202-144">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="22202-145">**Использованием метода ibackgroundcopyjob:: Cancel**</span><span class="sxs-lookup"><span data-stu-id="22202-145">**IBackgroundCopyJob::Cancel**</span></span>](ibackgroundcopyjob-cancel.md)
</dt> <dt>

[<span data-ttu-id="22202-146">**Использованием метода ibackgroundcopyjob:: Suspend**</span><span class="sxs-lookup"><span data-stu-id="22202-146">**IBackgroundCopyJob::Suspend**</span></span>](ibackgroundcopyjob-suspend.md)
</dt> </dl>

 

 





