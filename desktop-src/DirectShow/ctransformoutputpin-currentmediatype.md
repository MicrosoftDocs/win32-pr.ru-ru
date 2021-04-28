---
description: Ктрансформаутпутпин. Куррентмедиатипе, метод Куррентмедиатипе Извлекает тип носителя для текущего подключения ПИН-кода.
ms.assetid: 1c42664d-160a-4f76-9d7a-40414c5c1704
title: Ктрансформаутпутпин. Куррентмедиатипе, метод (Трансфрм. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.CurrentMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0cb40310afb1c22d00a5394c0a0667fc8d22eb03
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094912"
---
# <a name="ctransformoutputpincurrentmediatype-method"></a><span data-ttu-id="375f2-103">Ктрансформаутпутпин. Куррентмедиатипе, метод</span><span class="sxs-lookup"><span data-stu-id="375f2-103">CTransformOutputPin.CurrentMediaType method</span></span>

<span data-ttu-id="375f2-104">`CurrentMediaType`Метод извлекает тип носителя для текущего подключения ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="375f2-104">The `CurrentMediaType` method retrieves the media type for the current pin connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="375f2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="375f2-105">Syntax</span></span>


```C++
CMediaType& CurrentMediaType();
```



## <a name="parameters"></a><span data-ttu-id="375f2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="375f2-106">Parameters</span></span>

<span data-ttu-id="375f2-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="375f2-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="375f2-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="375f2-108">Return value</span></span>

<span data-ttu-id="375f2-109">Возвращает ссылку на переменную-член [**кбасепин:: m \_ MT**](cbasepin-m-mt.md) .</span><span class="sxs-lookup"><span data-stu-id="375f2-109">Returns a reference to the [**CBasePin::m\_mt**](cbasepin-m-mt.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="375f2-110">Требования</span><span class="sxs-lookup"><span data-stu-id="375f2-110">Requirements</span></span>



| <span data-ttu-id="375f2-111">Требование</span><span class="sxs-lookup"><span data-stu-id="375f2-111">Requirement</span></span> | <span data-ttu-id="375f2-112">Значение</span><span class="sxs-lookup"><span data-stu-id="375f2-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="375f2-113">Header</span><span class="sxs-lookup"><span data-stu-id="375f2-113">Header</span></span><br/>  | <dl> <span data-ttu-id="375f2-114"><dt>Трансфрм. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="375f2-114"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="375f2-115">Библиотека</span><span class="sxs-lookup"><span data-stu-id="375f2-115">Library</span></span><br/> | <dl> <span data-ttu-id="375f2-116"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="375f2-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




