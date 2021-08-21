---
description: 'Метод получения \_ скорости получает скорость воспроизведения. Этот метод реализует метод Имедиапоситион:: Get \_ .'
ms.assetid: 216cbcef-4874-4565-abb0-8c8bf67fe23c
title: Метод CPosPassThru.get_Rate (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.get_Rate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4fa8014d23bc488b4f0b8b0cc9b872dfdf4a56cced396cc22eefab5912df1706
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073539"
---
# <a name="cpospassthruget_rate-method"></a>Кпоспасссру. получение \_ метода Rate

`get_Rate`Метод получает скорость воспроизведения. Этот метод реализует метод [**имедиапоситион:: Get \_**](/windows/desktop/api/Control/nf-control-imediaposition-get_rate) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_Rate(
   double *pdRate
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пдрате* 
</dt> <dd>

Указатель на переменную, которая получает скорость воспроизведения.

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

 

 




