---
description: 'Метод Ендфлуш завершает операцию очистки. Этот метод реализует метод Ипин:: Ендфлуш.'
ms.assetid: 5c27bf76-6886-431d-9958-5064c53909ec
title: Крендерединпутпин. Ендфлуш, метод (Амекстра. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRenderedInputPin.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3d80f6cbc31a8bc5bf797847465a218f32631c1e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668738"
---
# <a name="crenderedinputpinendflush-method"></a>Крендерединпутпин. Ендфлуш, метод

`EndFlush`Метод завершает операцию очистки. Этот метод реализует метод [**Ипин:: ендфлуш**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT EndFlush();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает \_ ОК, если успешно, или код ошибки в противном случае.

## <a name="remarks"></a>Комментарии

Этот метод очищает все ожидающие события [**EC \_ Complete**](ec-complete.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Амекстра. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Крендерединпутпин**](crenderedinputpin.md)
</dt> </dl>

 

 




