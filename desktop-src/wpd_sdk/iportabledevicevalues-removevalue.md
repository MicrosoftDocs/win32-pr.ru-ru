---
description: Метод Ремовевалуе удаляет элемент из коллекции.
ms.assetid: 864c23ee-5a4e-4e06-add0-f6aef5562430
title: 'Метод Ипортабледевицевалуес:: Ремовевалуе (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.RemoveValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: f65160cc2798524d88471382c855f65dea2e6033
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717840"
---
# <a name="iportabledevicevaluesremovevalue-method"></a><span data-ttu-id="2eb54-103">Метод Ипортабледевицевалуес:: Ремовевалуе</span><span class="sxs-lookup"><span data-stu-id="2eb54-103">IPortableDeviceValues::RemoveValue method</span></span>

<span data-ttu-id="2eb54-104">Метод **ремовевалуе** удаляет элемент из коллекции.</span><span class="sxs-lookup"><span data-stu-id="2eb54-104">The **RemoveValue** method removes an item from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="2eb54-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2eb54-105">Syntax</span></span>


```C++
HRESULT RemoveValue(
  [in] REFPROPERTYKEY key
);
```



## <a name="parameters"></a><span data-ttu-id="2eb54-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2eb54-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2eb54-107">*ключ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2eb54-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2eb54-108">Объект **рефпропертикэй** , указывающий удаляемый элемент.</span><span class="sxs-lookup"><span data-stu-id="2eb54-108">A **REFPROPERTYKEY** that specifies the item to remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2eb54-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2eb54-109">Return value</span></span>

<span data-ttu-id="2eb54-110">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="2eb54-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="2eb54-111">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="2eb54-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="2eb54-112">Код возврата</span><span class="sxs-lookup"><span data-stu-id="2eb54-112">Return code</span></span>                                                                          | <span data-ttu-id="2eb54-113">Описание</span><span class="sxs-lookup"><span data-stu-id="2eb54-113">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="2eb54-114"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="2eb54-114"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="2eb54-115">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="2eb54-115">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="2eb54-116">Требования</span><span class="sxs-lookup"><span data-stu-id="2eb54-116">Requirements</span></span>



| <span data-ttu-id="2eb54-117">Требование</span><span class="sxs-lookup"><span data-stu-id="2eb54-117">Requirement</span></span> | <span data-ttu-id="2eb54-118">Значение</span><span class="sxs-lookup"><span data-stu-id="2eb54-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2eb54-119">Header</span><span class="sxs-lookup"><span data-stu-id="2eb54-119">Header</span></span><br/>  | <dl> <span data-ttu-id="2eb54-120"><dt>Портабледевицетипес. h</dt></span><span class="sxs-lookup"><span data-stu-id="2eb54-120"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="2eb54-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2eb54-121">Library</span></span><br/> | <dl> <span data-ttu-id="2eb54-122"><dt>Портабледевицегуидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2eb54-122"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2eb54-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2eb54-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2eb54-124">**Интерфейс Ипортабледевицевалуес**</span><span class="sxs-lookup"><span data-stu-id="2eb54-124">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="2eb54-125">**Ипортабледевицевалуес:: GetValue**</span><span class="sxs-lookup"><span data-stu-id="2eb54-125">**IPortableDeviceValues::GetValue**</span></span>](iportabledevicevalues-getvalue.md)
</dt> <dt>

[<span data-ttu-id="2eb54-126">**Ипортабледевицевалуес:: SetValue**</span><span class="sxs-lookup"><span data-stu-id="2eb54-126">**IPortableDeviceValues::SetValue**</span></span>](iportabledevicevalues-setvalue.md)
</dt> </dl>

 

 




