---
description: Метод Каунтсетбитс возвращает число битов, заданное равным 1, в указанном битовом поле.
ms.assetid: fc5701b8-88ff-4c23-9d26-854bb65cc55c
title: Цимажедисплай. Каунтсетбитс, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CountSetBits
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cb425b08b524b1d36b622bcfffcc9f311dccbbdf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679950"
---
# <a name="cimagedisplaycountsetbits-method"></a>Цимажедисплай. Каунтсетбитс, метод

`CountSetBits`Метод возвращает число бит, установленное в 1, в указанном битовом поле.

## <a name="syntax"></a>Синтаксис


```C++
DWORD CountSetBits(
   const DWORD Field
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Поле* 
</dt> <dd>

Задает битовое поле в виде значения **типа DWORD** .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает число битов, для которых задано значение 1.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Винутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Цимажедисплай**](cimagedisplay.md)
</dt> </dl>

 

 




