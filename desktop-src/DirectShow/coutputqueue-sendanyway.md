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
ms.openlocfilehash: a6fa5495371e020310e2367aea7e7bed9ef113f2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674878"
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

## <a name="remarks"></a>Комментарии

Если переменная-член [**каутпуткуеуе:: m \_ Ббатчексакт**](coutputqueue-m-bbatchexact.md) имеет **значение true**, объект заполняет массив [**каутпуткуеуе:: m \_ ппсамплес**](coutputqueue-m-ppsamples.md) до того, как он доставляет пакет примеров. Вызовите этот метод для доставки частичного пакета. Например, метод [**каутпуткуеуе:: EOS**](coutputqueue-eos.md) вызывает `SendAnyway` сериализацию сообщений конца потока.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Аутпутк. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Каутпуткуеуе**](coutputqueue.md)
</dt> </dl>

 

 




