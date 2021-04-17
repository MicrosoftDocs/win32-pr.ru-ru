---
description: Метод Шаулддравсампленов определяет, следует ли рисовать видео без установки связи таймера с часами.
ms.assetid: 2cbefc66-0d99-4559-b210-3163cd413dbf
title: Кбасевидеорендерер. Шаулддравсампленов, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.ShouldDrawSampleNow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8c96b7453eb6009121fd6782030f7988663f5e8f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674999"
---
# <a name="cbasevideorenderershoulddrawsamplenow-method"></a>Кбасевидеорендерер. Шаулддравсампленов, метод

`ShouldDrawSampleNow`Метод определяет, следует ли рисовать видео без установки связи таймера с часами.

## <a name="syntax"></a>Синтаксис


```C++
virtual HRESULT ShouldDrawSampleNow(
   IMediaSample   *pMediaSample,
   REFERENCE_TIME *ptrStart,
   REFERENCE_TIME *ptrEnd
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пмедиасампле* 
</dt> <dd>

Указатель на интерфейс [**имедиасампле**](/windows/desktop/api/Strmif/nn-strmif-imediasample) для образца.

</dd> <dt>

*птрстарт* 
</dt> <dd>

Указатель на время начала подготовки к просмотру.

</dd> <dt>

*птренд* 
</dt> <dd>

Указатель на время, когда нужно прерывать отрисовку.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** . Возвращает \_ «ОК», означая, что рисуется один раз без ожидания, «ложь», \_ означающий прорисовку во времени *птрстарт*, или ошибка, означающая, что не Нарисуйте пример, то есть пропустите его, чтобы сэкономить время.

## <a name="remarks"></a>Комментарии

Эта функция члена переопределяет [**кбасерендерер:: шаулддравсампленов**](cbaserenderer-shoulddrawsamplenow.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ренбасе. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасевидеорендерер**](cbasevideorenderer.md)
</dt> </dl>

 

 




