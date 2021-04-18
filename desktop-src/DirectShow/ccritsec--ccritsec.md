---
description: Метод деструктора.
ms.assetid: cade850c-391c-41dc-adfe-56de8b2bbfff
title: Деструктор Ккритсек. ~ Ккритсек (Вксутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCritSec.~CCritSec
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 21029e2d53fd03ded2be4faa98e8b3e27681600c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105676067"
---
# <a name="ccritsecccritsec-destructor"></a>Деструктор Ккритсек. ~ Ккритсек

Метод деструктора.

## <a name="syntax"></a>Синтаксис


```C++
~CCritSec();
```



## <a name="remarks"></a>Примечания

Этот метод вызывает функцию [**делетекритикалсектион**](/windows/desktop/api/synchapi/nf-synchapi-deletecriticalsection) для удаления критической секции.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Вксутил. h (включение Streams. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Ккритсек**](ccritsec.md)
</dt> </dl>

 

