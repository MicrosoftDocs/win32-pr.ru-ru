---
title: Ибасикдевице IpAddresses, метод
description: Возвращает вектор IP-адресов.
ms.assetid: F48B91DC-3AE2-462F-835B-292BF86904B3
keywords:
- API потоковой передачи мультимедиа метода IpAddresses
- API потоковой передачи мультимедиа метода IpAddresses, интерфейс Ибасикдевице
- API потоковой передачи мультимедиа интерфейса Ибасикдевице, метод IpAddresses
topic_type:
- apiref
api_name:
- IBasicDevice.IpAddresses
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0623b6e2e5d96cb0a400ab1e820424b7eecf46c9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104411772"
---
# <a name="ibasicdeviceipaddresses-method"></a><span data-ttu-id="01e00-106">Метод Ибасикдевице:: IpAddresses</span><span class="sxs-lookup"><span data-stu-id="01e00-106">IBasicDevice::IpAddresses method</span></span>

<span data-ttu-id="01e00-107">Возвращает вектор IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="01e00-107">Returns a vector of IP addresses.</span></span>

## <a name="syntax"></a><span data-ttu-id="01e00-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="01e00-108">Syntax</span></span>


```C++
HRESULT IpAddresses(
  [out] IVector< HSTRING > **value
);
```



## <a name="parameters"></a><span data-ttu-id="01e00-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="01e00-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01e00-110">*значение* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="01e00-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="01e00-111">Получает перечисляемую коллекцию указателей на IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="01e00-111">Receives an enumerable collection of pointers to IP addresses.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01e00-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="01e00-112">Return value</span></span>

<span data-ttu-id="01e00-113">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="01e00-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="01e00-114">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="01e00-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="01e00-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="01e00-115">Return code</span></span>                                                                          | <span data-ttu-id="01e00-116">Описание</span><span class="sxs-lookup"><span data-stu-id="01e00-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="01e00-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="01e00-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="01e00-118">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="01e00-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="01e00-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="01e00-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01e00-120">**ибасикдевице**</span><span class="sxs-lookup"><span data-stu-id="01e00-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





