---
description: Метод Нотифифилтерстате уведомляет ПИН-код при изменении состояния фильтра.
ms.assetid: 0eb3b0e5-9c44-464e-b4ca-bcded731e813
title: Кбасестреамконтрол. Нотифифилтерстате, метод (Стрмктл. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.NotifyFilterState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a3433e5c40f86a9e333696774fe671eb7bb90d9803cb9cd6501d7971111e5d36
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120131424"
---
# <a name="cbasestreamcontrolnotifyfilterstate-method"></a>Кбасестреамконтрол. Нотифифилтерстате, метод

`NotifyFilterState`Метод уведомляет ПИН-код при изменении состояния фильтра.

## <a name="syntax"></a>Синтаксис


```C++
void NotifyFilterState(
   FILTER_STATE   new_state,
   REFERENCE_TIME tStart = 0
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*новое \_ состояние* 
</dt> <dd>

Задает новое состояние в качестве члена перечисления [**\_ состояния фильтра**](/windows/win32/api/strmif/ne-strmif-filter_state) .

</dd> <dt>

*тстарт* 
</dt> <dd>

Указывает время начала. Если новое состояние фильтра находится в состоянии \_ выполняется, передайте значение из метода [**имедиафилтер:: Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) . В противном случае используйте значение по умолчанию.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

Этот метод заставляет метод [**кбасестреамконтрол:: чеккстреамстате**](cbasestreamcontrol-checkstreamstate.md) прерывать ожидание. Этот метод следует вызывать каждый раз при изменении состояния фильтра-владельца.

## <a name="examples"></a>Примеры


```C++
STDMETHODIMP CMyFilter::Run(REFERENCE_TIME tStart)
{
   /* Do other things needed by the filter ... */
   m_pMyPin->NotifyFilterState(State_Running, tStart);
   return CBaseFilter::Run(tStart); // Call the filter base class.
}

STDMETHODIMP CMyFilter::Pause()
{
   /* Do other things needed by the filter ... */
   m_pMyPin->NotifyFilterState(State_Paused);
   return CBaseFilter::Pause();
}

STDMETHODIMP CMyFilter::Stop()
{
   /* Do other things needed by the filter ... */
   m_pMyPin->NotifyFilterState(State_Stopped);
   return CBaseFilter::Stop();
}
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>стрмктл. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбасестреамконтрол**](cbasestreamcontrol.md)
</dt> </dl>

 

 




