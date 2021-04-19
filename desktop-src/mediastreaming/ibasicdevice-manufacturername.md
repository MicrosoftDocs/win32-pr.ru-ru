---
title: Ибасикдевице ManufacturerName, метод
description: Получает имя изготовителя устройства.
ms.assetid: F04400C9-02FC-4CB5-B355-A7E84BECD098
keywords:
- API потоковой передачи мультимедиа метода ManufacturerName
- API потоковой передачи мультимедиа метода ManufacturerName, интерфейс Ибасикдевице
- API потоковой передачи мультимедиа интерфейса Ибасикдевице, метод ManufacturerName
topic_type:
- apiref
api_name:
- IBasicDevice.ManufacturerName
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 698b4b6c202ed157737b20296976a282c7f97ba3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "105691416"
---
# <a name="ibasicdevicemanufacturername-method"></a><span data-ttu-id="d16bc-106">Метод Ибасикдевице:: ManufacturerName</span><span class="sxs-lookup"><span data-stu-id="d16bc-106">IBasicDevice::ManufacturerName method</span></span>

<span data-ttu-id="d16bc-107">Получает имя изготовителя устройства.</span><span class="sxs-lookup"><span data-stu-id="d16bc-107">Retrieves the device s manufacturer name.</span></span>

## <a name="syntax"></a><span data-ttu-id="d16bc-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d16bc-108">Syntax</span></span>


```C++
HRESULT ManufacturerName(
  [out] HSTRING *value
);
```



## <a name="parameters"></a><span data-ttu-id="d16bc-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="d16bc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d16bc-110">*значение* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d16bc-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d16bc-111">Получает указатель на имя изготовителя устройства.</span><span class="sxs-lookup"><span data-stu-id="d16bc-111">Receives a pointer to the device s manufacturer name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d16bc-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d16bc-112">Return value</span></span>

<span data-ttu-id="d16bc-113">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="d16bc-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="d16bc-114">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="d16bc-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="d16bc-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="d16bc-115">Return code</span></span>                                                                          | <span data-ttu-id="d16bc-116">Описание</span><span class="sxs-lookup"><span data-stu-id="d16bc-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="d16bc-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="d16bc-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="d16bc-118">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="d16bc-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="d16bc-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d16bc-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d16bc-120">**ибасикдевице**</span><span class="sxs-lookup"><span data-stu-id="d16bc-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





