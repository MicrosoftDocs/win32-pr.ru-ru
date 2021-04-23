---
title: Метод Ибасикдевице ModelName
description: Извлекает имя модели устройства s.
ms.assetid: 8F871E89-97C1-4788-83AB-B7E0D8D6E0B5
keywords:
- API потоковой передачи мультимедиа метода ModelName
- API потоковой передачи мультимедиа метода ModelName, интерфейс Ибасикдевице
- API потоковой передачи мультимедиа интерфейса Ибасикдевице, метод ModelName
topic_type:
- apiref
api_name:
- IBasicDevice.ModelName
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6e486b372b2108bc85153f416032ef6bfbe8a397
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "105672205"
---
# <a name="ibasicdevicemodelname-method"></a><span data-ttu-id="46b34-106">Метод Ибасикдевице:: ModelName</span><span class="sxs-lookup"><span data-stu-id="46b34-106">IBasicDevice::ModelName method</span></span>

<span data-ttu-id="46b34-107">Извлекает имя модели устройства s.</span><span class="sxs-lookup"><span data-stu-id="46b34-107">Retrieves the device s model name.</span></span>

## <a name="syntax"></a><span data-ttu-id="46b34-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="46b34-108">Syntax</span></span>


```C++
HRESULT ModelName(
  [out] HSTRING *value
);
```



## <a name="parameters"></a><span data-ttu-id="46b34-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="46b34-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46b34-110">*значение* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="46b34-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="46b34-111">Получает указатель на имя модели устройства s.</span><span class="sxs-lookup"><span data-stu-id="46b34-111">Receives a pointer to the device s model name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46b34-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="46b34-112">Return value</span></span>

<span data-ttu-id="46b34-113">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="46b34-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="46b34-114">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="46b34-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="46b34-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="46b34-115">Return code</span></span>                                                                          | <span data-ttu-id="46b34-116">Описание</span><span class="sxs-lookup"><span data-stu-id="46b34-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="46b34-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="46b34-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="46b34-118">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="46b34-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="46b34-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="46b34-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46b34-120">**ибасикдевице**</span><span class="sxs-lookup"><span data-stu-id="46b34-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





