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
ms.openlocfilehash: 382b74f6314beb586b1e51c02a257cad8904c188
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675686"
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Пстреам. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кперсистстреам**](cpersiststream.md)
</dt> </dl>

 

 




