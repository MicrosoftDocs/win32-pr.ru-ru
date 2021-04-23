---
title: 'Метод IDeliveryOptimizationJob2:: SetProperty'
description: Этот метод не используется.
keywords:
- SetProperty — метод
- Метод SetProperty, интерфейс IDeliveryOptimizationJob2
- Интерфейс IDeliveryOptimizationJob2, метод SetProperty
topic_type:
- apiref
api_name:
- IDeliveryOptimizationJob2.SetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 41375ac3949dd4bcbdd22944f1f1a11d461fc3ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415652"
---
# <a name="ideliveryoptimizationjob2setproperty-method"></a><span data-ttu-id="39dd8-106">Метод IDeliveryOptimizationJob2:: SetProperty</span><span class="sxs-lookup"><span data-stu-id="39dd8-106">IDeliveryOptimizationJob2::SetProperty method</span></span>

<span data-ttu-id="39dd8-107">Этот метод не используется.</span><span class="sxs-lookup"><span data-stu-id="39dd8-107">This method is unused.</span></span>

## <a name="syntax"></a><span data-ttu-id="39dd8-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="39dd8-108">Syntax</span></span>

```C++
HRESULT SetProperty(
  [in]               DOJobPropertyId propId,
  [in, unique] const VARIANT         *propValue
);
```

## <a name="parameters"></a><span data-ttu-id="39dd8-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="39dd8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39dd8-110">*propId* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="39dd8-110">*propId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39dd8-111">Не используется.</span><span class="sxs-lookup"><span data-stu-id="39dd8-111">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="39dd8-112">*пропвалуе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="39dd8-112">*propValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39dd8-113">Не используется.</span><span class="sxs-lookup"><span data-stu-id="39dd8-113">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39dd8-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="39dd8-114">Return value</span></span>

<span data-ttu-id="39dd8-115">Если propId имеет **DOJobPropertyId_ExtendedErrorInfo**, возвращаемое значение равно **DO_E_READ_ONLY_PROPERTY**, в противном случае функция возвращает **DO_E_UNKNOWN_PROPERTY_ID**.</span><span class="sxs-lookup"><span data-stu-id="39dd8-115">If propId is **DOJobPropertyId_ExtendedErrorInfo**, the returned value is **DO_E_READ_ONLY_PROPERTY**, otherwise the function returns **DO_E_UNKNOWN_PROPERTY_ID**.</span></span>

## <a name="requirements"></a><span data-ttu-id="39dd8-116">Требования</span><span class="sxs-lookup"><span data-stu-id="39dd8-116">Requirements</span></span>

| <span data-ttu-id="39dd8-117">Требование</span><span class="sxs-lookup"><span data-stu-id="39dd8-117">Requirement</span></span> | <span data-ttu-id="39dd8-118">Значение</span><span class="sxs-lookup"><span data-stu-id="39dd8-118">Value</span></span> |
|---------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="39dd8-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="39dd8-119">Minimum supported client</span></span>  | <span data-ttu-id="39dd8-120">\[Только для настольных приложений Windows 10 версии 1803\]</span><span class="sxs-lookup"><span data-stu-id="39dd8-120">Windows 10, version 1803 \[desktop apps only\]</span></span>                                   |
| <span data-ttu-id="39dd8-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="39dd8-121">Minimum supported server</span></span>  | <span data-ttu-id="39dd8-122">\[Только для настольных приложений Windows Server версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="39dd8-122">Windows Server, version 1709 \[desktop apps only\]</span></span>                               |
| <span data-ttu-id="39dd8-123">Header</span><span class="sxs-lookup"><span data-stu-id="39dd8-123">Header</span></span>                    | <span data-ttu-id="39dd8-124">Deliveryoptimization. h</span><span class="sxs-lookup"><span data-stu-id="39dd8-124">Deliveryoptimization.h</span></span>                                                           |
| <span data-ttu-id="39dd8-125">IDL</span><span class="sxs-lookup"><span data-stu-id="39dd8-125">IDL</span></span>                       | <span data-ttu-id="39dd8-126">DeliveryOptimization. idl</span><span class="sxs-lookup"><span data-stu-id="39dd8-126">DeliveryOptimization.idl</span></span>                                                         |
| <span data-ttu-id="39dd8-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="39dd8-127">Library</span></span>                   | <span data-ttu-id="39dd8-128">Досвк. lib</span><span class="sxs-lookup"><span data-stu-id="39dd8-128">Dosvc.lib</span></span>                                                                        |
| <span data-ttu-id="39dd8-129">DLL</span><span class="sxs-lookup"><span data-stu-id="39dd8-129">DLL</span></span>                       | <span data-ttu-id="39dd8-130">Dosvc.dll</span><span class="sxs-lookup"><span data-stu-id="39dd8-130">Dosvc.dll</span></span>                                                                        |
| <span data-ttu-id="39dd8-131">IID</span><span class="sxs-lookup"><span data-stu-id="39dd8-131">IID</span></span>                       | <span data-ttu-id="39dd8-132">IID_IDeliveryOptimizationJob2 определен как 18995A26-BF59-4ABE-9F8B-D5092D5A2405</span><span class="sxs-lookup"><span data-stu-id="39dd8-132">IID_IDeliveryOptimizationJob2 is defined as 18995A26-BF59-4ABE-9F8B-D5092D5A2405</span></span> |

## <a name="see-also"></a><span data-ttu-id="39dd8-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="39dd8-133">See also</span></span>

[<span data-ttu-id="39dd8-134">**IDeliveryOptimizationJob2**</span><span class="sxs-lookup"><span data-stu-id="39dd8-134">**IDeliveryOptimizationJob2**</span></span>](ideliveryoptimizationjob2.md)
