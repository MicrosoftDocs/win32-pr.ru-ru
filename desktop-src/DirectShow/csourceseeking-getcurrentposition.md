---
description: Метод Жеткуррентпоситион извлекает текущую точку относительно общей продолжительности потока. Не реализован.
ms.assetid: 386f41e4-a673-4c67-a28f-e155810fbb5a
title: Ксаурцесикинг. Жеткуррентпоситион, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetCurrentPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 52f99323e5ce3a62f1964cad2586a18ad473cdc0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657506"
---
# <a name="csourceseekinggetcurrentposition-method"></a>Ксаурцесикинг. Жеткуррентпоситион, метод

`GetCurrentPosition`Метод получает текущую координату относительно общей продолжительности потока. Не реализован.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetCurrentPosition(
   LONGLONG *pCurrent
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пкуррент* 
</dt> <dd>

Указатель на переменную, которая получает текущую координату в единицах текущего формата времени.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает E \_ нотимпл.

## <a name="remarks"></a>Комментарии

Фильтры источников обычно не поддерживают этот метод. Вместо этого фильтры модуля подготовки отчетов сообщают о текущей позицией через класс [**крендерерпоспасссру**](crendererpospassthru.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ктлутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Ксаурцесикинг**](csourceseeking.md)
</dt> </dl>

 

 




