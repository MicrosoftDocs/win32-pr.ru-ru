---
description: Метод Reset сбрасывает объект, чтобы он мог получить больше данных.
ms.assetid: 7074ed71-1650-4b21-a9a2-ad74d0e3e882
title: Метод Каутпуткуеуе. Reset (Аутпутк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.Reset
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d380ef738af3b684606e86a7c36dc04217c54b7c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674879"
---
# <a name="coutputqueuereset-method"></a>Каутпуткуеуе. Reset, метод

`Reset`Метод сбрасывает объект, чтобы он мог получить больше данных.

## <a name="syntax"></a>Синтаксис


```C++
void Reset();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Этот метод сбрасывает переменную члена [**каутпуткуеуе:: m \_ HR**](coutputqueue-m-hr.md) в значение S \_ ОК. Объект может снова получать примеры мультимедиа; Например, после операции очистки.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Аутпутк. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Каутпуткуеуе**](coutputqueue.md)
</dt> </dl>

 

 




