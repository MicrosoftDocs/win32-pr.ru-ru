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
ms.openlocfilehash: 304ec081ce7087d822ce3382bf4784c05cbc8782fadb3cdfee887f6bd8f0acfd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119502644"
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

указатель на интерфейс [**имедиаевентсинк**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) диспетчера Graph Manager или **значение NULL** , если фильтр покидает граф фильтра.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

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



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>стрмктл. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбасестреамконтрол**](cbasestreamcontrol.md)
</dt> </dl>

 

 




