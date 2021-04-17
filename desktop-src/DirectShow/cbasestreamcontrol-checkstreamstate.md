---
description: Метод Чеккстреамстате определяет, должен ли пример носителя доставляться или отменяться.
ms.assetid: 1533f4b9-e13e-458b-9614-96d733cef4ed
title: Кбасестреамконтрол. Чеккстреамстате, метод (Стрмктл. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.CheckStreamState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e469e288e853ca88a0cf15c209882a8114e33509
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657119"
---
# <a name="cbasestreamcontrolcheckstreamstate-method"></a><span data-ttu-id="0ab6a-103">Кбасестреамконтрол. Чеккстреамстате, метод</span><span class="sxs-lookup"><span data-stu-id="0ab6a-103">CBaseStreamControl.CheckStreamState method</span></span>

<span data-ttu-id="0ab6a-104">`CheckStreamState`Метод определяет, следует ли доставлять или отменять образец носителя.</span><span class="sxs-lookup"><span data-stu-id="0ab6a-104">The `CheckStreamState` method determines whether a media sample should be delivered or discarded.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ab6a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0ab6a-105">Syntax</span></span>


```C++
enum CheckStreamState(
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="0ab6a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0ab6a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ab6a-107">*псампле*</span><span class="sxs-lookup"><span data-stu-id="0ab6a-107">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="0ab6a-108">Указатель на интерфейс [**имедиасампле**](/windows/desktop/api/Strmif/nn-strmif-imediasample) образца.</span><span class="sxs-lookup"><span data-stu-id="0ab6a-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ab6a-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0ab6a-109">Return value</span></span>

<span data-ttu-id="0ab6a-110">Возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="0ab6a-110">Returns one of the following values.</span></span>



| <span data-ttu-id="0ab6a-111">Код возврата</span><span class="sxs-lookup"><span data-stu-id="0ab6a-111">Return code</span></span>                                                                                       | <span data-ttu-id="0ab6a-112">Описание</span><span class="sxs-lookup"><span data-stu-id="0ab6a-112">Description</span></span>                     |
|---------------------------------------------------------------------------------------------------|---------------------------------|
| <dl> <span data-ttu-id="0ab6a-113"><dt>**\_Удаление потока**</dt></span><span class="sxs-lookup"><span data-stu-id="0ab6a-113"><dt>**STREAM\_DISCARDING**</dt></span></span> </dl> | <span data-ttu-id="0ab6a-114">Отбросить этот пример.</span><span class="sxs-lookup"><span data-stu-id="0ab6a-114">Discard this sample.</span></span><br/> |
| <dl> <span data-ttu-id="0ab6a-115"><dt>**ПОТОК передается \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0ab6a-115"><dt>**STREAM\_FLOWING**</dt></span></span> </dl>    | <span data-ttu-id="0ab6a-116">Доставьте этот пример.</span><span class="sxs-lookup"><span data-stu-id="0ab6a-116">Deliver this sample.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0ab6a-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0ab6a-117">Remarks</span></span>

<span data-ttu-id="0ab6a-118">Этот метод следует вызывать, когда ПИН-код получает пример.</span><span class="sxs-lookup"><span data-stu-id="0ab6a-118">Call this method when your pin receives a sample.</span></span> <span data-ttu-id="0ab6a-119">Доставьте пример только в том случае, если возвращаемое значение передается ПОТОКОМ \_ .</span><span class="sxs-lookup"><span data-stu-id="0ab6a-119">Deliver the sample only if the return value is STREAM\_FLOWING.</span></span> <span data-ttu-id="0ab6a-120">Если возвращаемое значение — это ПОТОКовая \_ Отмена, удалите пример.</span><span class="sxs-lookup"><span data-stu-id="0ab6a-120">If the return value is STREAM\_DISCARDING, discard the sample.</span></span>

<span data-ttu-id="0ab6a-121">Если ПИН-код отклоняет все выборки, он должен отметить следующий пример, который он доставляет как ненепрерывное, вызвав метод [**имедиасампле:: сетдисконтинуити**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) .</span><span class="sxs-lookup"><span data-stu-id="0ab6a-121">If the pin discards any samples, it should mark the next sample that it delivers as a discontinuity, by calling the [**IMediaSample::SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) method.</span></span>

<span data-ttu-id="0ab6a-122">Если фильтр реализует интерфейс [**иамдроппедфрамес**](/windows/desktop/api/Strmif/nn-strmif-iamdroppedframes) для подсчета количества кадров, которые он удаляет, не подсчитайте отклоненный кадр как отброшенный кадр.</span><span class="sxs-lookup"><span data-stu-id="0ab6a-122">If your filter implements the [**IAMDroppedFrames**](/windows/desktop/api/Strmif/nn-strmif-iamdroppedframes) interface to count how many frames it drops, do not count a discarded frame as a dropped frame.</span></span>

<span data-ttu-id="0ab6a-123">Если возвращаемое значение — это ПОТОКовая \_ Отмена, метод блокируется до момента, когда время ссылки достигнет времени начала выборки.</span><span class="sxs-lookup"><span data-stu-id="0ab6a-123">When the return value is STREAM\_DISCARDING, the method blocks until the reference time reaches the sample's start time.</span></span> <span data-ttu-id="0ab6a-124">Благодаря этому ПИН-код не сможет быстро отменять выборку.</span><span class="sxs-lookup"><span data-stu-id="0ab6a-124">This prevents your pin from discarding samples too quickly.</span></span> <span data-ttu-id="0ab6a-125">Если фильтр приостановлен, время ожидания будет бесконечным, пока фильтр не будет запущен, остановлен или сброшен данные.</span><span class="sxs-lookup"><span data-stu-id="0ab6a-125">If the filter is paused, the wait time is infinite, until the filter runs, stops, or flushes data.</span></span> <span data-ttu-id="0ab6a-126">(Изменения состояния фильтра и потоковая передача происходят в отдельных потоках, поэтому это не приводит к взаимоблокировке.)</span><span class="sxs-lookup"><span data-stu-id="0ab6a-126">(Filter state changes and streaming happen on separate threads, so this does not cause any deadlock.)</span></span>

<span data-ttu-id="0ab6a-127">Перечисление **кбасестреамконтрол:: стреамконтролстате** определяется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="0ab6a-127">The **CBaseStreamControl::StreamControlState** enumeration is defined as follows:</span></span>


```C++
enum StreamControlState{ 
    STREAM_FLOWING = 0x1000,
    STREAM_DISCARDING
};
```



## <a name="examples"></a><span data-ttu-id="0ab6a-128">Примеры</span><span class="sxs-lookup"><span data-stu-id="0ab6a-128">Examples</span></span>

<span data-ttu-id="0ab6a-129">В следующем примере предполагается, что закрепление использует переменную-член с именем m \_ фластсампледискардед для наблюдения за прекращениями.</span><span class="sxs-lookup"><span data-stu-id="0ab6a-129">The following example assumes that the pin uses a member variable named m\_fLastSampleDiscarded to keep track of discontinuities.</span></span>


```C++
CMyPin::Receive(IMediaSample *pSample)
{
    if (!pSample) return E_POINTER;

    int iStreamState = CheckStreamState(pSample);
    if (iStreamState == STREAM_FLOWING) 
    {
        if (m_fLastSampleDiscarded)
            pSample->SetDiscontinuity(TRUE);
        m_fLastSampleDiscarded = FALSE;
        /* Deliver the sample. */
    } 
    else 
    {
        m_fLastSampleDiscarded = TRUE;  
       // Discard this sample. Do not deliver it.
    }
}
```



## <a name="requirements"></a><span data-ttu-id="0ab6a-130">Требования</span><span class="sxs-lookup"><span data-stu-id="0ab6a-130">Requirements</span></span>



| <span data-ttu-id="0ab6a-131">Требование</span><span class="sxs-lookup"><span data-stu-id="0ab6a-131">Requirement</span></span> | <span data-ttu-id="0ab6a-132">Значение</span><span class="sxs-lookup"><span data-stu-id="0ab6a-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ab6a-133">Header</span><span class="sxs-lookup"><span data-stu-id="0ab6a-133">Header</span></span><br/>  | <dl> <span data-ttu-id="0ab6a-134"><dt>Стрмктл. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0ab6a-134"><dt>Strmctl.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0ab6a-135">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0ab6a-135">Library</span></span><br/> | <dl> <span data-ttu-id="0ab6a-136"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="0ab6a-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ab6a-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0ab6a-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ab6a-138">**Класс Кбасестреамконтрол**</span><span class="sxs-lookup"><span data-stu-id="0ab6a-138">**CBaseStreamControl Class**</span></span>](cbasestreamcontrol.md)
</dt> </dl>

 

 




