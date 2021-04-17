---
description: 'Метод Ендфлуш завершает операцию очистки. Этот метод переопределяет метод Ктрансформфилтер:: Ендфлуш.'
ms.assetid: e7dfc6f9-1630-426b-95b2-9814331b5e61
title: Квидеотрансформфилтер. Ендфлуш, метод (Втранс. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ca160bd2e3e66df3bcf6f293abe6f828309172c0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657651"
---
# <a name="cvideotransformfilterendflush-method"></a><span data-ttu-id="ce7e7-104">Квидеотрансформфилтер. Ендфлуш, метод</span><span class="sxs-lookup"><span data-stu-id="ce7e7-104">CVideoTransformFilter.EndFlush method</span></span>

<span data-ttu-id="ce7e7-105">`EndFlush`Метод завершает операцию очистки.</span><span class="sxs-lookup"><span data-stu-id="ce7e7-105">The `EndFlush` method ends a flush operation.</span></span> <span data-ttu-id="ce7e7-106">Этот метод переопределяет метод [**ктрансформфилтер:: ендфлуш**](ctransformfilter-endflush.md) .</span><span class="sxs-lookup"><span data-stu-id="ce7e7-106">This method overrides the [**CTransformFilter::EndFlush**](ctransformfilter-endflush.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce7e7-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ce7e7-107">Syntax</span></span>


```C++
HRESULT EndFlush();
```



## <a name="parameters"></a><span data-ttu-id="ce7e7-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ce7e7-108">Parameters</span></span>

<span data-ttu-id="ce7e7-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="ce7e7-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ce7e7-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ce7e7-110">Return value</span></span>

<span data-ttu-id="ce7e7-111">Возвращает значение \_ ОК, если успешно, или код ошибки.</span><span class="sxs-lookup"><span data-stu-id="ce7e7-111">Returns S\_OK if successful, or an error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce7e7-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ce7e7-112">Remarks</span></span>

<span data-ttu-id="ce7e7-113">Этот метод сбрасывает все внутренние измерения производительности фильтра.</span><span class="sxs-lookup"><span data-stu-id="ce7e7-113">This method resets all of the filter's internal performance measurements.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce7e7-114">Требования</span><span class="sxs-lookup"><span data-stu-id="ce7e7-114">Requirements</span></span>



| <span data-ttu-id="ce7e7-115">Требование</span><span class="sxs-lookup"><span data-stu-id="ce7e7-115">Requirement</span></span> | <span data-ttu-id="ce7e7-116">Значение</span><span class="sxs-lookup"><span data-stu-id="ce7e7-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce7e7-117">Header</span><span class="sxs-lookup"><span data-stu-id="ce7e7-117">Header</span></span><br/>  | <dl> <span data-ttu-id="ce7e7-118"><dt>Втранс. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ce7e7-118"><dt>Vtrans.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="ce7e7-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ce7e7-119">Library</span></span><br/> | <dl> <span data-ttu-id="ce7e7-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="ce7e7-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce7e7-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ce7e7-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce7e7-122">**Класс Квидеотрансформфилтер**</span><span class="sxs-lookup"><span data-stu-id="ce7e7-122">**CVideoTransformFilter Class**</span></span>](cvideotransformfilter.md)
</dt> </dl>

 

 




