---
description: 'Метод Среадпрок является процедурой потока для рабочего потока. Этот метод реализует чистый виртуальный метод Камсреад:: Среадпрок.'
ms.assetid: 8e66b609-d795-45a8-8fe5-774c659ee350
title: Метод Ксаурцестреам. Среадпрок (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.ThreadProc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6dc7d08643cc0ca76d3d05f0b9090f30200eb181
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675075"
---
# <a name="csourcestreamthreadproc-method"></a>Ксаурцестреам. Среадпрок, метод

`ThreadProc`Метод является процедурой потока для рабочего потока. Этот метод реализует чистый виртуальный метод [**камсреад:: среадпрок**](camthread-threadproc.md) .

## <a name="syntax"></a>Синтаксис


```C++
virtual DWORD ThreadProc();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает 0, если поток успешно завершился, или 1 в противном случае. Если возвращаемое значение равно 1, ресурсы потока по-прежнему могут быть распределены.

## <a name="remarks"></a>Комментарии

Этот метод в течение неограниченного времени ожидает запросов потока, вызывая метод [**камсреад:: WebRequest**](camthread-getrequest.md) . Если он получает запрос [**ксаурцестреам:: Run**](csourcestream-run.md) или [**ксаурцестреам::P Аусе**](csourcestream-pause.md) , он вызывает метод [**ксаурцестреам::D обуфферпроцессинглуп**](csourcestream-dobufferprocessingloop.md) . Метод **добуфферпроцессинглуп** передает данные, пока не получит запрос [**Ксаурцестреам:: останавливаться**](csourcestream-stop.md) . Процедура потока завершает работу при получении запроса [**ксаурцестреам:: Exit**](csourcestream-exit.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Source. h (включение Streams. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Ксаурцестреам**](csourcestream.md)
</dt> </dl>

 

 




