---
description: Функция Жетбиткаунт возвращает число бит на пиксель, используемых указанным подтипом видео. Эта функция допустима только для несжатых подтипов RGB.
ms.assetid: 876b91c8-50ba-4217-b79c-7f7ec1c22b83
title: Функция Жетбиткаунт (Вксутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetBitCount
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6fed9b24ebf2e95b2408de30a407904e6bd3c1c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675531"
---
# <a name="getbitcount-function"></a>Функция Жетбиткаунт

`GetBitCount`Функция возвращает число бит на пиксель, используемых указанным подтипом видео. Эта функция допустима только для несжатых подтипов RGB.

## <a name="syntax"></a>Синтаксис


```C++
WORD GetBitCount(
   const GUID *pSubtype
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*псубтипе* 
</dt> <dd>

Указатель на **GUID** подтипа видео.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает число битов на пиксель для этого подтипа или значение **ушрт \_ Max** , если подтип не распознан.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Вксутил. h (включение Streams. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции видео и изображений](video-and-image-functions.md)
</dt> </dl>

 

 




