---
title: Метод GetType использованием метода ibackgroundcopyjob (Deliveryoptimization. h)
description: Возвращает тип выполняемой передачи, например скачивание файла или его отправку.
ms.assetid: F543A601-9385-4A73-A4E2-DE61433E84D3
keywords:
- GetType - метод
- Метод GetType, интерфейс использованием метода ibackgroundcopyjob
- Интерфейс использованием метода ibackgroundcopyjob, метод GetType
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetType
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5b0a09a3c7387b5b911bf6731921e7ed4e9b9163
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071269"
---
# <a name="ibackgroundcopyjobgettype-method"></a><span data-ttu-id="2573f-106">Метод использованием метода ibackgroundcopyjob:: GetType</span><span class="sxs-lookup"><span data-stu-id="2573f-106">IBackgroundCopyJob::GetType method</span></span>

<span data-ttu-id="2573f-107">Возвращает тип выполняемой передачи, например скачивание файла или его отправку.</span><span class="sxs-lookup"><span data-stu-id="2573f-107">Retrieves the type of transfer being performed, such as a file download or upload.</span></span>

## <a name="syntax"></a><span data-ttu-id="2573f-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2573f-108">Syntax</span></span>


```C++
HRESULT GetType(
  [out] BG_JOB_TYPE *pJobType
);
```



## <a name="parameters"></a><span data-ttu-id="2573f-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="2573f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2573f-110">*пжобтипе* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="2573f-110">*pJobType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2573f-111">Тип выполняемой операции перемещения.</span><span class="sxs-lookup"><span data-stu-id="2573f-111">Type of transfer being performed.</span></span> <span data-ttu-id="2573f-112">Список типов перемещения см. в разделе Перечисление [**BG_JOB_TYPE**](bg-job-type.md) .</span><span class="sxs-lookup"><span data-stu-id="2573f-112">For a list of transfer types, see the [**BG_JOB_TYPE**](bg-job-type.md) enumeration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2573f-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2573f-113">Return value</span></span>

<span data-ttu-id="2573f-114">Этот метод возвращает следующие значения **HRESULT** , а также другие.</span><span class="sxs-lookup"><span data-stu-id="2573f-114">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="2573f-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="2573f-115">Return code</span></span>                                                                              | <span data-ttu-id="2573f-116">Описание</span><span class="sxs-lookup"><span data-stu-id="2573f-116">Description</span></span>                                          |
|------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="2573f-117"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="2573f-117"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="2573f-118">Тип перемещения успешно получен.</span><span class="sxs-lookup"><span data-stu-id="2573f-118">Transfer type was successfully retrieved.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2573f-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2573f-119">Remarks</span></span>

<span data-ttu-id="2573f-120">Укажите тип перемещения при создании задания.</span><span class="sxs-lookup"><span data-stu-id="2573f-120">Specify the type of transfer when you create the job.</span></span>

## <a name="requirements"></a><span data-ttu-id="2573f-121">Требования</span><span class="sxs-lookup"><span data-stu-id="2573f-121">Requirements</span></span>



| <span data-ttu-id="2573f-122">Требование</span><span class="sxs-lookup"><span data-stu-id="2573f-122">Requirement</span></span> | <span data-ttu-id="2573f-123">Значение</span><span class="sxs-lookup"><span data-stu-id="2573f-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2573f-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2573f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="2573f-125">\[Только для настольных приложений Windows 10 версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="2573f-125">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="2573f-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2573f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="2573f-127">\[Только для настольных приложений Windows Server версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="2573f-127">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="2573f-128">Header</span><span class="sxs-lookup"><span data-stu-id="2573f-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="2573f-129"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="2573f-129"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="2573f-130">IDL</span><span class="sxs-lookup"><span data-stu-id="2573f-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2573f-131"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2573f-131"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="2573f-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2573f-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="2573f-133"><dt>Досвк. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2573f-133"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="2573f-134">DLL</span><span class="sxs-lookup"><span data-stu-id="2573f-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2573f-135"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2573f-135"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="2573f-136">IID</span><span class="sxs-lookup"><span data-stu-id="2573f-136">IID</span></span><br/>                      | <span data-ttu-id="2573f-137">IID_IBackgroundCopyJob определен как 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="2573f-137">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="2573f-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2573f-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2573f-139">**Использованием метода ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="2573f-139">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="2573f-140">**BG_JOB_TYPE**</span><span class="sxs-lookup"><span data-stu-id="2573f-140">**BG_JOB_TYPE**</span></span>](bg-job-type.md)
</dt> <dt>

[<span data-ttu-id="2573f-141">**Ибаккграундкопиманажер:: CreateJob**</span><span class="sxs-lookup"><span data-stu-id="2573f-141">**IBackgroundCopyManager::CreateJob**</span></span>](ibackgroundcopymanager-createjob.md)
</dt> </dl>

 

 





