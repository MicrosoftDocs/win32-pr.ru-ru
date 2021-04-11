---
title: Ибасикдевице Моделурл, метод
description: Извлекает URL-адрес модели устройства s.
ms.assetid: 093D306B-5DFC-4A68-803D-3DDE195A8B85
keywords:
- API потоковой передачи мультимедиа метода Моделурл
- API потоковой передачи мультимедиа метода Моделурл, интерфейс Ибасикдевице
- API потоковой передачи мультимедиа интерфейса Ибасикдевице, метод Моделурл
topic_type:
- apiref
api_name:
- IBasicDevice.ModelUrl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4f616d1a122f5fe6025c80742df61eb86d41514a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104333896"
---
# <a name="ibasicdevicemodelurl-method"></a><span data-ttu-id="0dd29-106">Метод Ибасикдевице:: Моделурл</span><span class="sxs-lookup"><span data-stu-id="0dd29-106">IBasicDevice::ModelUrl method</span></span>

<span data-ttu-id="0dd29-107">Извлекает URL-адрес модели устройства s.</span><span class="sxs-lookup"><span data-stu-id="0dd29-107">Retrieves the device s model URL.</span></span>

## <a name="syntax"></a><span data-ttu-id="0dd29-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0dd29-108">Syntax</span></span>


```C++
HRESULT ModelUrl(
  [out] HSTRING *value
);
```



## <a name="parameters"></a><span data-ttu-id="0dd29-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="0dd29-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0dd29-110">*значение* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="0dd29-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0dd29-111">Получает указатель на URL-адрес модели устройства s.</span><span class="sxs-lookup"><span data-stu-id="0dd29-111">Receives a pointer to the device s model URL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0dd29-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0dd29-112">Return value</span></span>

<span data-ttu-id="0dd29-113">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="0dd29-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="0dd29-114">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="0dd29-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="0dd29-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="0dd29-115">Return code</span></span>                                                                          | <span data-ttu-id="0dd29-116">Описание</span><span class="sxs-lookup"><span data-stu-id="0dd29-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="0dd29-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="0dd29-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="0dd29-118">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="0dd29-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="0dd29-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0dd29-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0dd29-120">**ибасикдевице**</span><span class="sxs-lookup"><span data-stu-id="0dd29-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





