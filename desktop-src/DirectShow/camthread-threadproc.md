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
ms.openlocfilehash: 6419d315e162f859f49ee2448758999ca194adf8c16c6210f77d919fa2a18f47
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118662117"
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

## <a name="remarks"></a>Remarks

Это чистый виртуальный метод. Реализуйте этот метод в производном классе для предоставления потоковой процедуры. Когда метод [**камсреад:: Create**](camthread-create.md) создает поток, он предоставляет адрес метода [**Камсреад:: инитиалсреадпрок**](camthread-initialthreadproc.md) , который, в свою очередь, вызывает метод среадпрок.

Как правило, метод Среадпрок будет вводить цикл, который получает запросы (путем вызова методов [**камсреад:: WebRequest**](camthread-getrequest.md) или [**Камсреад:: чеккрекуест**](camthread-checkrequest.md) ) и обрабатывает данные.

При возврате из этого метода поток завершает работу.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>вксутил. h (включает Потоки. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Камсреад**](camthread.md)
</dt> </dl>

 

 




