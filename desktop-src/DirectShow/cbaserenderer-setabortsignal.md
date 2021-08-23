---
description: Метод Сетабортсигнал задает флаг, который указывает, следует ли прерывать отрисовку и отклонять дальнейшие выборки.
ms.assetid: 2dbf3b4d-e285-4d17-a77c-01a16c09d148
title: Кбасерендерер. Сетабортсигнал, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SetAbortSignal
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 819f279d20192ff82d9021e03780713f714682abf47aaf854b4568312572e8d8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119526541"
---
# <a name="cbaserenderersetabortsignal-method"></a>Кбасерендерер. Сетабортсигнал, метод

`SetAbortSignal`Метод задает флаг, указывающий, следует ли прерывать отрисовку и отклонять дальнейшие выборки.

## <a name="syntax"></a>Синтаксис


```C++
void SetAbortSignal(
   BOOL bAbort
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*баборт* 
</dt> <dd>

Логическое значение, указывающее, следует ли прерывать подготовку к просмотру. Если **значение равно true**, то фильтр не будет отображать больше выборок.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

Этот метод задает флаг [**кбасерендерер:: m \_ баборт**](cbaserenderer-m-babort.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>ренбасе. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбасерендерер**](cbaserenderer.md)
</dt> </dl>

 

 




