---
description: Метод Счедулесампле переопределяет базовый класс, который выполняет основную работу, чтобы обеспечить Количество рисуемых и удаленных выборок (которые используются реализацией Икуалпроп).
ms.assetid: 66e4e318-a7ff-4ba0-9ac5-24ba39ac86f1
title: Кбасевидеорендерер. Счедулесампле, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.ScheduleSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f68701fd4c4d682d6bcd89c3b82d6bf054188a9bbdcb47c9019b563fad4a877f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118658238"
---
# <a name="cbasevideorendererschedulesample-method"></a>Кбасевидеорендерер. Счедулесампле, метод

`ScheduleSample`Метод переопределяет базовый класс, который выполняет основную работу, чтобы обеспечить количество выводимых и удаленных выборок (которые используются реализацией [**икуалпроп**](/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop) ).

## <a name="syntax"></a>Синтаксис


```C++
BOOL ScheduleSample(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пмедиасампле* 
</dt> <dd>

Указатель на пример носителя.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если выборка запланирована. в противном случае возвращает **значение false**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>ренбасе. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасевидеорендерер**](cbasevideorenderer.md)
</dt> </dl>

 

 




