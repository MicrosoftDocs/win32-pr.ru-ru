---
title: Метод использованием метода ibackgroundcopyjob GetId (Deliveryoptimization. h)
description: Возвращает идентификатор, используемый для идентификации задания в очереди.
ms.assetid: 05CE5420-22F8-4CFE-BC40-3A29C775854B
keywords:
- GetId - метод
- Метод GetId, интерфейс использованием метода ibackgroundcopyjob
- Интерфейс использованием метода ibackgroundcopyjob, метод GetId
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetId
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ade12d72d68b43df7d9ae3d1f33010bb95b7052a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691840"
---
# <a name="ibackgroundcopyjobgetid-method"></a><span data-ttu-id="a7a2d-106">Метод использованием метода ibackgroundcopyjob:: GetId</span><span class="sxs-lookup"><span data-stu-id="a7a2d-106">IBackgroundCopyJob::GetId method</span></span>

<span data-ttu-id="a7a2d-107">Возвращает идентификатор, используемый для идентификации задания в очереди.</span><span class="sxs-lookup"><span data-stu-id="a7a2d-107">Retrieves the identifier used to identify the job in the queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7a2d-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a7a2d-108">Syntax</span></span>


```C++
HRESULT GetId(
  [out] GUID *pJobID
);
```



## <a name="parameters"></a><span data-ttu-id="a7a2d-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="a7a2d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7a2d-110">*пжобид* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="a7a2d-110">*pJobID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a7a2d-111">Идентификатор GUID, определяющий задание в очереди DO.</span><span class="sxs-lookup"><span data-stu-id="a7a2d-111">GUID that identifies the job within the DO queue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7a2d-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a7a2d-112">Return value</span></span>

<span data-ttu-id="a7a2d-113">Этот метод возвращает **S_OK** при успешном или одном из стандартных значений **HRESULT** com при ошибке.</span><span class="sxs-lookup"><span data-stu-id="a7a2d-113">This method returns **S_OK** on success or one of the standard COM **HRESULT** values on error.</span></span>

## <a name="remarks"></a><span data-ttu-id="a7a2d-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a7a2d-114">Remarks</span></span>

<span data-ttu-id="a7a2d-115">Служба создает идентификатор при [создании](ibackgroundcopymanager-createjob.md) задания.</span><span class="sxs-lookup"><span data-stu-id="a7a2d-115">The service generates the identifier when you [create](ibackgroundcopymanager-createjob.md) the job.</span></span> <span data-ttu-id="a7a2d-116">Чтобы использовать идентификатор для получения указателя на интерфейс [**использованием метода ibackgroundcopyjob**](ibackgroundcopyjob-.md) для задания, вызовите метод [**Ибаккграундкопиманажер:: жетжоб**](ibackgroundcopymanager-getjob.md) .</span><span class="sxs-lookup"><span data-stu-id="a7a2d-116">To use the identifier to retrieve an [**IBackgroundCopyJob**](ibackgroundcopyjob-.md) interface pointer for the job, call the [**IBackgroundCopyManager::GetJob**](ibackgroundcopymanager-getjob.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7a2d-117">Требования</span><span class="sxs-lookup"><span data-stu-id="a7a2d-117">Requirements</span></span>



| <span data-ttu-id="a7a2d-118">Требование</span><span class="sxs-lookup"><span data-stu-id="a7a2d-118">Requirement</span></span> | <span data-ttu-id="a7a2d-119">Значение</span><span class="sxs-lookup"><span data-stu-id="a7a2d-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7a2d-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a7a2d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a7a2d-121">\[Только для настольных приложений Windows 10 версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="a7a2d-121">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="a7a2d-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a7a2d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a7a2d-123">\[Только для настольных приложений Windows Server версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="a7a2d-123">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="a7a2d-124">Header</span><span class="sxs-lookup"><span data-stu-id="a7a2d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a7a2d-125"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="a7a2d-125"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="a7a2d-126">IDL</span><span class="sxs-lookup"><span data-stu-id="a7a2d-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a7a2d-127"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a7a2d-127"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="a7a2d-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a7a2d-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="a7a2d-129"><dt>Досвк. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a7a2d-129"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="a7a2d-130">DLL</span><span class="sxs-lookup"><span data-stu-id="a7a2d-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a7a2d-131"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a7a2d-131"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="a7a2d-132">IID</span><span class="sxs-lookup"><span data-stu-id="a7a2d-132">IID</span></span><br/>                      | <span data-ttu-id="a7a2d-133">IID_IBackgroundCopyJob определен как 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="a7a2d-133">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="a7a2d-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a7a2d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7a2d-135">**Использованием метода ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="a7a2d-135">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="a7a2d-136">**Ибаккграундкопиманажер:: CreateJob**</span><span class="sxs-lookup"><span data-stu-id="a7a2d-136">**IBackgroundCopyManager::CreateJob**</span></span>](ibackgroundcopymanager-createjob.md)
</dt> <dt>

[<span data-ttu-id="a7a2d-137">**Ибаккграундкопиманажер:: Жетжоб**</span><span class="sxs-lookup"><span data-stu-id="a7a2d-137">**IBackgroundCopyManager::GetJob**</span></span>](ibackgroundcopymanager-getjob.md)
</dt> </dl>

 

 





