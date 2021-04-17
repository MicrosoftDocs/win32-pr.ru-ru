---
description: Метод Препаререндер вызывается до того, как фильтр отрисовывает пример.
ms.assetid: 0b137da9-eac0-469f-b457-719a36569c82
title: Кбасерендерер. Препаререндер, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.PrepareRender
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ee5739a839222900458ae334de6f97fb6d18876b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669402"
---
# <a name="cbaserendererpreparerender-method"></a>Кбасерендерер. Препаререндер, метод

`PrepareRender`Метод вызывается до того, как фильтр отрисовывает пример.

## <a name="syntax"></a>Синтаксис


```C++
virtual void PrepareRender();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Фильтр вызывает этот метод перед вызовом метода [**кбасерендерер:: онрецеивефирстсампле**](cbaserenderer-onreceivefirstsample.md) или метода [**Кбасерендерер:: Render**](cbaserenderer-render.md) . `PrepareRender` не выполняет никаких действий в базовом классе. Производный класс может переопределить его для выполнения любых действий, необходимых перед отрисовкой. Например, модуль подготовки видео может переопределить этот метод, чтобы реализовать его палитру.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ренбасе. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасерендерер**](cbaserenderer.md)
</dt> </dl>

 

 




