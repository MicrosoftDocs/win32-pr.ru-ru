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
ms.openlocfilehash: 10ef0d29ab46ada118dc97c2d767b8377556086b949b6b9969cf5671b51e5359
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915274"
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

## <a name="remarks"></a>Remarks

Этот метод в течение неограниченного времени ожидает запросов потока, вызывая метод [**камсреад:: WebRequest**](camthread-getrequest.md) . Если он получает запрос [**ксаурцестреам:: Run**](csourcestream-run.md) или [**ксаурцестреам::P Аусе**](csourcestream-pause.md) , он вызывает метод [**ксаурцестреам::D обуфферпроцессинглуп**](csourcestream-dobufferprocessingloop.md) . Метод **добуфферпроцессинглуп** передает данные, пока не получит запрос [**Ксаурцестреам:: останавливаться**](csourcestream-stop.md) . Процедура потока завершает работу при получении запроса [**ксаурцестреам:: Exit**](csourcestream-exit.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>Source. h (включает Потоки. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Ксаурцестреам**](csourcestream.md)
</dt> </dl>

 

 




