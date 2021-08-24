---
description: Метод Duration извлекает длительность потока.
ms.assetid: 82fbd7f5-36dc-4e81-9ce5-9ee28adf73ef
title: Метод Кпуллпин. Duration (Пуллпин. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Duration
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fdc944400bc80fbd5228ac06e2ba1c01f7315305071f7a24c0b38eb125ee1399
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119767984"
---
# <a name="cpullpinduration-method"></a>Кпуллпин. Duration, метод

`Duration`Метод получает длительность потока.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Duration(
   REFERENCE_TIME *ptDuration
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*птдуратион* 
</dt> <dd>

Указатель на переменную, которая получает длительность, в байтах, умноженную на 10 000 000.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение S \_ ОК.

## <a name="remarks"></a>Remarks

длительность не определена до вызова метода [**кпуллпин:: Подключение**](cpullpin-connect.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>Пуллпин. h</dt> </dl>                                                                                                       |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кпуллпин**](cpullpin.md)
</dt> </dl>

 

 




