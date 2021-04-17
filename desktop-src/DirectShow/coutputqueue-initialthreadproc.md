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
ms.openlocfilehash: dfc7b8660d838b6ad31dd298c509b6282ab61810
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679702"
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

## <a name="remarks"></a>Комментарии

Этот метод является процедурой потока для рабочего потока объекта. `this`Указатель объекта является параметром потока. Метод отменяет ссылку на него для вызова **среадпрок**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Аутпутк. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Каутпуткуеуе**](coutputqueue.md)
</dt> </dl>

 

 




