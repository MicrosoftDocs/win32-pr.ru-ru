---
description: Метод Жетмедиатипеверсион извлекает номер версии для набора предпочтительных типов мультимедиа.
ms.assetid: bd7b8070-eac5-458c-ada0-7fb0d789dd54
title: Кбасепин. Жетмедиатипеверсион, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.GetMediaTypeVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1f1b50b16a099c8698bbf5bef270173334f1c3ac2c3d2d67ff87778cffddf2ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955193"
---
# <a name="cbasepingetmediatypeversion-method"></a>Кбасепин. Жетмедиатипеверсион, метод

`GetMediaTypeVersion`Метод получает номер версии для набора предпочтительных типов мультимедиа.

## <a name="syntax"></a>Синтаксис


```C++
virtual LONG GetMediaTypeVersion();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает переменную члена [**кбасепин:: m \_ типеверсион**](cbasepin-m-typeversion.md) .

## <a name="remarks"></a>Remarks

Конструктор **кбасепин** Инициализирует номер версии равным 1. В базовом классе это число никогда не изменяется. Если ПИН-код динамически изменяет свой список предпочтительных типов мультимедиа, он должен увеличивать номер версии при каждом изменении списка. Чтобы увеличить номер версии, вызовите метод [**кбасепин:: инкременттипеверсион**](cbasepin-incrementtypeversion.md) .

Перечислитель типа мультимедиа, реализуемый классом [**ценуммедиатипес**](cenummediatypes.md) , использует номер версии для синхронизации с ПИН-кодом.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>амфилтер. h (включает Потоки. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбасепин**](cbasepin.md)
</dt> </dl>

 

 




