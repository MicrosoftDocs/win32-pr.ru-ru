---
title: 'Метод IDeliveryOptimizationFile2:: SetProperty'
description: 'Этот метод возвращает одно свойство файла DO. | Метод IDeliveryOptimizationFile2:: SetProperty'
keywords:
- SetProperty — метод
- Метод SetProperty, интерфейс IDeliveryOptimizationFile2
- Интерфейс IDeliveryOptimizationFile2, метод SetProperty
topic_type:
- apiref
api_name:
- IDeliveryOptimizationFile2.SetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 74113fca944e79e9ecba8f822f73769775631821
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105713397"
---
# <a name="ideliveryoptimizationfile2setproperty-method"></a><span data-ttu-id="d5919-107">Метод IDeliveryOptimizationFile2:: SetProperty</span><span class="sxs-lookup"><span data-stu-id="d5919-107">IDeliveryOptimizationFile2::SetProperty method</span></span>

<span data-ttu-id="d5919-108">Этот метод возвращает одно свойство файла DO.</span><span class="sxs-lookup"><span data-stu-id="d5919-108">This method returns a single property of the DO file.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5919-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d5919-109">Syntax</span></span>

```C++
HRESULT SetProperty(
  [in]               DOFilePropertyId propId,
  [in, unique] const VARIANT          *propValue
);
```

## <a name="parameters"></a><span data-ttu-id="d5919-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="d5919-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5919-111">*propId* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d5919-111">*propId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5919-112">Обязательный идентификатор свойства для набора типа Дофилепропертид.</span><span class="sxs-lookup"><span data-stu-id="d5919-112">The required property ID to set of type DOFilePropertyId.</span></span>

</dd> <dt>

<span data-ttu-id="d5919-113">*пропвалуе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d5919-113">*propValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5919-114">Заданное значение свойства типа VARIANT.</span><span class="sxs-lookup"><span data-stu-id="d5919-114">The property value to set, of type VARIANT.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5919-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d5919-115">Return value</span></span>

<span data-ttu-id="d5919-116">Этот метод возвращает следующие значения HRESULT.</span><span class="sxs-lookup"><span data-stu-id="d5919-116">This method returns the following HRESULT values.</span></span>

| <span data-ttu-id="d5919-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="d5919-117">Return code</span></span>                  | <span data-ttu-id="d5919-118">Описание</span><span class="sxs-lookup"><span data-stu-id="d5919-118">Description</span></span>                                                        |
|------------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="d5919-119">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="d5919-119">**S_OK**</span></span>                     | <span data-ttu-id="d5919-120">Успешно</span><span class="sxs-lookup"><span data-stu-id="d5919-120">Success</span></span>                                                            |
| <span data-ttu-id="d5919-121">**DO_E_UNKNOWN_PROPERTY_ID**</span><span class="sxs-lookup"><span data-stu-id="d5919-121">**DO_E_UNKNOWN_PROPERTY_ID**</span></span> | <span data-ttu-id="d5919-122">Неизвестный идентификатор свойства</span><span class="sxs-lookup"><span data-stu-id="d5919-122">Unknown property ID</span></span>                                                |
| <span data-ttu-id="d5919-123">**DO_E_INVALID_STATE**</span><span class="sxs-lookup"><span data-stu-id="d5919-123">**DO_E_INVALID_STATE**</span></span>       | <span data-ttu-id="d5919-124">Задание в настоящее время не находится в состоянии, допускающем установку свойства</span><span class="sxs-lookup"><span data-stu-id="d5919-124">The job is not currently in a state that allows a property setting</span></span> |

## <a name="requirements"></a><span data-ttu-id="d5919-125">Требования</span><span class="sxs-lookup"><span data-stu-id="d5919-125">Requirements</span></span>

| <span data-ttu-id="d5919-126">Требование</span><span class="sxs-lookup"><span data-stu-id="d5919-126">Requirement</span></span> | <span data-ttu-id="d5919-127">Значение</span><span class="sxs-lookup"><span data-stu-id="d5919-127">Value</span></span> |
|---------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="d5919-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d5919-128">Minimum supported client</span></span>  | <span data-ttu-id="d5919-129">\[Только для настольных приложений Windows 10 версии 1803\]</span><span class="sxs-lookup"><span data-stu-id="d5919-129">Windows 10, version 1803 \[desktop apps only\]</span></span>                                   |
| <span data-ttu-id="d5919-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d5919-130">Minimum supported server</span></span>  | <span data-ttu-id="d5919-131">\[Только для настольных приложений Windows Server версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="d5919-131">Windows Server, version 1709 \[desktop apps only\]</span></span>                               |
| <span data-ttu-id="d5919-132">Header</span><span class="sxs-lookup"><span data-stu-id="d5919-132">Header</span></span>                    | <span data-ttu-id="d5919-133">Deliveryoptimization. h</span><span class="sxs-lookup"><span data-stu-id="d5919-133">Deliveryoptimization.h</span></span>                                                           |
| <span data-ttu-id="d5919-134">IDL</span><span class="sxs-lookup"><span data-stu-id="d5919-134">IDL</span></span>                       | <span data-ttu-id="d5919-135">DeliveryOptimization. idl</span><span class="sxs-lookup"><span data-stu-id="d5919-135">DeliveryOptimization.idl</span></span>                                                         |
| <span data-ttu-id="d5919-136">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d5919-136">Library</span></span>                   | <span data-ttu-id="d5919-137">Досвк. lib</span><span class="sxs-lookup"><span data-stu-id="d5919-137">Dosvc.lib</span></span>                                                                        |
| <span data-ttu-id="d5919-138">DLL</span><span class="sxs-lookup"><span data-stu-id="d5919-138">DLL</span></span>                       | <span data-ttu-id="d5919-139">Dosvc.dll</span><span class="sxs-lookup"><span data-stu-id="d5919-139">Dosvc.dll</span></span>                                                                        |
| <span data-ttu-id="d5919-140">IID</span><span class="sxs-lookup"><span data-stu-id="d5919-140">IID</span></span>                       | <span data-ttu-id="d5919-141">IID_IDeliveryOptimizationJob2 определен как 18995A26-BF59-4ABE-9F8B-D5092D5A2405</span><span class="sxs-lookup"><span data-stu-id="d5919-141">IID_IDeliveryOptimizationJob2 is defined as 18995A26-BF59-4ABE-9F8B-D5092D5A2405</span></span> |

## <a name="see-also"></a><span data-ttu-id="d5919-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d5919-142">See also</span></span>

[<span data-ttu-id="d5919-143">**IDeliveryOptimizationFile2**</span><span class="sxs-lookup"><span data-stu-id="d5919-143">**IDeliveryOptimizationFile2**</span></span>](ideliveryoptimizationfile2.md)
