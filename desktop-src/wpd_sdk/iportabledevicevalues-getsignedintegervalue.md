---
description: Метод Жетсигнединтежервалуе извлекает ДЛИННое значение (тип VT \_ i4), заданное ключом.
ms.assetid: d2291a64-d0b3-4a30-a37c-2b6cd9880a11
title: 'Метод Ипортабледевицевалуес:: Жетсигнединтежервалуе (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetSignedIntegerValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: f2fe0c2f8714d3fa28f61624924eba169f9f1c5d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649091"
---
# <a name="iportabledevicevaluesgetsignedintegervalue-method"></a><span data-ttu-id="6aa29-103">Метод Ипортабледевицевалуес:: Жетсигнединтежервалуе</span><span class="sxs-lookup"><span data-stu-id="6aa29-103">IPortableDeviceValues::GetSignedIntegerValue method</span></span>

<span data-ttu-id="6aa29-104">Метод **жетсигнединтежервалуе** извлекает **длинное** значение (тип VT \_ i4), заданное ключом.</span><span class="sxs-lookup"><span data-stu-id="6aa29-104">The **GetSignedIntegerValue** method retrieves a **LONG** value (type VT\_I4) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="6aa29-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6aa29-105">Syntax</span></span>


```C++
HRESULT GetSignedIntegerValue(
  [in]  REFPROPERTYKEY key,
  [out] LONG           *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="6aa29-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6aa29-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6aa29-107">*ключ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6aa29-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6aa29-108">Ключ **рефпропертикэй** , указывающий извлекаемый элемент.</span><span class="sxs-lookup"><span data-stu-id="6aa29-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="6aa29-109">*pValue* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="6aa29-109">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6aa29-110">Указатель на полученное значение **Long** .</span><span class="sxs-lookup"><span data-stu-id="6aa29-110">Pointer to the retrieved **LONG** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6aa29-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6aa29-111">Return value</span></span>

<span data-ttu-id="6aa29-112">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="6aa29-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="6aa29-113">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="6aa29-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="6aa29-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="6aa29-114">Return code</span></span>                                                                                                            | <span data-ttu-id="6aa29-115">Описание</span><span class="sxs-lookup"><span data-stu-id="6aa29-115">Description</span></span>                                                          |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <span data-ttu-id="6aa29-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="6aa29-116"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="6aa29-117">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="6aa29-117">The method succeeded.</span></span><br/>                                     |
| <dl> <span data-ttu-id="6aa29-118"><dt>**\_вытипемисматч E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6aa29-118"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="6aa29-119">Свойство, указанное *ключом* , имеет тип, отличный от **Long** .</span><span class="sxs-lookup"><span data-stu-id="6aa29-119">The property specified by *key* is not a **LONG** type.</span></span><br/>   |
| <dl> <span data-ttu-id="6aa29-120"><dt>**HRESULT \_ из \_ Win32 (ошибка \_ не \_ найдена)**</dt></span><span class="sxs-lookup"><span data-stu-id="6aa29-120"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="6aa29-121">Свойство, указанное *ключом* , отсутствует в коллекции.</span><span class="sxs-lookup"><span data-stu-id="6aa29-121">The property specified by *key* is not in the collection.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="6aa29-122">Требования</span><span class="sxs-lookup"><span data-stu-id="6aa29-122">Requirements</span></span>



| <span data-ttu-id="6aa29-123">Требование</span><span class="sxs-lookup"><span data-stu-id="6aa29-123">Requirement</span></span> | <span data-ttu-id="6aa29-124">Значение</span><span class="sxs-lookup"><span data-stu-id="6aa29-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6aa29-125">Header</span><span class="sxs-lookup"><span data-stu-id="6aa29-125">Header</span></span><br/>  | <dl> <span data-ttu-id="6aa29-126"><dt>Портабледевицетипес. h</dt></span><span class="sxs-lookup"><span data-stu-id="6aa29-126"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="6aa29-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6aa29-127">Library</span></span><br/> | <dl> <span data-ttu-id="6aa29-128"><dt>Портабледевицегуидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6aa29-128"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6aa29-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6aa29-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6aa29-130">**Интерфейс Ипортабледевицевалуес**</span><span class="sxs-lookup"><span data-stu-id="6aa29-130">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="6aa29-131">**Ипортабледевицевалуес:: Сетсигнединтежервалуе**</span><span class="sxs-lookup"><span data-stu-id="6aa29-131">**IPortableDeviceValues::SetSignedIntegerValue**</span></span>](iportabledevicevalues-setsignedintegervalue.md)
</dt> </dl>

 

 




