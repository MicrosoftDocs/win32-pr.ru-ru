---
description: 'Метод Ипортабледевицепропвариантколлектион:: GetAt — метод GetAt извлекает элемент из коллекции по индексу, начинающимся с нуля.'
ms.assetid: c7119ba6-e6fc-4cb6-a8ab-3bf7b6bfe850
title: 'Метод Ипортабледевицепропвариантколлектион:: GetAt (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.GetAt
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: b901e8fcfa065813e4c0942632f80901800ef0a9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106802"
---
# <a name="iportabledevicepropvariantcollectiongetat-method"></a><span data-ttu-id="5e096-103">Метод Ипортабледевицепропвариантколлектион:: GetAt</span><span class="sxs-lookup"><span data-stu-id="5e096-103">IPortableDevicePropVariantCollection::GetAt method</span></span>

<span data-ttu-id="5e096-104">Метод **GetAt** извлекает элемент из коллекции по индексу, начинающимся с нуля.</span><span class="sxs-lookup"><span data-stu-id="5e096-104">The **GetAt** method retrieves an item from the collection by a zero-based index.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e096-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5e096-105">Syntax</span></span>


```C++
HRESULT GetAt(
  [in]  const DWORD       dwIndex,
  [out]       PROPVARIANT *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="5e096-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5e096-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e096-107">*двиндекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5e096-107">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e096-108">Значение **типа DWORD** , содержащее Отсчитываемый от нуля индекс извлекаемого элемента.</span><span class="sxs-lookup"><span data-stu-id="5e096-108">**DWORD** that contains the zero-based index of the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="5e096-109">*pValue* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="5e096-109">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5e096-110">Указатель на структуру **пропвариант** .</span><span class="sxs-lookup"><span data-stu-id="5e096-110">Pointer to a **PROPVARIANT** structure.</span></span> <span data-ttu-id="5e096-111">Вызывающий объект отвечает за освобождение этой памяти путем вызова **пропвариантклеар**.</span><span class="sxs-lookup"><span data-stu-id="5e096-111">The caller is responsible for freeing this memory by calling **PropVariantClear**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e096-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5e096-112">Return value</span></span>

<span data-ttu-id="5e096-113">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="5e096-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="5e096-114">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="5e096-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="5e096-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="5e096-115">Return code</span></span>                                                                                  | <span data-ttu-id="5e096-116">Описание</span><span class="sxs-lookup"><span data-stu-id="5e096-116">Description</span></span>                                               |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <span data-ttu-id="5e096-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="5e096-117"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="5e096-118">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="5e096-118">The method succeeded.</span></span><br/>                          |
| <dl> <span data-ttu-id="5e096-119"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="5e096-119"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="5e096-120">Обязательный аргумент-указатель имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="5e096-120">A required pointer argument was **NULL**.</span></span><br/>      |
| <dl> <span data-ttu-id="5e096-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="5e096-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="5e096-122">Переданный индекс был вне допустимого диапазона.</span><span class="sxs-lookup"><span data-stu-id="5e096-122">The index that was passed in was out of range.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="5e096-123">Примеры</span><span class="sxs-lookup"><span data-stu-id="5e096-123">Examples</span></span>

<span data-ttu-id="5e096-124">Пример использования этого метода см. [в статье получение функциональных категорий, поддерживаемых устройством](retrieving-the-functional-categories-supported-by-a-device.md).</span><span class="sxs-lookup"><span data-stu-id="5e096-124">For an example of how to use this method see [Retrieving the Functional Categories Supported by a Device](retrieving-the-functional-categories-supported-by-a-device.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5e096-125">Требования</span><span class="sxs-lookup"><span data-stu-id="5e096-125">Requirements</span></span>



| <span data-ttu-id="5e096-126">Требование</span><span class="sxs-lookup"><span data-stu-id="5e096-126">Requirement</span></span> | <span data-ttu-id="5e096-127">Значение</span><span class="sxs-lookup"><span data-stu-id="5e096-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e096-128">Header</span><span class="sxs-lookup"><span data-stu-id="5e096-128">Header</span></span><br/>  | <dl> <span data-ttu-id="5e096-129"><dt>Портабледевицетипес. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e096-129"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="5e096-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5e096-130">Library</span></span><br/> | <dl> <span data-ttu-id="5e096-131"><dt>Портабледевицегуидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5e096-131"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e096-132">См. также</span><span class="sxs-lookup"><span data-stu-id="5e096-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e096-133">**Интерфейс Ипортабледевицепропвариантколлектион**</span><span class="sxs-lookup"><span data-stu-id="5e096-133">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="5e096-134">Получение идентификатора объекта из постоянного уникального идентификатора</span><span class="sxs-lookup"><span data-stu-id="5e096-134">Retrieving an Object Identifier from a Persistent Unique Identifier</span></span>](retrieving-an-object-identifier-from-a-persistent-unique-identifier.md)
</dt> <dt>

[<span data-ttu-id="5e096-135">Получение поддерживаемых событий службы</span><span class="sxs-lookup"><span data-stu-id="5e096-135">Retrieving Supported Service Events</span></span>](retrieving-supported-events.md)
</dt> <dt>

[<span data-ttu-id="5e096-136">Получение поддерживаемых форматов службы</span><span class="sxs-lookup"><span data-stu-id="5e096-136">Retrieving Supported Service Formats</span></span>](retrieving-supported-formats.md)
</dt> <dt>

[<span data-ttu-id="5e096-137">Получение поддерживаемых методов службы</span><span class="sxs-lookup"><span data-stu-id="5e096-137">Retrieving Supported Service Methods</span></span>](retrieving-supported-methods.md)
</dt> <dt>

[<span data-ttu-id="5e096-138">Получение типов содержимого, поддерживаемых устройством</span><span class="sxs-lookup"><span data-stu-id="5e096-138">Retrieving the Content Types Supported by a Device</span></span>](retrieving-the-content-types-supported-by-a-device.md)
</dt> <dt>

[<span data-ttu-id="5e096-139">Получение функциональных категорий, поддерживаемых устройством</span><span class="sxs-lookup"><span data-stu-id="5e096-139">Retrieving the Functional Categories Supported by a Device</span></span>](retrieving-the-functional-categories-supported-by-a-device.md)
</dt> <dt>

[<span data-ttu-id="5e096-140">Получение идентификаторов функциональных объектов для устройства</span><span class="sxs-lookup"><span data-stu-id="5e096-140">Retrieving the Functional Object Identifiers for a Device</span></span>](retrieving-the-functional-object-identifiers-for-a-device.md)
</dt> <dt>

[<span data-ttu-id="5e096-141">Получение возможностей отрисовки, поддерживаемых устройством</span><span class="sxs-lookup"><span data-stu-id="5e096-141">Retrieving the Rendering Capabilities Supported by a Device</span></span>](retrieving-the-rendering-capabilities-supported-by-a-device.md)
</dt> <dt>

[<span data-ttu-id="5e096-142">Задание свойств для нескольких объектов</span><span class="sxs-lookup"><span data-stu-id="5e096-142">Setting Properties for Multiple Objects</span></span>](setting-properties-for-multiple-objects.md)
</dt> </dl>

 

 




