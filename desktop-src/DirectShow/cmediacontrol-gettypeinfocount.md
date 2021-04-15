---
description: Извлекает количество интерфейсов типа данных, предоставленных объектом.
ms.assetid: 29575325-8f97-4f39-8272-86a917d9144f
title: Кмедиаконтрол. Жеттипеинфокаунт, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaControl.GetTypeInfoCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f2454e503a045a02db20c0dc457b6367f6d3b427
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669192"
---
# <a name="cmediacontrolgettypeinfocount-method"></a>Кмедиаконтрол. Жеттипеинфокаунт, метод

Извлекает количество интерфейсов типа данных, предоставленных объектом.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetTypeInfoCount(
   UINT *pctinfo
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пктинфо* 
</dt> <dd>

Указатель на число интерфейсов типа-данных, предоставляемых объектом. Если объект предоставляет сведения о типе, это число равно 1; в противном случае число равно 0.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает \_ указатель E, если *пктинфо* является недопустимым; в противном случае возвращает значение S \_ ОК.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ктлутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кмедиаконтрол**](cmediacontrol.md)
</dt> </dl>

 

 




