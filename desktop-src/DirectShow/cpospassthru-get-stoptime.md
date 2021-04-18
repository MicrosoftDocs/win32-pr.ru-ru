---
description: 'Метод Get \_ StopTime извлекает время, когда воспроизведение будет прервано относительно длительности потока. Этот метод реализует метод Имедиапоситион:: Get \_ StopTime.'
ms.assetid: 0ca3f047-ac43-419e-a1ed-b406f89f7af7
title: Метод CPosPassThru.get_StopTime (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.get_StopTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 227b054a9737c06e56f7311acc7e0093766608b7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657230"
---
# <a name="cpospassthruget_stoptime-method"></a>Кпоспасссру. Get \_ StopTime, метод

`get_StopTime`Метод получает время, когда воспроизведение будет прервано относительно длительности потока. Этот метод реализует метод [**имедиапоситион:: Get \_ StopTime**](/windows/desktop/api/Control/nf-control-imediaposition-get_stoptime) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_StopTime(
   REFTIME *pllTime
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пллтиме* 
</dt> <dd>

Указатель на переменную, которая получает время окончания (в секундах).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** из подключенного ПИН-кода.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ктлутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кпоспасссру**](cpospassthru.md)
</dt> </dl>

 

 




