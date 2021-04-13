---
title: 'IDeliveryOptimizationFile2:: метод Property'
description: 'Этот метод возвращает одно свойство файла DO. | IDeliveryOptimizationFile2:: метод Property'
keywords:
- Метод GetProperty
- Метод Property, интерфейс IDeliveryOptimizationFile2
- Интерфейс IDeliveryOptimizationFile2, метод метода Property
topic_type:
- apiref
api_name:
- IDeliveryOptimizationFile2.GetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c53167287cf821ceca26782dab9b8011d40a1785
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353725"
---
# <a name="ideliveryoptimizationfile2getproperty-method"></a><span data-ttu-id="c8c99-107">IDeliveryOptimizationFile2:: метод Property</span><span class="sxs-lookup"><span data-stu-id="c8c99-107">IDeliveryOptimizationFile2::GetProperty method</span></span>

<span data-ttu-id="c8c99-108">Этот метод возвращает одно свойство файла DO.</span><span class="sxs-lookup"><span data-stu-id="c8c99-108">This method returns a single property of the DO file.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8c99-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c8c99-109">Syntax</span></span>

```C++
HRESULT GetProperty(
  [in]  DOFilePropertyId propId,
  [out] VARIANT          *propValue
);
```

## <a name="parameters"></a><span data-ttu-id="c8c99-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="c8c99-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8c99-111">*propId* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c8c99-111">*propId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8c99-112">Обязательный идентификатор свойства для получения типа Дофилепропертид.</span><span class="sxs-lookup"><span data-stu-id="c8c99-112">The required property ID to get of type DOFilePropertyId.</span></span>

</dd> <dt>

<span data-ttu-id="c8c99-113">*пропвалуе* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="c8c99-113">*propValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c8c99-114">Значение свойства, хранящееся в ВАРИАНТе.</span><span class="sxs-lookup"><span data-stu-id="c8c99-114">The property value stored in a VARIANT.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8c99-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c8c99-115">Return value</span></span>

<span data-ttu-id="c8c99-116">Этот метод возвращает следующие значения HRESULT.</span><span class="sxs-lookup"><span data-stu-id="c8c99-116">This method returns the following HRESULT values.</span></span>

| <span data-ttu-id="c8c99-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="c8c99-117">Return code</span></span>                  | <span data-ttu-id="c8c99-118">Описание</span><span class="sxs-lookup"><span data-stu-id="c8c99-118">Description</span></span>                                         |
|------------------------------|-----------------------------------------------------|
| <span data-ttu-id="c8c99-119">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="c8c99-119">**S_OK**</span></span>                     | <span data-ttu-id="c8c99-120">Успешно</span><span class="sxs-lookup"><span data-stu-id="c8c99-120">Success</span></span>                                             |
| <span data-ttu-id="c8c99-121">**DO_E_UNKNOWN_PROPERTY_ID**</span><span class="sxs-lookup"><span data-stu-id="c8c99-121">**DO_E_UNKNOWN_PROPERTY_ID**</span></span> | <span data-ttu-id="c8c99-122">Неизвестный идентификатор свойства.</span><span class="sxs-lookup"><span data-stu-id="c8c99-122">Unknown property ID.</span></span>                                |
| <span data-ttu-id="c8c99-123">**DO_E_WRITE_ONLY_PROPERTY**</span><span class="sxs-lookup"><span data-stu-id="c8c99-123">**DO_E_WRITE_ONLY_PROPERTY**</span></span> | <span data-ttu-id="c8c99-124">Свойство доступно только для записи и не может быть прочитано.</span><span class="sxs-lookup"><span data-stu-id="c8c99-124">The property is Write only and cannot be read.</span></span>      |
| <span data-ttu-id="c8c99-125">**E_NOT_SET**</span><span class="sxs-lookup"><span data-stu-id="c8c99-125">**E_NOT_SET**</span></span>                | <span data-ttu-id="c8c99-126">Свойство не было задано с помощью метода SetProperty.</span><span class="sxs-lookup"><span data-stu-id="c8c99-126">No property was set through the SetProperty method.</span></span> |
| <span data-ttu-id="c8c99-127">**E_OUTOFMEMORY**</span><span class="sxs-lookup"><span data-stu-id="c8c99-127">**E_OUTOFMEMORY**</span></span>            |  <span data-ttu-id="c8c99-128">Ошибка выделения памяти</span><span class="sxs-lookup"><span data-stu-id="c8c99-128">Memory allocation failure</span></span>                          |

