---
description: Текущее максимальное число удаляемых разностных кадров.
ms.assetid: d14c594e-55ab-42c2-bdb0-6829f71d02dd
title: 'Элемент Квидеотрансформфилтер:: m_nWaitForKey (Втранс. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_nWaitForKey
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a168a26816825c33c0e047d93cc8b14ebd0f3536
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674850"
---
# <a name="cvideotransformfilterm_nwaitforkey-member"></a>Элемент Квидеотрансформфилтер:: m \_ нваитфоркэй

Текущее максимальное число удаляемых разностных кадров. Хотя эта переменная больше нуля, фильтр будет удалять кадры до тех пор, пока не достигнет ключевого кадра. Для каждого удаляемого кадра фильтр уменьшает значение этой переменной на единицу, что предотвращает удаление фильтром чрезмерного количества кадров. После 30 Дельта-кадров в строке без ключевых кадров фильтр начнет доставлять кадры снова.

## <a name="syntax"></a>Синтаксис


```C++
int m_nWaitForKey;
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Втранс. h (включение Streams. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Квидеотрансформфилтер**](cvideotransformfilter.md)
</dt> </dl>

 

 




