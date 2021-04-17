---
description: Метод Сетсинк задает объект Икуалитиконтрол, который будет принимать сообщения о контроле качества.
ms.assetid: f5789781-1871-4fea-9d1f-bd1a21b70439
title: Кбасевидеорендерер. Сетсинк, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.SetSink
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9658ab4a1099e7baaef0a3e1a0ae3c0d495e89e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675000"
---
# <a name="cbasevideorenderersetsink-method"></a>Кбасевидеорендерер. Сетсинк, метод

`SetSink`Метод задает объект [**икуалитиконтрол**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) , который будет принимать сообщения качества.

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

Указатель на объект [**икуалитиконтрол**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) , в который должны отправляться уведомления.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** .

## <a name="remarks"></a>Комментарии

Эта функция члена реализует метод [**икуалитиконтрол:: сетсинк**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink) для модуля подготовки видео.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ренбасе. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасевидеорендерер**](cbasevideorenderer.md)
</dt> </dl>

 

 




