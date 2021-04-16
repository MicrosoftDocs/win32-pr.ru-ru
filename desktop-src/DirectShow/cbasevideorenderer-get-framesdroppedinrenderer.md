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
ms.openlocfilehash: ef81678fce8d349c7c047b0453cc480d8673f8f8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657102"
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

## <a name="remarks"></a>Комментарии

Эта функция члена реализует метод [**икуалпроп:: Get \_ фрамесдроппединрендерер**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_framesdroppedinrenderer) . Таким способом страница свойств получает данные от планировщика. Кадры также можно удалить из восходящего потока, не просматривая при этом модуль подготовки отчетов.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ренбасе. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасевидеорендерер**](cbasevideorenderer.md)
</dt> </dl>

 

 




