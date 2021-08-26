---
description: 'Метод Кансикбакквард определяет, возможен ли обратный поиск в потоке. Этот метод реализует метод Имедиапоситион:: Кансикбакквард.'
ms.assetid: 6443980f-6863-4941-b2dd-4a31257b5810
title: Кпоспасссру. Кансикбакквард, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.CanSeekBackward
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c1d989acf074eb20e6ea3387c37129700320ce782e3c5d7c8bd4320641839ca1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108434"
---
# <a name="cpospassthrucanseekbackward-method"></a>Кпоспасссру. Кансикбакквард, метод

`CanSeekBackward`Метод определяет, можно ли выполнить поиск в потоке обратно. Этот метод реализует метод [**имедиапоситион:: кансикбакквард**](/windows/desktop/api/Control/nf-control-imediaposition-canseekbackward) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT CanSeekBackward(
   LONG *pCanSeekBackward
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пкансикбакквард* 
</dt> <dd>

Указатель на переменную, которая получает значение ОАТРУЕ, если фильтр может искать назад, или ОАФАЛСЕ в противном случае.

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

 

 




