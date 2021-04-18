---
description: Метод Куррентмедиатипе Извлекает тип носителя для текущего подключения ПИН-кода.
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
ms.openlocfilehash: ee9ee15c3cda2baf8ab8d6e9cb0ec3c797e91a1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105676060"
---
# <a name="ctransformoutputpincurrentmediatype-method"></a><span data-ttu-id="0120c-103">Ктрансформаутпутпин. Куррентмедиатипе, метод</span><span class="sxs-lookup"><span data-stu-id="0120c-103">CTransformOutputPin.CurrentMediaType method</span></span>

<span data-ttu-id="0120c-104">`CurrentMediaType`Метод извлекает тип носителя для текущего подключения ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="0120c-104">The `CurrentMediaType` method retrieves the media type for the current pin connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="0120c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0120c-105">Syntax</span></span>


```C++
CMediaType& CurrentMediaType();
```



## <a name="parameters"></a><span data-ttu-id="0120c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0120c-106">Parameters</span></span>

<span data-ttu-id="0120c-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="0120c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0120c-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0120c-108">Return value</span></span>

<span data-ttu-id="0120c-109">Возвращает ссылку на переменную-член [**кбасепин:: m \_ MT**](cbasepin-m-mt.md) .</span><span class="sxs-lookup"><span data-stu-id="0120c-109">Returns a reference to the [**CBasePin::m\_mt**](cbasepin-m-mt.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="0120c-110">Требования</span><span class="sxs-lookup"><span data-stu-id="0120c-110">Requirements</span></span>



| <span data-ttu-id="0120c-111">Требование</span><span class="sxs-lookup"><span data-stu-id="0120c-111">Requirement</span></span> | <span data-ttu-id="0120c-112">Значение</span><span class="sxs-lookup"><span data-stu-id="0120c-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0120c-113">Header</span><span class="sxs-lookup"><span data-stu-id="0120c-113">Header</span></span><br/>  | <dl> <span data-ttu-id="0120c-114"><dt>Трансфрм. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0120c-114"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="0120c-115">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0120c-115">Library</span></span><br/> | <dl> <span data-ttu-id="0120c-116"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="0120c-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




