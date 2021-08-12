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
ms.openlocfilehash: 894d75512c6c7909f617e13999e7290efea663fa843bf64424aad8371965de75
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118655603"
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

## <a name="remarks"></a>Remarks

Перед вызовом этого метода вызывающий объект должен инициализировать структуру **дибдата** ; Проверьте значение **Цимажесампле:: m \_ Бинит**. Чтобы инициализировать структуру, вызовите метод [**Цимажесампле:: сетдибдата**](cimagesample-setdibdata.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>винутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Цимажесампле**](cimagesample.md)
</dt> </dl>

 

 




