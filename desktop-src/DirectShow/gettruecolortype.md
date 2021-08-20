---
description: Функция Жеттруеколортипе извлекает удобное для восприятия имя подтипа видео.
ms.assetid: 479a020c-b55c-44ec-9096-5528113a4b74
title: Функция Жеттруеколортипе (Вксутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetTrueColorType
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3fb25d4539d4b929362241ffacbfafd97b08844508ec2c1f38c619fe40901475
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119564714"
---
# <a name="gettruecolortype-function"></a>Функция Жеттруеколортипе

Функция **жеттруеколортипе** извлекает удобное для восприятия имя подтипа видео.

## <a name="syntax"></a>Синтаксис


```C++
const GUID GetTrueColorType(
   const BITMAPINFOHEADER *pHeader
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*феадер* 
</dt> <dd>

Указатель на структуру [**битмапинфохеадер**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) , определяющую точечный рисунок.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает МЕДИАСУБТИПЕ \_ RGB555 или медиасубтипе \_ RGB565.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>вксутил. h (включает Потоки. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Функции видео и изображений](video-and-image-functions.md)
</dt> </dl>

 

 




