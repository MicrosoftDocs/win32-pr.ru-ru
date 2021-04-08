---
title: Метод Cancel использованием метода ibackgroundcopyjob (Deliveryoptimization. h)
description: Удаляет задание из очереди передачи и удаляет связанные временные файлы из клиента (загрузки) и сервера (отправки).
ms.assetid: DC502DC2-1335-476F-A1B8-FDB6BA595FF1
keywords:
- Метод Cancel
- Метод Cancel, интерфейс использованием метода ibackgroundcopyjob
- Интерфейс использованием метода ibackgroundcopyjob, метод Cancel
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.Cancel
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f72cdcea82ef7db30de141af295bb74594a7a630
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891809"
---
# <a name="ibackgroundcopyjobcancel-method"></a><span data-ttu-id="ef4cc-106">Метод использованием метода ibackgroundcopyjob:: Cancel</span><span class="sxs-lookup"><span data-stu-id="ef4cc-106">IBackgroundCopyJob::Cancel method</span></span>

<span data-ttu-id="ef4cc-107">Удаляет задание из очереди передачи и удаляет связанные временные файлы из клиента (загрузки) и сервера (отправки).</span><span class="sxs-lookup"><span data-stu-id="ef4cc-107">Deletes the job from the transfer queue and removes related temporary files from the client (downloads) and server (uploads).</span></span>

## <a name="syntax"></a><span data-ttu-id="ef4cc-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ef4cc-108">Syntax</span></span>


```C++
HRESULT Cancel();
```



## <a name="parameters"></a><span data-ttu-id="ef4cc-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="ef4cc-109">Parameters</span></span>

<span data-ttu-id="ef4cc-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="ef4cc-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ef4cc-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ef4cc-111">Return value</span></span>

<span data-ttu-id="ef4cc-112">Этот метод возвращает следующие значения **HRESULT** , а также другие.</span><span class="sxs-lookup"><span data-stu-id="ef4cc-112">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="ef4cc-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="ef4cc-113">Return code</span></span>                                                                                          | <span data-ttu-id="ef4cc-114">Описание</span><span class="sxs-lookup"><span data-stu-id="ef4cc-114">Description</span></span>                                                                                              |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ef4cc-115"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="ef4cc-115"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl>             | <span data-ttu-id="ef4cc-116">Задание успешно отменено.</span><span class="sxs-lookup"><span data-stu-id="ef4cc-116">Job was successfully canceled.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="ef4cc-117"><dt>**DO_E_INVALID_STATE**</dt></span><span class="sxs-lookup"><span data-stu-id="ef4cc-117"><dt>**DO_E_INVALID_STATE**</dt></span></span> </dl> | <span data-ttu-id="ef4cc-118">Невозможно отменить задание, состояние которого BG_JOB_STATE_CANCELLED или BG_JOB_STATE_ACKNOWLEDGED.</span><span class="sxs-lookup"><span data-stu-id="ef4cc-118">Cannot cancel a job whose state is BG_JOB_STATE_CANCELLED or BG_JOB_STATE_ACKNOWLEDGED.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ef4cc-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ef4cc-119">Remarks</span></span>

<span data-ttu-id="ef4cc-120">Задание можно отменить в любое время. Однако задание нельзя восстановить после его отмены.</span><span class="sxs-lookup"><span data-stu-id="ef4cc-120">You can cancel a job at any time; however, the job cannot be recovered after it is canceled.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef4cc-121">Требования</span><span class="sxs-lookup"><span data-stu-id="ef4cc-121">Requirements</span></span>



| <span data-ttu-id="ef4cc-122">Требование</span><span class="sxs-lookup"><span data-stu-id="ef4cc-122">Requirement</span></span> | <span data-ttu-id="ef4cc-123">Значение</span><span class="sxs-lookup"><span data-stu-id="ef4cc-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef4cc-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ef4cc-124">Minimum supported client</span></span><br/> | <span data-ttu-id="ef4cc-125">\[Только для настольных приложений Windows 10 версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="ef4cc-125">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="ef4cc-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ef4cc-126">Minimum supported server</span></span><br/> | <span data-ttu-id="ef4cc-127">\[Только для настольных приложений Windows Server версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="ef4cc-127">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="ef4cc-128">Header</span><span class="sxs-lookup"><span data-stu-id="ef4cc-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef4cc-129"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef4cc-129"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="ef4cc-130">IDL</span><span class="sxs-lookup"><span data-stu-id="ef4cc-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ef4cc-131"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ef4cc-131"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="ef4cc-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ef4cc-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="ef4cc-133"><dt>Досвк. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ef4cc-133"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="ef4cc-134">DLL</span><span class="sxs-lookup"><span data-stu-id="ef4cc-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ef4cc-135"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ef4cc-135"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="ef4cc-136">IID</span><span class="sxs-lookup"><span data-stu-id="ef4cc-136">IID</span></span><br/>                      | <span data-ttu-id="ef4cc-137">IID_IBackgroundCopyJob определен как 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="ef4cc-137">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="ef4cc-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ef4cc-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef4cc-139">**Использованием метода ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="ef4cc-139">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="ef4cc-140">**Использованием метода ibackgroundcopyjob:: Complete**</span><span class="sxs-lookup"><span data-stu-id="ef4cc-140">**IBackgroundCopyJob::Complete**</span></span>](ibackgroundcopyjob-complete.md)
</dt> <dt>

[<span data-ttu-id="ef4cc-141">**Использованием метода ibackgroundcopyjob:: Resume**</span><span class="sxs-lookup"><span data-stu-id="ef4cc-141">**IBackgroundCopyJob::Resume**</span></span>](ibackgroundcopyjob-resume.md)
</dt> <dt>

[<span data-ttu-id="ef4cc-142">**Использованием метода ibackgroundcopyjob:: Suspend**</span><span class="sxs-lookup"><span data-stu-id="ef4cc-142">**IBackgroundCopyJob::Suspend**</span></span>](ibackgroundcopyjob-suspend.md)
</dt> </dl>

 

 





