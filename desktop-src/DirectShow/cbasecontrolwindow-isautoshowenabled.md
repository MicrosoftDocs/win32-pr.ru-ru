---
description: Метод Исаутошовенаблед извлекает сведения о том, отображается ли видеоокно автоматически при приостановке или запуске фильтра подготовки отчетов.
ms.assetid: 769e3023-a515-4b80-a979-2e4fa9612e65
title: Кбасеконтролвиндов. Исаутошовенаблед, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.IsAutoShowEnabled
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2c4b4a894593cb3be26a1034098cd2a0cdacf926
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657459"
---
# <a name="cbasecontrolwindowisautoshowenabled-method"></a>Кбасеконтролвиндов. Исаутошовенаблед, метод

`IsAutoShowEnabled`Метод получает сведения о том, отображается ли окно видео автоматически при приостановке или запуске фильтра подготовки отчетов.

## <a name="syntax"></a>Синтаксис


```C++
BOOL IsAutoShowEnabled();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если элемент **m \_ баутошов** имеет значение 1 или **false** , если он имеет значение 0.

## <a name="remarks"></a>Комментарии

Если элемент **m \_ баутошов** имеет значение 1 в скрытом окне видео, окно становится видимым при приостановке или запуске фильтра. Если для этого элемента задано значение 0, окно будет отображаться только при использовании функции-члена [**кбасеконтролвиндов::p UT \_ Visible**](cbasecontrolwindow-put-visible.md) или [**кбасеконтролвиндов::p UT \_ WindowState**](cbasecontrolwindow-put-windowstate.md) с соответствующими параметрами.

Эта функция члена получает параметр **\_ баутошов элемента m** и имеет тот же результат, что и использование метода [**ивидеовиндов:: \_ Get**](/windows/desktop/api/Control/nf-control-ivideowindow-get_autoshow) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ктлутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасеконтролвиндов**](cbasecontrolwindow.md)
</dt> </dl>

 

 




