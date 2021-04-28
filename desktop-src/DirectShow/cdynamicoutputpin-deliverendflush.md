---
description: Кдинамикаутпутпин. Деливерендфлуш, метод Деливерендфлуш запрашивает подключенный входной ПИН-код для завершения операции очистки.
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
ms.openlocfilehash: c8b6952ff50dc2266655c58bd5c2e1ed13105598
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095712"
---
# <a name="cdynamicoutputpindeliverendflush-method"></a><span data-ttu-id="54957-103">Кдинамикаутпутпин. Деливерендфлуш, метод</span><span class="sxs-lookup"><span data-stu-id="54957-103">CDynamicOutputPin.DeliverEndFlush method</span></span>

<span data-ttu-id="54957-104">`DeliverEndFlush`Метод запрашивает подключенный входной ПИН-код для завершения операции очистки.</span><span class="sxs-lookup"><span data-stu-id="54957-104">The `DeliverEndFlush` method requests the connected input pin to end a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="54957-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="54957-105">Syntax</span></span>


```C++
HRESULT DeliverEndFlush();
```



## <a name="parameters"></a><span data-ttu-id="54957-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="54957-106">Parameters</span></span>

<span data-ttu-id="54957-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="54957-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="54957-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="54957-108">Return value</span></span>

<span data-ttu-id="54957-109">Возвращает \_ значение ОК в случае успешного выполнения или **HRESULT** , указывающий на причину сбоя.</span><span class="sxs-lookup"><span data-stu-id="54957-109">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="54957-110">Remarks</span><span class="sxs-lookup"><span data-stu-id="54957-110">Remarks</span></span>

<span data-ttu-id="54957-111">Этот метод переопределяет метод [**кбасеаутпутпин::D еливерендфлуш**](cbaseoutputpin-deliverendflush.md) .</span><span class="sxs-lookup"><span data-stu-id="54957-111">This method overrides the [**CBaseOutputPin::DeliverEndFlush**](cbaseoutputpin-deliverendflush.md) method.</span></span> <span data-ttu-id="54957-112">Он сбрасывает событие [**кдинамикаутпутпин:: m \_ хстопевент**](cdynamicoutputpin-m-hstopevent.md) .</span><span class="sxs-lookup"><span data-stu-id="54957-112">It resets the [**CDynamicOutputPin::m\_hStopEvent**](cdynamicoutputpin-m-hstopevent.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="54957-113">Требования</span><span class="sxs-lookup"><span data-stu-id="54957-113">Requirements</span></span>



| <span data-ttu-id="54957-114">Требование</span><span class="sxs-lookup"><span data-stu-id="54957-114">Requirement</span></span> | <span data-ttu-id="54957-115">Значение</span><span class="sxs-lookup"><span data-stu-id="54957-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54957-116">Header</span><span class="sxs-lookup"><span data-stu-id="54957-116">Header</span></span><br/>  | <dl> <span data-ttu-id="54957-117"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="54957-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="54957-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="54957-118">Library</span></span><br/> | <dl> <span data-ttu-id="54957-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="54957-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54957-120">См. также</span><span class="sxs-lookup"><span data-stu-id="54957-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54957-121">**Класс Кдинамикаутпутпин**</span><span class="sxs-lookup"><span data-stu-id="54957-121">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




