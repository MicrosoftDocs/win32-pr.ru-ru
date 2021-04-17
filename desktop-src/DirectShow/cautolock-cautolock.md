---
description: Метод конструктора. Конструктор блокирует указанный объект критической секции.
ms.assetid: 5a0d74f9-bb99-4922-9a92-2e7c1863421f
title: Конструктор Каутолокк. Каутолокк (Вксутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAutoLock.CAutoLock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fed29011d4fe581ed146f64800351a3f1053d957
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668492"
---
# <a name="cautolockcautolock-constructor"></a>Каутолокк. Каутолокк, конструктор

Метод конструктора. Конструктор блокирует указанный объект критической секции.

## <a name="syntax"></a>Синтаксис


```C++
CAutoLock(
   CCritSec *plock
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*плокк* 
</dt> <dd>

Указатель на объект [**ккритсек**](ccritsec.md) , который содержит объект критической секции.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Вксутил. h (включение Streams. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Каутолокк**](cautolock.md)
</dt> </dl>

 

 




