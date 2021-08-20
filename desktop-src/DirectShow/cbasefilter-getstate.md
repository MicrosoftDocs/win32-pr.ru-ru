---
description: 'Метод WebMethod получает состояние фильтров (запущено, остановлено или приостановлено). Этот метод реализует метод Имедиафилтер:: WebMethod.'
ms.assetid: e32e3a1d-857f-4db3-b52c-5b6b802ded42
title: Метод Кбасефилтер. WebMethod (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9b6ed61b8b1e72652e9590d11827322256d4923bd92405206e5c5419cd5e7ae5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017172"
---
# <a name="cbasefiltergetstate-method"></a>Кбасефилтер. метод State

`GetState`Метод получает состояние фильтров (запущено, остановлено или приостановлено). Этот метод реализует метод [**имедиафилтер::**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate) WebMethod.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetState(
   DWORD        dwMilliSecsTimeout,
   FILTER_STATE *State
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*двмиллисекстимеаут* 
</dt> <dd>

Интервал времени ожидания (в миллисекундах).

</dd> <dt>

*Состояние* 
</dt> <dd>

Указатель на переменную, которая получает Член перечисляемого [**типа \_ состояния фильтра**](/windows/win32/api/strmif/ne-strmif-filter_state) , указывающий состояние фильтра.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение S \_ (ОК) или \_ указатель E.

## <a name="remarks"></a>Remarks

В базовом классе все переходы состояния являются синхронными, а параметр *двмиллисекстимеаут* игнорируется. Если производный класс выполняет асинхронные переходы состояний, он должен переопределять этот метод для ожидания во время переходов состояния с истечением времени ожидания *двмиллисекстимеаут* миллисекунд.

Если фильтр не доставляет данные при приостановке, переопределите `GetState` метод, чтобы он возвращал значение VFW S не может быть \_ \_ \_ подсказкой, если фильтр приостановлен (см. раздел [Доставка образцов](delivering-samples.md)). Например:


```C++
CMyFilter::GetState(DWORD dw, FILTER_STATE *pState)
{
    CheckPointer(pState, E_POINTER);
    *pState = m_State;
    if (m_State == State_Paused)
        return VFW_S_CANT_CUE;
    else
        return S_OK;
}
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>амфилтер. h (включает Потоки. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасефилтер**](cbasefilter.md)
</dt> </dl>

 

 




