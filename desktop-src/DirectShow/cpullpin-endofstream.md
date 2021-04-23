---
description: Метод EndOfStream вызывается после того, как объект доставляет последнюю выборку. Производный класс должен реализовывать этот метод.
ms.assetid: 55a32c17-9993-4ad7-8829-6aa5c1407622
title: Кпуллпин. EndOfStream, метод (Пуллпин. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a1df28430cdb71edd2ef9791e6c26092bbb21d0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679650"
---
# <a name="cpullpinendofstream-method"></a><span data-ttu-id="b5bc6-104">Кпуллпин. EndOfStream, метод</span><span class="sxs-lookup"><span data-stu-id="b5bc6-104">CPullPin.EndOfStream method</span></span>

<span data-ttu-id="b5bc6-105">`EndOfStream`Метод вызывается после того, как объект доставляет последнюю выборку.</span><span class="sxs-lookup"><span data-stu-id="b5bc6-105">The `EndOfStream` method is called after the object delivers the last sample.</span></span> <span data-ttu-id="b5bc6-106">Производный класс должен реализовывать этот метод.</span><span class="sxs-lookup"><span data-stu-id="b5bc6-106">The derived class must implement this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5bc6-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b5bc6-107">Syntax</span></span>


```C++
virtual HRESULT EndOfStream() = 0;
```



## <a name="parameters"></a><span data-ttu-id="b5bc6-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="b5bc6-108">Parameters</span></span>

<span data-ttu-id="b5bc6-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="b5bc6-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b5bc6-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b5bc6-110">Return value</span></span>

<span data-ttu-id="b5bc6-111">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b5bc6-111">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5bc6-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b5bc6-112">Remarks</span></span>

<span data-ttu-id="b5bc6-113">Этот метод используется для вызова [**Ипин:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) для каждого подчиненного входного контакта, получающего данные от этого объекта.</span><span class="sxs-lookup"><span data-stu-id="b5bc6-113">Use this method to call [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) on each downstream input pin that receives data from this object.</span></span> <span data-ttu-id="b5bc6-114">Если закрепление вывода фильтра является производным от [**кбасеаутпутпин**](cbaseoutputpin.md), вызовите метод [**Кбасеаутпутпин::D еливерендофстреам**](cbaseoutputpin-deliverendofstream.md) .</span><span class="sxs-lookup"><span data-stu-id="b5bc6-114">If your filter's output pin(s) derive from [**CBaseOutputPin**](cbaseoutputpin.md), call the [**CBaseOutputPin::DeliverEndOfStream**](cbaseoutputpin-deliverendofstream.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5bc6-115">Требования</span><span class="sxs-lookup"><span data-stu-id="b5bc6-115">Requirements</span></span>



| <span data-ttu-id="b5bc6-116">Требование</span><span class="sxs-lookup"><span data-stu-id="b5bc6-116">Requirement</span></span> | <span data-ttu-id="b5bc6-117">Значение</span><span class="sxs-lookup"><span data-stu-id="b5bc6-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5bc6-118">Header</span><span class="sxs-lookup"><span data-stu-id="b5bc6-118">Header</span></span><br/>  | <dl> <span data-ttu-id="b5bc6-119"><dt>Пуллпин. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5bc6-119"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="b5bc6-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b5bc6-120">Library</span></span><br/> | <dl> <span data-ttu-id="b5bc6-121"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="b5bc6-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5bc6-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b5bc6-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5bc6-123">**Класс Кпуллпин**</span><span class="sxs-lookup"><span data-stu-id="b5bc6-123">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




