---
description: Функция Ваитдиспатчингмессажес ожидает сигнала объекта, во время диспетчеризации сообщений окна.
ms.assetid: d15f6736-d141-47a3-b767-fbf774982fb4
title: Функция Ваитдиспатчингмессажес (Вксутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WaitDispatchingMessages
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9e509a081243f28293dc2d8abf8311f69eaf9a44
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685365"
---
# <a name="waitdispatchingmessages-function"></a>Функция Ваитдиспатчингмессажес

`WaitDispatchingMessages`Функция ожидает сигнала объекта, во время диспетчеризации сообщений окна.

## <a name="syntax"></a>Синтаксис


```C++
DWORD WINAPI WaitDispatchingMessages(
   HANDLE hObject,
   DWORD  dwWait,
   HWND   hwnd = NULL,
   UINT   uMsg = 0,
   HANDLE hEvent = NULL
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хобжект* 
</dt> <dd>

Обрабатываемый объект для ожидания.

</dd> <dt>

*двваит* 
</dt> <dd>

Интервал времени ожидания (в миллисекундах).

</dd> <dt>

*HWND* 
</dt> <dd>

Необязательный обработчик для окна.

</dd> <dt>

*Uiacp* 
</dt> <dd>

Необязательное окно сообщения с указанием отправляемого сообщения.

</dd> <dt>

*хевент* 
</dt> <dd>

Необязательный обработчик события для ожидания.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение из функции **WaitForMultipleObjects** .

## <a name="remarks"></a>Комментарии

Если объект владеет окном, он должен отправлять сообщения окна в ожидании. Эта функция позволяет объекту ожидать события, семафора или другого взаимоисключающего объекта во время диспетчеризации сообщений.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Вксутил. h (включение Streams. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Различные вспомогательные функции](miscellaneous-helper-functions.md)
</dt> </dl>

 

 




