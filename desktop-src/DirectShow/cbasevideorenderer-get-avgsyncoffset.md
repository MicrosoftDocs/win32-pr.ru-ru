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
ms.openlocfilehash: 4550445d0a2596edcb9d76b88b371eb060257b29730a386c4f9444dae2624b55
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119526504"
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

## <a name="remarks"></a>Remarks

Эта функция члена реализует метод [**икуалпроп:: Get \_ авгсинкоффсет**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_avgsyncoffset) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>ренбасе. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбасевидеорендерер**](cbasevideorenderer.md)
</dt> </dl>

 

 




