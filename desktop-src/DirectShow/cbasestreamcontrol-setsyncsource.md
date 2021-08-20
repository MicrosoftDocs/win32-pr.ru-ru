---
description: Метод Сетсинксаурце уведомляет базовый класс о текущем ссылочном времени.
ms.assetid: 056385ac-682c-456e-9a5f-86490bd6e05f
title: Кбасестреамконтрол. Сетсинксаурце, метод (Стрмктл. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.SetSyncSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b2b7fa5a4f627b33bbca1665e3d1ff2c5bc347cfa0e35adec37e0afffa81f198
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954783"
---
# <a name="cbasestreamcontrolsetsyncsource-method"></a>Кбасестреамконтрол. Сетсинксаурце, метод

`SetSyncSource`Метод уведомляет базовый класс о текущем ссылочном времени.

## <a name="syntax"></a>Синтаксис


```C++
void SetSyncSource(
   IReferenceClock *pRefClock
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*префклокк* 
</dt> <dd>

Указатель на интерфейс [**иреференцеклокк**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) ссылочного времени.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

Вызовите этот метод из метода [**имедиафилтер:: сетсинксаурце**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) фильтра. Класс **кбасестреамконтрол** использует интерфейс **иреференцеклокк** , чтобы предотвратить слишком быстрое удаление примеров.

## <a name="examples"></a>Примеры


```C++
STDMETHODIMP CMyFilter::SetSyncSource(IReferenceClock *pClock)
{
    // Note: It's OK if pClock is NULL.

    m_pMyPin->SetSyncSource(pClock);
    return CBaseFilter::SetSyncSource(pClock);
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

 

 




