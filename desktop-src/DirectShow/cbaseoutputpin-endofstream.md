---
description: 'Кбасеаутпутпин. EndOfStream, метод EndOfStream уведомляет ПИН-код о том, что дополнительные данные не ожидаются. Этот метод реализует метод Ипин:: EndOfStream.'
ms.assetid: 5c3b5f90-4194-4d65-9f1a-55edf327e3b3
title: Кбасеаутпутпин. EndOfStream, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c5f293b8026456618ad1196c491bce58cf481f07
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096152"
---
# <a name="cbaseoutputpinendofstream-method"></a><span data-ttu-id="831a7-104">Кбасеаутпутпин. EndOfStream, метод</span><span class="sxs-lookup"><span data-stu-id="831a7-104">CBaseOutputPin.EndOfStream method</span></span>

<span data-ttu-id="831a7-105">`EndOfStream`Метод уведомляет ПИН-код о том, что дополнительные данные не ожидаются.</span><span class="sxs-lookup"><span data-stu-id="831a7-105">The `EndOfStream` method notifies the pin that no additional data is expected.</span></span> <span data-ttu-id="831a7-106">Этот метод реализует метод [**Ипин:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) .</span><span class="sxs-lookup"><span data-stu-id="831a7-106">This method implements the [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="831a7-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="831a7-107">Syntax</span></span>


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a><span data-ttu-id="831a7-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="831a7-108">Parameters</span></span>

<span data-ttu-id="831a7-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="831a7-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="831a7-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="831a7-110">Return value</span></span>

<span data-ttu-id="831a7-111">Возвращает \_ непредвиденное значение E.</span><span class="sxs-lookup"><span data-stu-id="831a7-111">Returns E\_UNEXPECTED.</span></span>

## <a name="remarks"></a><span data-ttu-id="831a7-112">Remarks</span><span class="sxs-lookup"><span data-stu-id="831a7-112">Remarks</span></span>

<span data-ttu-id="831a7-113">Этот метод должен вызываться только на входных ПИН-кодах, поэтому реализация **кбасеаутпутпин** возвращает E \_ непредвиденное значение.</span><span class="sxs-lookup"><span data-stu-id="831a7-113">This method should only be called on input pins, so the **CBaseOutputPin** implementation returns E\_UNEXPECTED.</span></span>

## <a name="requirements"></a><span data-ttu-id="831a7-114">Требования</span><span class="sxs-lookup"><span data-stu-id="831a7-114">Requirements</span></span>



| <span data-ttu-id="831a7-115">Требование</span><span class="sxs-lookup"><span data-stu-id="831a7-115">Requirement</span></span> | <span data-ttu-id="831a7-116">Значение</span><span class="sxs-lookup"><span data-stu-id="831a7-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="831a7-117">Header</span><span class="sxs-lookup"><span data-stu-id="831a7-117">Header</span></span><br/>  | <dl> <span data-ttu-id="831a7-118"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="831a7-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="831a7-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="831a7-119">Library</span></span><br/> | <dl> <span data-ttu-id="831a7-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="831a7-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="831a7-121">См. также</span><span class="sxs-lookup"><span data-stu-id="831a7-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="831a7-122">**Класс Кбасеаутпутпин**</span><span class="sxs-lookup"><span data-stu-id="831a7-122">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




