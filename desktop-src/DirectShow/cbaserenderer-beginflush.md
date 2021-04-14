---
description: Метод Бегинфлуш начинает операцию очистки.
ms.assetid: dc652394-c24e-4cea-ac28-30a1e6de205f
title: Кбасерендерер. Бегинфлуш, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e218e3b2d9c0cef8ce0fe052ad1b3c4b6f786858
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668752"
---
# <a name="cbaserendererbeginflush-method"></a>Кбасерендерер. Бегинфлуш, метод

`BeginFlush`Метод начинает операцию записи на диск.

## <a name="syntax"></a>Синтаксис


```C++
virtual HRESULT BeginFlush();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение S \_ ОК.

## <a name="remarks"></a>Комментарии

Входной ПИН-код фильтра вызывает этот метод при получении вызова метода [**Ипин:: бегинфлуш**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) . Фильтр освобождает поток потоковой передачи и освобождает все примеры, которые он удерживает для подготовки к просмотру.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ренбасе. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасерендерер**](cbaserenderer.md)
</dt> </dl>

 

 




