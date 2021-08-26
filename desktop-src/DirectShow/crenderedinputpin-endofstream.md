---
description: 'Метод EndOfStream уведомляет ПИН-код о том, что дополнительные данные не ожидаются, пока для фильтра не будет выдана новая команда Run. Этот метод реализует метод Ипин:: EndOfStream.'
ms.assetid: 915beab4-2fc3-4acd-bb30-c0851df058db
title: Крендерединпутпин. EndOfStream, метод (Амекстра. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRenderedInputPin.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 26f7a5075e06a3943978a8e938f034fbabcaddfa31c9ffa2a2b37d33a0120640
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107994"
---
# <a name="crenderedinputpinendofstream-method"></a>Крендерединпутпин. EndOfStream, метод

`EndOfStream`Метод уведомляет ПИН-код о том, что дополнительные данные не ожидаются, пока не будет выполнена новая команда запуска для фильтра. Этот метод реализует метод [**Ипин:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает \_ ОК, если успешно, или код ошибки в противном случае.

## <a name="remarks"></a>Remarks

если фильтр выполняется, этот метод отправляет событие [**\_ завершения EC**](ec-complete.md) в фильтр Graph Manager. В противном случае устанавливает флаг, чтобы \_ при следующем запуске фильтра было отправлено событие EC Complete. При сбросе фильтра снимается флажок.

Этот метод следует переопределить для удержания потоковой блокировки ПИН-кода:


```C++
class CMyInputPin : public CRenderedInputPin
{
private:
    CCritSec * const m_pReceiveLock; // Streaming lock.
public:
    STDMETHODIMP EndOfStream(void);

    /* (Remainder of the class declaration not shown.) */
};

STDMETHODIMP CMyInputPin::EndOfStream(void)
{
    CAutoLock lock(m_pReceiveLock);  
    return CRenderedInputPin::EndOfStream();
} 
```



Кроме того, если фильтр обрабатывает вызовы **Receive** асинхронно, ПИН-код должен подождать отправки события EC \_ Complete до тех пор, пока фильтр не обработал все отложенные выборки.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>амекстра. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Крендерединпутпин**](crenderedinputpin.md)
</dt> </dl>

 

 




