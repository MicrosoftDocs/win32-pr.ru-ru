---
description: Метод unadvise удаляет запрос Advise.
ms.assetid: b3dfda82-577e-4499-a114-1c8721e4af9e
title: Метод Камсчедуле. unadvise (Дссчедуле. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMSchedule.Unadvise
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 25dd70a46fcc2b6572500b3164b64fd0facbcbe0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657526"
---
# <a name="camscheduleunadvise-method"></a>Камсчедуле. unadvise, метод

`Unadvise`Метод удаляет запрос Advise.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Unadvise(
   DWORD_PTR dwAdviseCookie
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*двадвисекукие* 
</dt> <dd>

Идентификатор запроса advise, возвращаемый методом [**камсчедуле:: аддадвисепаккет**](camschedule-addadvisepacket.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает одно из значений **HRESULT** , приведенных в следующей таблице.



| Код возврата                                                                             | Описание          |
|-----------------------------------------------------------------------------------------|----------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | Не найдено<br/> |
| <dl> <dt>**\_ОК**</dt> </dl>    | Успешно<br/>   |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Дссчедуле. h (включение Streams. h)</dt> </dl>                                                                                |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Камсчедуле**](camschedule.md)
</dt> </dl>

 

 




