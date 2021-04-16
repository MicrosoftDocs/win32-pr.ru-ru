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
ms.openlocfilehash: 4237e342f8f49059cab017b17a1f116ca6e2da67
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657204"
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

## <a name="remarks"></a>Комментарии

Вызовите этот метод, чтобы перенаправить сообщения контроля качества внешнему диспетчеру качества. Дополнительные сведения см. в разделе [Управление качеством](quality-control-management.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Амфилтер. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасепин**](cbasepin.md)
</dt> </dl>

 

 




