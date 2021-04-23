---
description: Метод Ендфлуш завершает операцию очистки.
ms.assetid: ebb6beec-84e2-49a7-9771-bbd191faada7
title: Ктрансформфилтер. Ендфлуш, метод (Трансфрм. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 348675f1369ec9b0deb5415ad14a864a8befef73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657344"
---
# <a name="ctransformfilterendflush-method"></a><span data-ttu-id="076a4-103">Ктрансформфилтер. Ендфлуш, метод</span><span class="sxs-lookup"><span data-stu-id="076a4-103">CTransformFilter.EndFlush method</span></span>

<span data-ttu-id="076a4-104">`EndFlush`Метод завершает операцию очистки.</span><span class="sxs-lookup"><span data-stu-id="076a4-104">The `EndFlush` method ends a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="076a4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="076a4-105">Syntax</span></span>


```C++
virtual HRESULT EndFlush();
```



## <a name="parameters"></a><span data-ttu-id="076a4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="076a4-106">Parameters</span></span>

<span data-ttu-id="076a4-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="076a4-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="076a4-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="076a4-108">Return value</span></span>

<span data-ttu-id="076a4-109">Возвращает \_ значение, равное ОК или другому значению **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="076a4-109">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="076a4-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="076a4-110">Remarks</span></span>

<span data-ttu-id="076a4-111">В конце операции записи на диск метод [**ктрансформинпутпин:: ендфлуш**](ctransforminputpin-endflush.md) закрепления вызывает этот метод.</span><span class="sxs-lookup"><span data-stu-id="076a4-111">At the end of a flush operation, the input pin's [**CTransformInputPin::EndFlush**](ctransforminputpin-endflush.md) method calls this method.</span></span> <span data-ttu-id="076a4-112">Этот метод передает `EndFlush` вызов в нисходящем порядке.</span><span class="sxs-lookup"><span data-stu-id="076a4-112">This method passes the `EndFlush` call downstream.</span></span>

<span data-ttu-id="076a4-113">Если производный класс использует рабочий поток для доставки образцов, он должен отбросить все данные, помещенные в очередь, прежде чем отправлять `EndFlush` вызов в нисходящем направлении.</span><span class="sxs-lookup"><span data-stu-id="076a4-113">If the derived class uses a worker thread to deliver samples, it must discard any queued data before sending the `EndFlush` call downstream.</span></span> <span data-ttu-id="076a4-114">Дополнительные сведения см. в разделе [поток данных для разработчиков фильтров](data-flow-for-filter-developers.md).</span><span class="sxs-lookup"><span data-stu-id="076a4-114">For more information, see [Data Flow for Filter Developers](data-flow-for-filter-developers.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="076a4-115">Требования</span><span class="sxs-lookup"><span data-stu-id="076a4-115">Requirements</span></span>



| <span data-ttu-id="076a4-116">Требование</span><span class="sxs-lookup"><span data-stu-id="076a4-116">Requirement</span></span> | <span data-ttu-id="076a4-117">Значение</span><span class="sxs-lookup"><span data-stu-id="076a4-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="076a4-118">Header</span><span class="sxs-lookup"><span data-stu-id="076a4-118">Header</span></span><br/>  | <dl> <span data-ttu-id="076a4-119"><dt>Трансфрм. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="076a4-119"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="076a4-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="076a4-120">Library</span></span><br/> | <dl> <span data-ttu-id="076a4-121"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="076a4-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="076a4-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="076a4-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="076a4-123">**Класс Ктрансформфилтер**</span><span class="sxs-lookup"><span data-stu-id="076a4-123">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




