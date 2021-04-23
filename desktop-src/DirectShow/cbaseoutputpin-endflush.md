---
description: 'Метод Ендфлуш завершает операцию очистки. Этот метод реализует метод Ипин:: Ендфлуш.'
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
ms.openlocfilehash: b40bc7db4e8d290ae0cd7e26a9d751e44b0daa4c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657885"
---
# <a name="cbaseoutputpinendflush-method"></a><span data-ttu-id="1a1c1-104">Кбасеаутпутпин. Ендфлуш, метод</span><span class="sxs-lookup"><span data-stu-id="1a1c1-104">CBaseOutputPin.EndFlush method</span></span>

<span data-ttu-id="1a1c1-105">`EndFlush`Метод завершает операцию очистки.</span><span class="sxs-lookup"><span data-stu-id="1a1c1-105">The `EndFlush` method ends a flush operation.</span></span> <span data-ttu-id="1a1c1-106">Этот метод реализует метод [**Ипин:: ендфлуш**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) .</span><span class="sxs-lookup"><span data-stu-id="1a1c1-106">This method implements the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a1c1-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1a1c1-107">Syntax</span></span>


```C++
HRESULT EndFlush();
```



## <a name="parameters"></a><span data-ttu-id="1a1c1-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="1a1c1-108">Parameters</span></span>

<span data-ttu-id="1a1c1-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="1a1c1-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1a1c1-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1a1c1-110">Return value</span></span>

<span data-ttu-id="1a1c1-111">Возвращает \_ непредвиденное значение E.</span><span class="sxs-lookup"><span data-stu-id="1a1c1-111">Returns E\_UNEXPECTED.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a1c1-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1a1c1-112">Remarks</span></span>

<span data-ttu-id="1a1c1-113">Этот метод должен вызываться только на входных ПИН-кодах, поэтому реализация **кбасеаутпутпин** возвращает E \_ непредвиденное значение.</span><span class="sxs-lookup"><span data-stu-id="1a1c1-113">This method should only be called on input pins, so the **CBaseOutputPin** implementation returns E\_UNEXPECTED.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a1c1-114">Требования</span><span class="sxs-lookup"><span data-stu-id="1a1c1-114">Requirements</span></span>



| <span data-ttu-id="1a1c1-115">Требование</span><span class="sxs-lookup"><span data-stu-id="1a1c1-115">Requirement</span></span> | <span data-ttu-id="1a1c1-116">Значение</span><span class="sxs-lookup"><span data-stu-id="1a1c1-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a1c1-117">Header</span><span class="sxs-lookup"><span data-stu-id="1a1c1-117">Header</span></span><br/>  | <dl> <span data-ttu-id="1a1c1-118"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1a1c1-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="1a1c1-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1a1c1-119">Library</span></span><br/> | <dl> <span data-ttu-id="1a1c1-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="1a1c1-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a1c1-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1a1c1-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a1c1-122">**Класс Кбасеаутпутпин**</span><span class="sxs-lookup"><span data-stu-id="1a1c1-122">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




