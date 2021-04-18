---
description: Метод Жетипортабледевицепропвариантколлектионвалуе извлекает значение Ипортабледевицепропвариантколлектион (тип VT \_ Unknown), заданный ключом.
ms.assetid: a7b5ba64-c28e-42ae-9f04-2bdb67e93328
title: 'Метод Ипортабледевицевалуес:: Жетипортабледевицепропвариантколлектионвалуе (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetIPortableDevicePropVariantCollectionValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 7deb73d10f2e2daa5d06d6cb4394c43778af2ad4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708572"
---
# <a name="iportabledevicevaluesgetiportabledevicepropvariantcollectionvalue-method"></a><span data-ttu-id="ad7be-103">Метод Ипортабледевицевалуес:: Жетипортабледевицепропвариантколлектионвалуе</span><span class="sxs-lookup"><span data-stu-id="ad7be-103">IPortableDeviceValues::GetIPortableDevicePropVariantCollectionValue method</span></span>

<span data-ttu-id="ad7be-104">Метод **жетипортабледевицепропвариантколлектионвалуе** извлекает значение **ИПОРТАБЛЕДЕВИЦЕПРОПВАРИАНТКОЛЛЕКТИОН** (тип VT \_ Unknown), заданный ключом.</span><span class="sxs-lookup"><span data-stu-id="ad7be-104">The **GetIPortableDevicePropVariantCollectionValue** method retrieves an **IPortableDevicePropVariantCollection** value (type VT\_UNKNOWN) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad7be-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ad7be-105">Syntax</span></span>


```C++
HRESULT GetIPortableDevicePropVariantCollectionValue(
  [in]  REFPROPERTYKEY                       key,
  [out] IPortableDevicePropVariantCollection **ppValue
);
```



## <a name="parameters"></a><span data-ttu-id="ad7be-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ad7be-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad7be-107">*ключ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ad7be-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad7be-108">Ключ **рефпропертикэй** , указывающий извлекаемый элемент.</span><span class="sxs-lookup"><span data-stu-id="ad7be-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="ad7be-109">*ппвалуе* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ad7be-109">*ppValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ad7be-110">Адрес переменной, которая получает указатель на полученный интерфейс [**ипортабледевицепропвариантколлектион**](iportabledevicepropvariantcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="ad7be-110">Address of a variable that receives a pointer to the retrieved [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) interface.</span></span> <span data-ttu-id="ad7be-111">Вызывающий объект отвечает за вызов метода **Release** на полученном интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="ad7be-111">The caller is responsible for calling **Release** on the retrieved interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad7be-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ad7be-112">Return value</span></span>

<span data-ttu-id="ad7be-113">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="ad7be-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="ad7be-114">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="ad7be-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="ad7be-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="ad7be-115">Return code</span></span>                                                                                                            | <span data-ttu-id="ad7be-116">Описание</span><span class="sxs-lookup"><span data-stu-id="ad7be-116">Description</span></span>                                                                                              |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ad7be-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="ad7be-117"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="ad7be-118">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="ad7be-118">The method succeeded.</span></span><br/>                                                                         |
| <dl> <span data-ttu-id="ad7be-119"><dt>**\_вытипемисматч E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ad7be-119"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="ad7be-120">Свойство, заданное *ключом* , не является интерфейсом **ипортабледевицепропвариантколлектион** .</span><span class="sxs-lookup"><span data-stu-id="ad7be-120">The property specified by *key* is not an **IPortableDevicePropVariantCollection** interface.</span></span><br/> |
| <dl> <span data-ttu-id="ad7be-121"><dt>**HRESULT \_ из \_ Win32 (ошибка \_ не \_ найдена)**</dt></span><span class="sxs-lookup"><span data-stu-id="ad7be-121"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="ad7be-122">Свойство, указанное *ключом* , отсутствует в коллекции.</span><span class="sxs-lookup"><span data-stu-id="ad7be-122">The property specified by *key* is not in the collection.</span></span><br/>                                     |



 

## <a name="requirements"></a><span data-ttu-id="ad7be-123">Требования</span><span class="sxs-lookup"><span data-stu-id="ad7be-123">Requirements</span></span>



| <span data-ttu-id="ad7be-124">Требование</span><span class="sxs-lookup"><span data-stu-id="ad7be-124">Requirement</span></span> | <span data-ttu-id="ad7be-125">Значение</span><span class="sxs-lookup"><span data-stu-id="ad7be-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad7be-126">Header</span><span class="sxs-lookup"><span data-stu-id="ad7be-126">Header</span></span><br/>  | <dl> <span data-ttu-id="ad7be-127"><dt>Портабледевицетипес. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad7be-127"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="ad7be-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ad7be-128">Library</span></span><br/> | <dl> <span data-ttu-id="ad7be-129"><dt>Портабледевицегуидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ad7be-129"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad7be-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ad7be-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad7be-131">**Интерфейс Ипортабледевицевалуес**</span><span class="sxs-lookup"><span data-stu-id="ad7be-131">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="ad7be-132">**Ипортабледевицевалуес:: Сетипортабледевицепропвариантколлектионвалуе**</span><span class="sxs-lookup"><span data-stu-id="ad7be-132">**IPortableDeviceValues::SetIPortableDevicePropVariantCollectionValue**</span></span>](iportabledevicevalues-setiportabledevicepropvariantcollectionvalue.md)
</dt> </dl>

 

 




