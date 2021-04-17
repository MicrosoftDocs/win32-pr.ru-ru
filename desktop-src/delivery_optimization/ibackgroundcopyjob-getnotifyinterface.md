---
title: Метод использованием метода ibackgroundcopyjob Жетнотифинтерфаце (Deliveryoptimization. h)
description: Получает указатель интерфейса на реализацию интерфейса Ибаккграундкопикаллбакк.
ms.assetid: 1AA50C03-AC84-4AA9-8EC3-3FBA865C70C0
keywords:
- Метод Жетнотифинтерфаце
- Метод Жетнотифинтерфаце, интерфейс использованием метода ibackgroundcopyjob
- Интерфейс использованием метода ibackgroundcopyjob, метод Жетнотифинтерфаце
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetNotifyInterface
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6586a90de5783ceb24e5a7677f699a9cf6dfa60c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691958"
---
# <a name="ibackgroundcopyjobgetnotifyinterface-method"></a><span data-ttu-id="4fc35-106">Метод использованием метода ibackgroundcopyjob:: Жетнотифинтерфаце</span><span class="sxs-lookup"><span data-stu-id="4fc35-106">IBackgroundCopyJob::GetNotifyInterface method</span></span>

<span data-ttu-id="4fc35-107">Получает указатель интерфейса на реализацию интерфейса [**ибаккграундкопикаллбакк**](ibackgroundcopycallback.md) .</span><span class="sxs-lookup"><span data-stu-id="4fc35-107">Retrieves the interface pointer to your implementation of the [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="4fc35-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4fc35-108">Syntax</span></span>


```C++
HRESULT GetNotifyInterface(
  [out] IUnknown **ppNotifyInterface
);
```



## <a name="parameters"></a><span data-ttu-id="4fc35-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="4fc35-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4fc35-110">*ппнотифинтерфаце* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="4fc35-110">*ppNotifyInterface* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4fc35-111">Указатель интерфейса на реализацию интерфейса [**ибаккграундкопикаллбакк**](ibackgroundcopycallback.md) .</span><span class="sxs-lookup"><span data-stu-id="4fc35-111">Interface pointer to your implementation of the [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) interface.</span></span> <span data-ttu-id="4fc35-112">По завершении выпустите *ппнотифинтерфаце*.</span><span class="sxs-lookup"><span data-stu-id="4fc35-112">When done, release *ppNotifyInterface*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4fc35-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4fc35-113">Return value</span></span>

<span data-ttu-id="4fc35-114">Этот метод возвращает следующие значения **HRESULT** , а также другие.</span><span class="sxs-lookup"><span data-stu-id="4fc35-114">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="4fc35-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="4fc35-115">Return code</span></span>                                                                              | <span data-ttu-id="4fc35-116">Описание</span><span class="sxs-lookup"><span data-stu-id="4fc35-116">Description</span></span>                                                           |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <span data-ttu-id="4fc35-117"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="4fc35-117"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="4fc35-118">Указатель интерфейса уведомления успешно извлечен.</span><span class="sxs-lookup"><span data-stu-id="4fc35-118">Notification interface pointer was successfully retrieved.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="4fc35-119">Требования</span><span class="sxs-lookup"><span data-stu-id="4fc35-119">Requirements</span></span>



| <span data-ttu-id="4fc35-120">Требование</span><span class="sxs-lookup"><span data-stu-id="4fc35-120">Requirement</span></span> | <span data-ttu-id="4fc35-121">Значение</span><span class="sxs-lookup"><span data-stu-id="4fc35-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4fc35-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4fc35-122">Minimum supported client</span></span><br/> | <span data-ttu-id="4fc35-123">\[Только для настольных приложений Windows 10 версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="4fc35-123">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="4fc35-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4fc35-124">Minimum supported server</span></span><br/> | <span data-ttu-id="4fc35-125">\[Только для настольных приложений Windows Server версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="4fc35-125">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="4fc35-126">Header</span><span class="sxs-lookup"><span data-stu-id="4fc35-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="4fc35-127"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="4fc35-127"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="4fc35-128">IDL</span><span class="sxs-lookup"><span data-stu-id="4fc35-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4fc35-129"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4fc35-129"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="4fc35-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4fc35-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="4fc35-131"><dt>Досвк. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4fc35-131"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="4fc35-132">DLL</span><span class="sxs-lookup"><span data-stu-id="4fc35-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4fc35-133"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4fc35-133"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="4fc35-134">IID</span><span class="sxs-lookup"><span data-stu-id="4fc35-134">IID</span></span><br/>                      | <span data-ttu-id="4fc35-135">IID_IBackgroundCopyJob определен как 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="4fc35-135">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="4fc35-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4fc35-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fc35-137">**Использованием метода ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="4fc35-137">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="4fc35-138">**ибаккграундкопикаллбакк**</span><span class="sxs-lookup"><span data-stu-id="4fc35-138">**IBackgroundCopyCallback**</span></span>](ibackgroundcopycallback.md)
</dt> <dt>

[<span data-ttu-id="4fc35-139">**Использованием метода ibackgroundcopyjob:: Жетнотифифлагс**</span><span class="sxs-lookup"><span data-stu-id="4fc35-139">**IBackgroundCopyJob::GetNotifyFlags**</span></span>](ibackgroundcopyjob-getnotifyflags.md)
</dt> <dt>

[<span data-ttu-id="4fc35-140">**Использованием метода ibackgroundcopyjob:: Сетнотифинтерфаце**</span><span class="sxs-lookup"><span data-stu-id="4fc35-140">**IBackgroundCopyJob::SetNotifyInterface**</span></span>](ibackgroundcopyjob-setnotifyinterface.md)
</dt> </dl>

 

 





