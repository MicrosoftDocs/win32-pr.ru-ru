---
description: Изменяет флаг «грязных» для текущего потока.
ms.assetid: 65fa7fbe-4fa7-45a3-91a4-4a3547b035b9
title: Кперсистстреам. Сетдирти, метод (Пстреам. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.SetDirty
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 31a00de873f33cedd1451ebebd0ec21f1dfaa83690923712d867ec4a8d34d502
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119909304"
---
# <a name="cpersiststreamsetdirty-method"></a>Кперсистстреам. Сетдирти, метод

Изменяет флаг «грязных» для текущего потока.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetDirty(
   BOOL fDirty
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*фдирти* 
</dt> <dd>

Новый "грязный" флаг для этого потока. **Значение true** означает, что данные не были сохранены.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>пстреам. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кперсистстреам**](cpersiststream.md)
</dt> </dl>

 

 




