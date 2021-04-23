---
description: Метод Деливерендфлуш запрашивает подключенный входной ПИН-код для завершения операции очистки.
ms.assetid: e37bf06a-6cdc-4f14-bf2e-7a7d7004cff6
title: Кдинамикаутпутпин. Деливерендфлуш, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.DeliverEndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2666681dcd5637a8e919ced2c61d6536663d7b30
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105656907"
---
# <a name="cdynamicoutputpindeliverendflush-method"></a><span data-ttu-id="a72b9-103">Кдинамикаутпутпин. Деливерендфлуш, метод</span><span class="sxs-lookup"><span data-stu-id="a72b9-103">CDynamicOutputPin.DeliverEndFlush method</span></span>

<span data-ttu-id="a72b9-104">`DeliverEndFlush`Метод запрашивает подключенный входной ПИН-код для завершения операции очистки.</span><span class="sxs-lookup"><span data-stu-id="a72b9-104">The `DeliverEndFlush` method requests the connected input pin to end a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="a72b9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a72b9-105">Syntax</span></span>


```C++
HRESULT DeliverEndFlush();
```



## <a name="parameters"></a><span data-ttu-id="a72b9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a72b9-106">Parameters</span></span>

<span data-ttu-id="a72b9-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="a72b9-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a72b9-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a72b9-108">Return value</span></span>

<span data-ttu-id="a72b9-109">Возвращает \_ значение ОК в случае успешного выполнения или **HRESULT** , указывающий на причину сбоя.</span><span class="sxs-lookup"><span data-stu-id="a72b9-109">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="a72b9-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a72b9-110">Remarks</span></span>

<span data-ttu-id="a72b9-111">Этот метод переопределяет метод [**кбасеаутпутпин::D еливерендфлуш**](cbaseoutputpin-deliverendflush.md) .</span><span class="sxs-lookup"><span data-stu-id="a72b9-111">This method overrides the [**CBaseOutputPin::DeliverEndFlush**](cbaseoutputpin-deliverendflush.md) method.</span></span> <span data-ttu-id="a72b9-112">Он сбрасывает событие [**кдинамикаутпутпин:: m \_ хстопевент**](cdynamicoutputpin-m-hstopevent.md) .</span><span class="sxs-lookup"><span data-stu-id="a72b9-112">It resets the [**CDynamicOutputPin::m\_hStopEvent**](cdynamicoutputpin-m-hstopevent.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="a72b9-113">Требования</span><span class="sxs-lookup"><span data-stu-id="a72b9-113">Requirements</span></span>



| <span data-ttu-id="a72b9-114">Требование</span><span class="sxs-lookup"><span data-stu-id="a72b9-114">Requirement</span></span> | <span data-ttu-id="a72b9-115">Значение</span><span class="sxs-lookup"><span data-stu-id="a72b9-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a72b9-116">Header</span><span class="sxs-lookup"><span data-stu-id="a72b9-116">Header</span></span><br/>  | <dl> <span data-ttu-id="a72b9-117"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a72b9-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a72b9-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a72b9-118">Library</span></span><br/> | <dl> <span data-ttu-id="a72b9-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="a72b9-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a72b9-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a72b9-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a72b9-121">**Класс Кдинамикаутпутпин**</span><span class="sxs-lookup"><span data-stu-id="a72b9-121">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




