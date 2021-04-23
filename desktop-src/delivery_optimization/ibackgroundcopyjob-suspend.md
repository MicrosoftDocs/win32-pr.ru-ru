---
title: Метод приостановки использованием метода ibackgroundcopyjob (Deliveryoptimization. h)
description: Приостанавливает задание. Новые задания, задания с ошибками и задания, в которых передача файлов завершена, автоматически приостанавливаются.
ms.assetid: 23EED354-A3AC-4865-8C06-ADA097851F96
keywords:
- Метод Suspend
- Метод Suspend, интерфейс использованием метода ibackgroundcopyjob
- Интерфейс использованием метода ibackgroundcopyjob, метод Suspend
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.Suspend
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: dd4464a04f87a7759e9b51974eef2188ba1d0c2a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415529"
---
# <a name="ibackgroundcopyjobsuspend-method"></a><span data-ttu-id="11e16-107">Метод использованием метода ibackgroundcopyjob:: Suspend</span><span class="sxs-lookup"><span data-stu-id="11e16-107">IBackgroundCopyJob::Suspend method</span></span>

<span data-ttu-id="11e16-108">Приостанавливает задание.</span><span class="sxs-lookup"><span data-stu-id="11e16-108">Suspends a job.</span></span> <span data-ttu-id="11e16-109">Новые задания, задания с ошибками и задания, в которых передача файлов завершена, автоматически приостанавливаются.</span><span class="sxs-lookup"><span data-stu-id="11e16-109">New jobs, jobs that are in error, and jobs that have finished transferring files are automatically suspended.</span></span>

## <a name="syntax"></a><span data-ttu-id="11e16-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="11e16-110">Syntax</span></span>


```C++
HRESULT Suspend();
```



## <a name="parameters"></a><span data-ttu-id="11e16-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="11e16-111">Parameters</span></span>

<span data-ttu-id="11e16-112">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="11e16-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="11e16-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="11e16-113">Return value</span></span>

<span data-ttu-id="11e16-114">Этот метод возвращает следующие значения **HRESULT** , а также другие.</span><span class="sxs-lookup"><span data-stu-id="11e16-114">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="11e16-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="11e16-115">Return code</span></span>                                                                                          | <span data-ttu-id="11e16-116">Описание</span><span class="sxs-lookup"><span data-stu-id="11e16-116">Description</span></span>                                                                                          |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="11e16-117"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="11e16-117"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl>             | <span data-ttu-id="11e16-118">Задание успешно приостановлено.</span><span class="sxs-lookup"><span data-stu-id="11e16-118">Successfully suspended the job.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="11e16-119"><dt>**DO_E_INVALID_STATE**</dt></span><span class="sxs-lookup"><span data-stu-id="11e16-119"><dt>**DO_E_INVALID_STATE**</dt></span></span> </dl> | <span data-ttu-id="11e16-120">Состояние задания не может быть BG_JOB_STATE_CANCELLED или BG_JOB_STATE_ACKNOWLEDGED.</span><span class="sxs-lookup"><span data-stu-id="11e16-120">The state of the job cannot be BG_JOB_STATE_CANCELLED or BG_JOB_STATE_ACKNOWLEDGED.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="11e16-121">Требования</span><span class="sxs-lookup"><span data-stu-id="11e16-121">Requirements</span></span>



| <span data-ttu-id="11e16-122">Требование</span><span class="sxs-lookup"><span data-stu-id="11e16-122">Requirement</span></span> | <span data-ttu-id="11e16-123">Значение</span><span class="sxs-lookup"><span data-stu-id="11e16-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11e16-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="11e16-124">Minimum supported client</span></span><br/> | <span data-ttu-id="11e16-125">\[Только для настольных приложений Windows 10 версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="11e16-125">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="11e16-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="11e16-126">Minimum supported server</span></span><br/> | <span data-ttu-id="11e16-127">\[Только для настольных приложений Windows Server версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="11e16-127">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="11e16-128">Header</span><span class="sxs-lookup"><span data-stu-id="11e16-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="11e16-129"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="11e16-129"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="11e16-130">IDL</span><span class="sxs-lookup"><span data-stu-id="11e16-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="11e16-131"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="11e16-131"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="11e16-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="11e16-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="11e16-133"><dt>Досвк. lib</dt></span><span class="sxs-lookup"><span data-stu-id="11e16-133"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="11e16-134">DLL</span><span class="sxs-lookup"><span data-stu-id="11e16-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11e16-135"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11e16-135"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="11e16-136">IID</span><span class="sxs-lookup"><span data-stu-id="11e16-136">IID</span></span><br/>                      | <span data-ttu-id="11e16-137">IID_IBackgroundCopyJob определен как 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="11e16-137">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="11e16-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="11e16-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11e16-139">**Использованием метода ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="11e16-139">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="11e16-140">**Использованием метода ibackgroundcopyjob:: Cancel**</span><span class="sxs-lookup"><span data-stu-id="11e16-140">**IBackgroundCopyJob::Cancel**</span></span>](ibackgroundcopyjob-cancel.md)
</dt> <dt>

[<span data-ttu-id="11e16-141">**Использованием метода ibackgroundcopyjob:: Resume**</span><span class="sxs-lookup"><span data-stu-id="11e16-141">**IBackgroundCopyJob::Resume**</span></span>](ibackgroundcopyjob-resume.md)
</dt> </dl>

 

 





