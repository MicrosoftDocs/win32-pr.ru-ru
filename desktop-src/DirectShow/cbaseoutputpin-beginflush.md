---
description: 'Метод Бегинфлуш начинает операцию очистки. Реализует метод Ипин:: Бегинфлуш.'
ms.assetid: f16c8337-5b7f-47e8-810d-00ffb3b5a1b4
title: Кбасеаутпутпин. Бегинфлуш, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0216f74094d0c024d9b354dc594ff8d65315efbe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668780"
---
# <a name="cbaseoutputpinbeginflush-method"></a><span data-ttu-id="a2516-104">Кбасеаутпутпин. Бегинфлуш, метод</span><span class="sxs-lookup"><span data-stu-id="a2516-104">CBaseOutputPin.BeginFlush method</span></span>

<span data-ttu-id="a2516-105">`BeginFlush`Метод начинает операцию записи на диск.</span><span class="sxs-lookup"><span data-stu-id="a2516-105">The `BeginFlush` method begins a flush operation.</span></span> <span data-ttu-id="a2516-106">Реализует метод [**Ипин:: бегинфлуш**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) .</span><span class="sxs-lookup"><span data-stu-id="a2516-106">Implements the [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2516-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a2516-107">Syntax</span></span>


```C++
HRESULT BeginFlush();
```



## <a name="parameters"></a><span data-ttu-id="a2516-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a2516-108">Parameters</span></span>

<span data-ttu-id="a2516-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="a2516-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a2516-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a2516-110">Return value</span></span>

<span data-ttu-id="a2516-111">Возвращает \_ непредвиденное значение E.</span><span class="sxs-lookup"><span data-stu-id="a2516-111">Returns E\_UNEXPECTED.</span></span>

## <a name="remarks"></a><span data-ttu-id="a2516-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a2516-112">Remarks</span></span>

<span data-ttu-id="a2516-113">Этот метод должен вызываться только на входных ПИН-кодах, поэтому реализация **кбасеаутпутпин** возвращает E \_ непредвиденное значение.</span><span class="sxs-lookup"><span data-stu-id="a2516-113">This method should only be called on input pins, so the **CBaseOutputPin** implementation returns E\_UNEXPECTED.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2516-114">Требования</span><span class="sxs-lookup"><span data-stu-id="a2516-114">Requirements</span></span>



| <span data-ttu-id="a2516-115">Требование</span><span class="sxs-lookup"><span data-stu-id="a2516-115">Requirement</span></span> | <span data-ttu-id="a2516-116">Значение</span><span class="sxs-lookup"><span data-stu-id="a2516-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2516-117">Header</span><span class="sxs-lookup"><span data-stu-id="a2516-117">Header</span></span><br/>  | <dl> <span data-ttu-id="a2516-118"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a2516-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a2516-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a2516-119">Library</span></span><br/> | <dl> <span data-ttu-id="a2516-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="a2516-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2516-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a2516-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2516-122">**Класс Кбасеаутпутпин**</span><span class="sxs-lookup"><span data-stu-id="a2516-122">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




