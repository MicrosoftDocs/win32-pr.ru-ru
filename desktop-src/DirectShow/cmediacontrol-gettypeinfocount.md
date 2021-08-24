---
description: Кмедиаконтрол. Жеттипеинфокаунт, метод возвращает количество интерфейсов типа данных, предоставленных объектом.
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
ms.openlocfilehash: a751c7ed9d10547d34ec491f2e90e5ca6f1ab1f19bc1221c04b15da427da4570
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119832524"
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
| Заголовок<br/>  | <dl> <dt>ктлутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кмедиаконтрол**](cmediacontrol.md)
</dt> </dl>

 

 




