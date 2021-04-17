---
description: Метод Финдпиннумбер извлекает номер указанного пин-кода в фильтре.
ms.assetid: c9366fcc-7b13-4e43-883e-6003c32fadec
title: Метод Ксаурце. Финдпиннумбер (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.FindPinNumber
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a6a71c65efd97c48eed58fb7d0b5aa8fcc2f178e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685113"
---
# <a name="csourcefindpinnumber-method"></a>Ксаурце. Финдпиннумбер, метод

`FindPinNumber`Метод извлекает номер указанного пин-кода в фильтре.

## <a name="syntax"></a>Синтаксис


```C++
int FindPinNumber(
   IPin *iPin
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ипин* 
</dt> <dd>

Указатель на интерфейс [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin) ПИН-кода.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает PIN-код или значение 1, если ПИН-код не найден в этом фильтре. Первый ПИН-код имеет нулевое значение.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Source. h (включение Streams. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Ксаурце**](csource.md)
</dt> </dl>

 

 




