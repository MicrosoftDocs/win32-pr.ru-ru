---
description: Метод Clear освобождает, а затем удаляет все элементы из коллекции. После вызова этого метода коллекция считается пустой.
ms.assetid: f4b46713-8224-443a-99cc-13fa75e59e5d
title: 'Метод Ипортабледевицепропвариантколлектион:: Clear (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.Clear
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: fa7c2a8dddeb74b5ac666da2561bd6ee6536821a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718048"
---
# <a name="iportabledevicepropvariantcollectionclear-method"></a><span data-ttu-id="66602-104">Метод Ипортабледевицепропвариантколлектион:: Clear</span><span class="sxs-lookup"><span data-stu-id="66602-104">IPortableDevicePropVariantCollection::Clear method</span></span>

<span data-ttu-id="66602-105">Метод **clear** освобождает, а затем удаляет все элементы из коллекции.</span><span class="sxs-lookup"><span data-stu-id="66602-105">The **Clear** method frees, and then removes, all items from the collection.</span></span> <span data-ttu-id="66602-106">После вызова этого метода коллекция считается пустой.</span><span class="sxs-lookup"><span data-stu-id="66602-106">The collection is considered empty after calling this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="66602-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="66602-107">Syntax</span></span>


```C++
HRESULT Clear();
```



## <a name="parameters"></a><span data-ttu-id="66602-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="66602-108">Parameters</span></span>

<span data-ttu-id="66602-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="66602-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="66602-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="66602-110">Return value</span></span>

<span data-ttu-id="66602-111">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="66602-111">The method returns an **HRESULT**.</span></span> <span data-ttu-id="66602-112">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="66602-112">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="66602-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="66602-113">Return code</span></span>                                                                          | <span data-ttu-id="66602-114">Описание</span><span class="sxs-lookup"><span data-stu-id="66602-114">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="66602-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="66602-115"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="66602-116">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="66602-116">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="66602-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="66602-117">Remarks</span></span>

<span data-ttu-id="66602-118">После вызова метода **clear** коллекция считается нетипизированной, что означает, что значение VarType, заданное ранее, больше не ограничено операциями **добавления** .</span><span class="sxs-lookup"><span data-stu-id="66602-118">After calling **Clear**, the collection is considered type-less, meaning that the VARTYPE it was previously set to is no longer restricting **Add** operations.</span></span> <span data-ttu-id="66602-119">Вызов **Add** после вызова **clear** считается "первым" **добавлением** для этой коллекции.</span><span class="sxs-lookup"><span data-stu-id="66602-119">A call to **Add** after calling **Clear** is considered the "first" **Add** for this collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="66602-120">Требования</span><span class="sxs-lookup"><span data-stu-id="66602-120">Requirements</span></span>



| <span data-ttu-id="66602-121">Требование</span><span class="sxs-lookup"><span data-stu-id="66602-121">Requirement</span></span> | <span data-ttu-id="66602-122">Значение</span><span class="sxs-lookup"><span data-stu-id="66602-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66602-123">Header</span><span class="sxs-lookup"><span data-stu-id="66602-123">Header</span></span><br/>  | <dl> <span data-ttu-id="66602-124"><dt>Портабледевицетипес. h</dt></span><span class="sxs-lookup"><span data-stu-id="66602-124"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="66602-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="66602-125">Library</span></span><br/> | <dl> <span data-ttu-id="66602-126"><dt>Портабледевицегуидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="66602-126"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66602-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="66602-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66602-128">**Интерфейс Ипортабледевицепропвариантколлектион**</span><span class="sxs-lookup"><span data-stu-id="66602-128">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> </dl>

 

 




