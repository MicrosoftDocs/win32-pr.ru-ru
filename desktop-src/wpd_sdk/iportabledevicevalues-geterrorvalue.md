---
description: Метод Жетеррорвалуе извлекает значение HRESULT (тип \_ "ошибка VT"), заданное ключом.
ms.assetid: af57ddbd-5503-4b9b-bd75-ba9c9c202b73
title: 'Метод Ипортабледевицевалуес:: Жетеррорвалуе (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetErrorValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 86e5dacfa398cfe2bb57bfd289e4c8e792f14a66
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648744"
---
# <a name="iportabledevicevaluesgeterrorvalue-method"></a><span data-ttu-id="3609a-103">Метод Ипортабледевицевалуес:: Жетеррорвалуе</span><span class="sxs-lookup"><span data-stu-id="3609a-103">IPortableDeviceValues::GetErrorValue method</span></span>

<span data-ttu-id="3609a-104">Метод **жетеррорвалуе** извлекает значение **HRESULT** (тип \_ "ошибка VT"), заданное ключом.</span><span class="sxs-lookup"><span data-stu-id="3609a-104">The **GetErrorValue** method retrieves an **HRESULT** value (type VT\_ERROR) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="3609a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3609a-105">Syntax</span></span>


```C++
HRESULT GetErrorValue(
  [in]  REFPROPERTYKEY key,
  [out] HRESULT        *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="3609a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3609a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3609a-107">*ключ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3609a-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3609a-108">Ключ **рефпропертикэй** , указывающий извлекаемый элемент.</span><span class="sxs-lookup"><span data-stu-id="3609a-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="3609a-109">*pValue* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="3609a-109">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3609a-110">Указатель на полученное значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3609a-110">Pointer to the retrieved **HRESULT** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3609a-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3609a-111">Return value</span></span>

<span data-ttu-id="3609a-112">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="3609a-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="3609a-113">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="3609a-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="3609a-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="3609a-114">Return code</span></span>                                                                                                            | <span data-ttu-id="3609a-115">Описание</span><span class="sxs-lookup"><span data-stu-id="3609a-115">Description</span></span>                                                            |
|------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3609a-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="3609a-116"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="3609a-117">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="3609a-117">The method succeeded.</span></span><br/>                                       |
| <dl> <span data-ttu-id="3609a-118"><dt>**\_вытипемисматч E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3609a-118"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="3609a-119">Свойство, заданное *ключом* , не является типом **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3609a-119">The property specified by *key* is not an **HRESULT** type.</span></span><br/> |
| <dl> <span data-ttu-id="3609a-120"><dt>**HRESULT \_ из \_ Win32 (ошибка \_ не \_ найдена)**</dt></span><span class="sxs-lookup"><span data-stu-id="3609a-120"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="3609a-121">Свойство, указанное *ключом* , отсутствует в коллекции.</span><span class="sxs-lookup"><span data-stu-id="3609a-121">The property specified by *key* is not in the collection.</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="3609a-122">Требования</span><span class="sxs-lookup"><span data-stu-id="3609a-122">Requirements</span></span>



| <span data-ttu-id="3609a-123">Требование</span><span class="sxs-lookup"><span data-stu-id="3609a-123">Requirement</span></span> | <span data-ttu-id="3609a-124">Значение</span><span class="sxs-lookup"><span data-stu-id="3609a-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3609a-125">Header</span><span class="sxs-lookup"><span data-stu-id="3609a-125">Header</span></span><br/>  | <dl> <span data-ttu-id="3609a-126"><dt>Портабледевицетипес. h</dt></span><span class="sxs-lookup"><span data-stu-id="3609a-126"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="3609a-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3609a-127">Library</span></span><br/> | <dl> <span data-ttu-id="3609a-128"><dt>Портабледевицегуидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3609a-128"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3609a-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3609a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3609a-130">**Интерфейс Ипортабледевицевалуес**</span><span class="sxs-lookup"><span data-stu-id="3609a-130">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="3609a-131">**Ипортабледевицевалуес:: Сетеррорвалуе**</span><span class="sxs-lookup"><span data-stu-id="3609a-131">**IPortableDeviceValues::SetErrorValue**</span></span>](iportabledevicevalues-seterrorvalue.md)
</dt> </dl>

 

 




