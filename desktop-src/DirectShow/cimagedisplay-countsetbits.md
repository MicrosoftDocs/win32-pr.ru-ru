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
ms.openlocfilehash: d334111c18c2c94c79a8b49ed7c0601efabb2bd13922a68c292970d4d2c379bd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119824074"
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
| Заголовок<br/>  | <dl> <dt>винутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Цимажедисплай**](cimagedisplay.md)
</dt> </dl>

 

 




