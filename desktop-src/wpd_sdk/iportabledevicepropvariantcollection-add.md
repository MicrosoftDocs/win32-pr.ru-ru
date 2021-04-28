---
description: 'Метод Ипортабледевицепропвариантколлектион:: Add — метод Add добавляет элемент в коллекцию.'
ms.assetid: e9e8975f-f9b8-4940-b967-020cf3812582
title: 'Метод Ипортабледевицепропвариантколлектион:: Add (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.Add
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 7aed732cb92ea7e0f2fb3c2ebdd615f643bc3107
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112462"
---
# <a name="iportabledevicepropvariantcollectionadd-method"></a><span data-ttu-id="ea4e7-103">Метод Ипортабледевицепропвариантколлектион:: Add</span><span class="sxs-lookup"><span data-stu-id="ea4e7-103">IPortableDevicePropVariantCollection::Add method</span></span>

<span data-ttu-id="ea4e7-104">Метод **Add** добавляет элемент в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="ea4e7-104">The **Add** method adds an item to the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea4e7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ea4e7-105">Syntax</span></span>


```C++
HRESULT Add(
  [in] const PROPVARIANT *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="ea4e7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ea4e7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea4e7-107">*pValue* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ea4e7-107">*pValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea4e7-108">Указатель на новый объект **пропвариант** для добавления в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="ea4e7-108">Pointer to a new **PROPVARIANT** object to add to the collection.</span></span> <span data-ttu-id="ea4e7-109">Этот метод копирует **пропвариант** в коллекцию, поэтому необходимо освободить локальную копию переменной путем вызова **пропвариантклеар** после вызова этого метода.</span><span class="sxs-lookup"><span data-stu-id="ea4e7-109">This method copies the **PROPVARIANT** to the collection, so you should release your local copy of the variable by calling **PropVariantClear** after calling this method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea4e7-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ea4e7-110">Return value</span></span>

<span data-ttu-id="ea4e7-111">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="ea4e7-111">The method returns an **HRESULT**.</span></span> <span data-ttu-id="ea4e7-112">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="ea4e7-112">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="ea4e7-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="ea4e7-113">Return code</span></span>                                                                          | <span data-ttu-id="ea4e7-114">Описание</span><span class="sxs-lookup"><span data-stu-id="ea4e7-114">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="ea4e7-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="ea4e7-115"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="ea4e7-116">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="ea4e7-116">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ea4e7-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="ea4e7-117">Remarks</span></span>

<span data-ttu-id="ea4e7-118">Если VARTYPE для *pValue* является VT \_ Vector или VT \_ UI1, установка и извлечение буфера со **значением NULL** или нулевым размером не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="ea4e7-118">When the VARTYPE for *pValue* is VT\_VECTOR or VT\_UI1, setting and retrieving a **NULL** or zero-sized buffer is not supported.</span></span> <span data-ttu-id="ea4e7-119">Например, не допускаются значения pValue. Кауб. Пелемс = **null** или pValue. Кауб. целемс = 0.</span><span class="sxs-lookup"><span data-stu-id="ea4e7-119">For example, neither pValue.caub.pElems = **NULL** nor pValue.caub.cElems = 0 are allowed.</span></span>

<span data-ttu-id="ea4e7-120">Если вызывающий объект пытается добавить элемент другого объекта VARTYPE, содержащегося в коллекции, и значение ПРОПВАРИАНТ не может быть изменено этим интерфейсом автоматически, этот метод завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="ea4e7-120">If a caller tries to add an item of a different VARTYPE contained in the collection and the PROPVARIANT value cannot be changed by this interface automatically, this method will fail.</span></span> <span data-ttu-id="ea4e7-121">Чтобы изменить тип коллекции вручную, вызовите метод [**ипортабледевицепропвариантколлектион:: ChangeType**](iportabledevicepropvariantcollection-changetype.md).</span><span class="sxs-lookup"><span data-stu-id="ea4e7-121">To change the collection type manually, call [**IPortableDevicePropVariantCollection::ChangeType**](iportabledevicepropvariantcollection-changetype.md).</span></span>

## <a name="examples"></a><span data-ttu-id="ea4e7-122">Примеры</span><span class="sxs-lookup"><span data-stu-id="ea4e7-122">Examples</span></span>

<span data-ttu-id="ea4e7-123">Пример использования этого метода см. в разделе [Получение идентификатора объекта из постоянного уникального идентификатора](retrieving-an-object-identifier-from-a-persistent-unique-identifier.md) .</span><span class="sxs-lookup"><span data-stu-id="ea4e7-123">For an example of how to use this method, see [Retrieving an Object Identifier from a Persistent Unique Identifier](retrieving-an-object-identifier-from-a-persistent-unique-identifier.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="ea4e7-124">Требования</span><span class="sxs-lookup"><span data-stu-id="ea4e7-124">Requirements</span></span>



| <span data-ttu-id="ea4e7-125">Требование</span><span class="sxs-lookup"><span data-stu-id="ea4e7-125">Requirement</span></span> | <span data-ttu-id="ea4e7-126">Значение</span><span class="sxs-lookup"><span data-stu-id="ea4e7-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea4e7-127">Header</span><span class="sxs-lookup"><span data-stu-id="ea4e7-127">Header</span></span><br/>  | <dl> <span data-ttu-id="ea4e7-128"><dt>Портабледевицетипес. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea4e7-128"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="ea4e7-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ea4e7-129">Library</span></span><br/> | <dl> <span data-ttu-id="ea4e7-130"><dt>Портабледевицегуидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ea4e7-130"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea4e7-131">См. также</span><span class="sxs-lookup"><span data-stu-id="ea4e7-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea4e7-132">**Интерфейс Ипортабледевицепропвариантколлектион**</span><span class="sxs-lookup"><span data-stu-id="ea4e7-132">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="ea4e7-133">Перемещение содержимого на устройстве</span><span class="sxs-lookup"><span data-stu-id="ea4e7-133">Moving Content on the Device</span></span>](moving-content-on-the-device.md)
</dt> <dt>

[<span data-ttu-id="ea4e7-134">Получение идентификатора объекта из постоянного уникального идентификатора</span><span class="sxs-lookup"><span data-stu-id="ea4e7-134">Retrieving an Object Identifier from a Persistent Unique Identifier</span></span>](retrieving-an-object-identifier-from-a-persistent-unique-identifier.md)
</dt> </dl>

 

 




