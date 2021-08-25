---
description: 'Кпоспасссру. Сетрате, метод Сетрате задает скорость воспроизведения. Этот метод реализует метод Имедиасикинг:: Сетрате.'
ms.assetid: 1b38eb5d-38fd-408b-9f20-4f8d18158f92
title: Кпоспасссру. Сетрате, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.SetRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8c411f2c342bd54f89ac85ad4275a05e9d7854908c1d8ba88b1181f34e56f57d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119909074"
---
# <a name="cpospassthrusetrate-method"></a>Кпоспасссру. Сетрате, метод

`SetRate`Метод задает скорость воспроизведения. Этот метод реализует метод [**имедиасикинг:: сетрате**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetRate(
   double dRate
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*драте* 
</dt> <dd>

Скорость воспроизведения. Не должно быть нулем.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает E \_ INVALIDARG, если *драте* равен нулю. В противном случае возвращает значение **HRESULT** из подключенного ПИН-кода.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>ктлутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кпоспасссру**](cpospassthru.md)
</dt> </dl>

 

 




