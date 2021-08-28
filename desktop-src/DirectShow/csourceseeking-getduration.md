---
description: Ксаурцесикинг. Duration-метод — метод методаической длительности извлекает длительность потока. Этот метод реализует метод Имедиасикинг::/Duration.
ms.assetid: 074eb2d0-a7a3-4bc1-82e8-2f42c6d43dac
title: Ксаурцесикинг. метод Duration (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetDuration
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d8520b39ca62d70152b544e8ae2f146a237c388d93e4786bb13371ad223fa73f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084044"
---
# <a name="csourceseekinggetduration-method"></a>Ксаурцесикинг. метод Duration

`GetDuration`Метод получает длительность потока. Этот метод реализует метод [**имедиасикинг::/Duration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetDuration(
   LONGLONG *pDuration
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пдуратион* 
</dt> <dd>

Указатель на переменную, которая получает длительность в единицах текущего формата времени.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает одно из значений **HRESULT** , перечисленных в следующей таблице.



| Код возврата                                                                               | Описание                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>      | Success<br/>                |
| <dl> <dt>**\_указатель E**</dt> </dl> | Значение указателя **null**<br/> |



 

## <a name="remarks"></a>Remarks

Длительность задается переменной-членом [**ксаурцесикинг:: m \_ ртдуратион**](csourceseeking-m-rtduration.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>ктлутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Ксаурцесикинг**](csourceseeking.md)
</dt> </dl>

 

 




