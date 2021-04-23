---
title: Ибасикдевице Пресентатионурл, метод
description: Извлекает URL-адрес презентации устройства с.
ms.assetid: F1EF1BBE-F35D-4828-B4F6-D6DEFF5A6391
keywords:
- API потоковой передачи мультимедиа метода Пресентатионурл
- API потоковой передачи мультимедиа метода Пресентатионурл, интерфейс Ибасикдевице
- API потоковой передачи мультимедиа интерфейса Ибасикдевице, метод Пресентатионурл
topic_type:
- apiref
api_name:
- IBasicDevice.PresentationUrl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 89d10187329692c4f279a94cde004455a182733e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104411760"
---
# <a name="ibasicdevicepresentationurl-method"></a><span data-ttu-id="bebaa-106">Ибасикдевице: метод:P Ресентатионурл</span><span class="sxs-lookup"><span data-stu-id="bebaa-106">IBasicDevice::PresentationUrl method</span></span>

<span data-ttu-id="bebaa-107">Извлекает URL-адрес презентации устройства с.</span><span class="sxs-lookup"><span data-stu-id="bebaa-107">Retrieves the device s presentation URL.</span></span>

## <a name="syntax"></a><span data-ttu-id="bebaa-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bebaa-108">Syntax</span></span>


```C++
HRESULT PresentationUrl(
  [out] HSTRING *value
);
```



## <a name="parameters"></a><span data-ttu-id="bebaa-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="bebaa-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bebaa-110">*значение* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="bebaa-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bebaa-111">Получает указатель на URL-адрес презентации устройства с.</span><span class="sxs-lookup"><span data-stu-id="bebaa-111">Receives a pointer to the device s presentation URL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bebaa-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bebaa-112">Return value</span></span>

<span data-ttu-id="bebaa-113">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="bebaa-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="bebaa-114">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="bebaa-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="bebaa-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="bebaa-115">Return code</span></span>                                                                          | <span data-ttu-id="bebaa-116">Описание</span><span class="sxs-lookup"><span data-stu-id="bebaa-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="bebaa-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="bebaa-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="bebaa-118">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="bebaa-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="bebaa-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bebaa-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bebaa-120">**ибасикдевице**</span><span class="sxs-lookup"><span data-stu-id="bebaa-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





