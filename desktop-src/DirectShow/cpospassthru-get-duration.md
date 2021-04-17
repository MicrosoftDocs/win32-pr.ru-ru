---
description: 'Метод получения \_ длительности извлекает длительность потока. Этот метод реализует метод Имедиапоситион:: Get \_ Duration.'
ms.assetid: 326a8cd3-d05f-49d0-941d-08f9778e9a06
title: Метод CPosPassThru.get_Duration (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.get_Duration
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: df518a0691a4fe1a6c0443ba93a83e65577efe21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679845"
---
# <a name="cpospassthruget_duration-method"></a>Кпоспасссру. Get \_ Duration, метод

`get_Duration`Метод получает длительность потока. Этот метод реализует метод [**имедиапоситион:: Get \_ Duration**](/windows/desktop/api/Control/nf-control-imediaposition-get_duration) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_Duration(
   REFTIME *plength
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пленгс* 
</dt> <dd>

Указатель на переменную, которая получает общую длину потока в секундах.

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

 

 




