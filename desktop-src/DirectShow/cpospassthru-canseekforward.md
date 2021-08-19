---
description: 'Метод Кансикфорвард определяет, можно ли выполнить поиск в потоке вперед. Этот метод реализует метод Имедиапоситион:: Кансикфорвард.'
ms.assetid: ccb2db8d-b52e-4e3d-b49b-9689197a974a
title: Кпоспасссру. Кансикфорвард, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.CanSeekForward
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f07491a94522280357c85d773d28ea4732f2f85879b55cf5d1b5a99ec72d23f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073568"
---
# <a name="cpospassthrucanseekforward-method"></a>Кпоспасссру. Кансикфорвард, метод

`CanSeekForward`Метод определяет, можно ли выполнить поиск в потоке вперед. Этот метод реализует метод [**имедиапоситион:: кансикфорвард**](/windows/desktop/api/Control/nf-control-imediaposition-canseekforward) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT CanSeekForward(
   LONG *pCanSeekForward
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пкансикфорвард* 
</dt> <dd>

Указатель на переменную, которая получает значение ОАТРУЕ, если фильтр может искать вперед или ОАФАЛСЕ в противном случае.

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

 

 




