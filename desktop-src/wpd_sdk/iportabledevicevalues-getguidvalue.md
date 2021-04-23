---
description: Метод Жетгуидвалуе извлекает значение GUID (тип VT \_ CLSID), заданное ключом.
ms.assetid: 1cfa75e8-2c3b-4893-954e-dae25a6b8220
title: 'Метод Ипортабледевицевалуес:: Жетгуидвалуе (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetGuidValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 362672daad835a2e843edeaf6dc517884c25f1ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649025"
---
# <a name="iportabledevicevaluesgetguidvalue-method"></a><span data-ttu-id="f5ebb-103">Метод Ипортабледевицевалуес:: Жетгуидвалуе</span><span class="sxs-lookup"><span data-stu-id="f5ebb-103">IPortableDeviceValues::GetGuidValue method</span></span>

<span data-ttu-id="f5ebb-104">Метод **жетгуидвалуе** извлекает значение **GUID** (тип VT \_ CLSID), заданное ключом.</span><span class="sxs-lookup"><span data-stu-id="f5ebb-104">The **GetGuidValue** method retrieves a **GUID** value (type VT\_CLSID) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5ebb-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f5ebb-105">Syntax</span></span>


```C++
HRESULT GetGuidValue(
  [in]  REFPROPERTYKEY key,
  [out] GUID           *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="f5ebb-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f5ebb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5ebb-107">*ключ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f5ebb-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5ebb-108">Ключ **рефпропертикэй** , указывающий извлекаемый элемент.</span><span class="sxs-lookup"><span data-stu-id="f5ebb-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="f5ebb-109">*pValue* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f5ebb-109">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f5ebb-110">Указатель на полученное значение **GUID** .</span><span class="sxs-lookup"><span data-stu-id="f5ebb-110">Pointer to the retrieved **GUID** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5ebb-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f5ebb-111">Return value</span></span>

<span data-ttu-id="f5ebb-112">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="f5ebb-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="f5ebb-113">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="f5ebb-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="f5ebb-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="f5ebb-114">Return code</span></span>                                                                                                            | <span data-ttu-id="f5ebb-115">Описание</span><span class="sxs-lookup"><span data-stu-id="f5ebb-115">Description</span></span>                                                          |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <span data-ttu-id="f5ebb-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="f5ebb-116"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="f5ebb-117">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="f5ebb-117">The method succeeded.</span></span><br/>                                     |
| <dl> <span data-ttu-id="f5ebb-118"><dt>**\_вытипемисматч E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f5ebb-118"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="f5ebb-119">Свойство, указанное *ключом* , не является типом **GUID** .</span><span class="sxs-lookup"><span data-stu-id="f5ebb-119">The property specified by *key* is not a **GUID** type.</span></span><br/>   |
| <dl> <span data-ttu-id="f5ebb-120"><dt>**HRESULT \_ из \_ Win32 (ошибка \_ не \_ найдена)**</dt></span><span class="sxs-lookup"><span data-stu-id="f5ebb-120"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="f5ebb-121">Свойство, указанное *ключом* , отсутствует в коллекции.</span><span class="sxs-lookup"><span data-stu-id="f5ebb-121">The property specified by *key* is not in the collection.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="f5ebb-122">Примеры</span><span class="sxs-lookup"><span data-stu-id="f5ebb-122">Examples</span></span>

<span data-ttu-id="f5ebb-123">Пример использования этого метода см. в разделе [Получение поддерживаемых методов службы](retrieving-supported-methods.md).</span><span class="sxs-lookup"><span data-stu-id="f5ebb-123">For an example of how to use this method, see [Retrieving Supported Service Methods](retrieving-supported-methods.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f5ebb-124">Требования</span><span class="sxs-lookup"><span data-stu-id="f5ebb-124">Requirements</span></span>



| <span data-ttu-id="f5ebb-125">Требование</span><span class="sxs-lookup"><span data-stu-id="f5ebb-125">Requirement</span></span> | <span data-ttu-id="f5ebb-126">Значение</span><span class="sxs-lookup"><span data-stu-id="f5ebb-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5ebb-127">Header</span><span class="sxs-lookup"><span data-stu-id="f5ebb-127">Header</span></span><br/>  | <dl> <span data-ttu-id="f5ebb-128"><dt>Портабледевицетипес. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5ebb-128"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="f5ebb-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f5ebb-129">Library</span></span><br/> | <dl> <span data-ttu-id="f5ebb-130"><dt>Портабледевицегуидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f5ebb-130"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5ebb-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f5ebb-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5ebb-132">**Интерфейс Ипортабледевицевалуес**</span><span class="sxs-lookup"><span data-stu-id="f5ebb-132">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="f5ebb-133">**Ипортабледевицевалуес:: Сетгуидвалуе**</span><span class="sxs-lookup"><span data-stu-id="f5ebb-133">**IPortableDeviceValues::SetGuidValue**</span></span>](iportabledevicevalues-setguidvalue.md)
</dt> <dt>

[<span data-ttu-id="f5ebb-134">Получение поддерживаемых методов службы</span><span class="sxs-lookup"><span data-stu-id="f5ebb-134">Retrieving Supported Service Methods</span></span>](retrieving-supported-methods.md)
</dt> <dt>

[<span data-ttu-id="f5ebb-135">Получение возможностей отрисовки, поддерживаемых устройством</span><span class="sxs-lookup"><span data-stu-id="f5ebb-135">Retrieving the Rendering Capabilities Supported by a Device</span></span>](retrieving-the-rendering-capabilities-supported-by-a-device.md)
</dt> </dl>

 

 




