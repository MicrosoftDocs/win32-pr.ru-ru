---
description: Метод Финдпиннумбер извлекает номер указанного пин-кода в фильтре.
ms.assetid: c9366fcc-7b13-4e43-883e-6003c32fadec
title: Метод Ксаурце. Финдпиннумбер (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.FindPinNumber
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a6a71c65efd97c48eed58fb7d0b5aa8fcc2f178e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685113"
---
# <a name="csourcefindpinnumber-method"></a><span data-ttu-id="7c5d0-103">Ксаурце. Финдпиннумбер, метод</span><span class="sxs-lookup"><span data-stu-id="7c5d0-103">CSource.FindPinNumber method</span></span>

<span data-ttu-id="7c5d0-104">`FindPinNumber`Метод извлекает номер указанного пин-кода в фильтре.</span><span class="sxs-lookup"><span data-stu-id="7c5d0-104">The `FindPinNumber` method retrieves the number of a specified pin on the filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c5d0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7c5d0-105">Syntax</span></span>


```C++
int FindPinNumber(
   IPin *iPin
);
```



## <a name="parameters"></a><span data-ttu-id="7c5d0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7c5d0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c5d0-107">*ипин*</span><span class="sxs-lookup"><span data-stu-id="7c5d0-107">*iPin*</span></span> 
</dt> <dd>

<span data-ttu-id="7c5d0-108">Указатель на интерфейс [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin) ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="7c5d0-108">Pointer to the pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c5d0-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7c5d0-109">Return value</span></span>

<span data-ttu-id="7c5d0-110">Возвращает PIN-код или значение 1, если ПИН-код не найден в этом фильтре.</span><span class="sxs-lookup"><span data-stu-id="7c5d0-110">Returns the pin number, or  1 if the pin is not found on this filter.</span></span> <span data-ttu-id="7c5d0-111">Первый ПИН-код имеет нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="7c5d0-111">The first pin is numbered zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c5d0-112">Требования</span><span class="sxs-lookup"><span data-stu-id="7c5d0-112">Requirements</span></span>



| <span data-ttu-id="7c5d0-113">Требование</span><span class="sxs-lookup"><span data-stu-id="7c5d0-113">Requirement</span></span> | <span data-ttu-id="7c5d0-114">Значение</span><span class="sxs-lookup"><span data-stu-id="7c5d0-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c5d0-115">Header</span><span class="sxs-lookup"><span data-stu-id="7c5d0-115">Header</span></span><br/>  | <dl> <span data-ttu-id="7c5d0-116"><dt>Source. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7c5d0-116"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="7c5d0-117">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7c5d0-117">Library</span></span><br/> | <dl> <span data-ttu-id="7c5d0-118"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="7c5d0-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c5d0-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7c5d0-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c5d0-120">**Класс Ксаурце**</span><span class="sxs-lookup"><span data-stu-id="7c5d0-120">**CSource Class**</span></span>](csource.md)
</dt> </dl>

 

 




