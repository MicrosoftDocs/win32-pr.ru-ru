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
# <a name="cbasestreamcontrolcheckstreamstate-method"></a>Кбасестреамконтрол. Чеккстреамстате, метод

`CheckStreamState`Метод определяет, следует ли доставлять или отменять образец носителя.

## <a name="syntax"></a>Синтаксис


```C++
enum CheckStreamState(
   IMediaSample *pSample
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*псампле* 
</dt> <dd>

Указатель на интерфейс [**имедиасампле**](/windows/desktop/api/Strmif/nn-strmif-imediasample) образца.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает одно из следующих значений.



| Код возврата                                                                                       | Описание                     |
|---------------------------------------------------------------------------------------------------|---------------------------------|
| <dl> <dt>**\_Удаление потока**</dt> </dl> | Отбросить этот пример.<br/> |
| <dl> <dt>**ПОТОК передается \_**</dt> </dl>    | Доставьте этот пример.<br/> |



 

## <a name="remarks"></a>Комментарии

Этот метод следует вызывать, когда ПИН-код получает пример. Доставьте пример только в том случае, если возвращаемое значение передается ПОТОКОМ \_ . Если возвращаемое значение — это ПОТОКовая \_ Отмена, удалите пример.

Если ПИН-код отклоняет все выборки, он должен отметить следующий пример, который он доставляет как ненепрерывное, вызвав метод [**имедиасампле:: сетдисконтинуити**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) .

Если фильтр реализует интерфейс [**иамдроппедфрамес**](/windows/desktop/api/Strmif/nn-strmif-iamdroppedframes) для подсчета количества кадров, которые он удаляет, не подсчитайте отклоненный кадр как отброшенный кадр.

Если возвращаемое значение — это ПОТОКовая \_ Отмена, метод блокируется до момента, когда время ссылки достигнет времени начала выборки. Благодаря этому ПИН-код не сможет быстро отменять выборку. Если фильтр приостановлен, время ожидания будет бесконечным, пока фильтр не будет запущен, остановлен или сброшен данные. (Изменения состояния фильтра и потоковая передача происходят в отдельных потоках, поэтому это не приводит к взаимоблокировке.)

Перечисление **кбасестреамконтрол:: стреамконтролстате** определяется следующим образом:


```C++
enum StreamControlState{ 
    STREAM_FLOWING = 0x1000,
    STREAM_DISCARDING
};
```



## <a name="examples"></a>Примеры

В следующем примере предполагается, что закрепление использует переменную-член с именем m \_ фластсампледискардед для наблюдения за прекращениями.


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



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Стрмктл. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасестреамконтрол**](cbasestreamcontrol.md)
</dt> </dl>

 

 




