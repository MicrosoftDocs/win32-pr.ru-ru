---
title: Ибасикдевице Уникуедевиценаме, метод
description: Извлекает уникальное имя устройства (УДН) устройства.
ms.assetid: 393EFF96-69E1-4081-905D-D8CC47B5FC4A
keywords:
- API потоковой передачи мультимедиа метода Уникуедевиценаме
- API потоковой передачи мультимедиа метода Уникуедевиценаме, интерфейс Ибасикдевице
- API потоковой передачи мультимедиа интерфейса Ибасикдевице, метод Уникуедевиценаме
topic_type:
- apiref
api_name:
- IBasicDevice.UniqueDeviceName
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4b3103640fd49880dc5ae5ca881618ac1091de62
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104411748"
---
# <a name="ibasicdeviceuniquedevicename-method"></a><span data-ttu-id="63241-106">Метод Ибасикдевице:: Уникуедевиценаме</span><span class="sxs-lookup"><span data-stu-id="63241-106">IBasicDevice::UniqueDeviceName method</span></span>

<span data-ttu-id="63241-107">Извлекает уникальное имя устройства (УДН) устройства.</span><span class="sxs-lookup"><span data-stu-id="63241-107">Retrieves the device s unique device name (UDN).</span></span>

## <a name="syntax"></a><span data-ttu-id="63241-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="63241-108">Syntax</span></span>


```C++
HRESULT UniqueDeviceName(
  [out] HSTRING *value
);
```



## <a name="parameters"></a><span data-ttu-id="63241-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="63241-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63241-110">*значение* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="63241-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="63241-111">Получает указатель на УДН модель устройства.</span><span class="sxs-lookup"><span data-stu-id="63241-111">Receives a pointer to the device s model UDN.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63241-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="63241-112">Return value</span></span>

<span data-ttu-id="63241-113">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="63241-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="63241-114">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="63241-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="63241-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="63241-115">Return code</span></span>                                                                          | <span data-ttu-id="63241-116">Описание</span><span class="sxs-lookup"><span data-stu-id="63241-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="63241-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="63241-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="63241-118">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="63241-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="63241-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="63241-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63241-120">**ибасикдевице**</span><span class="sxs-lookup"><span data-stu-id="63241-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





