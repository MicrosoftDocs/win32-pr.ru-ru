---
description: Метод Счедулесампле планирует пример для подготовки к просмотру.
ms.assetid: 08c218d1-6d0a-4c66-bbde-a39e5d31561c
title: Кбасерендерер. Счедулесампле, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.ScheduleSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c340e54f35b353820b128681cfbc0c5798d38849
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657859"
---
# <a name="cbaserendererschedulesample-method"></a>Кбасерендерер. Счедулесампле, метод

`ScheduleSample`Метод планирует пример для отрисовки.

## <a name="syntax"></a>Синтаксис


```C++
virtual BOOL ScheduleSample(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пмедиасампле* 
</dt> <dd>

Указатель на интерфейс [**имедиасампле**](/windows/desktop/api/Strmif/nn-strmif-imediasample) образца.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если образец был запланирован, или **значение false** , если образец был удален.

## <a name="remarks"></a>Комментарии

Этот метод сначала определяет, должен ли образец быть визуализирован немедленно, визуализирован в будущем или удален. (Для этого вызывается метод [**кбасерендерер:: жетсамплетимес**](cbaserenderer-getsampletimes.md) .) Если образец должен быть визуализирован немедленно, метод сигнализирует о событии [**кбасерендерер:: m \_ рендеревент**](cbaserenderer-m-renderevent.md) . Если образец должен быть визуализирован в будущем, метод вызывает метод [**иреференцеклокк:: адвисетиме**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime) для планирования.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ренбасе. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасерендерер**](cbaserenderer.md)
</dt> </dl>

 

 




