---
description: Метод NOCOUNT извлекает количество элементов в этой коллекции.
ms.assetid: b7c8acd2-67f2-47d3-b42a-26aa701fd613
title: 'Метод Ипортабледевицепропвариантколлектион:: NOCOUNT (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.GetCount
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: d3a06cb5d89bc09a35a58f9269ba19c488c11e0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105721017"
---
# <a name="iportabledevicepropvariantcollectiongetcount-method"></a><span data-ttu-id="653d2-103">Метод Ипортабледевицепропвариантколлектион:: NOCOUNT</span><span class="sxs-lookup"><span data-stu-id="653d2-103">IPortableDevicePropVariantCollection::GetCount method</span></span>

<span data-ttu-id="653d2-104">Метод **NOCOUNT** извлекает количество элементов в этой коллекции.</span><span class="sxs-lookup"><span data-stu-id="653d2-104">The **GetCount** method retrieves the number of items in this collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="653d2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="653d2-105">Syntax</span></span>


```C++
HRESULT GetCount(
  [in] DWORD *pcElems
);
```



## <a name="parameters"></a><span data-ttu-id="653d2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="653d2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="653d2-107">*пцелемс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="653d2-107">*pcElems* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="653d2-108">Указатель на **DWORD** , содержащий число элементов в коллекции.</span><span class="sxs-lookup"><span data-stu-id="653d2-108">Pointer to a **DWORD** that contains the number of items in the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="653d2-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="653d2-109">Return value</span></span>

<span data-ttu-id="653d2-110">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="653d2-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="653d2-111">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="653d2-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="653d2-112">Код возврата</span><span class="sxs-lookup"><span data-stu-id="653d2-112">Return code</span></span>                                                                               | <span data-ttu-id="653d2-113">Описание</span><span class="sxs-lookup"><span data-stu-id="653d2-113">Description</span></span>                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="653d2-114"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="653d2-114"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="653d2-115">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="653d2-115">The method succeeded.</span></span><br/>                     |
| <dl> <span data-ttu-id="653d2-116"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="653d2-116"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="653d2-117">Обязательный аргумент-указатель имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="653d2-117">A required pointer argument was **NULL**.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="653d2-118">Примеры</span><span class="sxs-lookup"><span data-stu-id="653d2-118">Examples</span></span>

<span data-ttu-id="653d2-119">Пример использования этого метода см. [в статье получение функциональных категорий, поддерживаемых устройством](retrieving-the-functional-categories-supported-by-a-device.md).</span><span class="sxs-lookup"><span data-stu-id="653d2-119">For an example of how to use this method see [Retrieving the Functional Categories Supported by a Device](retrieving-the-functional-categories-supported-by-a-device.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="653d2-120">Требования</span><span class="sxs-lookup"><span data-stu-id="653d2-120">Requirements</span></span>



| <span data-ttu-id="653d2-121">Требование</span><span class="sxs-lookup"><span data-stu-id="653d2-121">Requirement</span></span> | <span data-ttu-id="653d2-122">Значение</span><span class="sxs-lookup"><span data-stu-id="653d2-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="653d2-123">Header</span><span class="sxs-lookup"><span data-stu-id="653d2-123">Header</span></span><br/>  | <dl> <span data-ttu-id="653d2-124"><dt>Портабледевицетипес. h</dt></span><span class="sxs-lookup"><span data-stu-id="653d2-124"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="653d2-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="653d2-125">Library</span></span><br/> | <dl> <span data-ttu-id="653d2-126"><dt>Портабледевицегуидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="653d2-126"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="653d2-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="653d2-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="653d2-128">**Интерфейс Ипортабледевицепропвариантколлектион**</span><span class="sxs-lookup"><span data-stu-id="653d2-128">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="653d2-129">Получение поддерживаемых событий службы</span><span class="sxs-lookup"><span data-stu-id="653d2-129">Retrieving Supported Service Events</span></span>](retrieving-supported-events.md)
</dt> <dt>

[<span data-ttu-id="653d2-130">Получение поддерживаемых форматов службы</span><span class="sxs-lookup"><span data-stu-id="653d2-130">Retrieving Supported Service Formats</span></span>](retrieving-supported-formats.md)
</dt> <dt>

[<span data-ttu-id="653d2-131">Получение поддерживаемых методов службы</span><span class="sxs-lookup"><span data-stu-id="653d2-131">Retrieving Supported Service Methods</span></span>](retrieving-supported-methods.md)
</dt> <dt>

[<span data-ttu-id="653d2-132">Получение функциональных категорий, поддерживаемых устройством</span><span class="sxs-lookup"><span data-stu-id="653d2-132">Retrieving the Functional Categories Supported by a Device</span></span>](retrieving-the-functional-categories-supported-by-a-device.md)
</dt> <dt>

[<span data-ttu-id="653d2-133">Задание свойств для нескольких объектов</span><span class="sxs-lookup"><span data-stu-id="653d2-133">Setting Properties for Multiple Objects</span></span>](setting-properties-for-multiple-objects.md)
</dt> </dl>

 

 




