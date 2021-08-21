---
description: Метод Комплетеконнект уведомляет окно о том, что закреплен входной ПИН-код модуля подготовки отчетов подключен.
ms.assetid: 82347ded-eb37-4360-9333-7c837d532115
title: Кбасевиндов. Комплетеконнект, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5e04e0adf1d11a4878d860dd5c8a1eea9395095c71d8b5c86d6023a24ccdb28c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016712"
---
# <a name="cbasewindowcompleteconnect-method"></a>Кбасевиндов. Комплетеконнект, метод

`CompleteConnect`Метод уведомляет окно о том, что закреплен входной ПИН-код модуля подготовки отчетов подключен.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT CompleteConnect();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение S \_ ОК.

## <a name="remarks"></a>Remarks

Этот метод сбрасывает флаг активации окна ([**кбасевиндов:: m \_ бактиватед**](cbasewindow-m-bactivated.md)) в **значение false**. Когда модуль подготовки видео завершает соединение с закреплением, он может вызвать метод [**кбасевиндов:: активатевиндов**](cbasewindow-activatewindow.md) , чтобы задать размер и расположение окна. Чтобы принудительно выполнить **активатевиндов** для повторного вычисления этих атрибутов, сначала вызовите `CompleteConnect` метод.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>винутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбасевиндов**](cbasewindow.md)
</dt> </dl>

 

 




