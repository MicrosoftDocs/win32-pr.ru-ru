---
description: Возвращает идентификатор класса для этого фильтра.
ms.assetid: f0559437-5d0d-4522-a3dc-947e3494b576
title: Метод Кперсистстреам. ClassID (Пстреам. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.GetClassID
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e500b91453bd7c9d76f243939a98b0779f1873ed7b5f79128e639173710e62de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915564"
---
# <a name="cpersiststreamgetclassid-method"></a>Кперсистстреам. ClassID, метод

Возвращает идентификатор класса для этого фильтра.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetClassID(
   CLSID *pClsID
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пклсид* 
</dt> <dd>

Указатель на структуру CLSID. Скопируйте идентификатор класса здесь.

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

 

 




