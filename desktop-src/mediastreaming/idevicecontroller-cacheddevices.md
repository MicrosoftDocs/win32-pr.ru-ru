---
title: Идевицеконтроллер Качеддевицес, метод
description: Извлекает коллекцию указателей интерфейса Ибасикдевице, представляющих кэшированное представление всех обнаруживаемых устройств DLNA. | Идевицеконтроллер Качеддевицес, метод
ms.assetid: 94C2A7FF-5AF8-4F13-BBA5-54ED78C3BBF6
keywords:
- API потоковой передачи мультимедиа метода Качеддевицес
- API потоковой передачи мультимедиа метода Качеддевицес, интерфейс Идевицеконтроллер
- API потоковой передачи мультимедиа интерфейса Идевицеконтроллер, метод Качеддевицес
topic_type:
- apiref
api_name:
- IDeviceController.CachedDevices
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 69be1faea277fa8999ae5ddf3658aaa61a1116b9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104000280"
---
# <a name="idevicecontrollercacheddevices-method"></a><span data-ttu-id="aecd3-107">Метод Идевицеконтроллер:: Качеддевицес</span><span class="sxs-lookup"><span data-stu-id="aecd3-107">IDeviceController::CachedDevices method</span></span>

<span data-ttu-id="aecd3-108">Извлекает коллекцию указателей интерфейса [**ибасикдевице**](ibasicdevice.md) , представляющих кэшированное представление всех обнаруживаемых устройств DLNA.</span><span class="sxs-lookup"><span data-stu-id="aecd3-108">Retrieves a collection of [**IBasicDevice**](ibasicdevice.md) interface pointers that represents the cached view of all discoverable DLNA devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="aecd3-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="aecd3-109">Syntax</span></span>


```C++
HRESULT CachedDevices(
  [out] IVector< IBasicDevice > **value
);
```



## <a name="parameters"></a><span data-ttu-id="aecd3-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="aecd3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aecd3-111">*значение* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="aecd3-111">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aecd3-112">Получает перечисляемую коллекцию указателей интерфейса [**ибасикдевице**](ibasicdevice.md) .</span><span class="sxs-lookup"><span data-stu-id="aecd3-112">Receives an enumerable collection of [**IBasicDevice**](ibasicdevice.md) interface pointers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aecd3-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="aecd3-113">Return value</span></span>

<span data-ttu-id="aecd3-114">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="aecd3-114">The method returns an **HRESULT**.</span></span> <span data-ttu-id="aecd3-115">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="aecd3-115">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="aecd3-116">Код возврата</span><span class="sxs-lookup"><span data-stu-id="aecd3-116">Return code</span></span>                                                                          | <span data-ttu-id="aecd3-117">Описание</span><span class="sxs-lookup"><span data-stu-id="aecd3-117">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="aecd3-118"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="aecd3-118"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="aecd3-119">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="aecd3-119">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="aecd3-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="aecd3-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aecd3-121">**идевицеконтроллер**</span><span class="sxs-lookup"><span data-stu-id="aecd3-121">**IDeviceController**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-idevicecontroller)
</dt> </dl>

 

