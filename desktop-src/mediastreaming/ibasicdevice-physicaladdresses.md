---
title: Ибасикдевице Фисикаладдрессес, метод
description: Возвращает вектор физических адресов.
ms.assetid: 85F48EE3-14A1-46DA-A3C3-F94A8A43CF92
keywords:
- API потоковой передачи мультимедиа метода Фисикаладдрессес
- API потоковой передачи мультимедиа метода Фисикаладдрессес, интерфейс Ибасикдевице
- API потоковой передачи мультимедиа интерфейса Ибасикдевице, метод Фисикаладдрессес
topic_type:
- apiref
api_name:
- IBasicDevice.PhysicalAddresses
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2f1cd87435c78e1f6877d1bb6afd1b38981b05dc
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104333891"
---
# <a name="ibasicdevicephysicaladdresses-method"></a><span data-ttu-id="a9443-106">Ибасикдевице: метод:P Хисикаладдрессес</span><span class="sxs-lookup"><span data-stu-id="a9443-106">IBasicDevice::PhysicalAddresses method</span></span>

<span data-ttu-id="a9443-107">Возвращает вектор физических адресов.</span><span class="sxs-lookup"><span data-stu-id="a9443-107">Returns a vector of physical addresses.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9443-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a9443-108">Syntax</span></span>


```C++
HRESULT PhysicalAddresses(
  [out] IVector< HSTRING > **value
);
```



## <a name="parameters"></a><span data-ttu-id="a9443-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="a9443-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9443-110">*значение* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="a9443-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a9443-111">Получает перечисляемую коллекцию указателей на физические адреса.</span><span class="sxs-lookup"><span data-stu-id="a9443-111">Receives an enumerable collection of pointers to physical addresses.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9443-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a9443-112">Return value</span></span>

<span data-ttu-id="a9443-113">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="a9443-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="a9443-114">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="a9443-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="a9443-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="a9443-115">Return code</span></span>                                                                          | <span data-ttu-id="a9443-116">Описание</span><span class="sxs-lookup"><span data-stu-id="a9443-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="a9443-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="a9443-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="a9443-118">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="a9443-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="a9443-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a9443-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9443-120">**ибасикдевице**</span><span class="sxs-lookup"><span data-stu-id="a9443-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





