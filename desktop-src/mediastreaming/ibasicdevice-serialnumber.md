---
title: Метод SerialNumber Ибасикдевице
description: Извлекает серийный номер устройства s.
ms.assetid: 238A5999-0E8B-4462-AFCF-790DB58CFCB4
keywords:
- API потокового воспроизведения метода SerialNumber
- Метод SerialNumber API потоковой передачи мультимедиа, интерфейс Ибасикдевице
- API потоковой передачи мультимедиа интерфейса Ибасикдевице, метод SerialNumber
topic_type:
- apiref
api_name:
- IBasicDevice.SerialNumber
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f24fad2e74c3ec2a5b489d8f5dd57265ea6d21bf
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104333944"
---
# <a name="ibasicdeviceserialnumber-method"></a><span data-ttu-id="e27b7-106">Метод Ибасикдевице:: SerialNumber</span><span class="sxs-lookup"><span data-stu-id="e27b7-106">IBasicDevice::SerialNumber method</span></span>

<span data-ttu-id="e27b7-107">Извлекает серийный номер устройства s.</span><span class="sxs-lookup"><span data-stu-id="e27b7-107">Retrieves the device s serial number.</span></span>

## <a name="syntax"></a><span data-ttu-id="e27b7-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e27b7-108">Syntax</span></span>


```C++
HRESULT SerialNumber(
  [out] HSTRING *value
);
```



## <a name="parameters"></a><span data-ttu-id="e27b7-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="e27b7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e27b7-110">*значение* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e27b7-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e27b7-111">Получает указатель на серийный номер устройства.</span><span class="sxs-lookup"><span data-stu-id="e27b7-111">Receives a pointer to the device s serial number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e27b7-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e27b7-112">Return value</span></span>

<span data-ttu-id="e27b7-113">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="e27b7-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="e27b7-114">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="e27b7-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="e27b7-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="e27b7-115">Return code</span></span>                                                                          | <span data-ttu-id="e27b7-116">Описание</span><span class="sxs-lookup"><span data-stu-id="e27b7-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="e27b7-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="e27b7-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="e27b7-118">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="e27b7-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="e27b7-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e27b7-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e27b7-120">**ибасикдевице**</span><span class="sxs-lookup"><span data-stu-id="e27b7-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





