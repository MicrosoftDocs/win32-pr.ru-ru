---
description: Метод Lock блокирует объект критической секции.
ms.assetid: b08be5ec-3f02-4ed8-8791-20e4d2a0c55f
title: Метод Ккритсек. Lock (Вксутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCritSec.Lock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 19599e9cd3c3b8fa913bd07d22fe743aaaa1382f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680083"
---
# <a name="ccritseclock-method"></a>Ккритсек. Lock, метод

Метод **Lock** блокирует объект критической секции.

## <a name="syntax"></a>Синтаксис


```C++
void Lock();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Этот метод вызывает функцию [**EnterCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-entercriticalsection) .

Вызовите функцию члена [**ккритсек:: Unlock**](ccritsec-unlock.md) , чтобы разблокировать критическую секцию. В одном потоке можно выполнить несколько вызовов метода **Lock** . не забудьте вызвать **разблокировку** соответствующего числа раз.

Если объект уже заблокирован другим потоком, метод **ккритсек:: Lock** блокируется до освобождения объекта или до возникновения возможного исключения взаимоблокировки.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Вксутил. h (включение Streams. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Ккритсек**](ccritsec.md)
</dt> </dl>

 

