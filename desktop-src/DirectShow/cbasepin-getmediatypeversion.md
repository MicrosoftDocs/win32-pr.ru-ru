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
ms.openlocfilehash: fe01d33d7a7c1cb65bc0e2391af63e3519d9cce3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105658105"
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

## <a name="remarks"></a>Комментарии

Конструктор **кбасепин** Инициализирует номер версии равным 1. В базовом классе это число никогда не изменяется. Если ПИН-код динамически изменяет свой список предпочтительных типов мультимедиа, он должен увеличивать номер версии при каждом изменении списка. Чтобы увеличить номер версии, вызовите метод [**кбасепин:: инкременттипеверсион**](cbasepin-incrementtypeversion.md) .

Перечислитель типа мультимедиа, реализуемый классом [**ценуммедиатипес**](cenummediatypes.md) , использует номер версии для синхронизации с ПИН-кодом.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Амфилтер. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасепин**](cbasepin.md)
</dt> </dl>

 

 




