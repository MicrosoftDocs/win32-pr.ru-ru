---
description: 'Метод EndOfStream уведомляет ПИН-код о том, что дополнительные данные не ожидаются. Этот метод реализует метод Ипин:: EndOfStream.'
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
ms.openlocfilehash: e1cd903e811dbcd000ba202fc86c0fcb41bf221b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669207"
---
# <a name="cbaseoutputpinendofstream-method"></a><span data-ttu-id="4e39b-104">Кбасеаутпутпин. EndOfStream, метод</span><span class="sxs-lookup"><span data-stu-id="4e39b-104">CBaseOutputPin.EndOfStream method</span></span>

<span data-ttu-id="4e39b-105">`EndOfStream`Метод уведомляет ПИН-код о том, что дополнительные данные не ожидаются.</span><span class="sxs-lookup"><span data-stu-id="4e39b-105">The `EndOfStream` method notifies the pin that no additional data is expected.</span></span> <span data-ttu-id="4e39b-106">Этот метод реализует метод [**Ипин:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) .</span><span class="sxs-lookup"><span data-stu-id="4e39b-106">This method implements the [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e39b-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4e39b-107">Syntax</span></span>


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a><span data-ttu-id="4e39b-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="4e39b-108">Parameters</span></span>

<span data-ttu-id="4e39b-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="4e39b-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4e39b-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4e39b-110">Return value</span></span>

<span data-ttu-id="4e39b-111">Возвращает \_ непредвиденное значение E.</span><span class="sxs-lookup"><span data-stu-id="4e39b-111">Returns E\_UNEXPECTED.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e39b-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4e39b-112">Remarks</span></span>

<span data-ttu-id="4e39b-113">Этот метод должен вызываться только на входных ПИН-кодах, поэтому реализация **кбасеаутпутпин** возвращает E \_ непредвиденное значение.</span><span class="sxs-lookup"><span data-stu-id="4e39b-113">This method should only be called on input pins, so the **CBaseOutputPin** implementation returns E\_UNEXPECTED.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e39b-114">Требования</span><span class="sxs-lookup"><span data-stu-id="4e39b-114">Requirements</span></span>



| <span data-ttu-id="4e39b-115">Требование</span><span class="sxs-lookup"><span data-stu-id="4e39b-115">Requirement</span></span> | <span data-ttu-id="4e39b-116">Значение</span><span class="sxs-lookup"><span data-stu-id="4e39b-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e39b-117">Header</span><span class="sxs-lookup"><span data-stu-id="4e39b-117">Header</span></span><br/>  | <dl> <span data-ttu-id="4e39b-118"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4e39b-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="4e39b-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4e39b-119">Library</span></span><br/> | <dl> <span data-ttu-id="4e39b-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="4e39b-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e39b-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4e39b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e39b-122">**Класс Кбасеаутпутпин**</span><span class="sxs-lookup"><span data-stu-id="4e39b-122">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




