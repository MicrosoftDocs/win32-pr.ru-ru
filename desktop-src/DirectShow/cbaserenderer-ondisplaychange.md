---
description: Метод Ондисплайчанже отправляет событие EC о \_ \_ смене дисплея в Диспетчер графа фильтров.
ms.assetid: e4cdcdf2-7fc2-4893-9897-97bcf2c12610
title: Кбасерендерер. Ондисплайчанже, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnDisplayChange
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1e99a8626d523e8b14b013acc9d2ead462f48df3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105658056"
---
# <a name="cbaserendererondisplaychange-method"></a>Кбасерендерер. Ондисплайчанже, метод

`OnDisplayChange`Метод отправляет событие [**EC о \_ \_ смене дисплея**](ec-display-changed.md) в Диспетчер графа фильтров.

## <a name="syntax"></a>Синтаксис


```C++
BOOL OnDisplayChange();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если событие было опубликовано, или **значение false** в противном случае.

## <a name="remarks"></a>Комментарии

Модули подготовки видео должны вызывать этот метод в ответ на \_ сообщения ДИСПЛАЙЧАНЖЕ WM. Если входной ПИН-код подключен, метод отправляет \_ \_ событие EC "изменение дисплея" в Диспетчер графа фильтров.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ренбасе. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасерендерер**](cbaserenderer.md)
</dt> </dl>

 

 




