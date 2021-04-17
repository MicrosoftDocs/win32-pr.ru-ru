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
ms.openlocfilehash: 62827f1cda9423f9a5128c35289803027bfa78a6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675001"
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
| Header<br/>  | <dl> <dt>Ренбасе. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасевидеорендерер**](cbasevideorenderer.md)
</dt> </dl>

 

 




