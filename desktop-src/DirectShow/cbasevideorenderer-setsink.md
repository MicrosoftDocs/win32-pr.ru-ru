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
ms.openlocfilehash: 5b5fef3eb6bd1b959c6c7246e4aeebf5b42a01ddcecd211f3e1d7860102a6381
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697904"
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

## <a name="remarks"></a>Remarks

Эта функция члена реализует метод [**икуалитиконтрол:: сетсинк**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink) для модуля подготовки видео.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>ренбасе. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбасевидеорендерер**](cbasevideorenderer.md)
</dt> </dl>

 

 




