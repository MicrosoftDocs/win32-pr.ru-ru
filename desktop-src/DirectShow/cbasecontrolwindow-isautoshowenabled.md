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
ms.openlocfilehash: 81f5190d3b0634c763703a3e13aa711f097641285f49c469dab6bad6ce0d9055
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118660233"
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

## <a name="remarks"></a>Remarks

Если элемент **m \_ баутошов** имеет значение 1 в скрытом окне видео, окно становится видимым при приостановке или запуске фильтра. Если для этого элемента задано значение 0, окно будет отображаться только при использовании функции-члена [**кбасеконтролвиндов::p UT \_ Visible**](cbasecontrolwindow-put-visible.md) или [**кбасеконтролвиндов::p UT \_ WindowState**](cbasecontrolwindow-put-windowstate.md) с соответствующими параметрами.

Эта функция члена получает параметр **\_ баутошов элемента m** и имеет тот же результат, что и использование метода [**ивидеовиндов:: \_ Get**](/windows/desktop/api/Control/nf-control-ivideowindow-get_autoshow) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>ктлутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасеконтролвиндов**](cbasecontrolwindow.md)
</dt> </dl>

 

 




