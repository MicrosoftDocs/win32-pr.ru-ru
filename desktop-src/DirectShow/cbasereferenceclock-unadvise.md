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
ms.openlocfilehash: 26e6519d1a94091c0afc0bafffe40fdaac47364d25f54e068ae503f32abccbd3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119652454"
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



 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>рефклокк. h (включает Потоки. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбасереференцеклокк**](cbasereferenceclock.md)
</dt> </dl>

 

 




