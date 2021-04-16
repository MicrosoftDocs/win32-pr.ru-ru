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
# <a name="cbasestreamcontrolsetfiltergraph-method"></a>Кбасестреамконтрол. Сетфилтерграф, метод

`SetFilterGraph`Метод задает приемник событий для событий потокового управления.

## <a name="syntax"></a>Синтаксис


```C++
void SetFilterGraph(
   IMediaEventSink *pSink
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*псинк* 
</dt> <dd>

Указатель на интерфейс [**Имедиаевентсинк**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) диспетчера графа фильтров или **значение NULL** , если фильтр покидает граф фильтра.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Вызовите этот метод из метода [**ибасефилтер:: жоинфилтерграф**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) фильтра. Класс **кбасестреамконтрол** использует интерфейс **имедиаевентсинк** для отправки [**\_ \_ управления потоком \_ EC**](ec-stream-control-started.md) , а также для [**\_ \_ \_ остановленных событий управления потоком EC**](ec-stream-control-stopped.md) .

Если фильтр является производным от **кбасефилтер**, сначала вызовите метод [**Кбасефилтер:: жоинфилтерграф**](cbasefilter-joinfiltergraph.md) , который задает переменную члена [**кбасефилтер:: m \_ псинк**](cbasefilter-m-psink.md) . Затем передайте **m \_ псинк** в `SetFilterGraph` метод. Обратите внимание, что **m \_ Псинк** имеет **значение NULL** , если фильтр покидает граф, что является правильным.

## <a name="examples"></a>Примеры


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



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Стрмктл. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасестреамконтрол**](cbasestreamcontrol.md)
</dt> </dl>

 

 




