---
description: Метод WebMethod извлекает идентификатор класса. Этот метод реализует метод IPersist::/ClassID.
ms.assetid: 95038b11-b56f-4ab9-aefa-4735651c3731
title: Метод Кбасемедиафилтер. ClassID (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.GetClassID
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4dafacba684711c5c04a155d2609e0bc68450fa7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105656976"
---
# <a name="cbasemediafiltergetclassid-method"></a>Кбасемедиафилтер. ClassID, метод

`GetClassID`Метод получает идентификатор класса. Этот метод реализует метод **IPersist::/ClassID** .

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

Указатель на переменную, которая получает идентификатор класса.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение S \_ (ОК) или \_ указатель E.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Амфилтер. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасемедиафилтер**](cbasemediafilter.md)
</dt> </dl>

 

 




