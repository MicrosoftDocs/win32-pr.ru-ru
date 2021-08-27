---
description: 'Метод Кпоспасссру. дальнего действия. метод доступа к доступности извлекает диапазон времени, в течение которого поиск является эффективным. Этот метод реализует метод Имедиасикинг:: onavailable.'
ms.assetid: 5f4af41a-eb7b-4caa-97e0-aaed78467723
title: Метод Кпоспасссру. Available (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetAvailable
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e1db45b20264f192b2ade7d8863f9da86d5fc02159567611eff86e9cdfff1b10
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084254"
---
# <a name="cpospassthrugetavailable-method"></a>Кпоспасссру. доступный метод

`GetAvailable`Метод извлекает диапазон времени, в котором поиск является эффективным. Этот метод реализует метод [**имедиасикинг:: onavailable**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getavailable) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetAvailable(
   LONGLONG *pEarliest,
   LONGLONG *pLatest
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пеарлиест* 
</dt> <dd>

Указатель на переменную, которая получает самое раннее время для эффективного поиска.

</dd> <dt>

*Пластина* 
</dt> <dd>

Указатель на переменную, которая получает Последнее время для эффективного поиска.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** из подключенного ПИН-кода.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>ктлутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кпоспасссру**](cpospassthru.md)
</dt> </dl>

 

 




