---
description: Метод Сенданивай доставляет все ожидающие выборки.
ms.assetid: b4e3a0c6-0f72-4a00-963e-65ceed265f01
title: Каутпуткуеуе. Сенданивай, метод (Аутпутк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.SendAnyway
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4aed3cdd37c50f20b48922c8c711266a111680506813ab4572800abbca971343
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119831764"
---
# <a name="coutputqueuesendanyway-method"></a>Каутпуткуеуе. Сенданивай, метод

`SendAnyway`Метод доставляет все ожидающие выборки.

## <a name="syntax"></a>Синтаксис


```C++
void SendAnyway();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

Если переменная-член [**каутпуткуеуе:: m \_ Ббатчексакт**](coutputqueue-m-bbatchexact.md) имеет **значение true**, объект заполняет массив [**каутпуткуеуе:: m \_ ппсамплес**](coutputqueue-m-ppsamples.md) до того, как он доставляет пакет примеров. Вызовите этот метод для доставки частичного пакета. Например, метод [**каутпуткуеуе:: EOS**](coutputqueue-eos.md) вызывает `SendAnyway` сериализацию сообщений конца потока.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>аутпутк. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Каутпуткуеуе**](coutputqueue.md)
</dt> </dl>

 

 




