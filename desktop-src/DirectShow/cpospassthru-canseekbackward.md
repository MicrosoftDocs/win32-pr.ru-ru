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
ms.openlocfilehash: a6a016f5cfeea7ca1e63bb4d0e603784b8f95a85
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675076"
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ктлутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кпоспасссру**](cpospassthru.md)
</dt> </dl>

 

 




