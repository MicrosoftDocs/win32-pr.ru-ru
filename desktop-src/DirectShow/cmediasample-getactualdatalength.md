---
description: 'Метод Жетактуалдаталенгс извлекает длину допустимых данных в буфере. Этот метод реализует метод Имедиасампле:: Жетактуалдаталенгс.'
ms.assetid: bdb8c2b9-7be4-494b-bb96-34a9936d4a2f
title: Кмедиасампле. Жетактуалдаталенгс, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.GetActualDataLength
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2e65b72c1e0b6db85a271c10f76e5630b0799b78
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669223"
---
# <a name="cmediasamplegetactualdatalength-method"></a>Кмедиасампле. Жетактуалдаталенгс, метод

`GetActualDataLength`Метод получает длину допустимых данных в буфере. Этот метод реализует метод [**имедиасампле:: жетактуалдаталенгс**](/windows/win32/api/strmif/nf-strmif-imediasample-getactualdatalength) .

## <a name="syntax"></a>Синтаксис


```C++
LONG GetActualDataLength();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает длину допустимых данных в байтах.

## <a name="remarks"></a>Комментарии

Значение этого свойства указывается в переменной члена [**кмедиасампле:: m \_ лактуал**](cmediasample-m-lactual.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Амфилтер. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кмедиасампле**](cmediasample.md)
</dt> </dl>

 

