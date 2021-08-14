---
description: Метод Ремоветаили удаляет последний элемент в списке.
ms.assetid: 3e9f88a5-a681-4494-8977-d9a6ec62a849
title: Кбаселист. Ремоветаили, метод (Вкслист. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.RemoveTailI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c10f7acbb73fe2024308117c8548e789696ee65914aa698dc0478a900846e77d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119341634"
---
# <a name="cbaselistremovetaili-method"></a>Кбаселист. Ремоветаили, метод

`RemoveTailI`Метод удаляет последний элемент в списке.

## <a name="syntax"></a>Синтаксис


```C++
void* RemoveTailI();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает указатель на элемент или **значение NULL** , если список пуст.

## <a name="remarks"></a>Remarks

Этот метод удаляет узел списка, но не элемент, содержащийся в узле.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>вкслист. h (включает Потоки. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбаселист**](cbaselist.md)
</dt> </dl>

 

 




