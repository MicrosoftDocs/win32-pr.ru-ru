---
description: Кбасеинпутпин. Бреакконнект, метод Бреакконнект освобождает ПИН-код из соединения.
ms.assetid: 73b228a9-0a59-4647-b400-c33fa06c7e34
title: Кбасеинпутпин. Бреакконнект, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 625eab8cc070240d79456bff919317f884826fc6d14c26055b68de40aba4c969
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118403493"
---
# <a name="cbaseinputpinbreakconnect-method"></a>Кбасеинпутпин. Бреакконнект, метод

`BreakConnect`Метод освобождает ПИН-код из соединения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT BreakConnect();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает \_ значение ОК в случае успешного выполнения или **HRESULT** , указывающий на причину ошибки.

## <a name="remarks"></a>Remarks

Этот метод переопределяет метод [**кбасепин:: бреакконнект**](cbasepin-breakconnect.md) . Он снимает распределитель и освобождает интерфейс [**имемаллокатор**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) .

При переопределении этого метода вызовите метод базового класса из переопределяющего метода. В противном случае могут возникнуть утечки памяти.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>амфилтер. h (включает Потоки. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасеинпутпин**](cbaseinputpin.md)
</dt> </dl>

 

 




