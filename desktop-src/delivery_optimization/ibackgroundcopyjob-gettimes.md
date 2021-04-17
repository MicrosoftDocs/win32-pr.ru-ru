---
title: Метод использованием метода ibackgroundcopyjob-времени (Deliveryoptimization. h)
description: Получает отметки времени, связанные с заданием, например время создания или последнего изменения задания.
ms.assetid: 9002FB8D-08CB-4878-980F-15FE0DC952A6
keywords:
- Метод со временем
- Метод использованием метода ibackgroundcopyjob, интерфейс
- Интерфейс использованием метода ibackgroundcopyjob, метод Time
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetTimes
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 04e779b59e0976e77b287bc575f3b08f8d39340a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490923"
---
# <a name="ibackgroundcopyjobgettimes-method"></a><span data-ttu-id="cb9fa-106">Метод использованием метода ibackgroundcopyjob::/Time</span><span class="sxs-lookup"><span data-stu-id="cb9fa-106">IBackgroundCopyJob::GetTimes method</span></span>

<span data-ttu-id="cb9fa-107">Получает отметки времени, связанные с заданием, например время создания или последнего изменения задания.</span><span class="sxs-lookup"><span data-stu-id="cb9fa-107">Retrieves job-related time stamps, such as the time that the job was created or last modified.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb9fa-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cb9fa-108">Syntax</span></span>


```C++
HRESULT GetTimes(
  [out] BG_JOB_TIMES *pTimes
);
```



## <a name="parameters"></a><span data-ttu-id="cb9fa-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="cb9fa-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb9fa-110">*птимес* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="cb9fa-110">*pTimes* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cb9fa-111">Содержит отметки времени, связанные с заданиями.</span><span class="sxs-lookup"><span data-stu-id="cb9fa-111">Contains job-related time stamps.</span></span> <span data-ttu-id="cb9fa-112">Доступные метки времени см. в разделе Структура [**BG_JOB_TIMES**](bg-job-times.md) .</span><span class="sxs-lookup"><span data-stu-id="cb9fa-112">For available time stamps, see the [**BG_JOB_TIMES**](bg-job-times.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb9fa-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cb9fa-113">Return value</span></span>

<span data-ttu-id="cb9fa-114">Этот метод возвращает следующие значения **HRESULT** , а также другие.</span><span class="sxs-lookup"><span data-stu-id="cb9fa-114">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="cb9fa-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="cb9fa-115">Return code</span></span>                                                                              | <span data-ttu-id="cb9fa-116">Описание</span><span class="sxs-lookup"><span data-stu-id="cb9fa-116">Description</span></span>                                         |
|------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="cb9fa-117"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="cb9fa-117"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="cb9fa-118">Отметки времени успешно получены.</span><span class="sxs-lookup"><span data-stu-id="cb9fa-118">Time stamps were successfully retrieved.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="cb9fa-119">Требования</span><span class="sxs-lookup"><span data-stu-id="cb9fa-119">Requirements</span></span>



| <span data-ttu-id="cb9fa-120">Требование</span><span class="sxs-lookup"><span data-stu-id="cb9fa-120">Requirement</span></span> | <span data-ttu-id="cb9fa-121">Значение</span><span class="sxs-lookup"><span data-stu-id="cb9fa-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb9fa-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cb9fa-122">Minimum supported client</span></span><br/> | <span data-ttu-id="cb9fa-123">\[Только для настольных приложений Windows 10 версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="cb9fa-123">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="cb9fa-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cb9fa-124">Minimum supported server</span></span><br/> | <span data-ttu-id="cb9fa-125">\[Только для настольных приложений Windows Server версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="cb9fa-125">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="cb9fa-126">Header</span><span class="sxs-lookup"><span data-stu-id="cb9fa-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb9fa-127"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb9fa-127"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="cb9fa-128">IDL</span><span class="sxs-lookup"><span data-stu-id="cb9fa-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="cb9fa-129"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="cb9fa-129"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="cb9fa-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="cb9fa-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="cb9fa-131"><dt>Досвк. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cb9fa-131"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="cb9fa-132">DLL</span><span class="sxs-lookup"><span data-stu-id="cb9fa-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cb9fa-133"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cb9fa-133"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="cb9fa-134">IID</span><span class="sxs-lookup"><span data-stu-id="cb9fa-134">IID</span></span><br/>                      | <span data-ttu-id="cb9fa-135">IID_IBackgroundCopyJob определен как 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="cb9fa-135">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="cb9fa-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cb9fa-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb9fa-137">**Использованием метода ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="cb9fa-137">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="cb9fa-138">**BG_JOB_TIMES**</span><span class="sxs-lookup"><span data-stu-id="cb9fa-138">**BG_JOB_TIMES**</span></span>](bg-job-times.md)
</dt> </dl>

 

 





