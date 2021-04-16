---
description: Возвращает максимальный размер в байтах, необходимый для текущего потока, не включая номер версии.
ms.assetid: ca1a68e2-02b4-4eea-916a-e0418ae811ae
title: Кперсистстреам. Сиземакс, метод (Пстреам. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.SizeMax
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: afa29e2c81cc454a9e85b9038486221f6f44aaf5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668665"
---
# <a name="cpersiststreamsizemax-method"></a>Кперсистстреам. Сиземакс, метод

Возвращает максимальный размер в байтах, необходимый для текущего потока, не включая номер версии.

## <a name="syntax"></a>Синтаксис


```C++
virtual int SizeMax();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает число байтов, необходимых для данных, не включая номер версии.

## <a name="remarks"></a>Комментарии

Версия по умолчанию возвращает нуль. Он должен быть переопределен для предоставления другого подходящего значения.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Пстреам. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кперсистстреам**](cpersiststream.md)
</dt> </dl>

 

 




