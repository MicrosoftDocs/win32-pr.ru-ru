---
description: Метод Add добавляет элемент в коллекцию.
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
ms.openlocfilehash: d9d5b4ee664d2fbbcc78550b1af5a48874d153d6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708347"
---
# <a name="iportabledevicepropvariantcollectionadd-method"></a><span data-ttu-id="8e86d-103">Метод Ипортабледевицепропвариантколлектион:: Add</span><span class="sxs-lookup"><span data-stu-id="8e86d-103">IPortableDevicePropVariantCollection::Add method</span></span>

<span data-ttu-id="8e86d-104">Метод **Add** добавляет элемент в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="8e86d-104">The **Add** method adds an item to the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e86d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8e86d-105">Syntax</span></span>


```C++
HRESULT Add(
  [in] const PROPVARIANT *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="8e86d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8e86d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e86d-107">*pValue* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8e86d-107">*pValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e86d-108">Указатель на новый объект **пропвариант** для добавления в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="8e86d-108">Pointer to a new **PROPVARIANT** object to add to the collection.</span></span> <span data-ttu-id="8e86d-109">Этот метод копирует **пропвариант** в коллекцию, поэтому необходимо освободить локальную копию переменной путем вызова **пропвариантклеар** после вызова этого метода.</span><span class="sxs-lookup"><span data-stu-id="8e86d-109">This method copies the **PROPVARIANT** to the collection, so you should release your local copy of the variable by calling **PropVariantClear** after calling this method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e86d-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8e86d-110">Return value</span></span>

<span data-ttu-id="8e86d-111">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="8e86d-111">The method returns an **HRESULT**.</span></span> <span data-ttu-id="8e86d-112">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="8e86d-112">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="8e86d-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="8e86d-113">Return code</span></span>                                                                          | <span data-ttu-id="8e86d-114">Описание</span><span class="sxs-lookup"><span data-stu-id="8e86d-114">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="8e86d-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="8e86d-115"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="8e86d-116">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="8e86d-116">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8e86d-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8e86d-117">Remarks</span></span>

<span data-ttu-id="8e86d-118">Если VARTYPE для *pValue* является VT \_ Vector или VT \_ UI1, установка и извлечение буфера со **значением NULL** или нулевым размером не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="8e86d-118">When the VARTYPE for *pValue* is VT\_VECTOR or VT\_UI1, setting and retrieving a **NULL** or zero-sized buffer is not supported.</span></span> <span data-ttu-id="8e86d-119">Например, не допускаются значения pValue. Кауб. Пелемс = **null** или pValue. Кауб. целемс = 0.</span><span class="sxs-lookup"><span data-stu-id="8e86d-119">For example, neither pValue.caub.pElems = **NULL** nor pValue.caub.cElems = 0 are allowed.</span></span>

<span data-ttu-id="8e86d-120">Если вызывающий объект пытается добавить элемент другого объекта VARTYPE, содержащегося в коллекции, и значение ПРОПВАРИАНТ не может быть изменено этим интерфейсом автоматически, этот метод завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="8e86d-120">If a caller tries to add an item of a different VARTYPE contained in the collection and the PROPVARIANT value cannot be changed by this interface automatically, this method will fail.</span></span> <span data-ttu-id="8e86d-121">Чтобы изменить тип коллекции вручную, вызовите метод [**ипортабледевицепропвариантколлектион:: ChangeType**](iportabledevicepropvariantcollection-changetype.md).</span><span class="sxs-lookup"><span data-stu-id="8e86d-121">To change the collection type manually, call [**IPortableDevicePropVariantCollection::ChangeType**](iportabledevicepropvariantcollection-changetype.md).</span></span>

## <a name="examples"></a><span data-ttu-id="8e86d-122">Примеры</span><span class="sxs-lookup"><span data-stu-id="8e86d-122">Examples</span></span>

<span data-ttu-id="8e86d-123">Пример использования этого метода см. в разделе [Получение идентификатора объекта из постоянного уникального идентификатора](retrieving-an-object-identifier-from-a-persistent-unique-identifier.md) .</span><span class="sxs-lookup"><span data-stu-id="8e86d-123">For an example of how to use this method, see [Retrieving an Object Identifier from a Persistent Unique Identifier](retrieving-an-object-identifier-from-a-persistent-unique-identifier.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="8e86d-124">Требования</span><span class="sxs-lookup"><span data-stu-id="8e86d-124">Requirements</span></span>



| <span data-ttu-id="8e86d-125">Требование</span><span class="sxs-lookup"><span data-stu-id="8e86d-125">Requirement</span></span> | <span data-ttu-id="8e86d-126">Значение</span><span class="sxs-lookup"><span data-stu-id="8e86d-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e86d-127">Header</span><span class="sxs-lookup"><span data-stu-id="8e86d-127">Header</span></span><br/>  | <dl> <span data-ttu-id="8e86d-128"><dt>Портабледевицетипес. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e86d-128"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="8e86d-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8e86d-129">Library</span></span><br/> | <dl> <span data-ttu-id="8e86d-130"><dt>Портабледевицегуидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8e86d-130"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e86d-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8e86d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e86d-132">**Интерфейс Ипортабледевицепропвариантколлектион**</span><span class="sxs-lookup"><span data-stu-id="8e86d-132">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="8e86d-133">Перемещение содержимого на устройстве</span><span class="sxs-lookup"><span data-stu-id="8e86d-133">Moving Content on the Device</span></span>](moving-content-on-the-device.md)
</dt> <dt>

[<span data-ttu-id="8e86d-134">Получение идентификатора объекта из постоянного уникального идентификатора</span><span class="sxs-lookup"><span data-stu-id="8e86d-134">Retrieving an Object Identifier from a Persistent Unique Identifier</span></span>](retrieving-an-object-identifier-from-a-persistent-unique-identifier.md)
</dt> </dl>

 

 




