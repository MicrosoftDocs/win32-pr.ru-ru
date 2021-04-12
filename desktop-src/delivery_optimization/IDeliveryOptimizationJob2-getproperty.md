---
title: 'IDeliveryOptimizationJob2:: метод Property'
description: Возвращает одно свойство задания DO.
keywords:
- Метод GetProperty
- Метод Property, интерфейс IDeliveryOptimizationJob2
- Интерфейс IDeliveryOptimizationJob2, метод метода Property
topic_type:
- apiref
api_name:
- IDeliveryOptimizationJob2.GetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 52e405685534c0dbae7c8c205dc5e114a3dbe68b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489825"
---
# <a name="ideliveryoptimizationjob2getproperty-method"></a><span data-ttu-id="98e0b-106">IDeliveryOptimizationJob2:: метод Property</span><span class="sxs-lookup"><span data-stu-id="98e0b-106">IDeliveryOptimizationJob2::GetProperty method</span></span>

<span data-ttu-id="98e0b-107">Этот метод возвращает одно свойство задания DO.</span><span class="sxs-lookup"><span data-stu-id="98e0b-107">This method returns a single property of the DO job.</span></span>

## <a name="syntax"></a><span data-ttu-id="98e0b-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="98e0b-108">Syntax</span></span>

```C++
HRESULT GetProperty(
  [in]  DOJobPropertyId propId,
  [out] VARIANT         *propValue
);
```

## <a name="parameters"></a><span data-ttu-id="98e0b-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="98e0b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98e0b-110">*propId* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="98e0b-110">*propId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98e0b-111">Требуемый идентификатор свойства для получения.</span><span class="sxs-lookup"><span data-stu-id="98e0b-111">The required property ID to get.</span></span> <span data-ttu-id="98e0b-112">Поддерживается только **DOJobPropertyId_ExtendedErrorInfo** типа VT_BSTR.</span><span class="sxs-lookup"><span data-stu-id="98e0b-112">Only **DOJobPropertyId_ExtendedErrorInfo** of type VT_BSTR is supported.</span></span>

</dd> <dt>

<span data-ttu-id="98e0b-113">*пропвалуе* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="98e0b-113">*propValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="98e0b-114">Результирующее значение свойства, хранящееся в типе VARIANT.</span><span class="sxs-lookup"><span data-stu-id="98e0b-114">The resultant property value, stored in a VARIANT type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98e0b-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="98e0b-115">Return value</span></span>

<span data-ttu-id="98e0b-116">Этот метод возвращает следующие значения HRESULT.</span><span class="sxs-lookup"><span data-stu-id="98e0b-116">This method returns the following HRESULT values.</span></span>

| <span data-ttu-id="98e0b-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="98e0b-117">Return code</span></span>                  | <span data-ttu-id="98e0b-118">Описание</span><span class="sxs-lookup"><span data-stu-id="98e0b-118">Description</span></span>          |
|------------------------------|----------------------|
| <span data-ttu-id="98e0b-119">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="98e0b-119">**S_OK**</span></span>                     | <span data-ttu-id="98e0b-120">Успешно</span><span class="sxs-lookup"><span data-stu-id="98e0b-120">Success</span></span>              |
| <span data-ttu-id="98e0b-121">**DO_E_UNKNOWN_PROPERTY_ID**</span><span class="sxs-lookup"><span data-stu-id="98e0b-121">**DO_E_UNKNOWN_PROPERTY_ID**</span></span> | <span data-ttu-id="98e0b-122">Неизвестный идентификатор свойства.</span><span class="sxs-lookup"><span data-stu-id="98e0b-122">Unknown property ID.</span></span> |

## <a name="requirements"></a><span data-ttu-id="98e0b-123">Требования</span><span class="sxs-lookup"><span data-stu-id="98e0b-123">Requirements</span></span>

| <span data-ttu-id="98e0b-124">Требование</span><span class="sxs-lookup"><span data-stu-id="98e0b-124">Requirement</span></span> | <span data-ttu-id="98e0b-125">Значение</span><span class="sxs-lookup"><span data-stu-id="98e0b-125">Value</span></span> |
|---------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="98e0b-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="98e0b-126">Minimum supported client</span></span>  | <span data-ttu-id="98e0b-127">\[Только для настольных приложений Windows 10 версии 1803\]</span><span class="sxs-lookup"><span data-stu-id="98e0b-127">Windows 10, version 1803 \[desktop apps only\]</span></span>                                   |
| <span data-ttu-id="98e0b-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="98e0b-128">Minimum supported server</span></span>  | <span data-ttu-id="98e0b-129">\[Только для настольных приложений Windows Server версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="98e0b-129">Windows Server, version 1709 \[desktop apps only\]</span></span>                               |
| <span data-ttu-id="98e0b-130">Header</span><span class="sxs-lookup"><span data-stu-id="98e0b-130">Header</span></span>                    | <span data-ttu-id="98e0b-131">Deliveryoptimization. h</span><span class="sxs-lookup"><span data-stu-id="98e0b-131">Deliveryoptimization.h</span></span>                                                           |
| <span data-ttu-id="98e0b-132">IDL</span><span class="sxs-lookup"><span data-stu-id="98e0b-132">IDL</span></span>                       | <span data-ttu-id="98e0b-133">DeliveryOptimization. idl</span><span class="sxs-lookup"><span data-stu-id="98e0b-133">DeliveryOptimization.idl</span></span>                                                         |
| <span data-ttu-id="98e0b-134">Библиотека</span><span class="sxs-lookup"><span data-stu-id="98e0b-134">Library</span></span>                   | <span data-ttu-id="98e0b-135">Досвк. lib</span><span class="sxs-lookup"><span data-stu-id="98e0b-135">Dosvc.lib</span></span>                                                                        |
| <span data-ttu-id="98e0b-136">DLL</span><span class="sxs-lookup"><span data-stu-id="98e0b-136">DLL</span></span>                       | <span data-ttu-id="98e0b-137">Dosvc.dll</span><span class="sxs-lookup"><span data-stu-id="98e0b-137">Dosvc.dll</span></span>                                                                        |
| <span data-ttu-id="98e0b-138">IID</span><span class="sxs-lookup"><span data-stu-id="98e0b-138">IID</span></span>                       | <span data-ttu-id="98e0b-139">IID_IDeliveryOptimizationJob2 определен как 18995A26-BF59-4ABE-9F8B-D5092D5A2405</span><span class="sxs-lookup"><span data-stu-id="98e0b-139">IID_IDeliveryOptimizationJob2 is defined as 18995A26-BF59-4ABE-9F8B-D5092D5A2405</span></span> |

## <a name="see-also"></a><span data-ttu-id="98e0b-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="98e0b-140">See also</span></span>

[<span data-ttu-id="98e0b-141">**IDeliveryOptimizationJob2**</span><span class="sxs-lookup"><span data-stu-id="98e0b-141">**IDeliveryOptimizationJob2**</span></span>](ideliveryoptimizationjob2.md)
