---
description: 'Метод Get \_ CurrentPosition извлекает текущую координату относительно общей продолжительности потока. Этот метод реализует метод Имедиапоситион:: Get \_ CurrentPosition.'
ms.assetid: 6e68af98-440d-4ecc-b1aa-d5e241de4999
title: Метод CPosPassThru.get_CurrentPosition (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.get_CurrentPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: db49717284f597249603b3c18340855793ebd342632aeb2091861f9742963a02
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084244"
---
# <a name="cpospassthruget_currentposition-method"></a>Кпоспасссру. Get \_ CurrentPosition, метод

`get_CurrentPosition`Метод получает текущую координату относительно общей продолжительности потока. Этот метод реализует метод [**имедиапоситион:: Get \_ CurrentPosition**](/windows/desktop/api/Control/nf-control-imediaposition-get_currentposition) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_CurrentPosition(
   REFTIME *pllTime
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пллтиме* 
</dt> <dd>

Указатель на переменную, которая получает текущую точку в секундах.

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

 

 




