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
ms.openlocfilehash: 2b8f2c547e75303e4c54a49651f2118a90768bc0f42161ee3dae0de9bec2dcad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813304"
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

## <a name="remarks"></a>Remarks

Версия по умолчанию возвращает нуль. Он должен быть переопределен для предоставления другого подходящего значения.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>пстреам. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кперсистстреам**](cpersiststream.md)
</dt> </dl>

 

 




