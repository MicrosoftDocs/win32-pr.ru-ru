---
description: Метод Жетипортабледевицевалуесколлектионвалуе извлекает значение Ипортабледевицевалуесколлектион (тип VT \_ Unknown), заданный ключом.
ms.assetid: 07b41ef8-d299-4d69-98ad-f1818c09ef6c
title: 'Метод Ипортабледевицевалуес:: Жетипортабледевицевалуесколлектионвалуе (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetIPortableDeviceValuesCollectionValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 3db3b8410ca82a97a41fdf45ee3f866cb8d2e4b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704286"
---
# <a name="iportabledevicevaluesgetiportabledevicevaluescollectionvalue-method"></a><span data-ttu-id="65c38-103">Метод Ипортабледевицевалуес:: Жетипортабледевицевалуесколлектионвалуе</span><span class="sxs-lookup"><span data-stu-id="65c38-103">IPortableDeviceValues::GetIPortableDeviceValuesCollectionValue method</span></span>

<span data-ttu-id="65c38-104">Метод **жетипортабледевицевалуесколлектионвалуе** извлекает значение **ИПОРТАБЛЕДЕВИЦЕВАЛУЕСКОЛЛЕКТИОН** (тип VT \_ Unknown), заданный ключом.</span><span class="sxs-lookup"><span data-stu-id="65c38-104">The **GetIPortableDeviceValuesCollectionValue** method retrieves an **IPortableDeviceValuesCollection** value (type VT\_UNKNOWN) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="65c38-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="65c38-105">Syntax</span></span>


```C++
HRESULT GetIPortableDeviceValuesCollectionValue(
  [in]  REFPROPERTYKEY                  key,
  [out] IPortableDeviceValuesCollection **ppValue
);
```



## <a name="parameters"></a><span data-ttu-id="65c38-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="65c38-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65c38-107">*ключ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="65c38-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65c38-108">Ключ **рефпропертикэй** , указывающий извлекаемый элемент.</span><span class="sxs-lookup"><span data-stu-id="65c38-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="65c38-109">*ппвалуе* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="65c38-109">*ppValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="65c38-110">Адрес переменной, которая получает указатель на полученный интерфейс [**ипортабледевицевалуесколлектион**](iportabledevicevaluescollection.md) .</span><span class="sxs-lookup"><span data-stu-id="65c38-110">Address of a variable that receives a pointer to the retrieved [**IPortableDeviceValuesCollection**](iportabledevicevaluescollection.md) interface.</span></span> <span data-ttu-id="65c38-111">Вызывающий объект отвечает за вызов метода **Release** на полученном интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="65c38-111">The caller is responsible for calling **Release** on the retrieved interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65c38-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="65c38-112">Return value</span></span>

<span data-ttu-id="65c38-113">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="65c38-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="65c38-114">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="65c38-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="65c38-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="65c38-115">Return code</span></span>                                                                                                            | <span data-ttu-id="65c38-116">Описание</span><span class="sxs-lookup"><span data-stu-id="65c38-116">Description</span></span>                                                                                         |
|------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="65c38-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="65c38-117"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="65c38-118">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="65c38-118">The method succeeded.</span></span><br/>                                                                    |
| <dl> <span data-ttu-id="65c38-119"><dt>**\_вытипемисматч E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="65c38-119"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="65c38-120">Свойство, заданное *ключом* , не является интерфейсом **ипортабледевицевалуесколлектион** .</span><span class="sxs-lookup"><span data-stu-id="65c38-120">The property specified by *key* is not an **IPortableDeviceValuesCollection** interface.</span></span><br/> |
| <dl> <span data-ttu-id="65c38-121"><dt>**HRESULT \_ из \_ Win32 (ошибка \_ не \_ найдена)**</dt></span><span class="sxs-lookup"><span data-stu-id="65c38-121"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="65c38-122">Свойство, указанное *ключом* , отсутствует в коллекции.</span><span class="sxs-lookup"><span data-stu-id="65c38-122">The property specified by *key* is not in the collection.</span></span><br/>                                |



 

## <a name="examples"></a><span data-ttu-id="65c38-123">Примеры</span><span class="sxs-lookup"><span data-stu-id="65c38-123">Examples</span></span>

<span data-ttu-id="65c38-124">Пример использования этого метода см. [в разделе Получение возможностей отрисовки, поддерживаемых устройством](retrieving-the-rendering-capabilities-supported-by-a-device.md).</span><span class="sxs-lookup"><span data-stu-id="65c38-124">For an example of how to use this method, see [Retrieving the Rendering Capabilities Supported by a Device](retrieving-the-rendering-capabilities-supported-by-a-device.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="65c38-125">Требования</span><span class="sxs-lookup"><span data-stu-id="65c38-125">Requirements</span></span>



| <span data-ttu-id="65c38-126">Требование</span><span class="sxs-lookup"><span data-stu-id="65c38-126">Requirement</span></span> | <span data-ttu-id="65c38-127">Значение</span><span class="sxs-lookup"><span data-stu-id="65c38-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65c38-128">Header</span><span class="sxs-lookup"><span data-stu-id="65c38-128">Header</span></span><br/>  | <dl> <span data-ttu-id="65c38-129"><dt>Портабледевицетипес. h</dt></span><span class="sxs-lookup"><span data-stu-id="65c38-129"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="65c38-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="65c38-130">Library</span></span><br/> | <dl> <span data-ttu-id="65c38-131"><dt>Портабледевицегуидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="65c38-131"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65c38-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="65c38-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65c38-133">**Интерфейс Ипортабледевицевалуес**</span><span class="sxs-lookup"><span data-stu-id="65c38-133">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="65c38-134">Получение возможностей отрисовки, поддерживаемых устройством</span><span class="sxs-lookup"><span data-stu-id="65c38-134">Retrieving the Rendering Capabilities Supported by a Device</span></span>](retrieving-the-rendering-capabilities-supported-by-a-device.md)
</dt> <dt>

[<span data-ttu-id="65c38-135">**сетипортабледевицевалуесколлектионвалуе**</span><span class="sxs-lookup"><span data-stu-id="65c38-135">**SetIPortableDeviceValuesCollectionValue**</span></span>](iportabledevicevalues-setiportabledevicevaluescollectionvalue.md)
</dt> </dl>

 

 




