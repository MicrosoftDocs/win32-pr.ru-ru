---
description: Метод Get \_ фрамесдроппединрендерер Извлекает число кадров, отброшенных модулем подготовки отчетов.
ms.assetid: d890f285-b3bb-426c-80f6-e273cf0cccbb
title: Метод CBaseVideoRenderer.get_FramesDroppedInRenderer (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.get_FramesDroppedInRenderer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 21bd2e9c2f9edb50ca3800c95b59ba19fd91674d5ef343cf35842380ce617978
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016762"
---
# <a name="cbasevideorendererget_framesdroppedinrenderer-method"></a>Кбасевидеорендерер. Get \_ фрамесдроппединрендерер, метод

`get_FramesDroppedInRenderer`Метод получает число кадров, отброшенных модулем подготовки отчетов.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_FramesDroppedInRenderer(
   int *pcFramesDropped
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пкфрамесдроппед* 
</dt> <dd>

Указатель на число отброшенных кадров.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** .

## <a name="remarks"></a>Remarks

Эта функция члена реализует метод [**икуалпроп:: Get \_ фрамесдроппединрендерер**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_framesdroppedinrenderer) . Таким способом страница свойств получает данные от планировщика. Кадры также можно удалить из восходящего потока, не просматривая при этом модуль подготовки отчетов.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>ренбасе. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбасевидеорендерер**](cbasevideorenderer.md)
</dt> </dl>

 

 