## <a name="requirements"></a><span data-ttu-id="c8c99-129">Требования</span><span class="sxs-lookup"><span data-stu-id="c8c99-129">Requirements</span></span>

| <span data-ttu-id="c8c99-130">Требование</span><span class="sxs-lookup"><span data-stu-id="c8c99-130">Requirement</span></span> | <span data-ttu-id="c8c99-131">Значение</span><span class="sxs-lookup"><span data-stu-id="c8c99-131">Value</span></span> |
|---------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="c8c99-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c8c99-132">Minimum supported client</span></span>  | <span data-ttu-id="c8c99-133">\[Только для настольных приложений Windows 10 версии 1803\]</span><span class="sxs-lookup"><span data-stu-id="c8c99-133">Windows 10, version 1803 \[desktop apps only\]</span></span>                                   |
| <span data-ttu-id="c8c99-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c8c99-134">Minimum supported server</span></span>  | <span data-ttu-id="c8c99-135">\[Только для настольных приложений Windows Server версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="c8c99-135">Windows Server, version 1709 \[desktop apps only\]</span></span>                               |
| <span data-ttu-id="c8c99-136">Header</span><span class="sxs-lookup"><span data-stu-id="c8c99-136">Header</span></span>                    | <span data-ttu-id="c8c99-137">Deliveryoptimization. h</span><span class="sxs-lookup"><span data-stu-id="c8c99-137">Deliveryoptimization.h</span></span>                                                           |
| <span data-ttu-id="c8c99-138">IDL</span><span class="sxs-lookup"><span data-stu-id="c8c99-138">IDL</span></span>                       | <span data-ttu-id="c8c99-139">DeliveryOptimization. idl</span><span class="sxs-lookup"><span data-stu-id="c8c99-139">DeliveryOptimization.idl</span></span>                                                         |
| <span data-ttu-id="c8c99-140">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c8c99-140">Library</span></span>                   | <span data-ttu-id="c8c99-141">Досвк. lib</span><span class="sxs-lookup"><span data-stu-id="c8c99-141">Dosvc.lib</span></span>                                                                        |
| <span data-ttu-id="c8c99-142">DLL</span><span class="sxs-lookup"><span data-stu-id="c8c99-142">DLL</span></span>                       | <span data-ttu-id="c8c99-143">Dosvc.dll</span><span class="sxs-lookup"><span data-stu-id="c8c99-143">Dosvc.dll</span></span>                                                                        |
| <span data-ttu-id="c8c99-144">IID</span><span class="sxs-lookup"><span data-stu-id="c8c99-144">IID</span></span>                       | <span data-ttu-id="c8c99-145">IID_IDeliveryOptimizationJob2 определен как 18995A26-BF59-4ABE-9F8B-D5092D5A2405</span><span class="sxs-lookup"><span data-stu-id="c8c99-145">IID_IDeliveryOptimizationJob2 is defined as 18995A26-BF59-4ABE-9F8B-D5092D5A2405</span></span> |

## <a name="see-also"></a><span data-ttu-id="c8c99-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c8c99-146">See also</span></span>

[<span data-ttu-id="c8c99-147">**IDeliveryOptimizationFile2**</span><span class="sxs-lookup"><span data-stu-id="c8c99-147">**IDeliveryOptimizationFile2**</span></span>](ideliveryoptimizationfile2.md)
