---
description: Метод Сетдибдата указывает сведения о независимом от устройства GDI (DIB), который управляет этим объектом. Вызовите этот метод, чтобы инициализировать объект Цимажесампле.
ms.assetid: 850fa16b-d4b9-4fe6-b202-7b54c49a4589
title: Цимажесампле. Сетдибдата, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageSample.SetDIBData
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 418263da0416b325b1b080713dd6289f3bcc688e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665227"
---
# <a name="cimagesamplesetdibdata-method"></a>Цимажесампле. Сетдибдата, метод

`SetDIBData`Метод указывает сведения о независимом от устройства GDI (DIB), который управляет этим объектом. Вызовите этот метод, чтобы инициализировать объект **Цимажесампле** .

## <a name="syntax"></a>Синтаксис


```C++
void SetDIBData(
   DIBDATA *pDibData
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пдибдата* 
</dt> <dd>

Указатель на структуру [**дибдата**](dibdata.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Винутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Цимажесампле**](cimagesample.md)
</dt> </dl>

 

 




