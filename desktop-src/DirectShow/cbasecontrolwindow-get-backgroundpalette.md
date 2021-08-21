---
description: Метод Get \_ баккграундпалетте извлекает реализованную палитру в фоновом флаге.
ms.assetid: cc649dbd-d049-4993-b187-4e297bef5152
title: Метод CBaseControlWindow.get_BackgroundPalette (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_BackgroundPalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 63ea3fa8ecbc6e644ccc5f4b1fac7a2fcd9c18270474f45dc08faa164f76cbec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118660779"
---
# <a name="cbasecontrolwindowget_backgroundpalette-method"></a>Кбасеконтролвиндов. Get \_ баккграундпалетте, метод

`get_BackgroundPalette`Метод извлекает реализованную палитру в фоновом флаге.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_BackgroundPalette(
   long *pBackgroundPalette
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пбаккграундпалетте* 
</dt> <dd>

Указатель на логический флаг автоматизации (0 — Off, 1 — включено).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** .

## <a name="remarks"></a>Remarks

Эта функция члена реализует метод [**ивидеовиндов:: Get \_ баккграундпалетте**](/windows/desktop/api/Control/nf-control-ivideowindow-get_backgroundpalette) . Если видео будет воспроизводиться в другом приложении или документе, может потребоваться использовать собственную палитру приложения. Он может задать, чтобы видео использовало текущую палитру переднего плана, а не собственную, установив для этого флага значение 1. Если задано значение 0, окно будет установлено и использовать собственную предпочтительную палитру. Обратите внимание, что запрос на использование другой палитры приведет к значительному снижению производительности.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>ктлутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасеконтролвиндов**](cbasecontrolwindow.md)
</dt> </dl>

 

 




