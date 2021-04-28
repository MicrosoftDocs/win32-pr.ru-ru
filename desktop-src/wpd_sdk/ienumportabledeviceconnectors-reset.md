---
description: 'Метод Иенумпортабледевицеконнекторс:: Reset — сбрасывает последовательность перечисления до начала.'
ms.assetid: 1df1ff95-06ae-4e5e-8064-17f832c5f0b3
title: 'Метод Иенумпортабледевицеконнекторс:: Reset (Девпкэй. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPortableDeviceConnectors.Reset
api_type:
- COM
api_location:
- PortableDeviceGuids.lib
- PortableDeviceGuids.dll
ms.openlocfilehash: 10a356fbb8591568a9f99d9b92d681a46754a960
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083211"
---
# <a name="ienumportabledeviceconnectorsreset-method"></a><span data-ttu-id="a7a89-103">Метод Иенумпортабледевицеконнекторс:: Reset</span><span class="sxs-lookup"><span data-stu-id="a7a89-103">IEnumPortableDeviceConnectors::Reset method</span></span>

<span data-ttu-id="a7a89-104">Метод **Reset** Сбрасывает последовательность перечисления до начала.</span><span class="sxs-lookup"><span data-stu-id="a7a89-104">The **Reset** method resets the enumeration sequence to the beginning.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7a89-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a7a89-105">Syntax</span></span>


```C++
HRESULT Reset();
```



## <a name="parameters"></a><span data-ttu-id="a7a89-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a7a89-106">Parameters</span></span>

<span data-ttu-id="a7a89-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="a7a89-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a7a89-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a7a89-108">Return value</span></span>

<span data-ttu-id="a7a89-109">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="a7a89-109">The method returns an **HRESULT**.</span></span> <span data-ttu-id="a7a89-110">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="a7a89-110">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="a7a89-111">Код возврата</span><span class="sxs-lookup"><span data-stu-id="a7a89-111">Return code</span></span>                                                                          | <span data-ttu-id="a7a89-112">Описание</span><span class="sxs-lookup"><span data-stu-id="a7a89-112">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="a7a89-113"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="a7a89-113"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="a7a89-114">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="a7a89-114">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="a7a89-115">Требования</span><span class="sxs-lookup"><span data-stu-id="a7a89-115">Requirements</span></span>



| <span data-ttu-id="a7a89-116">Требование</span><span class="sxs-lookup"><span data-stu-id="a7a89-116">Requirement</span></span> | <span data-ttu-id="a7a89-117">Значение</span><span class="sxs-lookup"><span data-stu-id="a7a89-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7a89-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a7a89-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a7a89-119">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="a7a89-119">Windows 7 \[desktop apps only\]</span></span><br/>                                                                                                                             |
| <span data-ttu-id="a7a89-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a7a89-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a7a89-121">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="a7a89-121">None supported</span></span><br/>                                                                                                                                              |
| <span data-ttu-id="a7a89-122">Header</span><span class="sxs-lookup"><span data-stu-id="a7a89-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a7a89-123"><dt>Девпкэй. h; </dt> <dt>Портабледевицеконнектапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="a7a89-123"><dt>Devpkey.h; </dt> <dt>Portabledeviceconnectapi.h</dt></span></span> </dl> |
| <span data-ttu-id="a7a89-124">IDL</span><span class="sxs-lookup"><span data-stu-id="a7a89-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a7a89-125"><dt>Портабледевицеконнектапи. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a7a89-125"><dt>Portabledeviceconnectapi.idl</dt></span></span> </dl>                                                                |
| <span data-ttu-id="a7a89-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a7a89-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="a7a89-127"><dt>Портабледевицегуидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a7a89-127"><dt>PortableDeviceGuids.lib</dt></span></span> </dl>                                                                     |



## <a name="see-also"></a><span data-ttu-id="a7a89-128">См. также</span><span class="sxs-lookup"><span data-stu-id="a7a89-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7a89-129">**иенумпортабледевицеконнекторс**</span><span class="sxs-lookup"><span data-stu-id="a7a89-129">**IEnumPortableDeviceConnectors**</span></span>](ienumportabledeviceconnectors.md)
</dt> </dl>

 

 




