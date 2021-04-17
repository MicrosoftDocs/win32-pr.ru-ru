---
title: Девицеконтроллер. Качеддевицес, метод
description: Извлекает коллекцию указателей интерфейса Ибасикдевице, представляющих кэшированное представление всех обнаруживаемых устройств DLNA. | Девицеконтроллер. Качеддевицес, метод
ms.assetid: 89CFA4BB-EDA8-461A-A3A0-A84CBDA99EA4
keywords:
- API потоковой передачи мультимедиа метода Качеддевицес
- API потоковой передачи мультимедиа метода Качеддевицес, интерфейс Девицеконтроллер
- API потоковой передачи мультимедиа интерфейса Девицеконтроллер, метод Качеддевицес
topic_type:
- apiref
api_name:
- DeviceController.CachedDevices
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c0bb39e03a9788e0c444f682b61d39fc1c65781b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105713381"
---
# <a name="devicecontrollercacheddevices-method"></a><span data-ttu-id="c24a7-107">Девицеконтроллер. Качеддевицес, метод</span><span class="sxs-lookup"><span data-stu-id="c24a7-107">DeviceController.CachedDevices method</span></span>

<span data-ttu-id="c24a7-108">Извлекает коллекцию указателей интерфейса [**ибасикдевице**](ibasicdevice.md) , представляющих кэшированное представление всех обнаруживаемых устройств DLNA.</span><span class="sxs-lookup"><span data-stu-id="c24a7-108">Retrieves a collection of [**IBasicDevice**](ibasicdevice.md) interface pointers that represents the cached view of all discoverable DLNA devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="c24a7-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c24a7-109">Syntax</span></span>


```C++
HRESULT CachedDevices(
  [out] IVector< IBasicDevice > **value
);
```



## <a name="parameters"></a><span data-ttu-id="c24a7-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="c24a7-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c24a7-111">*значение* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="c24a7-111">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c24a7-112">Получает перечисляемую коллекцию указателей интерфейса [**ибасикдевице**](ibasicdevice.md) .</span><span class="sxs-lookup"><span data-stu-id="c24a7-112">Receives an enumerable collection of [**IBasicDevice**](ibasicdevice.md) interface pointers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c24a7-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c24a7-113">Return value</span></span>

<span data-ttu-id="c24a7-114">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="c24a7-114">The method returns an **HRESULT**.</span></span> <span data-ttu-id="c24a7-115">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="c24a7-115">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="c24a7-116">Код возврата</span><span class="sxs-lookup"><span data-stu-id="c24a7-116">Return code</span></span>                                                                          | <span data-ttu-id="c24a7-117">Описание</span><span class="sxs-lookup"><span data-stu-id="c24a7-117">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="c24a7-118"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="c24a7-118"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="c24a7-119">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="c24a7-119">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="c24a7-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c24a7-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="c24a7-121">[**девицеконтроллер**](/previous-versions/windows/desktop/legacy/hh828842(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c24a7-121">[**DeviceController**](/previous-versions/windows/desktop/legacy/hh828842(v=vs.85))</span></span>
</dt> </dl>

 

