---
title: Метод использованием метода ibackgroundcopyjob-предыдущих версий (Deliveryoptimization. h)
description: Возвращает уровень приоритета для задания. Уровень приоритета определяет, когда задание обрабатывается относительно других заданий в очереди обмена.
ms.assetid: 2F778B35-8DBB-4540-88C2-A2E18EBB0D89
keywords:
- Метод предшествовал
- Метод использованием метода ibackgroundcopyjob, интерфейс
- Интерфейс использованием метода ibackgroundcopyjob, метод предшествовал
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetPriority
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7ae9a865045ee1264a0598a3d3c1db8cc3c3b8bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691852"
---
# <a name="ibackgroundcopyjobgetpriority-method"></a><span data-ttu-id="e5248-107">Метод использованием метода ibackgroundcopyjob:: предшествовал</span><span class="sxs-lookup"><span data-stu-id="e5248-107">IBackgroundCopyJob::GetPriority method</span></span>

<span data-ttu-id="e5248-108">Возвращает уровень приоритета для задания.</span><span class="sxs-lookup"><span data-stu-id="e5248-108">Retrieves the priority level for the job.</span></span> <span data-ttu-id="e5248-109">Уровень приоритета определяет, когда задание обрабатывается относительно других заданий в очереди обмена.</span><span class="sxs-lookup"><span data-stu-id="e5248-109">The priority level determines when the job is processed relative to other jobs in the transfer queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5248-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e5248-110">Syntax</span></span>


```C++
HRESULT GetPriority(
  [out] BG_JOB_PRIORITY *pPriority
);
```



## <a name="parameters"></a><span data-ttu-id="e5248-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="e5248-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5248-112">*пприорити* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e5248-112">*pPriority* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e5248-113">Приоритет задания относительно других заданий в очереди обмена.</span><span class="sxs-lookup"><span data-stu-id="e5248-113">Priority of the job relative to other jobs in the transfer queue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5248-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e5248-114">Return value</span></span>

<span data-ttu-id="e5248-115">Этот метод возвращает следующие значения **HRESULT** , а также другие.</span><span class="sxs-lookup"><span data-stu-id="e5248-115">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="e5248-116">Код возврата</span><span class="sxs-lookup"><span data-stu-id="e5248-116">Return code</span></span>                                                                              | <span data-ttu-id="e5248-117">Описание</span><span class="sxs-lookup"><span data-stu-id="e5248-117">Description</span></span>                                           |
|------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <span data-ttu-id="e5248-118"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="e5248-118"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="e5248-119">Уровень приоритета успешно получен.</span><span class="sxs-lookup"><span data-stu-id="e5248-119">Priority level was successfully retrieved.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="e5248-120">Требования</span><span class="sxs-lookup"><span data-stu-id="e5248-120">Requirements</span></span>



| <span data-ttu-id="e5248-121">Требование</span><span class="sxs-lookup"><span data-stu-id="e5248-121">Requirement</span></span> | <span data-ttu-id="e5248-122">Значение</span><span class="sxs-lookup"><span data-stu-id="e5248-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5248-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e5248-123">Minimum supported client</span></span><br/> | <span data-ttu-id="e5248-124">\[Только для настольных приложений Windows 10 версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="e5248-124">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="e5248-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e5248-125">Minimum supported server</span></span><br/> | <span data-ttu-id="e5248-126">\[Только для настольных приложений Windows Server версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="e5248-126">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="e5248-127">Header</span><span class="sxs-lookup"><span data-stu-id="e5248-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="e5248-128"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5248-128"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="e5248-129">IDL</span><span class="sxs-lookup"><span data-stu-id="e5248-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e5248-130"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e5248-130"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="e5248-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e5248-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="e5248-132"><dt>Досвк. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e5248-132"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="e5248-133">DLL</span><span class="sxs-lookup"><span data-stu-id="e5248-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e5248-134"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e5248-134"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="e5248-135">IID</span><span class="sxs-lookup"><span data-stu-id="e5248-135">IID</span></span><br/>                      | <span data-ttu-id="e5248-136">IID_IBackgroundCopyJob определен как 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="e5248-136">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="e5248-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e5248-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5248-138">**Использованием метода ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="e5248-138">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="e5248-139">**Использованием метода ibackgroundcopyjob:: SetPriority**</span><span class="sxs-lookup"><span data-stu-id="e5248-139">**IBackgroundCopyJob::SetPriority**</span></span>](ibackgroundcopyjob-setpriority.md)
</dt> </dl>

 

 





