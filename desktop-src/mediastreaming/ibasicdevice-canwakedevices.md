---
title: Ибасикдевице Канвакедевицес, метод
description: Возвращает значение, указывающее, может ли устройство пробудиться.
ms.assetid: AAD0597C-AD33-40EE-A5DA-27AC66375D38
keywords:
- API потоковой передачи мультимедиа метода Канвакедевицес
- API потоковой передачи мультимедиа метода Канвакедевицес, интерфейс Ибасикдевице
- API потоковой передачи мультимедиа интерфейса Ибасикдевице, метод Канвакедевицес
topic_type:
- apiref
api_name:
- IBasicDevice.CanWakeDevices
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 08a893ac880a426f604f2dc1c73173585e507cc0
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104069068"
---
# <a name="ibasicdevicecanwakedevices-method"></a><span data-ttu-id="5d817-106">Метод Ибасикдевице:: Канвакедевицес</span><span class="sxs-lookup"><span data-stu-id="5d817-106">IBasicDevice::CanWakeDevices method</span></span>

<span data-ttu-id="5d817-107">Возвращает значение, указывающее, может ли устройство пробудиться.</span><span class="sxs-lookup"><span data-stu-id="5d817-107">Retrieves a value that indicates if the device can wake.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d817-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5d817-108">Syntax</span></span>


```C++
HRESULT CanWakeDevices(
  [out] boolean *value
);
```



## <a name="parameters"></a><span data-ttu-id="5d817-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="5d817-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d817-110">*значение* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="5d817-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5d817-111">Получает указатель на логическое значение, равное **true** , если устройство может пробудиться.</span><span class="sxs-lookup"><span data-stu-id="5d817-111">Receives a pointer to a boolean value that is **True** if the device can wake.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d817-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5d817-112">Return value</span></span>

<span data-ttu-id="5d817-113">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="5d817-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="5d817-114">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="5d817-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="5d817-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="5d817-115">Return code</span></span>                                                                          | <span data-ttu-id="5d817-116">Описание</span><span class="sxs-lookup"><span data-stu-id="5d817-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="5d817-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="5d817-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="5d817-118">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="5d817-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="5d817-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5d817-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d817-120">**ибасикдевице**</span><span class="sxs-lookup"><span data-stu-id="5d817-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





