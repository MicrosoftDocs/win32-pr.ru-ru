---
title: Ибасикдевице Моделнумбер, метод
description: Извлекает номер модели устройства s.
ms.assetid: C4199135-0C6C-4427-8152-224D7D29C270
keywords:
- API потоковой передачи мультимедиа метода Моделнумбер
- API потоковой передачи мультимедиа метода Моделнумбер, интерфейс Ибасикдевице
- API потоковой передачи мультимедиа интерфейса Ибасикдевице, метод Моделнумбер
topic_type:
- apiref
api_name:
- IBasicDevice.ModelNumber
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8034e67e5f3c552f0af83678d75e33881f1318f4
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "103889571"
---
# <a name="ibasicdevicemodelnumber-method"></a><span data-ttu-id="27992-106">Метод Ибасикдевице:: Моделнумбер</span><span class="sxs-lookup"><span data-stu-id="27992-106">IBasicDevice::ModelNumber method</span></span>

<span data-ttu-id="27992-107">Извлекает номер модели устройства s.</span><span class="sxs-lookup"><span data-stu-id="27992-107">Retrieves the device s model number.</span></span>

## <a name="syntax"></a><span data-ttu-id="27992-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="27992-108">Syntax</span></span>


```C++
HRESULT ModelNumber(
  [out] HSTRING *value
);
```



## <a name="parameters"></a><span data-ttu-id="27992-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="27992-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27992-110">*значение* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="27992-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="27992-111">Получает указатель на номер модели устройства s.</span><span class="sxs-lookup"><span data-stu-id="27992-111">Receives a pointer to the device s model number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27992-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="27992-112">Return value</span></span>

<span data-ttu-id="27992-113">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="27992-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="27992-114">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="27992-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="27992-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="27992-115">Return code</span></span>                                                                          | <span data-ttu-id="27992-116">Описание</span><span class="sxs-lookup"><span data-stu-id="27992-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="27992-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="27992-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="27992-118">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="27992-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="27992-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="27992-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27992-120">**ибасикдевице**</span><span class="sxs-lookup"><span data-stu-id="27992-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





