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
ms.openlocfilehash: bf12a80cd967832755f476db0e8810867326e84598ddce835e1da10dc6943419
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118158935"
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

## <a name="remarks"></a>Remarks

Перед вызовом этого метода необходимо предоставить способ выхода из потока. Например, в методе [**камсреад:: среадпрок**](camthread-threadproc.md) Определите запрос, который сообщает потоку о выходе. Затем вызовите метод [**камсреад:: каллворкер**](camthread-callworker.md) с этим значением.

Метод деструктора [**~ камсреад**](camthread--camthread.md) вызывает этот метод.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>вксутил. h (включает Потоки. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Камсреад**](camthread.md)
</dt> </dl>

 

 




