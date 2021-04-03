---
title: Ибасикдевице FriendlyName, метод
description: Получает понятное имя устройства s.
ms.assetid: 693806E1-CA66-457D-A25B-D79064776965
keywords:
- Метод FriendlyName API потоковой передачи мультимедиа
- Метод FriendlyName API потоковой передачи мультимедиа, интерфейс Ибасикдевице
- API потоковой передачи мультимедиа интерфейса Ибасикдевице, метод FriendlyName
topic_type:
- apiref
api_name:
- IBasicDevice.FriendlyName
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ec2b2edfa3a98dfdbbdd1d236acb6e1f1433f141
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "103784101"
---
# <a name="ibasicdevicefriendlyname-method"></a><span data-ttu-id="a0cf1-106">Метод Ибасикдевице:: FriendlyName</span><span class="sxs-lookup"><span data-stu-id="a0cf1-106">IBasicDevice::FriendlyName method</span></span>

<span data-ttu-id="a0cf1-107">Получает понятное имя устройства s.</span><span class="sxs-lookup"><span data-stu-id="a0cf1-107">Retrieves the device s friendly name.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0cf1-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a0cf1-108">Syntax</span></span>


```C++
HRESULT FriendlyName(
  [out] HSTRING *value
);
```



## <a name="parameters"></a><span data-ttu-id="a0cf1-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="a0cf1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0cf1-110">*значение* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="a0cf1-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a0cf1-111">Получает указатель на понятное имя устройства.</span><span class="sxs-lookup"><span data-stu-id="a0cf1-111">Receives a pointer to the device s friendly name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0cf1-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a0cf1-112">Return value</span></span>

<span data-ttu-id="a0cf1-113">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="a0cf1-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="a0cf1-114">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="a0cf1-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="a0cf1-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="a0cf1-115">Return code</span></span>                                                                          | <span data-ttu-id="a0cf1-116">Описание</span><span class="sxs-lookup"><span data-stu-id="a0cf1-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="a0cf1-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="a0cf1-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="a0cf1-118">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="a0cf1-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="a0cf1-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a0cf1-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0cf1-120">**ибасикдевице**</span><span class="sxs-lookup"><span data-stu-id="a0cf1-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





