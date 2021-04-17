---
description: 'Метод Get \_ прероллтиме извлекает объем данных, которые будут помещены в очередь перед начальной позицией. Этот метод реализует метод Имедиапоситион:: Get \_ прероллтиме.'
ms.assetid: 37c12798-eb0d-4859-8b2e-52d6ae147863
title: Метод CPosPassThru.get_PrerollTime (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.get_PrerollTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 55cb2cc37a18c9ea00b4eb7115590f472b8d467e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657273"
---
# <a name="cpospassthruget_prerolltime-method"></a>Кпоспасссру. Get \_ прероллтиме, метод

`get_PrerollTime`Метод получает объем данных, которые будут помещены в очередь перед начальной позицией. Этот метод реализует метод [**имедиапоситион:: Get \_ прероллтиме**](/windows/desktop/api/Control/nf-control-imediaposition-get_prerolltime) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_PrerollTime(
   REFTIME *pllTime
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пллтиме* 
</dt> <dd>

Указатель на переменную, которая получает время в секундах.

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

 

 




