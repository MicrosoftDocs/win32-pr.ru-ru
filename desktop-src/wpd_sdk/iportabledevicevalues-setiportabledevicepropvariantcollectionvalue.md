---
description: Метод Сетипортабледевицепропвариантколлектионвалуе добавляет новое значение Ипортабледевицепропвариантколлектион (тип VT \_ Unknown) или перезаписывает существующий.
ms.assetid: 8ea6be5e-1d03-4d59-9acc-5cd56ee81cd3
title: 'Метод Ипортабледевицевалуес:: Сетипортабледевицепропвариантколлектионвалуе (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetIPortableDevicePropVariantCollectionValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 1f39ad6745dbf30df87e87be7fba358b4d9ad2c9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704276"
---
# <a name="iportabledevicevaluessetiportabledevicepropvariantcollectionvalue-method"></a><span data-ttu-id="4db57-103">Метод Ипортабледевицевалуес:: Сетипортабледевицепропвариантколлектионвалуе</span><span class="sxs-lookup"><span data-stu-id="4db57-103">IPortableDeviceValues::SetIPortableDevicePropVariantCollectionValue method</span></span>

<span data-ttu-id="4db57-104">Метод **сетипортабледевицепропвариантколлектионвалуе** добавляет новое значение **ИПОРТАБЛЕДЕВИЦЕПРОПВАРИАНТКОЛЛЕКТИОН** (тип VT \_ Unknown) или перезаписывает существующий.</span><span class="sxs-lookup"><span data-stu-id="4db57-104">The **SetIPortableDevicePropVariantCollectionValue** method adds a new **IPortableDevicePropVariantCollection** value (type VT\_UNKNOWN) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="4db57-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4db57-105">Syntax</span></span>


```C++
HRESULT SetIPortableDevicePropVariantCollectionValue(
  [in] REFPROPERTYKEY                       key,
  [in] IPortableDevicePropVariantCollection *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="4db57-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4db57-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4db57-107">*ключ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4db57-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4db57-108">Объект **рефпропертикэй** , указывающий элемент для создания или перезаписи.</span><span class="sxs-lookup"><span data-stu-id="4db57-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="4db57-109">*pValue* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4db57-109">*pValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4db57-110">Указатель на интерфейс **ипортабледевицепропвариантколлектион** , указывающий новое значение.</span><span class="sxs-lookup"><span data-stu-id="4db57-110">Pointer to an **IPortableDevicePropVariantCollection** interface that specifies the new value.</span></span> <span data-ttu-id="4db57-111">Пакет SDK копирует ссылку на отправленный интерфейс и вызывает **AddRef** для него.</span><span class="sxs-lookup"><span data-stu-id="4db57-111">The SDK copies a reference to the submitted interface and calls **AddRef** on it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4db57-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4db57-112">Return value</span></span>

<span data-ttu-id="4db57-113">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="4db57-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="4db57-114">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="4db57-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="4db57-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="4db57-115">Return code</span></span>                                                                          | <span data-ttu-id="4db57-116">Описание</span><span class="sxs-lookup"><span data-stu-id="4db57-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="4db57-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="4db57-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="4db57-118">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="4db57-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4db57-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4db57-119">Remarks</span></span>

<span data-ttu-id="4db57-120">Если существующее значение имеет тот же ключ, что и параметр *Key* , он перезаписывает существующее значение без предупреждения.</span><span class="sxs-lookup"><span data-stu-id="4db57-120">If an existing value has the same key that is specified by the *key* parameter, it overwrites the existing value without any warning.</span></span> <span data-ttu-id="4db57-121">Существующий ключ памяти освобождается соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="4db57-121">The existing key memory is released appropriately.</span></span>

## <a name="requirements"></a><span data-ttu-id="4db57-122">Требования</span><span class="sxs-lookup"><span data-stu-id="4db57-122">Requirements</span></span>



| <span data-ttu-id="4db57-123">Требование</span><span class="sxs-lookup"><span data-stu-id="4db57-123">Requirement</span></span> | <span data-ttu-id="4db57-124">Значение</span><span class="sxs-lookup"><span data-stu-id="4db57-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4db57-125">Header</span><span class="sxs-lookup"><span data-stu-id="4db57-125">Header</span></span><br/>  | <dl> <span data-ttu-id="4db57-126"><dt>Портабледевицетипес. h</dt></span><span class="sxs-lookup"><span data-stu-id="4db57-126"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="4db57-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4db57-127">Library</span></span><br/> | <dl> <span data-ttu-id="4db57-128"><dt>Портабледевицегуидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4db57-128"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4db57-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4db57-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4db57-130">**Интерфейс Ипортабледевицевалуес**</span><span class="sxs-lookup"><span data-stu-id="4db57-130">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="4db57-131">**Ипортабледевицевалуес:: Жетипортабледевицепропвариантколлектионвалуе**</span><span class="sxs-lookup"><span data-stu-id="4db57-131">**IPortableDeviceValues::GetIPortableDevicePropVariantCollectionValue**</span></span>](iportabledevicevalues-getiportabledevicepropvariantcollectionvalue.md)
</dt> </dl>

 

 




