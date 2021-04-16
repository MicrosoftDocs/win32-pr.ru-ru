---
description: Метод Усингдифференталлокаторс определяет, используют ли контакты ввода и вывода различные распределителя.
ms.assetid: 75feaa6e-6395-4d47-ae92-10a857f8764b
title: Ктрансинплацефилтер. Усингдифференталлокаторс, метод (Трансип. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.UsingDifferentAllocators
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f20802836adb665614e2bbfb8cb79bdccd5a36ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657984"
---
# <a name="ctransinplacefilterusingdifferentallocators-method"></a><span data-ttu-id="2a976-103">Ктрансинплацефилтер. Усингдифференталлокаторс, метод</span><span class="sxs-lookup"><span data-stu-id="2a976-103">CTransInPlaceFilter.UsingDifferentAllocators method</span></span>

<span data-ttu-id="2a976-104">`UsingDifferentAllocators`Метод определяет, используют ли контакты ввода и вывода различные распределителя.</span><span class="sxs-lookup"><span data-stu-id="2a976-104">The `UsingDifferentAllocators` method determines whether the input and output pins are using different allocators.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a976-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2a976-105">Syntax</span></span>


```C++
BOOL UsingDifferentAllocators() const;
```



## <a name="parameters"></a><span data-ttu-id="2a976-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2a976-106">Parameters</span></span>

<span data-ttu-id="2a976-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="2a976-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2a976-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2a976-108">Return value</span></span>

<span data-ttu-id="2a976-109">Возвращает **значение true** , если крепления ввода и вывода используют разные распределителя, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="2a976-109">Returns **TRUE** if the input and output pins are using different allocators, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a976-110">Требования</span><span class="sxs-lookup"><span data-stu-id="2a976-110">Requirements</span></span>



| <span data-ttu-id="2a976-111">Требование</span><span class="sxs-lookup"><span data-stu-id="2a976-111">Requirement</span></span> | <span data-ttu-id="2a976-112">Значение</span><span class="sxs-lookup"><span data-stu-id="2a976-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a976-113">Header</span><span class="sxs-lookup"><span data-stu-id="2a976-113">Header</span></span><br/>  | <dl> <span data-ttu-id="2a976-114"><dt>Трансип. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2a976-114"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2a976-115">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2a976-115">Library</span></span><br/> | <dl> <span data-ttu-id="2a976-116"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="2a976-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a976-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2a976-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a976-118">**Класс Ктрансинплацефилтер**</span><span class="sxs-lookup"><span data-stu-id="2a976-118">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 




