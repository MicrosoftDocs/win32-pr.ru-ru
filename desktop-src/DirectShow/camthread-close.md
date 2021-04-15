---
description: Метод Close ожидает выхода из потока, а затем освобождает его ресурсы.
ms.assetid: 57e27ff7-3665-416e-8a6e-660483c5aed2
title: Метод Камсреад. Close (Вксутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.Close
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9cac5ee4a1e1a9cc3fecc8d09096d031e9fc9a63
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689190"
---
# <a name="camthreadclose-method"></a>Камсреад. Close, метод

`Close`Метод ожидает выхода из потока, а затем освобождает его ресурсы.

## <a name="syntax"></a>Синтаксис


```C++
void Close();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="remarks"></a>Комментарии

Перед вызовом этого метода необходимо предоставить способ выхода из потока. Например, в методе [**камсреад:: среадпрок**](camthread-threadproc.md) Определите запрос, который сообщает потоку о выходе. Затем вызовите метод [**камсреад:: каллворкер**](camthread-callworker.md) с этим значением.

Метод деструктора [**~ камсреад**](camthread--camthread.md) вызывает этот метод.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Вксутил. h (включение Streams. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Камсреад**](camthread.md)
</dt> </dl>

 

 




