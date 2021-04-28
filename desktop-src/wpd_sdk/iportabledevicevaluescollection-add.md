---
description: 'Метод Ипортабледевицевалуесколлектион:: Add — метод Add добавляет элемент в коллекцию.'
ms.assetid: 3b06abc4-f0ab-4b02-b3a7-360615f86a2a
title: 'Метод Ипортабледевицевалуесколлектион:: Add (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValuesCollection.Add
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 765100e1272fc6766e9f305f37f3b699bd96beb8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083249"
---
# <a name="iportabledevicevaluescollectionadd-method"></a><span data-ttu-id="3c352-103">Метод Ипортабледевицевалуесколлектион:: Add</span><span class="sxs-lookup"><span data-stu-id="3c352-103">IPortableDeviceValuesCollection::Add method</span></span>

<span data-ttu-id="3c352-104">Метод **Add** добавляет элемент в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="3c352-104">The **Add** method adds an item to the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c352-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3c352-105">Syntax</span></span>


```C++
HRESULT Add(
  [in] IPortableDeviceValues *pValues
);
```



## <a name="parameters"></a><span data-ttu-id="3c352-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3c352-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c352-107">*пвалуес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3c352-107">*pValues* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c352-108">Указатель на интерфейс **ипортабледевицевалуес** для добавления в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="3c352-108">Pointer to an **IPortableDeviceValues** interface to add to the collection.</span></span> <span data-ttu-id="3c352-109">Интерфейс на самом деле не копируется, но на нем вызывается метод **AddRef** .</span><span class="sxs-lookup"><span data-stu-id="3c352-109">The interface is not actually copied, but **AddRef** is called on it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c352-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3c352-110">Return value</span></span>

<span data-ttu-id="3c352-111">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="3c352-111">The method returns an **HRESULT**.</span></span> <span data-ttu-id="3c352-112">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="3c352-112">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="3c352-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="3c352-113">Return code</span></span>                                                                                   | <span data-ttu-id="3c352-114">Описание</span><span class="sxs-lookup"><span data-stu-id="3c352-114">Description</span></span>                                                                         |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3c352-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="3c352-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="3c352-116">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="3c352-116">The method succeeded.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="3c352-117"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="3c352-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="3c352-118">Недостаточно памяти для добавления значения в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="3c352-118">There is not enough memory available to add the value to the collection.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="3c352-119">Требования</span><span class="sxs-lookup"><span data-stu-id="3c352-119">Requirements</span></span>



| <span data-ttu-id="3c352-120">Требование</span><span class="sxs-lookup"><span data-stu-id="3c352-120">Requirement</span></span> | <span data-ttu-id="3c352-121">Значение</span><span class="sxs-lookup"><span data-stu-id="3c352-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c352-122">Header</span><span class="sxs-lookup"><span data-stu-id="3c352-122">Header</span></span><br/>  | <dl> <span data-ttu-id="3c352-123"><dt>Портабледевицетипес. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c352-123"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="3c352-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3c352-124">Library</span></span><br/> | <dl> <span data-ttu-id="3c352-125"><dt>Портабледевицегуидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3c352-125"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c352-126">См. также</span><span class="sxs-lookup"><span data-stu-id="3c352-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c352-127">**Интерфейс Ипортабледевицевалуесколлектион**</span><span class="sxs-lookup"><span data-stu-id="3c352-127">**IPortableDeviceValuesCollection Interface**</span></span>](iportabledevicevaluescollection.md)
</dt> </dl>

 

 




