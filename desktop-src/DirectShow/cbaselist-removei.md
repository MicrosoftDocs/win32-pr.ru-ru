---
description: Метод Ремовеи удаляет элемент в указанной позиции.
ms.assetid: 6a6d54ce-7ab3-48dd-8d5d-1315816bcbb9
title: Кбаселист. Ремовеи, метод (Вкслист. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.RemoveI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ac3277f30e959e42cf2fd2d1aeeb13f81cb17515abb8434a8ae13406d244aaec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117823741"
---
# <a name="cbaselistremovei-method"></a>Кбаселист. Ремовеи, метод

`RemoveI`Метод удаляет элемент в указанной позиции.

## <a name="syntax"></a>Синтаксис


```C++
void* RemoveI(
   POSITION pos
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pos* 
</dt> <dd>

Значение позиции, указывающее удаляемый элемент.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает указатель на элемент.

## <a name="remarks"></a>Remarks

Этот метод удаляет узел из списка, но не удаляет элемент, содержащийся в этом узле.

Если *POS* имеет **значение NULL**, метод возвращает **значение NULL**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>вкслист. h (включает Потоки. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбаселист**](cbaselist.md)
</dt> </dl>

 

 




