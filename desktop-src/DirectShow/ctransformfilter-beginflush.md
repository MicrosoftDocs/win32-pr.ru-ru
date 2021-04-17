---
description: Метод Бегинфлуш начинает операцию очистки.
ms.assetid: 15bea993-f862-4791-b784-0d0468c6c05c
title: Ктрансформфилтер. Бегинфлуш, метод (Трансфрм. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bd9a4bf1543f4899d4c879e9d1a9d9cf1035b765
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657026"
---
# <a name="ctransformfilterbeginflush-method"></a><span data-ttu-id="0214a-103">Ктрансформфилтер. Бегинфлуш, метод</span><span class="sxs-lookup"><span data-stu-id="0214a-103">CTransformFilter.BeginFlush method</span></span>

<span data-ttu-id="0214a-104">`BeginFlush`Метод начинает операцию записи на диск.</span><span class="sxs-lookup"><span data-stu-id="0214a-104">The `BeginFlush` method begins a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="0214a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0214a-105">Syntax</span></span>


```C++
virtual HRESULT BeginFlush();
```



## <a name="parameters"></a><span data-ttu-id="0214a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0214a-106">Parameters</span></span>

<span data-ttu-id="0214a-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="0214a-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0214a-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0214a-108">Return value</span></span>

<span data-ttu-id="0214a-109">Возвращает \_ значение, равное ОК или другому значению **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0214a-109">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0214a-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0214a-110">Remarks</span></span>

<span data-ttu-id="0214a-111">В начале операции очистки метод [**ктрансформинпутпин:: бегинфлуш**](ctransforminputpin-beginflush.md) закрепления вызывает этот метод.</span><span class="sxs-lookup"><span data-stu-id="0214a-111">At the start of a flush operation, the input pin's [**CTransformInputPin::BeginFlush**](ctransforminputpin-beginflush.md) method calls this method.</span></span> <span data-ttu-id="0214a-112">Этот метод передает `BeginFlush` вызов в нисходящем порядке.</span><span class="sxs-lookup"><span data-stu-id="0214a-112">This method passes the `BeginFlush` call downstream.</span></span>

<span data-ttu-id="0214a-113">Если производный класс использует рабочий поток для доставки образцов, он должен отбросить все данные в очереди во время операции очистки.</span><span class="sxs-lookup"><span data-stu-id="0214a-113">If the derived class uses a worker thread to deliver samples, it should discard any queued data during a flush operation.</span></span> <span data-ttu-id="0214a-114">Это можно сделать либо в `BeginFlush` методе, либо в методе [**ендфлуш**](ctransformfilter-endflush.md) .</span><span class="sxs-lookup"><span data-stu-id="0214a-114">That can be done either in the `BeginFlush` method, or in the [**EndFlush**](ctransformfilter-endflush.md) method.</span></span> <span data-ttu-id="0214a-115">Однако обратите внимание, что вызовы метода `BeginFlush` не синхронизируются с потоком потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="0214a-115">However, note that calls to `BeginFlush` are not synchronized with the streaming thread.</span></span> <span data-ttu-id="0214a-116">Если `BeginFlush` метод отклоняет данные в очереди, то фильтр должен быть аккуратным, чтобы не обрабатывать больше данных между `BeginFlush` вызовами и **ендфлуш** .</span><span class="sxs-lookup"><span data-stu-id="0214a-116">If the `BeginFlush` method discards the queued data, the filter must be careful not to process any more data between the `BeginFlush` and **EndFlush** calls.</span></span> <span data-ttu-id="0214a-117">Дополнительные сведения см. в разделе [поток данных для разработчиков фильтров](data-flow-for-filter-developers.md).</span><span class="sxs-lookup"><span data-stu-id="0214a-117">For more information, see [Data Flow for Filter Developers](data-flow-for-filter-developers.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0214a-118">Требования</span><span class="sxs-lookup"><span data-stu-id="0214a-118">Requirements</span></span>



| <span data-ttu-id="0214a-119">Требование</span><span class="sxs-lookup"><span data-stu-id="0214a-119">Requirement</span></span> | <span data-ttu-id="0214a-120">Значение</span><span class="sxs-lookup"><span data-stu-id="0214a-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0214a-121">Header</span><span class="sxs-lookup"><span data-stu-id="0214a-121">Header</span></span><br/>  | <dl> <span data-ttu-id="0214a-122"><dt>Трансфрм. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0214a-122"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="0214a-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0214a-123">Library</span></span><br/> | <dl> <span data-ttu-id="0214a-124"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="0214a-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0214a-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0214a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0214a-126">**Класс Ктрансформфилтер**</span><span class="sxs-lookup"><span data-stu-id="0214a-126">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




