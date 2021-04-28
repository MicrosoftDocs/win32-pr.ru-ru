---
description: 'Метод Ипортабледевицевалуесколлектион:: GetAt — метод GetAt извлекает элемент из коллекции по индексу, начинающимся с нуля.'
ms.assetid: b219b052-a74b-466a-a2ee-d2e9c466f393
title: 'Метод Ипортабледевицевалуесколлектион:: GetAt (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValuesCollection.GetAt
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 2ad10a7b9cc3c252a0cee4cb71df05cb108e0a18
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083262"
---
# <a name="iportabledevicevaluescollectiongetat-method"></a><span data-ttu-id="ecfb0-103">Метод Ипортабледевицевалуесколлектион:: GetAt</span><span class="sxs-lookup"><span data-stu-id="ecfb0-103">IPortableDeviceValuesCollection::GetAt method</span></span>

<span data-ttu-id="ecfb0-104">Метод **GetAt** извлекает элемент из коллекции по индексу, начинающимся с нуля.</span><span class="sxs-lookup"><span data-stu-id="ecfb0-104">The **GetAt** method retrieves an item from the collection by a zero-based index.</span></span>

## <a name="syntax"></a><span data-ttu-id="ecfb0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ecfb0-105">Syntax</span></span>


```C++
HRESULT GetAt(
  [in]  const DWORD                 dwIndex,
  [out]       IPortableDeviceValues **ppValues
);
```



## <a name="parameters"></a><span data-ttu-id="ecfb0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ecfb0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ecfb0-107">*двиндекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ecfb0-107">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ecfb0-108">Значение **типа DWORD** , указывающее Отсчитываемый от нуля индекс в коллекции.</span><span class="sxs-lookup"><span data-stu-id="ecfb0-108">**DWORD** that specifies a zero-based index in the collection.</span></span>

</dd> <dt>

<span data-ttu-id="ecfb0-109">*ппвалуес* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ecfb0-109">*ppValues* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ecfb0-110">Адрес переменной, которая получает указатель на интерфейс [**ипортабледевицевалуес**](iportabledevicevalues.md) из коллекции.</span><span class="sxs-lookup"><span data-stu-id="ecfb0-110">Address of a variable that receives a pointer to an [**IPortableDeviceValues**](iportabledevicevalues.md) interface from the collection.</span></span> <span data-ttu-id="ecfb0-111">Вызывающий объект отвечает за вызов **Release** на этом интерфейсе, когда он выполняется.</span><span class="sxs-lookup"><span data-stu-id="ecfb0-111">The caller is responsible for calling **Release** on this interface when done with it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ecfb0-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ecfb0-112">Return value</span></span>

<span data-ttu-id="ecfb0-113">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="ecfb0-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="ecfb0-114">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="ecfb0-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="ecfb0-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="ecfb0-115">Return code</span></span>                                                                                  | <span data-ttu-id="ecfb0-116">Описание</span><span class="sxs-lookup"><span data-stu-id="ecfb0-116">Description</span></span>                                                                      |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ecfb0-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="ecfb0-117"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="ecfb0-118">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="ecfb0-118">The method succeeded.</span></span><br/>                                                 |
| <dl> <span data-ttu-id="ecfb0-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="ecfb0-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="ecfb0-120">Отсчитываемый от нуля индекс, который был передан, был вне допустимого диапазона.</span><span class="sxs-lookup"><span data-stu-id="ecfb0-120">The zero-based index that was passed in was out of range.</span></span><br/>             |
| <dl> <span data-ttu-id="ecfb0-121"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="ecfb0-121"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="ecfb0-122">Обязательный аргумент-указатель имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="ecfb0-122">A required pointer argument was **NULL**.</span></span><br/>                             |
| <dl> <span data-ttu-id="ecfb0-123"><dt>**\_непредвиденная E**</dt></span><span class="sxs-lookup"><span data-stu-id="ecfb0-123"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="ecfb0-124">Коллекция содержит указатель ипортабледевицевалуес **со значением NULL**  .</span><span class="sxs-lookup"><span data-stu-id="ecfb0-124">The collection contains a **NULL** **IPortableDeviceValues** pointer.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ecfb0-125">Remarks</span><span class="sxs-lookup"><span data-stu-id="ecfb0-125">Remarks</span></span>

<span data-ttu-id="ecfb0-126">Все изменения, внесенные в значения в полученном интерфейсе, будут внесены в версию, хранящуюся в коллекции.</span><span class="sxs-lookup"><span data-stu-id="ecfb0-126">Any changes that are made to values in the retrieved interface will be made to the version stored in the collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="ecfb0-127">Требования</span><span class="sxs-lookup"><span data-stu-id="ecfb0-127">Requirements</span></span>



| <span data-ttu-id="ecfb0-128">Требование</span><span class="sxs-lookup"><span data-stu-id="ecfb0-128">Requirement</span></span> | <span data-ttu-id="ecfb0-129">Значение</span><span class="sxs-lookup"><span data-stu-id="ecfb0-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ecfb0-130">Header</span><span class="sxs-lookup"><span data-stu-id="ecfb0-130">Header</span></span><br/>  | <dl> <span data-ttu-id="ecfb0-131"><dt>Портабледевицетипес. h</dt></span><span class="sxs-lookup"><span data-stu-id="ecfb0-131"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="ecfb0-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ecfb0-132">Library</span></span><br/> | <dl> <span data-ttu-id="ecfb0-133"><dt>Портабледевицегуидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ecfb0-133"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ecfb0-134">См. также</span><span class="sxs-lookup"><span data-stu-id="ecfb0-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecfb0-135">**Интерфейс Ипортабледевицевалуесколлектион**</span><span class="sxs-lookup"><span data-stu-id="ecfb0-135">**IPortableDeviceValuesCollection Interface**</span></span>](iportabledevicevaluescollection.md)
</dt> </dl>

 

 




