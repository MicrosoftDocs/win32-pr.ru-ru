---
description: Метод Добуфферпроцессинглуп создает данные мультимедиа и доставляет их в последующий входной ПИН-код.
ms.assetid: a8dce761-eed6-402d-9115-e21822d7a853
title: Метод Ксаурцестреам. Добуфферпроцессинглуп (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.DoBufferProcessingLoop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 809694cacf0c30acf88ddf7d14c7f5ea1f654436
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688969"
---
# <a name="csourcestreamdobufferprocessingloop-method"></a><span data-ttu-id="cf8ce-103">Ксаурцестреам. Добуфферпроцессинглуп, метод</span><span class="sxs-lookup"><span data-stu-id="cf8ce-103">CSourceStream.DoBufferProcessingLoop method</span></span>

<span data-ttu-id="cf8ce-104">`DoBufferProcessingLoop`Метод создает данные мультимедиа и доставляет их в последующий входной ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="cf8ce-104">The `DoBufferProcessingLoop` method generates media data and delivers it to the downstream input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf8ce-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cf8ce-105">Syntax</span></span>


```C++
virtual HRESULT DoBufferProcessingLoop();
```



## <a name="parameters"></a><span data-ttu-id="cf8ce-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="cf8ce-106">Parameters</span></span>

<span data-ttu-id="cf8ce-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="cf8ce-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cf8ce-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cf8ce-108">Return value</span></span>

<span data-ttu-id="cf8ce-109">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="cf8ce-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="cf8ce-110">Возможные значения включают в себя, показанные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="cf8ce-110">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="cf8ce-111">Код возврата</span><span class="sxs-lookup"><span data-stu-id="cf8ce-111">Return code</span></span>                                                                             | <span data-ttu-id="cf8ce-112">Описание</span><span class="sxs-lookup"><span data-stu-id="cf8ce-112">Description</span></span>                                                             |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <span data-ttu-id="cf8ce-113"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="cf8ce-113"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="cf8ce-114">Поток получил запрос на завершение.</span><span class="sxs-lookup"><span data-stu-id="cf8ce-114">Thread received a stop request.</span></span><br/>                              |
| <dl> <span data-ttu-id="cf8ce-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="cf8ce-115"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="cf8ce-116">Поток завершился, или нисходящий фильтр не принимает выборки.</span><span class="sxs-lookup"><span data-stu-id="cf8ce-116">Stream ended, or downstream filter is not accepting samples.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="cf8ce-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cf8ce-117">Remarks</span></span>

<span data-ttu-id="cf8ce-118">Этот метод реализует главный цикл, который обрабатывает данные и доставляет их нисходящим.</span><span class="sxs-lookup"><span data-stu-id="cf8ce-118">This method implements the main loop that processes data and delivers it downstream.</span></span> <span data-ttu-id="cf8ce-119">Каждый раз через цикл метод получает пустой пример носителя из распределителя.</span><span class="sxs-lookup"><span data-stu-id="cf8ce-119">Each time through the loop, the method retrieves an empty media sample from the allocator.</span></span> <span data-ttu-id="cf8ce-120">Он передает пример методу [**ксаурцестреам:: филлбуффер**](csourcestream-fillbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="cf8ce-120">It passes the sample to the [**CSourceStream::FillBuffer**](csourcestream-fillbuffer.md) method.</span></span> <span data-ttu-id="cf8ce-121">Метод **филлбуффер** , который должен реализовываться производным классом, создает данные мультимедиа и помещает их в буфер выборки.</span><span class="sxs-lookup"><span data-stu-id="cf8ce-121">The **FillBuffer** method, which the derived class must implement, generates media data and places it in the sample buffer.</span></span>

<span data-ttu-id="cf8ce-122">Цикл завершается, когда происходит одно из следующих событий:</span><span class="sxs-lookup"><span data-stu-id="cf8ce-122">The loop ends when any of the following occurs:</span></span>

-   <span data-ttu-id="cf8ce-123">Метод [**имеминпутпин:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) входного контакта отклоняет выборку.</span><span class="sxs-lookup"><span data-stu-id="cf8ce-123">The input pin's [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method rejects a sample.</span></span>
-   <span data-ttu-id="cf8ce-124">Метод **филлбуффер** возвращает \_ значение false, указывающее конец потока, или возвращает код ошибки.</span><span class="sxs-lookup"><span data-stu-id="cf8ce-124">The **FillBuffer** method returns S\_FALSE, indicating the end of the stream, or returns an error code.</span></span>
-   <span data-ttu-id="cf8ce-125">Поток получает запрос [**ксаурцестреам:: останавливаться**](csourcestream-stop.md) .</span><span class="sxs-lookup"><span data-stu-id="cf8ce-125">The thread receives a [**CSourceStream::Stop**](csourcestream-stop.md) request.</span></span>

<span data-ttu-id="cf8ce-126">`DoBufferProcessingLoop`Метод обрабатывает уведомление о завершении потока.</span><span class="sxs-lookup"><span data-stu-id="cf8ce-126">The `DoBufferProcessingLoop` method handles the end-of-stream notification.</span></span> <span data-ttu-id="cf8ce-127">При возникновении ошибки оно отправляет событие [**EC \_ еррораборт**](ec-errorabort.md) в Диспетчер графа фильтров.</span><span class="sxs-lookup"><span data-stu-id="cf8ce-127">If an error occurs, it sends an [**EC\_ERRORABORT**](ec-errorabort.md) event to the filter graph manager.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf8ce-128">Требования</span><span class="sxs-lookup"><span data-stu-id="cf8ce-128">Requirements</span></span>



| <span data-ttu-id="cf8ce-129">Требование</span><span class="sxs-lookup"><span data-stu-id="cf8ce-129">Requirement</span></span> | <span data-ttu-id="cf8ce-130">Значение</span><span class="sxs-lookup"><span data-stu-id="cf8ce-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf8ce-131">Header</span><span class="sxs-lookup"><span data-stu-id="cf8ce-131">Header</span></span><br/>  | <dl> <span data-ttu-id="cf8ce-132"><dt>Source. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cf8ce-132"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="cf8ce-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="cf8ce-133">Library</span></span><br/> | <dl> <span data-ttu-id="cf8ce-134"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="cf8ce-134"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf8ce-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cf8ce-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf8ce-136">**Класс Ксаурцестреам**</span><span class="sxs-lookup"><span data-stu-id="cf8ce-136">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




