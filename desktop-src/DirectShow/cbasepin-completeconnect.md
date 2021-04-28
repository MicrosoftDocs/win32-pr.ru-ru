---
description: Кбасепин. Комплетеконнект, метод Комплетеконнект завершает подключение к другому ПИН-коду.
ms.assetid: 10cbf29c-2e1a-419c-b0c0-c99f9a285810
title: Кбасепин. Комплетеконнект, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fee207d7a17f12cc81036fbd4f82ec49a99f4a31
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096042"
---
# <a name="cbasepincompleteconnect-method"></a>Кбасепин. Комплетеконнект, метод

`CompleteConnect`Метод завершает подключение к другому ПИН-коду.

## <a name="syntax"></a>Синтаксис


```C++
virtual HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*прецеивепин* 
</dt> <dd>

Указатель на интерфейс [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin) другого ПИН-кода.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение S \_ ОК.

## <a name="remarks"></a>Remarks

Этот метод вызывается на обоих ПИН-кодах в конце процесса подключения. Соединительный ПИН-код вызывает его в методе [**кбасепин:: Connect**](cbasepin-connect.md) , а принимающий ПИН-код вызывает его из метода [**Кбасепин:: рецеивеконнектион**](cbasepin-receiveconnection.md) .

В базовом классе этот метод просто возвращает значение S \_ . Если производный класс имеет какие-либо требования для завершения соединения, он должен переопределить этот метод. Например, класс [**кбасеаутпутпин**](cbaseoutputpin.md) использует этот метод для выбора распределителя памяти.

Если этот метод завершается неудачно, Общая попытка подключения также завершается сбоем, а ПИН-код отключается от полученного PIN-кода.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Амфилтер. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбасепин**](cbasepin.md)
</dt> </dl>

 

 




