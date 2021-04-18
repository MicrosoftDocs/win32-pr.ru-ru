---
description: Метод Get \_ авгсинкоффсет извлекает среднее значение времени в миллисекундах между временем выполнения каждого кадра и моментом его отрисовки для всех кадров с момента запуска потоковой передачи.
ms.assetid: b41741e9-e0b5-4c49-93ef-cb8c0cf2ddeb
title: Метод CBaseVideoRenderer.get_AvgSyncOffset (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.get_AvgSyncOffset
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 35c682b8f4bb60ec629db5489e879d1ca7968b77
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675215"
---
# <a name="cbasevideorendererget_avgsyncoffset-method"></a>Кбасевидеорендерер. Get \_ авгсинкоффсет, метод

`get_AvgSyncOffset`Метод получает среднее значение времени в миллисекундах между временем выполнения каждого кадра и временем его отрисовки для всех кадров с момента запуска потоковой передачи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_AvgSyncOffset(
   int *piAvg
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пиавг* 
</dt> <dd>

Указатель на среднее значение времени, описанное ранее.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** .

## <a name="remarks"></a>Комментарии

Эта функция члена реализует метод [**икуалпроп:: Get \_ авгсинкоффсет**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_avgsyncoffset) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ренбасе. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасевидеорендерер**](cbasevideorenderer.md)
</dt> </dl>

 

 




