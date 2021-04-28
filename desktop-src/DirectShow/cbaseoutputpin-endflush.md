---
description: 'Кбасеаутпутпин. Ендфлуш, метод Ендфлуш завершает операцию очистки. Этот метод реализует метод Ипин:: Ендфлуш.'
ms.assetid: c5c76cf8-1ca1-4fef-8776-7f4dcca32939
title: Кбасеаутпутпин. Ендфлуш, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 53153c6dbd941390c7ef616ee36c56e01214c341
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099512"
---
# <a name="cbaseoutputpinendflush-method"></a><span data-ttu-id="c2683-104">Кбасеаутпутпин. Ендфлуш, метод</span><span class="sxs-lookup"><span data-stu-id="c2683-104">CBaseOutputPin.EndFlush method</span></span>

<span data-ttu-id="c2683-105">`EndFlush`Метод завершает операцию очистки.</span><span class="sxs-lookup"><span data-stu-id="c2683-105">The `EndFlush` method ends a flush operation.</span></span> <span data-ttu-id="c2683-106">Этот метод реализует метод [**Ипин:: ендфлуш**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) .</span><span class="sxs-lookup"><span data-stu-id="c2683-106">This method implements the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2683-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c2683-107">Syntax</span></span>


```C++
HRESULT EndFlush();
```



## <a name="parameters"></a><span data-ttu-id="c2683-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="c2683-108">Parameters</span></span>

<span data-ttu-id="c2683-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="c2683-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c2683-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c2683-110">Return value</span></span>

<span data-ttu-id="c2683-111">Возвращает \_ непредвиденное значение E.</span><span class="sxs-lookup"><span data-stu-id="c2683-111">Returns E\_UNEXPECTED.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2683-112">Remarks</span><span class="sxs-lookup"><span data-stu-id="c2683-112">Remarks</span></span>

<span data-ttu-id="c2683-113">Этот метод должен вызываться только на входных ПИН-кодах, поэтому реализация **кбасеаутпутпин** возвращает E \_ непредвиденное значение.</span><span class="sxs-lookup"><span data-stu-id="c2683-113">This method should only be called on input pins, so the **CBaseOutputPin** implementation returns E\_UNEXPECTED.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2683-114">Требования</span><span class="sxs-lookup"><span data-stu-id="c2683-114">Requirements</span></span>



| <span data-ttu-id="c2683-115">Требование</span><span class="sxs-lookup"><span data-stu-id="c2683-115">Requirement</span></span> | <span data-ttu-id="c2683-116">Значение</span><span class="sxs-lookup"><span data-stu-id="c2683-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2683-117">Header</span><span class="sxs-lookup"><span data-stu-id="c2683-117">Header</span></span><br/>  | <dl> <span data-ttu-id="c2683-118"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c2683-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="c2683-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c2683-119">Library</span></span><br/> | <dl> <span data-ttu-id="c2683-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="c2683-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2683-121">См. также</span><span class="sxs-lookup"><span data-stu-id="c2683-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2683-122">**Класс Кбасеаутпутпин**</span><span class="sxs-lookup"><span data-stu-id="c2683-122">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




