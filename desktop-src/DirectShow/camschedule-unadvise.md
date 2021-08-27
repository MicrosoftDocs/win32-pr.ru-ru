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
ms.openlocfilehash: 6bc9b1c964d698e1c1323846c7a25a29f60c0cd71009fbb60f1a09a6757b50b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057604"
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
| <dl> <dt>**\_ОК**</dt> </dl>    | Success<br/>   |



 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>дссчедуле. h (включает Потоки. h)</dt> </dl>                                                                                |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Камсчедуле**](camschedule.md)
</dt> </dl>

 

 




