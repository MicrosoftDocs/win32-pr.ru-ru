---
description: Метод Жетипортабледевицевалуесвалуе извлекает значение Ипортабледевицевалуес (тип VT \_ Unknown), заданный ключом.
ms.assetid: bf62c6a9-560b-4667-94d0-2dea6657eed1
title: 'Метод Ипортабледевицевалуес:: Жетипортабледевицевалуесвалуе (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetIPortableDeviceValuesValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 9583ea157c1e3395fd9814b1a2e78af3f1985b9c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649043"
---
# <a name="iportabledevicevaluesgetiportabledevicevaluesvalue-method"></a><span data-ttu-id="35394-103">Метод Ипортабледевицевалуес:: Жетипортабледевицевалуесвалуе</span><span class="sxs-lookup"><span data-stu-id="35394-103">IPortableDeviceValues::GetIPortableDeviceValuesValue method</span></span>

<span data-ttu-id="35394-104">Метод **жетипортабледевицевалуесвалуе** извлекает значение **ИПОРТАБЛЕДЕВИЦЕВАЛУЕС** (тип VT \_ Unknown), заданный ключом.</span><span class="sxs-lookup"><span data-stu-id="35394-104">The **GetIPortableDeviceValuesValue** method retrieves an **IPortableDeviceValues** value (type VT\_UNKNOWN) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="35394-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="35394-105">Syntax</span></span>


```C++
HRESULT GetIPortableDeviceValuesValue(
  [in]  REFPROPERTYKEY        key,
  [out] IPortableDeviceValues **ppValue
);
```



## <a name="parameters"></a><span data-ttu-id="35394-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="35394-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35394-107">*ключ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="35394-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35394-108">Ключ **рефпропертикэй** , указывающий извлекаемый элемент.</span><span class="sxs-lookup"><span data-stu-id="35394-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="35394-109">*ппвалуе* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="35394-109">*ppValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="35394-110">Адрес переменной, которая получает указатель на полученный интерфейс [**ипортабледевицевалуес**](iportabledevicevalues.md) .</span><span class="sxs-lookup"><span data-stu-id="35394-110">Address of a variable that receives a pointer to the retrieved [**IPortableDeviceValues**](iportabledevicevalues.md) interface.</span></span> <span data-ttu-id="35394-111">Вызывающий объект отвечает за вызов метода **Release** на полученном интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="35394-111">The caller is responsible for calling **Release** on the retrieved interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35394-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="35394-112">Return value</span></span>

<span data-ttu-id="35394-113">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="35394-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="35394-114">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="35394-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="35394-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="35394-115">Return code</span></span>                                                                                                            | <span data-ttu-id="35394-116">Описание</span><span class="sxs-lookup"><span data-stu-id="35394-116">Description</span></span>                                                                               |
|------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="35394-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="35394-117"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="35394-118">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="35394-118">The method succeeded.</span></span><br/>                                                          |
| <dl> <span data-ttu-id="35394-119"><dt>**\_вытипемисматч E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="35394-119"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="35394-120">Свойство, заданное *ключом* , не является интерфейсом **ипортабледевицевалуес** .</span><span class="sxs-lookup"><span data-stu-id="35394-120">The property specified by *key* is not an **IPortableDeviceValues** interface.</span></span><br/> |
| <dl> <span data-ttu-id="35394-121"><dt>**HRESULT \_ из \_ Win32 (ошибка \_ не \_ найдена)**</dt></span><span class="sxs-lookup"><span data-stu-id="35394-121"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="35394-122">Свойство, указанное *ключом* , отсутствует в коллекции.</span><span class="sxs-lookup"><span data-stu-id="35394-122">The property specified by *key* is not in the collection.</span></span><br/>                      |



 

## <a name="examples"></a><span data-ttu-id="35394-123">Примеры</span><span class="sxs-lookup"><span data-stu-id="35394-123">Examples</span></span>

<span data-ttu-id="35394-124">Пример использования этого метода см. в разделе [Получение поддерживаемых событий службы](retrieving-supported-events.md).</span><span class="sxs-lookup"><span data-stu-id="35394-124">For an example of how to use this method, see [Retrieving Supported Service Events](retrieving-supported-events.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="35394-125">Требования</span><span class="sxs-lookup"><span data-stu-id="35394-125">Requirements</span></span>



| <span data-ttu-id="35394-126">Требование</span><span class="sxs-lookup"><span data-stu-id="35394-126">Requirement</span></span> | <span data-ttu-id="35394-127">Значение</span><span class="sxs-lookup"><span data-stu-id="35394-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35394-128">Header</span><span class="sxs-lookup"><span data-stu-id="35394-128">Header</span></span><br/>  | <dl> <span data-ttu-id="35394-129"><dt>Портабледевицетипес. h</dt></span><span class="sxs-lookup"><span data-stu-id="35394-129"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="35394-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="35394-130">Library</span></span><br/> | <dl> <span data-ttu-id="35394-131"><dt>Портабледевицегуидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="35394-131"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35394-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="35394-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35394-133">**Интерфейс Ипортабледевицевалуес**</span><span class="sxs-lookup"><span data-stu-id="35394-133">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="35394-134">**Ипортабледевицевалуес:: Сетипортабледевицевалуесвалуе**</span><span class="sxs-lookup"><span data-stu-id="35394-134">**IPortableDeviceValues::SetIPortableDeviceValuesValue**</span></span>](iportabledevicevalues-setiportabledevicevaluesvalue.md)
</dt> <dt>

[<span data-ttu-id="35394-135">Получение поддерживаемых событий службы</span><span class="sxs-lookup"><span data-stu-id="35394-135">Retrieving Supported Service Events</span></span>](retrieving-supported-events.md)
</dt> <dt>

[<span data-ttu-id="35394-136">Получение возможностей отрисовки, поддерживаемых устройством</span><span class="sxs-lookup"><span data-stu-id="35394-136">Retrieving the Rendering Capabilities Supported by a Device</span></span>](retrieving-the-rendering-capabilities-supported-by-a-device.md)
</dt> </dl>

 

 




