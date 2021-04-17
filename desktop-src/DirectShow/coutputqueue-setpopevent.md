---
description: Метод Сетпопевент указывает событие, сообщающее, когда объект удаляет образец из очереди.
ms.assetid: 147a09b9-14d3-4739-843a-1bfb19d2d052
title: Каутпуткуеуе. Сетпопевент, метод (Аутпутк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.SetPopEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 764abf76265fce66c5798923ca1fa522edd682af
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674877"
---
# <a name="coutputqueuesetpopevent-method"></a>Каутпуткуеуе. Сетпопевент, метод

`SetPopEvent`Метод указывает событие, сообщающее, когда объект удаляет выборку из очереди.

## <a name="syntax"></a>Синтаксис


```C++
void SetPopEvent(
   HANDLE hEvent
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хевент* 
</dt> <dd>

Обработчик события, созданного вызывающим объектом.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Аутпутк. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Каутпуткуеуе**](coutputqueue.md)
</dt> </dl>

 

 




