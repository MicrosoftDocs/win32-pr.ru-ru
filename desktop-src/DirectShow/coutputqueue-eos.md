---
description: Метод EOS доставляет вызов конца потока входного ПИН-кода.
ms.assetid: 65e8db14-6ca8-4c4f-8bd8-2442f743499e
title: Каутпуткуеуе. EOS, метод (Аутпутк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.EOS
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ab05d4ab3f2620c11bd62d566be851e16b28cecd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675895"
---
# <a name="coutputqueueeos-method"></a>Каутпуткуеуе. EOS, метод

`EOS`Метод доставляет вызов конца потока входного ПИН-кода.

## <a name="syntax"></a>Синтаксис


```C++
void EOS();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Если объект использует поток, он помещает в очередь \_ сообщение управления пакетами EOS. Поток доставляет все ожидающие выборки и вызывает метод [**Ипин:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) для входного ПИН-кода.

Если объект не использует поток, он вызывает метод [**каутпуткуеуе:: сенданивай**](coutputqueue-sendanyway.md) для доставки всех ожидающих выборок. Затем он вызывает **Ипин:: EndOfStream** для входного ПИН-кода.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Аутпутк. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Каутпуткуеуе**](coutputqueue.md)
</dt> </dl>

 

 




