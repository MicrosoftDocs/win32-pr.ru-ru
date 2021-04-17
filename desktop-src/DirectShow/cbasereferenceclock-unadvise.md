---
description: 'Метод unadvise Удаляет ожидающий запрос Advise. Этот метод реализует метод Иреференцеклокк:: unadvise.'
ms.assetid: b137234a-e260-42f9-b583-9e6a5fd7bca4
title: Метод Кбасереференцеклокк. unadvise (Рефклокк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.Unadvise
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 14daf1d34c8a6a923ec7e181ac69f9ecbae0160a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657907"
---
# <a name="cbasereferenceclockunadvise-method"></a>Кбасереференцеклокк. unadvise, метод

`Unadvise`Метод удаляет ожидающий запрос рекомендаций. Этот метод реализует метод [**иреференцеклокк:: unadvise**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-unadvise) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Unadvise(
   DWORD_PTR dwAdviseToken
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*двадвисетокен* 
</dt> <dd>

Идентификатор удаляемого запроса. Используйте значение, возвращаемое методами [**кбасереференцеклокк:: адвисетиме**](cbasereferenceclock-advisetime.md) или [**Кбасереференцеклокк:: адвисепериодик**](cbasereferenceclock-adviseperiodic.md) в параметре *пдвадвисетокен* .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает одно из значений **HRESULT** , приведенных в следующей таблице.



| Код возврата                                                                             | Описание           |
|-----------------------------------------------------------------------------------------|-----------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | Не найдено.<br/> |
| <dl> <dt>**\_ОК**</dt> </dl>    | Успешно.<br/>   |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Рефклокк. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасереференцеклокк**](cbasereferenceclock.md)
</dt> </dl>

 

 




