---
description: Метод Жетунсигнединтежервалуе извлекает значение типа ULONG (тип VT \_ UI4), заданное ключом.
ms.assetid: 167163fa-6583-4e6b-b801-3a441a95644b
title: 'Метод Ипортабледевицевалуес:: Жетунсигнединтежервалуе (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetUnsignedIntegerValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 5c7deb0b6ebfdb8feb90248f9d8e1cdf68411d9d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648041"
---
# <a name="iportabledevicevaluesgetunsignedintegervalue-method"></a><span data-ttu-id="2c435-103">Метод Ипортабледевицевалуес:: Жетунсигнединтежервалуе</span><span class="sxs-lookup"><span data-stu-id="2c435-103">IPortableDeviceValues::GetUnsignedIntegerValue method</span></span>

<span data-ttu-id="2c435-104">Метод **жетунсигнединтежервалуе** извлекает значение типа **ulong** (тип VT \_ UI4), заданное ключом.</span><span class="sxs-lookup"><span data-stu-id="2c435-104">The **GetUnsignedIntegerValue** method retrieves a **ULONG** value (type VT\_UI4) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c435-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2c435-105">Syntax</span></span>


```C++
HRESULT GetUnsignedIntegerValue(
  [in]  REFPROPERTYKEY key,
  [out] ULONG          *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="2c435-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2c435-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c435-107">*ключ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2c435-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c435-108">Ключ **рефпропертикэй** , указывающий извлекаемый элемент.</span><span class="sxs-lookup"><span data-stu-id="2c435-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="2c435-109">*pValue* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="2c435-109">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2c435-110">Указатель на полученное значение **ulong** .</span><span class="sxs-lookup"><span data-stu-id="2c435-110">Pointer to the retrieved **ULONG** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c435-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2c435-111">Return value</span></span>

<span data-ttu-id="2c435-112">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="2c435-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="2c435-113">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="2c435-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="2c435-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="2c435-114">Return code</span></span>                                                                                                            | <span data-ttu-id="2c435-115">Описание</span><span class="sxs-lookup"><span data-stu-id="2c435-115">Description</span></span>                                                          |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <span data-ttu-id="2c435-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="2c435-116"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="2c435-117">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="2c435-117">The method succeeded.</span></span><br/>                                     |
| <dl> <span data-ttu-id="2c435-118"><dt>**\_вытипемисматч E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2c435-118"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="2c435-119">Свойство, указанное *ключом* , не является типом **ulong** .</span><span class="sxs-lookup"><span data-stu-id="2c435-119">The property specified by *key* is not a **ULONG** type.</span></span><br/>  |
| <dl> <span data-ttu-id="2c435-120"><dt>**HRESULT \_ из \_ Win32 (ошибка \_ не \_ найдена)**</dt></span><span class="sxs-lookup"><span data-stu-id="2c435-120"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="2c435-121">Свойство, указанное *ключом* , отсутствует в коллекции.</span><span class="sxs-lookup"><span data-stu-id="2c435-121">The property specified by *key* is not in the collection.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="2c435-122">Примеры</span><span class="sxs-lookup"><span data-stu-id="2c435-122">Examples</span></span>

<span data-ttu-id="2c435-123">Пример использования этого метода см. в разделе [Получение поддерживаемых событий службы](retrieving-supported-events.md).</span><span class="sxs-lookup"><span data-stu-id="2c435-123">For an example of how to use this method, see [Retrieving Supported Service Events](retrieving-supported-events.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2c435-124">Требования</span><span class="sxs-lookup"><span data-stu-id="2c435-124">Requirements</span></span>



| <span data-ttu-id="2c435-125">Требование</span><span class="sxs-lookup"><span data-stu-id="2c435-125">Requirement</span></span> | <span data-ttu-id="2c435-126">Значение</span><span class="sxs-lookup"><span data-stu-id="2c435-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c435-127">Header</span><span class="sxs-lookup"><span data-stu-id="2c435-127">Header</span></span><br/>  | <dl> <span data-ttu-id="2c435-128"><dt>Портабледевицетипес. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c435-128"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="2c435-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2c435-129">Library</span></span><br/> | <dl> <span data-ttu-id="2c435-130"><dt>Портабледевицегуидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2c435-130"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c435-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2c435-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c435-132">**Интерфейс Ипортабледевицевалуес**</span><span class="sxs-lookup"><span data-stu-id="2c435-132">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="2c435-133">**Ипортабледевицевалуес:: Сетунсигнединтежервалуе**</span><span class="sxs-lookup"><span data-stu-id="2c435-133">**IPortableDeviceValues::SetUnsignedIntegerValue**</span></span>](iportabledevicevalues-setunsignedintegervalue.md)
</dt> <dt>

[<span data-ttu-id="2c435-134">Получение поддерживаемых событий службы</span><span class="sxs-lookup"><span data-stu-id="2c435-134">Retrieving Supported Service Events</span></span>](retrieving-supported-events.md)
</dt> <dt>

[<span data-ttu-id="2c435-135">Получение поддерживаемых методов службы</span><span class="sxs-lookup"><span data-stu-id="2c435-135">Retrieving Supported Service Methods</span></span>](retrieving-supported-methods.md)
</dt> <dt>

[<span data-ttu-id="2c435-136">Получение возможностей отрисовки, поддерживаемых устройством</span><span class="sxs-lookup"><span data-stu-id="2c435-136">Retrieving the Rendering Capabilities Supported by a Device</span></span>](retrieving-the-rendering-capabilities-supported-by-a-device.md)
</dt> </dl>

 

 




