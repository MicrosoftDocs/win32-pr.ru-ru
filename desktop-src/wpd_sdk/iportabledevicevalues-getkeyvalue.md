---
description: Метод Жеткэйвалуе извлекает значение PROPERTYKEY, заданное ключом.
ms.assetid: 2c92b1c0-3ea6-4a14-8b63-d57752b649b8
title: 'Метод Ипортабледевицевалуес:: Жеткэйвалуе (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetKeyValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 3d5080a35faa5555d2813c6e419a1965def05bdd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648646"
---
# <a name="iportabledevicevaluesgetkeyvalue-method"></a><span data-ttu-id="43861-103">Метод Ипортабледевицевалуес:: Жеткэйвалуе</span><span class="sxs-lookup"><span data-stu-id="43861-103">IPortableDeviceValues::GetKeyValue method</span></span>

<span data-ttu-id="43861-104">Метод **жеткэйвалуе** извлекает значение **PROPERTYKEY** , заданное ключом.</span><span class="sxs-lookup"><span data-stu-id="43861-104">The **GetKeyValue** method retrieves a **PROPERTYKEY** value specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="43861-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="43861-105">Syntax</span></span>


```C++
HRESULT GetKeyValue(
  [in]  REFPROPERTYKEY key,
  [out] PROPERTYKEY    *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="43861-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="43861-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43861-107">*ключ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="43861-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43861-108">Ключ **рефпропертикэй** , указывающий извлекаемый элемент.</span><span class="sxs-lookup"><span data-stu-id="43861-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="43861-109">*pValue* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="43861-109">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="43861-110">Указатель на полученное значение **PROPERTYKEY** .</span><span class="sxs-lookup"><span data-stu-id="43861-110">Pointer to the retrieved **PROPERTYKEY** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43861-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="43861-111">Return value</span></span>

<span data-ttu-id="43861-112">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="43861-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="43861-113">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="43861-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="43861-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="43861-114">Return code</span></span>                                                                                                            | <span data-ttu-id="43861-115">Описание</span><span class="sxs-lookup"><span data-stu-id="43861-115">Description</span></span>                                                               |
|------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="43861-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="43861-116"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="43861-117">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="43861-117">The method succeeded.</span></span><br/>                                          |
| <dl> <span data-ttu-id="43861-118"><dt>**\_вытипемисматч E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="43861-118"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="43861-119">Свойство, указанное *ключом* , не является типом **PROPERTYKEY** .</span><span class="sxs-lookup"><span data-stu-id="43861-119">The property specified by *key* is not a **PROPERTYKEY** type.</span></span><br/> |
| <dl> <span data-ttu-id="43861-120"><dt>**HRESULT \_ из \_ Win32 (ошибка \_ не \_ найдена)**</dt></span><span class="sxs-lookup"><span data-stu-id="43861-120"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="43861-121">Свойство, указанное *ключом* , отсутствует в коллекции.</span><span class="sxs-lookup"><span data-stu-id="43861-121">The property specified by *key* is not in the collection.</span></span><br/>      |



 

## <a name="requirements"></a><span data-ttu-id="43861-122">Требования</span><span class="sxs-lookup"><span data-stu-id="43861-122">Requirements</span></span>



| <span data-ttu-id="43861-123">Требование</span><span class="sxs-lookup"><span data-stu-id="43861-123">Requirement</span></span> | <span data-ttu-id="43861-124">Значение</span><span class="sxs-lookup"><span data-stu-id="43861-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43861-125">Header</span><span class="sxs-lookup"><span data-stu-id="43861-125">Header</span></span><br/>  | <dl> <span data-ttu-id="43861-126"><dt>Портабледевицетипес. h</dt></span><span class="sxs-lookup"><span data-stu-id="43861-126"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="43861-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="43861-127">Library</span></span><br/> | <dl> <span data-ttu-id="43861-128"><dt>Портабледевицегуидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="43861-128"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43861-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="43861-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43861-130">**Интерфейс Ипортабледевицевалуес**</span><span class="sxs-lookup"><span data-stu-id="43861-130">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="43861-131">**Ипортабледевицевалуес:: Сеткэйвалуе**</span><span class="sxs-lookup"><span data-stu-id="43861-131">**IPortableDeviceValues::SetKeyValue**</span></span>](iportabledevicevalues-setkeyvalue.md)
</dt> </dl>

 

 




