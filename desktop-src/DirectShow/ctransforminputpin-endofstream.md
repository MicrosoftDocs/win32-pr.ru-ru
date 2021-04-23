---
description: 'Метод EndOfStream уведомляет ПИН-код о том, что дополнительные данные не ожидаются. Этот метод реализует метод Ипин:: EndOfStream.'
ms.assetid: db9896eb-3db2-4d58-a787-4d80ce8f0d0e
title: Ктрансформинпутпин. EndOfStream, метод (Трансфрм. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bc39770f081499be720c433301823cbc60f37d17
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675650"
---
# <a name="ctransforminputpinendofstream-method"></a><span data-ttu-id="a38d8-104">Ктрансформинпутпин. EndOfStream, метод</span><span class="sxs-lookup"><span data-stu-id="a38d8-104">CTransformInputPin.EndOfStream method</span></span>

<span data-ttu-id="a38d8-105">`EndOfStream`Метод уведомляет ПИН-код о том, что дополнительные данные не ожидаются.</span><span class="sxs-lookup"><span data-stu-id="a38d8-105">The `EndOfStream` method notifies the pin that no additional data is expected.</span></span> <span data-ttu-id="a38d8-106">Этот метод реализует метод [**Ипин:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) .</span><span class="sxs-lookup"><span data-stu-id="a38d8-106">This method implements the [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a38d8-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a38d8-107">Syntax</span></span>


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a><span data-ttu-id="a38d8-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a38d8-108">Parameters</span></span>

<span data-ttu-id="a38d8-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="a38d8-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a38d8-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a38d8-110">Return value</span></span>

<span data-ttu-id="a38d8-111">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a38d8-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="a38d8-112">Возможные значения включают в себя, показанные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="a38d8-112">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="a38d8-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="a38d8-113">Return code</span></span>                                                                                           | <span data-ttu-id="a38d8-114">Описание</span><span class="sxs-lookup"><span data-stu-id="a38d8-114">Description</span></span>                                 |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <span data-ttu-id="a38d8-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="a38d8-115"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="a38d8-116">Успешно.</span><span class="sxs-lookup"><span data-stu-id="a38d8-116">Success.</span></span><br/>                         |
| <dl> <span data-ttu-id="a38d8-117"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="a38d8-117"><dt>**S\_FALSE**</dt></span></span> </dl>               | <span data-ttu-id="a38d8-118">ПИН-код в данный момент очищается.</span><span class="sxs-lookup"><span data-stu-id="a38d8-118">Pin is currently flushing.</span></span><br/>       |
| <dl> <span data-ttu-id="a38d8-119"><dt>**VFW \_ E \_ не \_ подключен**</dt></span><span class="sxs-lookup"><span data-stu-id="a38d8-119"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="a38d8-120">Выходной ПИН-код не подключен.</span><span class="sxs-lookup"><span data-stu-id="a38d8-120">The output pin is not connected.</span></span><br/> |
| <dl> <span data-ttu-id="a38d8-121"><dt>**\_ \_ ошибка среды выполнения VFW E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a38d8-121"><dt>**VFW\_E\_RUNTIME\_ERROR**</dt></span></span> </dl> | <span data-ttu-id="a38d8-122">Произошла ошибка времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="a38d8-122">A run-time error occurred.</span></span><br/>       |
| <dl> <span data-ttu-id="a38d8-123"><dt>**VFW \_ E — \_ неправильное \_ состояние**</dt></span><span class="sxs-lookup"><span data-stu-id="a38d8-123"><dt>**VFW\_E\_WRONG\_STATE**</dt></span></span> </dl>   | <span data-ttu-id="a38d8-124">ПИН-код остановлен.</span><span class="sxs-lookup"><span data-stu-id="a38d8-124">The pin is stopped.</span></span><br/>              |



 

## <a name="remarks"></a><span data-ttu-id="a38d8-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a38d8-125">Remarks</span></span>

<span data-ttu-id="a38d8-126">Этот метод вызывает метод [**ктрансформфилтер:: EndOfStream**](ctransformfilter-endofstream.md) фильтра для доставки уведомления конца потока.</span><span class="sxs-lookup"><span data-stu-id="a38d8-126">This method calls the filter's [**CTransformFilter::EndOfStream**](ctransformfilter-endofstream.md) method to deliver the end-of-stream notification downstream.</span></span>

## <a name="requirements"></a><span data-ttu-id="a38d8-127">Требования</span><span class="sxs-lookup"><span data-stu-id="a38d8-127">Requirements</span></span>



| <span data-ttu-id="a38d8-128">Требование</span><span class="sxs-lookup"><span data-stu-id="a38d8-128">Requirement</span></span> | <span data-ttu-id="a38d8-129">Значение</span><span class="sxs-lookup"><span data-stu-id="a38d8-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a38d8-130">Header</span><span class="sxs-lookup"><span data-stu-id="a38d8-130">Header</span></span><br/>  | <dl> <span data-ttu-id="a38d8-131"><dt>Трансфрм. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a38d8-131"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a38d8-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a38d8-132">Library</span></span><br/> | <dl> <span data-ttu-id="a38d8-133"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="a38d8-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




