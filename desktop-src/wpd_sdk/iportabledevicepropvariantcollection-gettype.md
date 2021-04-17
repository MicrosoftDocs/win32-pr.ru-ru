---
description: Метод GetType Извлекает тип данных элементов в коллекции.
ms.assetid: 2e389090-74ef-47af-9490-a4820d925246
title: 'Метод Ипортабледевицепропвариантколлектион:: GetType (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.GetType
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: de5ea5b1eeaa9cf494c24e13b8b9b36f7490b84d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685266"
---
# <a name="iportabledevicepropvariantcollectiongettype-method"></a><span data-ttu-id="5bc67-103">Метод Ипортабледевицепропвариантколлектион:: GetType</span><span class="sxs-lookup"><span data-stu-id="5bc67-103">IPortableDevicePropVariantCollection::GetType method</span></span>

<span data-ttu-id="5bc67-104">Метод **GetType** Извлекает тип данных элементов в коллекции.</span><span class="sxs-lookup"><span data-stu-id="5bc67-104">The **GetType** method retrieves the data type of the items in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="5bc67-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5bc67-105">Syntax</span></span>


```C++
HRESULT GetType(
  [out] VARTYPE *pvt
);
```



## <a name="parameters"></a><span data-ttu-id="5bc67-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5bc67-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5bc67-107">*ПВТ* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="5bc67-107">*pvt* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5bc67-108">Значение перечисления **VarType** SDK платформы, указывающее тип данных всех элементов в коллекции.</span><span class="sxs-lookup"><span data-stu-id="5bc67-108">A Platform SDK **VARTYPE** enumeration value that indicates the data type of all the items in the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5bc67-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5bc67-109">Return value</span></span>

<span data-ttu-id="5bc67-110">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="5bc67-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="5bc67-111">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="5bc67-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="5bc67-112">Код возврата</span><span class="sxs-lookup"><span data-stu-id="5bc67-112">Return code</span></span>                                                                               | <span data-ttu-id="5bc67-113">Описание</span><span class="sxs-lookup"><span data-stu-id="5bc67-113">Description</span></span>                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="5bc67-114"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="5bc67-114"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="5bc67-115">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="5bc67-115">The method succeeded.</span></span><br/>                     |
| <dl> <span data-ttu-id="5bc67-116"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="5bc67-116"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="5bc67-117">Обязательный аргумент-указатель имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="5bc67-117">A required pointer argument was **NULL**.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5bc67-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5bc67-118">Remarks</span></span>

<span data-ttu-id="5bc67-119">Все элементы, хранящиеся в **ипортабледевицепропвариантколлектион** , имеют один и тот же тип.</span><span class="sxs-lookup"><span data-stu-id="5bc67-119">All items that are stored in an **IPortableDevicePropVariantCollection** are the same type.</span></span>

## <a name="requirements"></a><span data-ttu-id="5bc67-120">Требования</span><span class="sxs-lookup"><span data-stu-id="5bc67-120">Requirements</span></span>



| <span data-ttu-id="5bc67-121">Требование</span><span class="sxs-lookup"><span data-stu-id="5bc67-121">Requirement</span></span> | <span data-ttu-id="5bc67-122">Значение</span><span class="sxs-lookup"><span data-stu-id="5bc67-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5bc67-123">Header</span><span class="sxs-lookup"><span data-stu-id="5bc67-123">Header</span></span><br/>  | <dl> <span data-ttu-id="5bc67-124"><dt>Портабледевицетипес. h</dt></span><span class="sxs-lookup"><span data-stu-id="5bc67-124"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="5bc67-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5bc67-125">Library</span></span><br/> | <dl> <span data-ttu-id="5bc67-126"><dt>Портабледевицегуидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5bc67-126"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5bc67-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5bc67-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5bc67-128">**Интерфейс Ипортабледевицепропвариантколлектион**</span><span class="sxs-lookup"><span data-stu-id="5bc67-128">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> </dl>

 

 




