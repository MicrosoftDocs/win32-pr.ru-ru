---
description: Метод EndOfStream уведомляет фильтр о том, что из входного ПИН-кода не ожидается дополнительных данных.
ms.assetid: b8fc3976-e3d4-4f16-82b0-3900ad6a740c
title: Ктрансформфилтер. EndOfStream, метод (Трансфрм. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5dea676a42f6df46d0035fdbb6e812b1df15fbb2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657153"
---
# <a name="ctransformfilterendofstream-method"></a><span data-ttu-id="da941-103">Ктрансформфилтер. EndOfStream, метод</span><span class="sxs-lookup"><span data-stu-id="da941-103">CTransformFilter.EndOfStream method</span></span>

<span data-ttu-id="da941-104">`EndOfStream`Метод уведомляет фильтр о том, что из входного ПИН-кода не ожидается дополнительных данных.</span><span class="sxs-lookup"><span data-stu-id="da941-104">The `EndOfStream` method notifies the filter that no additional data is expected from the input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="da941-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="da941-105">Syntax</span></span>


```C++
virtual HRESULT EndOfStream();
```



## <a name="parameters"></a><span data-ttu-id="da941-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="da941-106">Parameters</span></span>

<span data-ttu-id="da941-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="da941-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="da941-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="da941-108">Return value</span></span>

<span data-ttu-id="da941-109">Возвращает \_ значение, равное ОК или другому значению **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="da941-109">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="da941-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="da941-110">Remarks</span></span>

<span data-ttu-id="da941-111">Метод [**ктрансформинпутпин:: EndOfStream**](ctransforminputpin-endofstream.md) входного контакта вызывает этот метод.</span><span class="sxs-lookup"><span data-stu-id="da941-111">The input pin's [**CTransformInputPin::EndOfStream**](ctransforminputpin-endofstream.md) method calls this method.</span></span> <span data-ttu-id="da941-112">Этот метод доставляет уведомление о завершении потока.</span><span class="sxs-lookup"><span data-stu-id="da941-112">This method delivers the end-of-stream notification downstream.</span></span> <span data-ttu-id="da941-113">Если производный класс использует рабочий поток для доставки образцов мультимедиа, он должен переопределить этот метод и поставить в очередь уведомление о завершении потока.</span><span class="sxs-lookup"><span data-stu-id="da941-113">If the derived class uses a worker thread to deliver media samples, it should override this method and queue the end-of-stream notification.</span></span>

## <a name="requirements"></a><span data-ttu-id="da941-114">Требования</span><span class="sxs-lookup"><span data-stu-id="da941-114">Requirements</span></span>



| <span data-ttu-id="da941-115">Требование</span><span class="sxs-lookup"><span data-stu-id="da941-115">Requirement</span></span> | <span data-ttu-id="da941-116">Значение</span><span class="sxs-lookup"><span data-stu-id="da941-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da941-117">Header</span><span class="sxs-lookup"><span data-stu-id="da941-117">Header</span></span><br/>  | <dl> <span data-ttu-id="da941-118"><dt>Трансфрм. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="da941-118"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="da941-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="da941-119">Library</span></span><br/> | <dl> <span data-ttu-id="da941-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="da941-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da941-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="da941-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da941-122">**Класс Ктрансформфилтер**</span><span class="sxs-lookup"><span data-stu-id="da941-122">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




