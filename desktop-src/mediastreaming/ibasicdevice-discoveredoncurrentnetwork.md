---
title: Ибасикдевице Дисковередонкуррентнетворк, метод
description: Возвращает значение, указывающее, находится ли устройство в текущей сети.
ms.assetid: E64D4E49-9790-4647-9A01-2C28C407F238
keywords:
- API потоковой передачи мультимедиа метода Дисковередонкуррентнетворк
- API потоковой передачи мультимедиа метода Дисковередонкуррентнетворк, интерфейс Ибасикдевице
- API потоковой передачи мультимедиа интерфейса Ибасикдевице, метод Дисковередонкуррентнетворк
topic_type:
- apiref
api_name:
- IBasicDevice.DiscoveredOnCurrentNetwork
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6e79a012413b3b3d78a9c4617f01ca6cc01cf7e1
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104411688"
---
# <a name="ibasicdevicediscoveredoncurrentnetwork-method"></a><span data-ttu-id="1a47d-106">Ибасикдевице: метод:D Исковередонкуррентнетворк</span><span class="sxs-lookup"><span data-stu-id="1a47d-106">IBasicDevice::DiscoveredOnCurrentNetwork method</span></span>

<span data-ttu-id="1a47d-107">Возвращает значение, указывающее, находится ли устройство в текущей сети.</span><span class="sxs-lookup"><span data-stu-id="1a47d-107">Retrieves a value that indicates if the device is on the current network.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a47d-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1a47d-108">Syntax</span></span>


```C++
HRESULT DiscoveredOnCurrentNetwork(
  [out] boolean *value
);
```



## <a name="parameters"></a><span data-ttu-id="1a47d-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="1a47d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a47d-110">*значение* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="1a47d-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1a47d-111">Получает указатель на логическое значение, равное **true** , если устройство находится в текущей сети.</span><span class="sxs-lookup"><span data-stu-id="1a47d-111">Receives a pointer to a boolean value that is **True** if the device is on the current network.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a47d-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1a47d-112">Return value</span></span>

<span data-ttu-id="1a47d-113">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="1a47d-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="1a47d-114">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="1a47d-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="1a47d-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="1a47d-115">Return code</span></span>                                                                          | <span data-ttu-id="1a47d-116">Описание</span><span class="sxs-lookup"><span data-stu-id="1a47d-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="1a47d-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="1a47d-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="1a47d-118">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="1a47d-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="1a47d-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1a47d-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a47d-120">**ибасикдевице**</span><span class="sxs-lookup"><span data-stu-id="1a47d-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





