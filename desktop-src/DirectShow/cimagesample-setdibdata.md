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
ms.openlocfilehash: 367fed37545e9498f9f6e753a57a7eeeb2ce8767779241284be9109676fafd38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118655528"
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
| Заголовок<br/>  | <dl> <dt>винутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Цимажесампле**](cimagesample.md)
</dt> </dl>

 

 




