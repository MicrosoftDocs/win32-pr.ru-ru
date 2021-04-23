---
description: Метод GetAt извлекает значение из коллекции, используя указанный индекс, начинающийся с нуля.
ms.assetid: d52675f0-55b4-43ef-bb1d-ff6aa8a70647
title: 'Метод Ипортабледевицевалуес:: GetAt (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetAt
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 44126b69dc4e8720fde687d47dc70dd97e104c72
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648795"
---
# <a name="iportabledevicevaluesgetat-method"></a><span data-ttu-id="227dd-103">Метод Ипортабледевицевалуес:: GetAt</span><span class="sxs-lookup"><span data-stu-id="227dd-103">IPortableDeviceValues::GetAt method</span></span>

<span data-ttu-id="227dd-104">Метод **GetAt** извлекает значение из коллекции, используя указанный индекс, начинающийся с нуля.</span><span class="sxs-lookup"><span data-stu-id="227dd-104">The **GetAt** method retrieves a value from the collection using the supplied zero-based index.</span></span>

## <a name="syntax"></a><span data-ttu-id="227dd-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="227dd-105">Syntax</span></span>


```C++
HRESULT GetAt(
  [in]      const DWORD       index,
  [in, out]       PROPERTYKEY *pKey,
  [in, out]       PROPVARIANT *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="227dd-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="227dd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="227dd-107">*индекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="227dd-107">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="227dd-108">Значение **типа DWORD** , указывающее Отсчитываемый от нуля индекс в коллекции.</span><span class="sxs-lookup"><span data-stu-id="227dd-108">A **DWORD** that specifies a zero-based index in the collection.</span></span>

</dd> <dt>

<span data-ttu-id="227dd-109">*pKey* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="227dd-109">*pKey* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="227dd-110">Необязательный указатель **PROPERTYKEY** , извлекающий ключ указанного элемента.</span><span class="sxs-lookup"><span data-stu-id="227dd-110">An optional **PROPERTYKEY** pointer that retrieves the key of the specified item.</span></span>

</dd> <dt>

<span data-ttu-id="227dd-111">*pValue* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="227dd-111">*pValue* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="227dd-112">Необязательный **пропвариант** , который получает значение указанного элемента.</span><span class="sxs-lookup"><span data-stu-id="227dd-112">An optional **PROPVARIANT** that retrieves the value of the specified item.</span></span> <span data-ttu-id="227dd-113">Вызывающий объект должен освободить память, вызвав **пропвариантклеар** , когда завершится с ней.</span><span class="sxs-lookup"><span data-stu-id="227dd-113">The caller must free the memory by calling **PropVariantClear** when done with it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="227dd-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="227dd-114">Return value</span></span>

<span data-ttu-id="227dd-115">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="227dd-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="227dd-116">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="227dd-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="227dd-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="227dd-117">Return code</span></span>                                                                                  | <span data-ttu-id="227dd-118">Описание</span><span class="sxs-lookup"><span data-stu-id="227dd-118">Description</span></span>                                       |
|----------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <span data-ttu-id="227dd-119"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="227dd-119"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="227dd-120">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="227dd-120">The method succeeded.</span></span><br/>                  |
| <dl> <span data-ttu-id="227dd-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="227dd-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="227dd-122">Указан недопустимый номер индекса.</span><span class="sxs-lookup"><span data-stu-id="227dd-122">An invalid index number was specified.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="227dd-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="227dd-123">Remarks</span></span>

<span data-ttu-id="227dd-124">Если свойство указывает значение типа VT \_ Unknown, свойство будет одним из портативных устройств Windows ([**ипортабледевицекэйколлектион**](iportabledevicekeycollection.md), [**Ипортабледевицевалуесколлектион**](iportabledevicevaluescollection.md), [**ипортабледевицевалуес**](iportabledevicevalues.md) или [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md)).</span><span class="sxs-lookup"><span data-stu-id="227dd-124">If a property indicates a value of type VT\_UNKNOWN, the property will be one of the Windows Portable Devices ([**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md), [**IPortableDeviceValuesCollection**](iportabledevicevaluescollection.md), [**IPortableDeviceValues**](iportabledevicevalues.md) or [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md)).</span></span> <span data-ttu-id="227dd-125">Переносные устройства Windows не могут возвращать другие интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="227dd-125">No other interfaces can be returned by Windows Portable Devices.</span></span>

## <a name="requirements"></a><span data-ttu-id="227dd-126">Требования</span><span class="sxs-lookup"><span data-stu-id="227dd-126">Requirements</span></span>



| <span data-ttu-id="227dd-127">Требование</span><span class="sxs-lookup"><span data-stu-id="227dd-127">Requirement</span></span> | <span data-ttu-id="227dd-128">Значение</span><span class="sxs-lookup"><span data-stu-id="227dd-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="227dd-129">Header</span><span class="sxs-lookup"><span data-stu-id="227dd-129">Header</span></span><br/>  | <dl> <span data-ttu-id="227dd-130"><dt>Портабледевицетипес. h</dt></span><span class="sxs-lookup"><span data-stu-id="227dd-130"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="227dd-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="227dd-131">Library</span></span><br/> | <dl> <span data-ttu-id="227dd-132"><dt>Портабледевицегуидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="227dd-132"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="227dd-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="227dd-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="227dd-134">**Интерфейс Ипортабледевицевалуес**</span><span class="sxs-lookup"><span data-stu-id="227dd-134">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="227dd-135">**Ипортабледевицевалуес:: GetStringValue**</span><span class="sxs-lookup"><span data-stu-id="227dd-135">**IPortableDeviceValues::GetStringValue**</span></span>](iportabledevicevalues-getstringvalue.md)
</dt> </dl>

 

 




