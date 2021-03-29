---
description: 'Метод Адвисепериодик создает периодические запросы рекомендаций. Этот метод реализует метод Иреференцеклокк:: Адвисепериодик.'
ms.assetid: ddaf0861-df11-4008-8e9c-a0c53929cd3f
title: Кбасереференцеклокк. Адвисепериодик, метод (Рефклокк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.AdvisePeriodic
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a582e05756e8d034e5b2d0a1cd8f7eb569dbb842
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668924"
---
# <a name="cbasereferenceclockadviseperiodic-method"></a>Кбасереференцеклокк. Адвисепериодик, метод

`AdvisePeriodic`Метод создает периодические запросы рекомендаций. Этот метод реализует метод [**иреференцеклокк:: адвисепериодик**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-adviseperiodic) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT AdvisePeriodic(
   REFERENCE_TIME StartTime,
   REFERENCE_TIME PeriodTime,
   HSEMAPHORE     hSemaphore,
   DWORD_PTR      *pdwAdviseToken
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*StartTime* 
</dt> <dd>

Время первого уведомления в единицах с 100 нс. Должно быть больше нуля и меньше максимального \_ времени.

</dd> <dt>

*периодтиме* 
</dt> <dd>

Время между уведомлениями (в 100-наносекундных единицах). Должен быть больше нуля.

</dd> <dt>

*хсемафоре* 
</dt> <dd>

Обработчик для семафора, созданного вызывающим объектом.

</dd> <dt>

*пдвадвисетокен* 
</dt> <dd>

Указатель на переменную, которая получает идентификатор для запроса Advise.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает одно из значений **HRESULT** , приведенных в следующей таблице.



| Код возврата                                                                                   | Описание                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>          | Успешно<br/>                   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Недопустимые значения времени<br/>       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Failure<br/>                   |
| <dl> <dt>**\_указатель E**</dt> </dl>     | **Пустой** аргумент указателя<br/> |



 

## <a name="remarks"></a>Комментарии

Во время каждого уведомления часы освобождают семафор, указанный в параметре *хсемафоре* . Если дальнейшие уведомления не требуются, вызовите метод [**кбасереференцеклокк:: unadvise**](cbasereferenceclock-unadvise.md) и передайте значение *пдвадвисетокен* , возвращенное этим вызовом.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Рефклокк. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасереференцеклокк**](cbasereferenceclock.md)
</dt> </dl>

 

 




