---
description: Метод Среадпрок является процедурой потока.
ms.assetid: 2d991f15-afea-4843-bc68-aeb5ca69d28b
title: Камсреад. Среадпрок, метод (Вксутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.ThreadProc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7081a7f7e1cd84a6bf8d482aa7dddf7a48b39f0a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657705"
---
# <a name="camthreadthreadproc-method"></a>Камсреад. Среадпрок, метод

`ThreadProc`Метод является процедурой потока.

## <a name="syntax"></a>Синтаксис


```C++
virtual DWORD ThreadProc() = 0;
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **типа DWORD** , значение которого определяется производным классом.

## <a name="remarks"></a>Комментарии

Это чистый виртуальный метод. Реализуйте этот метод в производном классе для предоставления потоковой процедуры. Когда метод [**камсреад:: Create**](camthread-create.md) создает поток, он предоставляет адрес метода [**Камсреад:: инитиалсреадпрок**](camthread-initialthreadproc.md) , который, в свою очередь, вызывает метод среадпрок.

Как правило, метод Среадпрок будет вводить цикл, который получает запросы (путем вызова методов [**камсреад:: WebRequest**](camthread-getrequest.md) или [**Камсреад:: чеккрекуест**](camthread-checkrequest.md) ) и обрабатывает данные.

При возврате из этого метода поток завершает работу.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Вксутил. h (включение Streams. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Камсреад**](camthread.md)
</dt> </dl>

 

 




