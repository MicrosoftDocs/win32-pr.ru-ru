---
description: Указывает, изменился ли объект со времени последнего сохранения в текущем потоке.
ms.assetid: 69840be6-062e-4505-8381-ea04e822c660
title: Метод Кперсистстреам. IsDirty (Пстреам. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.IsDirty
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5e28285bd5660d6ba81fe77718cd9d38f325c51184a7bbd035cf3d7cb2ce6aa8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108444"
---
# <a name="cpersiststreamisdirty-method"></a>Кперсистстреам. IsDirty, метод

Указывает, изменился ли объект со времени последнего сохранения в текущем потоке.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IsDirty();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение \_ ОК, если для фильтра требуется сохранение, и \_ false, если нет необходимости сохранять.

## <a name="remarks"></a>Remarks

Эта функция члена реализует метод **IPersistStream:: IsDirty** .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>пстреам. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кперсистстреам**](cpersiststream.md)
</dt> </dl>

 

 




