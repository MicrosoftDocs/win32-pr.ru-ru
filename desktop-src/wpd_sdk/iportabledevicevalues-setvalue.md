---
description: Метод SetValue добавляет новое значение ПРОПВАРИАНТ или перезаписывает существующий.
ms.assetid: 69630a21-79e9-4c96-8ed7-9a41ebb991cd
title: 'Метод Ипортабледевицевалуес:: SetValue (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 4c2ba6c5b6f015e5961356ff8e246605bfeddd31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685372"
---
# <a name="iportabledevicevaluessetvalue-method"></a><span data-ttu-id="de9b2-103">Метод Ипортабледевицевалуес:: SetValue</span><span class="sxs-lookup"><span data-stu-id="de9b2-103">IPortableDeviceValues::SetValue method</span></span>

<span data-ttu-id="de9b2-104">Метод **SetValue** добавляет новое значение **пропвариант** или перезаписывает существующий.</span><span class="sxs-lookup"><span data-stu-id="de9b2-104">The **SetValue** method adds a new **PROPVARIANT** value or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="de9b2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="de9b2-105">Syntax</span></span>


```C++
HRESULT SetValue(
  [in]       REFPROPERTYKEY key,
  [in] const PROPVARIANT    *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="de9b2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="de9b2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de9b2-107">*ключ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="de9b2-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de9b2-108">Объект **рефпропертикэй** , указывающий элемент для создания или перезаписи.</span><span class="sxs-lookup"><span data-stu-id="de9b2-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="de9b2-109">*pValue* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="de9b2-109">*pValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de9b2-110">Объект **пропвариант** , указывающий новое значение.</span><span class="sxs-lookup"><span data-stu-id="de9b2-110">A **PROPVARIANT** that specifies the new value.</span></span> <span data-ttu-id="de9b2-111">Пакет SDK копирует значение, поэтому вызывающий объект может освободить локальную переменную, вызвав **пропвариантклеар** после вызова этого метода.</span><span class="sxs-lookup"><span data-stu-id="de9b2-111">The SDK copies the value, so the caller can release the local variable by calling **PropVariantClear** after calling this method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de9b2-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="de9b2-112">Return value</span></span>

<span data-ttu-id="de9b2-113">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="de9b2-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="de9b2-114">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="de9b2-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="de9b2-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="de9b2-115">Return code</span></span>                                                                          | <span data-ttu-id="de9b2-116">Описание</span><span class="sxs-lookup"><span data-stu-id="de9b2-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="de9b2-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="de9b2-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="de9b2-118">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="de9b2-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="de9b2-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="de9b2-119">Remarks</span></span>

<span data-ttu-id="de9b2-120">Если VARTYPE для *pValue* является VT \_ Vector или VT \_ UI1, установка буфера **со значением NULL** или нулевым размером не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="de9b2-120">When the VARTYPE for *pValue* is VT\_VECTOR or VT\_UI1, setting a **NULL** or zero-sized buffer is not supported.</span></span> <span data-ttu-id="de9b2-121">Например, не допускаются значения pValue. Кауб. Пелемс = **null** или pValue. Кауб. целемс = 0.</span><span class="sxs-lookup"><span data-stu-id="de9b2-121">For example, neither pValue.caub.pElems = **NULL** nor pValue.caub.cElems = 0 are allowed.</span></span>

<span data-ttu-id="de9b2-122">Этот метод можно использовать для получения значения любого типа из коллекции.</span><span class="sxs-lookup"><span data-stu-id="de9b2-122">This method can be used to retrieve a value of any type from the collection.</span></span> <span data-ttu-id="de9b2-123">Однако если вы заранее знакомы с типом значения, используйте один из специализированных методов **Set...** этого интерфейса, чтобы избежать издержек на работу с пропвариант значениями напрямую.</span><span class="sxs-lookup"><span data-stu-id="de9b2-123">However, if you know the value type in advance, use one of the specialized **Set...** methods of this interface to avoid the overhead of working with PROPVARIANT values directly.</span></span>

<span data-ttu-id="de9b2-124">Если существующее значение имеет тот же ключ, что и параметр *Key* , он перезаписывает существующее значение без предупреждения.</span><span class="sxs-lookup"><span data-stu-id="de9b2-124">If an existing value has the same key that is specified by the *key* parameter, it overwrites the existing value without any warning.</span></span> <span data-ttu-id="de9b2-125">Существующий ключ памяти освобождается соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="de9b2-125">The existing key memory is released appropriately.</span></span>

## <a name="requirements"></a><span data-ttu-id="de9b2-126">Требования</span><span class="sxs-lookup"><span data-stu-id="de9b2-126">Requirements</span></span>



| <span data-ttu-id="de9b2-127">Требование</span><span class="sxs-lookup"><span data-stu-id="de9b2-127">Requirement</span></span> | <span data-ttu-id="de9b2-128">Значение</span><span class="sxs-lookup"><span data-stu-id="de9b2-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de9b2-129">Header</span><span class="sxs-lookup"><span data-stu-id="de9b2-129">Header</span></span><br/>  | <dl> <span data-ttu-id="de9b2-130"><dt>Портабледевицетипес. h</dt></span><span class="sxs-lookup"><span data-stu-id="de9b2-130"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="de9b2-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="de9b2-131">Library</span></span><br/> | <dl> <span data-ttu-id="de9b2-132"><dt>Портабледевицегуидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="de9b2-132"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de9b2-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="de9b2-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de9b2-134">**Интерфейс Ипортабледевицевалуес**</span><span class="sxs-lookup"><span data-stu-id="de9b2-134">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="de9b2-135">**Ипортабледевицевалуес:: GetValue**</span><span class="sxs-lookup"><span data-stu-id="de9b2-135">**IPortableDeviceValues::GetValue**</span></span>](iportabledevicevalues-getvalue.md)
</dt> <dt>

[<span data-ttu-id="de9b2-136">**Ипортабледевицевалуес:: Ремовевалуе**</span><span class="sxs-lookup"><span data-stu-id="de9b2-136">**IPortableDeviceValues::RemoveValue**</span></span>](iportabledevicevalues-removevalue.md)
</dt> </dl>

 

 




