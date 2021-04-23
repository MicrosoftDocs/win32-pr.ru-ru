---
title: Метод SetProperty IBackgroundCopyJob5 (Deliveryoptimization. h)
description: Универсальный метод для установки свойств задания оптимизации доставки (DO).
ms.assetid: 9A8CCE04-B3EB-43CC-A135-7054EC40ABEC
keywords:
- SetProperty — метод
- Метод SetProperty, интерфейс IBackgroundCopyJob5
- Интерфейс IBackgroundCopyJob5, метод SetProperty
topic_type:
- apiref
api_name:
- IBackgroundCopyJob5.SetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a3dbd1e7c66592ea959c9b1ff4f4864340c504d8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803293"
---
# <a name="ibackgroundcopyjob5setproperty-method"></a><span data-ttu-id="ef423-106">Метод IBackgroundCopyJob5:: SetProperty</span><span class="sxs-lookup"><span data-stu-id="ef423-106">IBackgroundCopyJob5::SetProperty method</span></span>

<span data-ttu-id="ef423-107">Универсальный метод для установки свойств задания оптимизации доставки (DO).</span><span class="sxs-lookup"><span data-stu-id="ef423-107">A generic method for setting Delivery Optimization (DO) job properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef423-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ef423-108">Syntax</span></span>


```C++
HRESULT SetProperty(
  [in] BITS_JOB_PROPERTY_ID    PropertyId,
  [in] BITS_JOB_PROPERTY_VALUE PropertyValue
);
```



## <a name="parameters"></a><span data-ttu-id="ef423-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="ef423-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef423-110">*PropertyId* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ef423-110">*PropertyId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef423-111">Идентификатор свойства, которое задается как значение перечисления [**BITS_JOB_PROPERTY_ID**](bits-job-property-id.md) .</span><span class="sxs-lookup"><span data-stu-id="ef423-111">The ID of the property that is being set specified as a [**BITS_JOB_PROPERTY_ID**](bits-job-property-id.md) enum value.</span></span>

</dd> <dt>

<span data-ttu-id="ef423-112">*Propertyvalue* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ef423-112">*PropertyValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef423-113">Значение свойства, которое задается.</span><span class="sxs-lookup"><span data-stu-id="ef423-113">The value of the property that is being set.</span></span> <span data-ttu-id="ef423-114">Для хранения значения, тип которого соответствует свойству, это значение указывается с помощью [**BITS_JOB_PROPERTY_VALUE**](bits-job-property-value-.md) объединения, состоящего из всех известных типов свойств.</span><span class="sxs-lookup"><span data-stu-id="ef423-114">In order to hold a value whose type is appropriate to the property, this value is specified via the [**BITS_JOB_PROPERTY_VALUE**](bits-job-property-value-.md) union that is composed of all the known property types.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef423-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ef423-115">Return value</span></span>

<span data-ttu-id="ef423-116">Метод возвращает следующие возвращаемые значения.</span><span class="sxs-lookup"><span data-stu-id="ef423-116">The method returns the following return values.</span></span>



| <span data-ttu-id="ef423-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="ef423-117">Return code</span></span>                                                                          | <span data-ttu-id="ef423-118">Описание</span><span class="sxs-lookup"><span data-stu-id="ef423-118">Description</span></span>        |
|--------------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="ef423-119"><dt>**S_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ef423-119"><dt>**S_OK**</dt></span></span> </dl> | <span data-ttu-id="ef423-120">Успешно</span><span class="sxs-lookup"><span data-stu-id="ef423-120">Success</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ef423-121">Требования</span><span class="sxs-lookup"><span data-stu-id="ef423-121">Requirements</span></span>



| <span data-ttu-id="ef423-122">Требование</span><span class="sxs-lookup"><span data-stu-id="ef423-122">Requirement</span></span> | <span data-ttu-id="ef423-123">Значение</span><span class="sxs-lookup"><span data-stu-id="ef423-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef423-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ef423-124">Minimum supported client</span></span><br/> | <span data-ttu-id="ef423-125">\[Только для настольных приложений Windows 10 версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="ef423-125">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="ef423-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ef423-126">Minimum supported server</span></span><br/> | <span data-ttu-id="ef423-127">\[Только для настольных приложений Windows Server версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="ef423-127">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="ef423-128">Header</span><span class="sxs-lookup"><span data-stu-id="ef423-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef423-129"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef423-129"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="ef423-130">IDL</span><span class="sxs-lookup"><span data-stu-id="ef423-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ef423-131"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ef423-131"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="ef423-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ef423-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="ef423-133"><dt>Досвк. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ef423-133"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="ef423-134">DLL</span><span class="sxs-lookup"><span data-stu-id="ef423-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ef423-135"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ef423-135"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="ef423-136">IID</span><span class="sxs-lookup"><span data-stu-id="ef423-136">IID</span></span><br/>                      | <span data-ttu-id="ef423-137">IID_IBackgroundCopyJob5 определяется как E847030C-БББА-4657-AF6D-484AA42BF1FE</span><span class="sxs-lookup"><span data-stu-id="ef423-137">IID_IBackgroundCopyJob5 is defined as E847030C-BBBA-4657-AF6D-484AA42BF1FE</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="ef423-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ef423-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef423-139">**IBackgroundCopyJob5**</span><span class="sxs-lookup"><span data-stu-id="ef423-139">**IBackgroundCopyJob5**</span></span>](ibackgroundcopyjob5.md)
</dt> <dt>

[<span data-ttu-id="ef423-140">**IBackgroundCopyJob5:: Property**</span><span class="sxs-lookup"><span data-stu-id="ef423-140">**IBackgroundCopyJob5::GetProperty**</span></span>](ibackgroundcopyjob5-getproperty.md)
</dt> </dl>

 

 





