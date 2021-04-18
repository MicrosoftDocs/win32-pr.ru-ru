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
ms.openlocfilehash: a4511a9867f61596572c959a3d763eb56d862311
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668997"
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

## <a name="remarks"></a>Комментарии

Этот метод удаляет узел из списка, но не удаляет элемент, содержащийся в этом узле.

Если *POS* имеет **значение NULL**, метод возвращает **значение NULL**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Вкслист. h (включение Streams. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбаселист**](cbaselist.md)
</dt> </dl>

 

 




