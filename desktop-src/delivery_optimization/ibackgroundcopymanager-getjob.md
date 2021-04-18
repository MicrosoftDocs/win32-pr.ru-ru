---
title: Метод Ибаккграундкопиманажер Жетжоб (Deliveryoptimization. h)
description: Извлекает указанное задание из очереди обмена. Как правило, приложение сохраняет идентификатор задания, поэтому позже можно получить задание из очереди.
ms.assetid: ED551A6B-66C7-47E9-93DA-E231BD637522
keywords:
- Метод Жетжоб
- Метод Жетжоб, интерфейс Ибаккграундкопиманажер
- Интерфейс Ибаккграундкопиманажер, метод Жетжоб
topic_type:
- apiref
api_name:
- IBackgroundCopyManager.GetJob
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a59956e68b5b656e7182e62969b3212c2ef6732c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105710501"
---
# <a name="ibackgroundcopymanagergetjob-method"></a><span data-ttu-id="1356c-107">Метод Ибаккграундкопиманажер:: Жетжоб</span><span class="sxs-lookup"><span data-stu-id="1356c-107">IBackgroundCopyManager::GetJob method</span></span>

<span data-ttu-id="1356c-108">Извлекает указанное задание из очереди обмена.</span><span class="sxs-lookup"><span data-stu-id="1356c-108">Retrieves a specified job from the transfer queue.</span></span> <span data-ttu-id="1356c-109">Как правило, приложение сохраняет идентификатор задания, поэтому позже можно получить задание из очереди.</span><span class="sxs-lookup"><span data-stu-id="1356c-109">Typically, your application persists the job identifier, so you can later retrieve the job from the queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="1356c-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1356c-110">Syntax</span></span>


```C++
HRESULT GetJob(
  [in]  REFGUID            JobID,
  [out] IBackgroundCopyJob **ppJob
);
```



## <a name="parameters"></a><span data-ttu-id="1356c-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="1356c-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1356c-112">Идентификатор *задания* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1356c-112">*JobID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1356c-113">Определяет задание, извлекаемое из очереди обмена.</span><span class="sxs-lookup"><span data-stu-id="1356c-113">Identifies the job to retrieve from the transfer queue.</span></span> <span data-ttu-id="1356c-114">Метод [**CreateJob**](ibackgroundcopymanager-createjob.md) возвращает идентификатор задания.</span><span class="sxs-lookup"><span data-stu-id="1356c-114">The [**CreateJob**](ibackgroundcopymanager-createjob.md) method returns the job identifier.</span></span>

</dd> <dt>

<span data-ttu-id="1356c-115">*ппжоб* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="1356c-115">*ppJob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1356c-116">Указатель интерфейса [**использованием метода ibackgroundcopyjob**](ibackgroundcopyjob-.md) на задание, заданное параметром *JOBID*.</span><span class="sxs-lookup"><span data-stu-id="1356c-116">An [**IBackgroundCopyJob**](ibackgroundcopyjob-.md) interface pointer to the job specified by *JobID*.</span></span> <span data-ttu-id="1356c-117">По завершении выпустите *ппжоб*.</span><span class="sxs-lookup"><span data-stu-id="1356c-117">When done, release *ppJob*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1356c-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1356c-118">Return value</span></span>

<span data-ttu-id="1356c-119">Этот метод возвращает следующие значения **HRESULT** , а также другие.</span><span class="sxs-lookup"><span data-stu-id="1356c-119">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="1356c-120">Код возврата</span><span class="sxs-lookup"><span data-stu-id="1356c-120">Return code</span></span>                                                                                      | <span data-ttu-id="1356c-121">Описание</span><span class="sxs-lookup"><span data-stu-id="1356c-121">Description</span></span>                                                        |
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="1356c-122"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="1356c-122"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl>         | <span data-ttu-id="1356c-123">Задание успешно получено из очереди обмена.</span><span class="sxs-lookup"><span data-stu-id="1356c-123">Job was successfully retrieved from the transfer queue.</span></span><br/> |
| <dl> <span data-ttu-id="1356c-124"><dt>**DO_E_NOT_FOUND**</dt></span><span class="sxs-lookup"><span data-stu-id="1356c-124"><dt>**DO_E_NOT_FOUND**</dt></span></span> </dl> | <span data-ttu-id="1356c-125">Задание не найдено в очереди.</span><span class="sxs-lookup"><span data-stu-id="1356c-125">The job was not found in the queue.</span></span><br/>                     |
| <dl> <span data-ttu-id="1356c-126"><dt>**E_ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="1356c-126"><dt>**E_ACCESSDENIED**</dt></span></span> </dl>   | <span data-ttu-id="1356c-127">У пользователя нет разрешения на получение задания.</span><span class="sxs-lookup"><span data-stu-id="1356c-127">User does not have permission to retrieve the job.</span></span><br/>      |



 

## <a name="requirements"></a><span data-ttu-id="1356c-128">Требования</span><span class="sxs-lookup"><span data-stu-id="1356c-128">Requirements</span></span>



| <span data-ttu-id="1356c-129">Требование</span><span class="sxs-lookup"><span data-stu-id="1356c-129">Requirement</span></span> | <span data-ttu-id="1356c-130">Значение</span><span class="sxs-lookup"><span data-stu-id="1356c-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1356c-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1356c-131">Minimum supported client</span></span><br/> | <span data-ttu-id="1356c-132">\[Только для настольных приложений Windows 10 версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="1356c-132">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="1356c-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1356c-133">Minimum supported server</span></span><br/> | <span data-ttu-id="1356c-134">\[Только для настольных приложений Windows Server версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="1356c-134">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="1356c-135">Header</span><span class="sxs-lookup"><span data-stu-id="1356c-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="1356c-136"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="1356c-136"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="1356c-137">IDL</span><span class="sxs-lookup"><span data-stu-id="1356c-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1356c-138"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1356c-138"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="1356c-139">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1356c-139">Library</span></span><br/>                  | <dl> <span data-ttu-id="1356c-140"><dt>Досвк. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1356c-140"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="1356c-141">DLL</span><span class="sxs-lookup"><span data-stu-id="1356c-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1356c-142"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1356c-142"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="1356c-143">IID</span><span class="sxs-lookup"><span data-stu-id="1356c-143">IID</span></span><br/>                      | <span data-ttu-id="1356c-144">IID_IBackgroundCopyManager определен как 5CE34C0D-0DC9-4C1F-897C-DAA1B78CEE7C</span><span class="sxs-lookup"><span data-stu-id="1356c-144">IID_IBackgroundCopyManager is defined as 5CE34C0D-0DC9-4C1F-897C-DAA1B78CEE7C</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="1356c-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1356c-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1356c-146">**ибаккграундкопиманажер**</span><span class="sxs-lookup"><span data-stu-id="1356c-146">**IBackgroundCopyManager**</span></span>](ibackgroundcopymanager.md)
</dt> <dt>

[<span data-ttu-id="1356c-147">**Использованием метода ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="1356c-147">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="1356c-148">**Использованием метода ibackgroundcopyjob:: GetId**</span><span class="sxs-lookup"><span data-stu-id="1356c-148">**IBackgroundCopyJob::GetId**</span></span>](ibackgroundcopyjob-getid.md)
</dt> <dt>

[<span data-ttu-id="1356c-149">**Ибаккграундкопиманажер:: CreateJob**</span><span class="sxs-lookup"><span data-stu-id="1356c-149">**IBackgroundCopyManager::CreateJob**</span></span>](ibackgroundcopymanager-createjob.md)
</dt> </dl>

 

 





