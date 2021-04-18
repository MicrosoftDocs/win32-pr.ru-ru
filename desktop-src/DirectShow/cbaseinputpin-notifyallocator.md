---
description: 'Метод Нотифяллокатор задает распределитель для соединения. Этот метод реализует метод Имеминпутпин:: Нотифяллокатор.'
ms.assetid: 16167bd5-2d33-4329-87ec-6a6c578e0060
title: Кбасеинпутпин. Нотифяллокатор, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.NotifyAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ce5bc3cfe165b1adb6b5b970ca43d31c8ace98f2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668998"
---
# <a name="cbaseinputpinnotifyallocator-method"></a>Кбасеинпутпин. Нотифяллокатор, метод

`NotifyAllocator`Метод задает распределитель для соединения. Этот метод реализует метод [**имеминпутпин:: нотифяллокатор**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT NotifyAllocator(
   IMemAllocator *pAllocator,
   BOOL          bReadOnly
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*паллокатор* 
</dt> <dd>

Указатель на интерфейс [**имемаллокатор**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) распределителя.

</dd> <dt>

*бреадонли* 
</dt> <dd>

Флаг, указывающий, доступны ли образцы из этого распределителя только для чтения. Если **значение — true**, образцы доступны только для чтения.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение S \_ ОК.

## <a name="remarks"></a>Комментарии

Во время соединения с закреплением выходной ПИН-код выбирает распределитель и вызывает этот метод, чтобы уведомить входной ПИН-код. Закрепление вывода может использовать распределитель, предложенный входным закреплением в методе [**имеминпутпин::-распределителя**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) , или предоставить собственный распределитель.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Амфилтер. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасеинпутпин**](cbaseinputpin.md)
</dt> </dl>

 

 




