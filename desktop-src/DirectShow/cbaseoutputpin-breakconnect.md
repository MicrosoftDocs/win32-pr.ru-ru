---
description: Метод Бреакконнект освобождает ПИН-код из соединения.
ms.assetid: 0dec3c9d-1adf-4fa3-ab5a-c351053f8054
title: Кбасеаутпутпин. Бреакконнект, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3ea23d6f74032c3fd2608209d1d1f4cd2babf121
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657521"
---
# <a name="cbaseoutputpinbreakconnect-method"></a>Кбасеаутпутпин. Бреакконнект, метод

`BreakConnect`Метод освобождает ПИН-код из соединения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT BreakConnect();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает \_ значение ОК в случае успешного выполнения или **HRESULT** , указывающий на причину ошибки.

## <a name="remarks"></a>Комментарии

Этот метод переопределяет метод [**кбасепин:: бреакконнект**](cbasepin-breakconnect.md) . Он снимает распределитель и освобождает интерфейсы [**имемаллокатор**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) и [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin) .

При переопределении этого метода вызовите метод базового класса из переопределяющего метода. В противном случае могут возникнуть утечки памяти.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Амфилтер. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасеаутпутпин**](cbaseoutputpin.md)
</dt> </dl>

 

 




