---
description: 'Кбасепин. notify, метод notify уведомляет ПИН-код о том, что запрошено изменение качества. Этот метод реализует метод Икуалитиконтрол:: notify.'
ms.assetid: 5e9394d9-8d3c-4091-b45f-345a3f7270db
title: Метод Кбасепин. notify (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Notify
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0e74a8880e446300ca142bfcf28633d267d184178a0c3572c3a8049667536978
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910444"
---
# <a name="cbasepinnotify-method"></a>Кбасепин. notify, метод

`Notify`Метод уведомляет ПИН-код о том, что запрошено изменение качества. Этот метод реализует метод [**икуалитиконтрол:: notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Notify(
   IBaseFilter *pSelf,
   Quality     q
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пселф* 
</dt> <dd>

Указатель на интерфейс [**ибасефилтер**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) фильтра, который доставил сообщение контроля качества.

</dd> <dt>

*формате* 
</dt> <dd>

Задает структуру [**качества**](/windows/win32/api/strmif/ns-strmif-quality) , содержащую сообщение контроля качества.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Базовый класс возвращает E \_ нотимпл.

## <a name="remarks"></a>Remarks

Выходные сигналы должны переопределять этот метод, чтобы принимать сообщения контроля качества.

Если установлен внешний диспетчер качества (см. раздел [**кбасепин:: сетсинк**](cbasepin-setsink.md)), передайте сообщение в Диспетчер качества. В противном случае фильтр должен обрабатывать само сообщение или передавать поток сообщений. Дополнительные сведения см. в разделе [Управление качеством](quality-control-management.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>амфилтер. h (включает Потоки. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасепин**](cbasepin.md)
</dt> </dl>

 

 




