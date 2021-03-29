---
description: Метод Жетунсигнедларжеинтежервалуе извлекает значение УЛОНГЛОНГ (Type VT \_ UI8), заданное ключом.
ms.assetid: de37c49b-a5f4-424d-8320-1de2d5a624aa
title: 'Метод Ипортабледевицевалуес:: Жетунсигнедларжеинтежервалуе (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetUnsignedLargeIntegerValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 48f6093f32d43737b1999c3474f74569ecd3f8cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648040"
---
# <a name="iportabledevicevaluesgetunsignedlargeintegervalue-method"></a><span data-ttu-id="42f1c-103">Метод Ипортабледевицевалуес:: Жетунсигнедларжеинтежервалуе</span><span class="sxs-lookup"><span data-stu-id="42f1c-103">IPortableDeviceValues::GetUnsignedLargeIntegerValue method</span></span>

<span data-ttu-id="42f1c-104">Метод **жетунсигнедларжеинтежервалуе** извлекает значение **УЛОНГЛОНГ** (Type VT \_ UI8), заданное ключом.</span><span class="sxs-lookup"><span data-stu-id="42f1c-104">The **GetUnsignedLargeIntegerValue** method retrieves a **ULONGLONG** value (type VT\_UI8) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="42f1c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="42f1c-105">Syntax</span></span>


```C++
HRESULT GetUnsignedLargeIntegerValue(
  [in]  REFPROPERTYKEY key,
  [out] ULONGLONG      *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="42f1c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="42f1c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42f1c-107">*ключ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="42f1c-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42f1c-108">Ключ **рефпропертикэй** , указывающий извлекаемый элемент.</span><span class="sxs-lookup"><span data-stu-id="42f1c-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="42f1c-109">*pValue* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="42f1c-109">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="42f1c-110">Указатель на полученное значение **улонглонг** .</span><span class="sxs-lookup"><span data-stu-id="42f1c-110">Pointer to the retrieved **ULONGLONG** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42f1c-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="42f1c-111">Return value</span></span>

<span data-ttu-id="42f1c-112">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="42f1c-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="42f1c-113">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="42f1c-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="42f1c-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="42f1c-114">Return code</span></span>                                                                                                            | <span data-ttu-id="42f1c-115">Описание</span><span class="sxs-lookup"><span data-stu-id="42f1c-115">Description</span></span>                                                             |
|------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <span data-ttu-id="42f1c-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="42f1c-116"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="42f1c-117">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="42f1c-117">The method succeeded.</span></span><br/>                                        |
| <dl> <span data-ttu-id="42f1c-118"><dt>**\_вытипемисматч E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="42f1c-118"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="42f1c-119">Свойство, указанное *ключом* , не является типом **улонглонг** .</span><span class="sxs-lookup"><span data-stu-id="42f1c-119">The property specified by *key* is not a **ULONGLONG** type.</span></span><br/> |
| <dl> <span data-ttu-id="42f1c-120"><dt>**HRESULT \_ из \_ Win32 (ошибка \_ не \_ найдена)**</dt></span><span class="sxs-lookup"><span data-stu-id="42f1c-120"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="42f1c-121">Свойство, указанное *ключом* , отсутствует в коллекции.</span><span class="sxs-lookup"><span data-stu-id="42f1c-121">The property specified by *key* is not in the collection.</span></span><br/>    |



 

## <a name="requirements"></a><span data-ttu-id="42f1c-122">Требования</span><span class="sxs-lookup"><span data-stu-id="42f1c-122">Requirements</span></span>



| <span data-ttu-id="42f1c-123">Требование</span><span class="sxs-lookup"><span data-stu-id="42f1c-123">Requirement</span></span> | <span data-ttu-id="42f1c-124">Значение</span><span class="sxs-lookup"><span data-stu-id="42f1c-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42f1c-125">Header</span><span class="sxs-lookup"><span data-stu-id="42f1c-125">Header</span></span><br/>  | <dl> <span data-ttu-id="42f1c-126"><dt>Портабледевицетипес. h</dt></span><span class="sxs-lookup"><span data-stu-id="42f1c-126"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="42f1c-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="42f1c-127">Library</span></span><br/> | <dl> <span data-ttu-id="42f1c-128"><dt>Портабледевицегуидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="42f1c-128"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42f1c-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="42f1c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42f1c-130">**Интерфейс Ипортабледевицевалуес**</span><span class="sxs-lookup"><span data-stu-id="42f1c-130">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="42f1c-131">**Ипортабледевицевалуес:: Сетунсигнедларжеинтежервалуе**</span><span class="sxs-lookup"><span data-stu-id="42f1c-131">**IPortableDeviceValues::SetUnsignedLargeIntegerValue**</span></span>](iportabledevicevalues-setunsignedlargeintegervalue.md)
</dt> </dl>

 

 




