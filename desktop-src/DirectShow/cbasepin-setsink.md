---
description: 'Метод Сетсинк задает внешний диспетчер качества. Этот метод реализует метод Икуалитиконтрол:: Сетсинк.'
ms.assetid: 714e6839-954e-4231-824d-72a45f270f59
title: Кбасепин. Сетсинк, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.SetSink
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6e94dc561e378ab526eee04f82e0f54a90889ee4396996d96d01f6c8da8c34d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108634"
---
# <a name="cbasepinsetsink-method"></a>Кбасепин. Сетсинк, метод

`SetSink`Метод задает внешний диспетчер качества. Этот метод реализует метод [**икуалитиконтрол:: сетсинк**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetSink(
   IQualityControl *piqc
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пикк* 
</dt> <dd>

Указатель на интерфейс [**икуалитиконтрол**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) диспетчера качества.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение S \_ ОК.

## <a name="remarks"></a>Remarks

Вызовите этот метод, чтобы перенаправить сообщения контроля качества внешнему диспетчеру качества. Дополнительные сведения см. в разделе [Управление качеством](quality-control-management.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>амфилтер. h (включает Потоки. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбасепин**](cbasepin.md)
</dt> </dl>

 

 




