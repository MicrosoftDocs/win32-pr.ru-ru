---
description: Метод GetValue извлекает значение ПРОПВАРИАНТ, заданное ключом.
ms.assetid: 927844f5-8f57-4596-ae0d-c67b8011ca87
title: 'Метод Ипортабледевицевалуес:: GetValue (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 6ab5ec24e67d5259eec86c6a33d32766a5426b38
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717841"
---
# <a name="iportabledevicevaluesgetvalue-method"></a><span data-ttu-id="3572e-103">Метод Ипортабледевицевалуес:: GetValue</span><span class="sxs-lookup"><span data-stu-id="3572e-103">IPortableDeviceValues::GetValue method</span></span>

<span data-ttu-id="3572e-104">Метод **GetValue** извлекает значение **пропвариант** , заданное ключом.</span><span class="sxs-lookup"><span data-stu-id="3572e-104">The **GetValue** method retrieves a **PROPVARIANT** value specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="3572e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3572e-105">Syntax</span></span>


```C++
HRESULT GetValue(
  [in]  REFPROPERTYKEY key,
  [out] PROPVARIANT    *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="3572e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3572e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3572e-107">*ключ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3572e-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3572e-108">Ключ **рефпропертикэй** , указывающий извлекаемый элемент.</span><span class="sxs-lookup"><span data-stu-id="3572e-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="3572e-109">*pValue* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="3572e-109">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3572e-110">Указатель на полученное значение **пропвариант** .</span><span class="sxs-lookup"><span data-stu-id="3572e-110">Pointer to the retrieved **PROPVARIANT** value.</span></span> <span data-ttu-id="3572e-111">Вызывающий объект должен освободить память, вызвав **пропвариантклеар** , когда завершится с ней.</span><span class="sxs-lookup"><span data-stu-id="3572e-111">The caller must release the memory by calling **PropVariantClear** when done with it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3572e-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3572e-112">Return value</span></span>

<span data-ttu-id="3572e-113">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="3572e-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="3572e-114">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="3572e-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="3572e-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="3572e-115">Return code</span></span>                                                                                                            | <span data-ttu-id="3572e-116">Описание</span><span class="sxs-lookup"><span data-stu-id="3572e-116">Description</span></span>                                                          |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <span data-ttu-id="3572e-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="3572e-117"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="3572e-118">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="3572e-118">The method succeeded.</span></span><br/>                                     |
| <dl> <span data-ttu-id="3572e-119"><dt>**HRESULT \_ из \_ Win32 (ошибка \_ не \_ найдена)**</dt></span><span class="sxs-lookup"><span data-stu-id="3572e-119"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="3572e-120">Свойство, указанное *ключом* , отсутствует в коллекции.</span><span class="sxs-lookup"><span data-stu-id="3572e-120">The property specified by *key* is not in the collection.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3572e-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3572e-121">Remarks</span></span>

<span data-ttu-id="3572e-122">Если VARTYPE для *pValue* является VT \_ Vector или VT \_ UI1, получение буфера **со значением NULL** или нулевым размером не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="3572e-122">When the VARTYPE for *pValue* is VT\_VECTOR or VT\_UI1, retrieving a **NULL** or zero-sized buffer is not supported.</span></span> <span data-ttu-id="3572e-123">Например, не допускаются значения pValue. Кауб. Пелемс = **null** или pValue. Кауб. целемс = 0.</span><span class="sxs-lookup"><span data-stu-id="3572e-123">For example, neither pValue.caub.pElems = **NULL** nor pValue.caub.cElems = 0 are allowed.</span></span>

<span data-ttu-id="3572e-124">Этот метод можно использовать для получения значения любого типа из коллекции.</span><span class="sxs-lookup"><span data-stu-id="3572e-124">This method can be used to retrieve a value of any type from the collection.</span></span> <span data-ttu-id="3572e-125">Однако если вы заранее знакомы с типом значения, используйте один из специализированных методов извлечения этого интерфейса, чтобы избежать издержек на работу с ПРОПВАРИАНТ значениями напрямую.</span><span class="sxs-lookup"><span data-stu-id="3572e-125">However, if you know the value type in advance, use one of the specialized retrieval methods of this interface to avoid the overhead of working with PROPVARIANT values directly.</span></span>

## <a name="requirements"></a><span data-ttu-id="3572e-126">Требования</span><span class="sxs-lookup"><span data-stu-id="3572e-126">Requirements</span></span>



| <span data-ttu-id="3572e-127">Требование</span><span class="sxs-lookup"><span data-stu-id="3572e-127">Requirement</span></span> | <span data-ttu-id="3572e-128">Значение</span><span class="sxs-lookup"><span data-stu-id="3572e-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3572e-129">Header</span><span class="sxs-lookup"><span data-stu-id="3572e-129">Header</span></span><br/>  | <dl> <span data-ttu-id="3572e-130"><dt>Портабледевицетипес. h</dt></span><span class="sxs-lookup"><span data-stu-id="3572e-130"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="3572e-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3572e-131">Library</span></span><br/> | <dl> <span data-ttu-id="3572e-132"><dt>Портабледевицегуидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3572e-132"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3572e-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3572e-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3572e-134">**Интерфейс Ипортабледевицевалуес**</span><span class="sxs-lookup"><span data-stu-id="3572e-134">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="3572e-135">**Ипортабледевицевалуес:: Ремовевалуе**</span><span class="sxs-lookup"><span data-stu-id="3572e-135">**IPortableDeviceValues::RemoveValue**</span></span>](iportabledevicevalues-removevalue.md)
</dt> <dt>

[<span data-ttu-id="3572e-136">**Ипортабледевицевалуес:: SetValue**</span><span class="sxs-lookup"><span data-stu-id="3572e-136">**IPortableDeviceValues::SetValue**</span></span>](iportabledevicevalues-setvalue.md)
</dt> </dl>

 

 




