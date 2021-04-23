---
title: Метод описания Ибасикдевице
description: Извлекает описание устройства.
ms.assetid: 9973AC46-E6BA-4931-BDEB-E64B147AB291
keywords:
- Метод описания API потоковой передачи мультимедиа
- Метод Description API потоковой передачи мультимедиа, интерфейс Ибасикдевице
- API потоковой передачи мультимедиа интерфейса Ибасикдевице, метод Description
topic_type:
- apiref
api_name:
- IBasicDevice.Description
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f094246d1424c458e624d4a49358b63a84b9b7d2
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104068874"
---
# <a name="ibasicdevicedescription-method"></a><span data-ttu-id="ca8dc-106">Ибасикдевице: метод:D Описание</span><span class="sxs-lookup"><span data-stu-id="ca8dc-106">IBasicDevice::Description method</span></span>

<span data-ttu-id="ca8dc-107">Извлекает описание устройства.</span><span class="sxs-lookup"><span data-stu-id="ca8dc-107">Retrieves a description of the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca8dc-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ca8dc-108">Syntax</span></span>


```C++
HRESULT Description(
  [out] HSTRING *value
);
```



## <a name="parameters"></a><span data-ttu-id="ca8dc-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="ca8dc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca8dc-110">*значение* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ca8dc-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ca8dc-111">Получает указатель на описание устройства.</span><span class="sxs-lookup"><span data-stu-id="ca8dc-111">Receives a pointer to the description of the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca8dc-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ca8dc-112">Return value</span></span>

<span data-ttu-id="ca8dc-113">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="ca8dc-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="ca8dc-114">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="ca8dc-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="ca8dc-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="ca8dc-115">Return code</span></span>                                                                          | <span data-ttu-id="ca8dc-116">Описание</span><span class="sxs-lookup"><span data-stu-id="ca8dc-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="ca8dc-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="ca8dc-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="ca8dc-118">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="ca8dc-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="ca8dc-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ca8dc-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca8dc-120">**ибасикдевице**</span><span class="sxs-lookup"><span data-stu-id="ca8dc-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





