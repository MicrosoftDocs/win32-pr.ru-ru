---
description: Неактивный метод вызывается при переключении состояния на Stopped.
ms.assetid: 2bad81ef-d2a4-4c20-a49b-e40e5097b430
title: Метод Кбасерендерер. Inactive (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9ac328c772b740a0d7ab05be4c6ea9f2a24f852e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665387"
---
# <a name="cbaserendererinactive-method"></a>Кбасерендерер. Inactive, метод

`Inactive`Метод вызывается при переключении состояния на Stopped.

## <a name="syntax"></a>Синтаксис


```C++
virtual HRESULT Inactive();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение S \_ ОК.

## <a name="remarks"></a>Комментарии

Входной ПИН-код вызывает этот метод из собственного метода [**крендереринпутпин:: Inactive**](crendererinputpin-inactive.md) . Фильтр вызывает метод [**кбасерендерер:: клеарпендингсампле**](cbaserenderer-clearpendingsample.md) , чтобы освободить самый последний пример.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ренбасе. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасерендерер**](cbaserenderer.md)
</dt> </dl>

 

 




