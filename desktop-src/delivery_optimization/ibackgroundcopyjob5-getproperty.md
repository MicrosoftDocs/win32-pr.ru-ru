---
title: Метод IBackgroundCopyJob5-Property (Deliveryoptimization. h)
description: Универсальный метод для получения свойств задания оптимизации доставки (DO).
ms.assetid: 22BA2FAB-3F24-4801-8FB7-CB6F9E8DFBB3
keywords:
- Метод GetProperty
- Метод Property, интерфейс IBackgroundCopyJob5
- Интерфейс IBackgroundCopyJob5, метод метода Property
topic_type:
- apiref
api_name:
- IBackgroundCopyJob5.GetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8200bb63a131db6fcab30b77f35a89fc9c943675
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988744"
---
# <a name="ibackgroundcopyjob5getproperty-method"></a><span data-ttu-id="d1ae3-106">IBackgroundCopyJob5:: метод Property</span><span class="sxs-lookup"><span data-stu-id="d1ae3-106">IBackgroundCopyJob5::GetProperty method</span></span>

<span data-ttu-id="d1ae3-107">Универсальный метод для получения свойств задания оптимизации доставки (DO).</span><span class="sxs-lookup"><span data-stu-id="d1ae3-107">A generic method for getting Delivery Optimization (DO) job properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1ae3-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d1ae3-108">Syntax</span></span>


```C++
HRESULT GetProperty(
  [in]  BITS_JOB_PROPERTY_ID    PropertyId,
  [out] BITS_JOB_PROPERTY_VALUE *pPropertyValue
);
```



## <a name="parameters"></a><span data-ttu-id="d1ae3-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="d1ae3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1ae3-110">*PropertyId* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d1ae3-110">*PropertyId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1ae3-111">Идентификатор свойства, которое получается в виде значения перечисления [**BITS_JOB_PROPERTY_ID**](bits-job-property-id.md) .</span><span class="sxs-lookup"><span data-stu-id="d1ae3-111">The ID of the property that is being obtained specified as a [**BITS_JOB_PROPERTY_ID**](bits-job-property-id.md) enum value.</span></span>

</dd> <dt>

<span data-ttu-id="d1ae3-112">*ппропертивалуе* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d1ae3-112">*pPropertyValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d1ae3-113">Значение свойства, возвращаемое в виде BITS_JOB_PROPERTY_VALUE объединения.</span><span class="sxs-lookup"><span data-stu-id="d1ae3-113">The property value returned as a BITS_JOB_PROPERTY_VALUE union.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1ae3-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d1ae3-114">Return value</span></span>

<span data-ttu-id="d1ae3-115">Метод возвращает следующие возвращаемые значения.</span><span class="sxs-lookup"><span data-stu-id="d1ae3-115">The method returns the following return values.</span></span>



| <span data-ttu-id="d1ae3-116">Код возврата</span><span class="sxs-lookup"><span data-stu-id="d1ae3-116">Return code</span></span>                                                                          | <span data-ttu-id="d1ae3-117">Описание</span><span class="sxs-lookup"><span data-stu-id="d1ae3-117">Description</span></span>        |
|--------------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="d1ae3-118"><dt>**S_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d1ae3-118"><dt>**S_OK**</dt></span></span> </dl> | <span data-ttu-id="d1ae3-119">Успешно</span><span class="sxs-lookup"><span data-stu-id="d1ae3-119">Success</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="d1ae3-120">Требования</span><span class="sxs-lookup"><span data-stu-id="d1ae3-120">Requirements</span></span>



| <span data-ttu-id="d1ae3-121">Требование</span><span class="sxs-lookup"><span data-stu-id="d1ae3-121">Requirement</span></span> | <span data-ttu-id="d1ae3-122">Значение</span><span class="sxs-lookup"><span data-stu-id="d1ae3-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1ae3-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d1ae3-123">Minimum supported client</span></span><br/> | <span data-ttu-id="d1ae3-124">\[Только для настольных приложений Windows 10 версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="d1ae3-124">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="d1ae3-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d1ae3-125">Minimum supported server</span></span><br/> | <span data-ttu-id="d1ae3-126">\[Только для настольных приложений Windows Server версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="d1ae3-126">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="d1ae3-127">Header</span><span class="sxs-lookup"><span data-stu-id="d1ae3-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1ae3-128"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1ae3-128"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="d1ae3-129">IDL</span><span class="sxs-lookup"><span data-stu-id="d1ae3-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d1ae3-130"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d1ae3-130"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="d1ae3-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d1ae3-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="d1ae3-132"><dt>Досвк. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d1ae3-132"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="d1ae3-133">DLL</span><span class="sxs-lookup"><span data-stu-id="d1ae3-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d1ae3-134"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d1ae3-134"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="d1ae3-135">IID</span><span class="sxs-lookup"><span data-stu-id="d1ae3-135">IID</span></span><br/>                      | <span data-ttu-id="d1ae3-136">IID_IBackgroundCopyJob5 определяется как E847030C-БББА-4657-AF6D-484AA42BF1FE</span><span class="sxs-lookup"><span data-stu-id="d1ae3-136">IID_IBackgroundCopyJob5 is defined as E847030C-BBBA-4657-AF6D-484AA42BF1FE</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="d1ae3-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d1ae3-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1ae3-138">**IBackgroundCopyJob5**</span><span class="sxs-lookup"><span data-stu-id="d1ae3-138">**IBackgroundCopyJob5**</span></span>](ibackgroundcopyjob5.md)
</dt> <dt>

[<span data-ttu-id="d1ae3-139">**IBackgroundCopyJob5:: SetProperty**</span><span class="sxs-lookup"><span data-stu-id="d1ae3-139">**IBackgroundCopyJob5::SetProperty**</span></span>](ibackgroundcopyjob5-setproperty.md)
</dt> </dl>

 

 





