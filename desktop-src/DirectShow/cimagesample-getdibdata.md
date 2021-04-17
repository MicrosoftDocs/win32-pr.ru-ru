---
description: Метод Жетдибдата извлекает сведения о независимом от устройства GDI (DIB), который управляет этим объектом.
ms.assetid: ec337336-69ec-47ff-a522-42c0388f9bc0
title: Цимажесампле. Жетдибдата, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageSample.GetDIBData
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0fd198152e7c0042a6d48cf942a48745540960d3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674939"
---
# <a name="cimagesamplegetdibdata-method"></a>Цимажесампле. Жетдибдата, метод

`GetDIBData`Метод извлекает сведения о независимом от устройства GDI (DIB), который управляет этим объектом.

## <a name="syntax"></a>Синтаксис


```C++
DIBDATA* GetDIBData();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает указатель на структуру [**дибдата**](dibdata.md) .

## <a name="remarks"></a>Комментарии

Перед вызовом этого метода вызывающий объект должен инициализировать структуру **дибдата** ; Проверьте значение **Цимажесампле:: m \_ Бинит**. Чтобы инициализировать структуру, вызовите метод [**Цимажесампле:: сетдибдата**](cimagesample-setdibdata.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Винутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Цимажесампле**](cimagesample.md)
</dt> </dl>

 

 




