---
description: Метод AddTail добавляет еще один список в конец этого списка.
ms.assetid: 996523cd-d9ba-406a-afdf-494d328dc9dd
title: Кбаселист. AddTail, метод (Вкслист. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddTail
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5663a69d803def2b37f9a1ba677966a5b26a8bfc6f7b6eb1eb98eef85bcd961d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118659157"
---
# <a name="cbaselistaddtail-method"></a>Кбаселист. AddTail, метод

`AddTail`Метод добавляет еще один список в конец этого списка.

## <a name="syntax"></a>Синтаксис


```C++
BOOL AddTail(
   CBaseList *pList
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pList* 
</dt> <dd>

Указатель на добавляемый список.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если успешно, или **false** в противном случае.

## <a name="remarks"></a>Remarks

В случае сбоя метода некоторые элементы могут быть добавлены в список.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>вкслист. h (включает Потоки. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбаселист**](cbaselist.md)
</dt> </dl>

 

 




