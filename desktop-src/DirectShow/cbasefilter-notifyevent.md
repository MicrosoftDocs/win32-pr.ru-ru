---
description: Метод Нотифевент отправляет уведомление о событии диспетчеру графа фильтров.
ms.assetid: 79587b72-4152-4443-9fde-c2746bf06191
title: Кбасефилтер. Нотифевент, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.NotifyEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 49fa689262d8f9b584c93a4b0485bbeaaacbf9a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657892"
---
# <a name="cbasefilternotifyevent-method"></a>Кбасефилтер. Нотифевент, метод

`NotifyEvent`Метод отправляет уведомление о событии диспетчеру графа фильтров.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT NotifyEvent(
   long     EventCode,
   LONG_PTR EventParam1,
   LONG_PTR EventParam2
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*EventCode* 
</dt> <dd>

Код уведомления о событии.

</dd> <dt>

*EventParam1* 
</dt> <dd>

Первый параметр события.

</dd> <dt>

*EventParam2* 
</dt> <dd>

Второй параметр события.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** . Возможные значения перечислены в следующей таблице.



| Код возврата                                                                               | Описание                                                                                            |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>   | Диспетчер графов фильтров не принимает уведомления о событиях.<br/>                              |
| <dl> <dt>**\_ОК**</dt> </dl>      | Успешно.<br/>                                                                                    |
| <dl> <dt>**E \_ нотимпл**</dt> </dl> | Фильтр не имеет указателя на интерфейс [**имедиаевентсинк**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) .<br/> |



 

## <a name="remarks"></a>Комментарии

Список кодов уведомлений и значений параметров см. в разделе [коды уведомлений о событиях](event-notification-codes.md).

В базовом классе, если код события является EC \_ завершен, метод устанавливает для параметра *EventParam2* указатель на интерфейс [**ибасефилтер**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) фильтра.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Амфилтер. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасефилтер**](cbasefilter.md)
</dt> </dl>

 

 




