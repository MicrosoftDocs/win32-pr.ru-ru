---
description: Каутпуткуеуе. Ендфлуш, метод Ендфлуш завершает операцию очистки.
ms.assetid: 9171a62a-9072-49a3-8e83-f66d7e1483da
title: Каутпуткуеуе. Ендфлуш, метод (Аутпутк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d9a283867036254b7a13b45ba152c3f16ecccbdb59d4d59e98c8d1dae7480e13
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634224"
---
# <a name="coutputqueueendflush-method"></a>Каутпуткуеуе. Ендфлуш, метод

`EndFlush`Метод завершает операцию очистки.

## <a name="syntax"></a>Синтаксис


```C++
void EndFlush();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

Если объект использует поток, этот метод ожидает события [**каутпуткуеуе:: m \_ евфлушкомплете**](coutputqueue-m-evflushcomplete.md) . Поток сигнализирует об этом событии после освобождения всех ожидающих выборок. Если объект не использует поток, этот метод вызывает метод [**каутпуткуеуе:: фрисамплес**](coutputqueue-freesamples.md) . Затем `EndFlush` метод вызывает метод [**Ипин:: ендфлуш**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) для входного ПИН-кода.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>аутпутк. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Каутпуткуеуе**](coutputqueue.md)
</dt> </dl>

 

 




