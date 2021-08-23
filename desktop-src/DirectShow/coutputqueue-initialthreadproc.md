---
description: 'Метод Инитиалсреадпрок вызывает метод Каутпуткуеуе:: Среадпрок при создании потока.'
ms.assetid: 6093f0c3-ec58-418d-bb8c-618163c43ac7
title: COutputQueue.Iniметод Тиалсреадпрок (Аутпутк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.InitialThreadProc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a80561ae652df7168ad09c1cf6e9fde767154e6c72a8fe5360a5d09c784941f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813594"
---
# <a name="coutputqueueinitialthreadproc-method"></a>COutputQueue.Iniметод Тиалсреадпрок

`InitialThreadProc`При создании потока метод вызывает метод [**каутпуткуеуе:: среадпрок**](coutputqueue-threadproc.md) .

## <a name="syntax"></a>Синтаксис


```C++
static DWORD WINAPI InitialThreadProc(
   LPVOID pv
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*PV* 
</dt> <dd>

`this` вид.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение, возвращаемое методом [**каутпуткуеуе:: среадпрок**](coutputqueue-threadproc.md) .

## <a name="remarks"></a>Remarks

Этот метод является процедурой потока для рабочего потока объекта. `this`Указатель объекта является параметром потока. Метод отменяет ссылку на него для вызова **среадпрок**.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>аутпутк. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Каутпуткуеуе**](coutputqueue.md)
</dt> </dl>

 

 




