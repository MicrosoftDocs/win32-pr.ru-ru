---
description: Метод Комплетестатечанже определяет, завершен ли переход в приостановленное состояние.
ms.assetid: 505a0b31-deaa-46be-91e6-f9bc8e47dd3a
title: Кбасерендерер. Комплетестатечанже, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.CompleteStateChange
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 260cd5692e10fb6e6adaa3ed715944eb773064afaea68f5e0909fa08f45adfb9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119872364"
---
# <a name="cbaserenderercompletestatechange-method"></a>Кбасерендерер. Комплетестатечанже, метод

`CompleteStateChange`Метод определяет, завершен ли переход в приостановленное состояние.

## <a name="syntax"></a>Синтаксис


```C++
virtual HRESULT CompleteStateChange(
   FILTER_STATE OldState
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*олдстате* 
</dt> <dd>

Состояние до перехода.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение \_ ОК, если переход завершен. В противном случае возвращает \_ значение S false.

## <a name="remarks"></a>Remarks

Метод [**кбасерендерер::P Аусе**](cbaserenderer-pause.md) вызывает этот метод для обновления состояния перехода состояния. Как правило, переход на приостановку не завершается до тех пор, пока фильтр не получит пример. Однако в некоторых ситуациях переход завершается немедленно: например, если фильтр не подключен или достигнут конец потока. Этот метод проверяет различные критерии, а затем вызывает метод [**кбасерендерер:: Ready**](cbaserenderer-ready.md) или метод [**Кбасерендерер:: NotReady**](cbaserenderer-notready.md) для обновления состояния перехода.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>ренбасе. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбасерендерер**](cbaserenderer.md)
</dt> </dl>

 

 




