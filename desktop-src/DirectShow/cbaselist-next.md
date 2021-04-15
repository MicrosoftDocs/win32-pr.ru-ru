---
description: Следующий метод извлекает следующее расположение в списке.
ms.assetid: ba9753b0-c82e-4772-84a7-e9982de3b8ad
title: Метод Кбаселист. Next (Вкслист. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.Next
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f8a09ec91191437fbfb851ce92824b118a5440ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668596"
---
# <a name="cbaselistnext-method"></a>Кбаселист. Next, метод

`Next`Метод получает следующую точку в списке.

## <a name="syntax"></a>Синтаксис


```C++
POSITION Next(
   POSITION pos
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pos* 
</dt> <dd>

Значение расположения.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает индикатор положения, следующий за позицией, заданной в *POS*.

## <a name="remarks"></a>Комментарии

Если *POS* является последней позицией в списке, метод возвращает **значение NULL**. Если *POS* имеет **значение NULL**, метод возвращает первую точку в списке.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Вкслист. h (включение Streams. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбаселист**](cbaselist.md)
</dt> </dl>

 

 




