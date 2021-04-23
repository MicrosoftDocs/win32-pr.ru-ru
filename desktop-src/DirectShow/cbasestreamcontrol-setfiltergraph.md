---
description: Метод Сетфилтерграф задает приемник событий для событий потокового управления.
ms.assetid: a4c3dca6-6c80-4eca-87d6-875e746e9ed3
title: Кбасестреамконтрол. Сетфилтерграф, метод (Стрмктл. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.SetFilterGraph
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1cf8b571ee5d017acd056e00a06af54cd90b943a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105656837"
---
# <a name="cbasestreamcontrolsetfiltergraph-method"></a><span data-ttu-id="d9b26-103">Кбасестреамконтрол. Сетфилтерграф, метод</span><span class="sxs-lookup"><span data-stu-id="d9b26-103">CBaseStreamControl.SetFilterGraph method</span></span>

<span data-ttu-id="d9b26-104">`SetFilterGraph`Метод задает приемник событий для событий потокового управления.</span><span class="sxs-lookup"><span data-stu-id="d9b26-104">The `SetFilterGraph` method specifies the event sink for stream control events.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9b26-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d9b26-105">Syntax</span></span>


```C++
void SetFilterGraph(
   IMediaEventSink *pSink
);
```



## <a name="parameters"></a><span data-ttu-id="d9b26-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d9b26-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9b26-107">*псинк*</span><span class="sxs-lookup"><span data-stu-id="d9b26-107">*pSink*</span></span> 
</dt> <dd>

<span data-ttu-id="d9b26-108">Указатель на интерфейс [**Имедиаевентсинк**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) диспетчера графа фильтров или **значение NULL** , если фильтр покидает граф фильтра.</span><span class="sxs-lookup"><span data-stu-id="d9b26-108">Pointer to the Filter Graph Manager's [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) interface, or **NULL** when the filter leaves the filter graph.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9b26-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d9b26-109">Return value</span></span>

<span data-ttu-id="d9b26-110">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="d9b26-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9b26-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d9b26-111">Remarks</span></span>

<span data-ttu-id="d9b26-112">Вызовите этот метод из метода [**ибасефилтер:: жоинфилтерграф**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) фильтра.</span><span class="sxs-lookup"><span data-stu-id="d9b26-112">Call this method from inside the filter's [**IBaseFilter::JoinFilterGraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) method.</span></span> <span data-ttu-id="d9b26-113">Класс **кбасестреамконтрол** использует интерфейс **имедиаевентсинк** для отправки [**\_ \_ управления потоком \_ EC**](ec-stream-control-started.md) , а также для [**\_ \_ \_ остановленных событий управления потоком EC**](ec-stream-control-stopped.md) .</span><span class="sxs-lookup"><span data-stu-id="d9b26-113">The **CBaseStreamControl** class uses the **IMediaEventSink** interface to send [**EC\_STREAM\_CONTROL\_STARTED**](ec-stream-control-started.md) and [**EC\_STREAM\_CONTROL\_STOPPED**](ec-stream-control-stopped.md) events.</span></span>

<span data-ttu-id="d9b26-114">Если фильтр является производным от **кбасефилтер**, сначала вызовите метод [**Кбасефилтер:: жоинфилтерграф**](cbasefilter-joinfiltergraph.md) , который задает переменную члена [**кбасефилтер:: m \_ псинк**](cbasefilter-m-psink.md) .</span><span class="sxs-lookup"><span data-stu-id="d9b26-114">If your filter derives from **CBaseFilter**, first call the [**CBaseFilter::JoinFilterGraph**](cbasefilter-joinfiltergraph.md) method, which sets the [**CBaseFilter::m\_pSink**](cbasefilter-m-psink.md) member variable.</span></span> <span data-ttu-id="d9b26-115">Затем передайте **m \_ псинк** в `SetFilterGraph` метод.</span><span class="sxs-lookup"><span data-stu-id="d9b26-115">Then pass **m\_pSink** to the `SetFilterGraph` method.</span></span> <span data-ttu-id="d9b26-116">Обратите внимание, что **m \_ Псинк** имеет **значение NULL** , если фильтр покидает граф, что является правильным.</span><span class="sxs-lookup"><span data-stu-id="d9b26-116">Note that **m\_pSink** is **NULL** when the filter leaves the graph, which is correct.</span></span>

## <a name="examples"></a><span data-ttu-id="d9b26-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="d9b26-117">Examples</span></span>


```C++
STDMETHODIMP CMyFilter::JoinFilterGraph(IFilterGraph * pGraph, LPCWSTR pName)
{
    // Note: It's OK if pGraph is NULL.

    HRESULT hr = CBaseFilter::JoinFilterGraph(pGraph, pName);
    if (SUCCEEDED(hr)) 
    {
        m_pMyPin->SetFilterGraph(m_pSink);
    }
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="d9b26-118">Требования</span><span class="sxs-lookup"><span data-stu-id="d9b26-118">Requirements</span></span>



| <span data-ttu-id="d9b26-119">Требование</span><span class="sxs-lookup"><span data-stu-id="d9b26-119">Requirement</span></span> | <span data-ttu-id="d9b26-120">Значение</span><span class="sxs-lookup"><span data-stu-id="d9b26-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9b26-121">Header</span><span class="sxs-lookup"><span data-stu-id="d9b26-121">Header</span></span><br/>  | <dl> <span data-ttu-id="d9b26-122"><dt>Стрмктл. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d9b26-122"><dt>Strmctl.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d9b26-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d9b26-123">Library</span></span><br/> | <dl> <span data-ttu-id="d9b26-124"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="d9b26-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9b26-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d9b26-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9b26-126">**Класс Кбасестреамконтрол**</span><span class="sxs-lookup"><span data-stu-id="d9b26-126">**CBaseStreamControl Class**</span></span>](cbasestreamcontrol.md)
</dt> </dl>

 

 




