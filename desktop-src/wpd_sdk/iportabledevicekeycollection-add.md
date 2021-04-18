---
description: Метод Add добавляет ключ свойства в коллекцию.
ms.assetid: 640ef1c4-2843-48dd-a30a-9a2ef9de35b9
title: 'Метод Ипортабледевицекэйколлектион:: Add (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceKeyCollection.Add
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: e43fea25a08969b2ae8169884d51ddc46f8c7136
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718107"
---
# <a name="iportabledevicekeycollectionadd-method"></a><span data-ttu-id="05abc-103">Метод Ипортабледевицекэйколлектион:: Add</span><span class="sxs-lookup"><span data-stu-id="05abc-103">IPortableDeviceKeyCollection::Add method</span></span>

<span data-ttu-id="05abc-104">Метод **Add** добавляет ключ свойства в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="05abc-104">The **Add** method adds a property key to the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="05abc-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="05abc-105">Syntax</span></span>


```C++
HRESULT Add(
  [in] REFPROPERTYKEY Key
);
```



## <a name="parameters"></a><span data-ttu-id="05abc-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="05abc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05abc-107">*Ключ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="05abc-107">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05abc-108">Объект **рефпропертикэй** , добавляемый в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="05abc-108">A **REFPROPERTYKEY** to add to the collection.</span></span> <span data-ttu-id="05abc-109">Этот метод копирует ключ в коллекцию, чтобы можно было освободить локальную переменную после вызова этого метода.</span><span class="sxs-lookup"><span data-stu-id="05abc-109">This method copies the key to the collection, so you can release the local variable after calling this method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05abc-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="05abc-110">Return value</span></span>

<span data-ttu-id="05abc-111">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="05abc-111">The method returns an **HRESULT**.</span></span> <span data-ttu-id="05abc-112">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="05abc-112">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="05abc-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="05abc-113">Return code</span></span>                                                                                   | <span data-ttu-id="05abc-114">Описание</span><span class="sxs-lookup"><span data-stu-id="05abc-114">Description</span></span>                                                                       |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="05abc-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="05abc-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="05abc-116">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="05abc-116">The method succeeded.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="05abc-117"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="05abc-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="05abc-118">Недостаточно памяти для добавления ключа в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="05abc-118">There is not enough memory available to add the key to the collection.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="05abc-119">Примеры</span><span class="sxs-lookup"><span data-stu-id="05abc-119">Examples</span></span>

<span data-ttu-id="05abc-120">Пример использования этого метода см. в разделе [Получение свойств для одного объекта](retrieving-properties-for-a-single-object.md).</span><span class="sxs-lookup"><span data-stu-id="05abc-120">For an example of how to use this method, see [Retrieving Properties for a Single Object](retrieving-properties-for-a-single-object.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="05abc-121">Требования</span><span class="sxs-lookup"><span data-stu-id="05abc-121">Requirements</span></span>



| <span data-ttu-id="05abc-122">Требование</span><span class="sxs-lookup"><span data-stu-id="05abc-122">Requirement</span></span> | <span data-ttu-id="05abc-123">Значение</span><span class="sxs-lookup"><span data-stu-id="05abc-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05abc-124">Header</span><span class="sxs-lookup"><span data-stu-id="05abc-124">Header</span></span><br/>  | <dl> <span data-ttu-id="05abc-125"><dt>Портабледевицетипес. h</dt></span><span class="sxs-lookup"><span data-stu-id="05abc-125"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="05abc-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="05abc-126">Library</span></span><br/> | <dl> <span data-ttu-id="05abc-127"><dt>Портабледевицегуидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="05abc-127"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05abc-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="05abc-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05abc-129">**Интерфейс Ипортабледевицекэйколлектион**</span><span class="sxs-lookup"><span data-stu-id="05abc-129">**IPortableDeviceKeyCollection Interface**</span></span>](iportabledevicekeycollection.md)
</dt> <dt>

[<span data-ttu-id="05abc-130">Получение свойств содержимого объекта</span><span class="sxs-lookup"><span data-stu-id="05abc-130">Retrieving Content-Object Properties</span></span>](retrieving-content-object-properties.md)
</dt> <dt>

[<span data-ttu-id="05abc-131">Получение свойств для одного объекта</span><span class="sxs-lookup"><span data-stu-id="05abc-131">Retrieving Properties for a Single Object</span></span>](retrieving-properties-for-a-single-object.md)
</dt> <dt>

[<span data-ttu-id="05abc-132">Получение возможностей отрисовки, поддерживаемых устройством</span><span class="sxs-lookup"><span data-stu-id="05abc-132">Retrieving the Rendering Capabilities Supported by a Device</span></span>](retrieving-the-rendering-capabilities-supported-by-a-device.md)
</dt> </dl>

 

 




