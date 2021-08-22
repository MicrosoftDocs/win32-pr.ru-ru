---
description: Метод WebMethod извлекает идентификатор класса (CLSID) объекта. Этот метод реализует метод IPersist::/ClassID.
ms.assetid: 3d2cc6a3-67d1-4dd9-916b-7c350ce6a542
title: Метод Ксистемклокк. ClassID (Сисклокк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSystemClock.GetClassID
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2afb141c3a79255504eb13dadb39cc0fb5094c19e0979db04c251f1e2fe75133
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119317194"
---
# <a name="csystemclockgetclassid-method"></a>Ксистемклокк. ClassID, метод

`GetClassID`Метод получает идентификатор класса (CLSID) объекта. Этот метод реализует метод **IPersist::/ClassID** .

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

Указатель на переменную, которая получает значение CLSID \_ системклокк.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение S \_ (ОК) или \_ указатель E.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Класс Ксистемклокк<br/>                                                                                                                                                              |
| Header<br/>  | <dl> <dt>сисклокк. h (включает Потоки. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



 

 




