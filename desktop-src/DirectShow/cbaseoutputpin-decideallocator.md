---
description: Метод ДеЦидеаллокатор выбирает распределитель памяти.
ms.assetid: cdc15b0e-ea1b-43aa-9267-95fa9db56ed5
title: Кбасеаутпутпин. ДеЦидеаллокатор, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.DecideAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 73d822450d635fe5f7620d59f39fcc7ed85fe1e2465f34af3ef561dfc2f3828f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119814214"
---
# <a name="cbaseoutputpindecideallocator-method"></a>Кбасеаутпутпин. ДеЦидеаллокатор, метод

`DecideAllocator`Метод выбирает распределитель памяти.

## <a name="syntax"></a>Синтаксис


```C++
virtual HRESULT DecideAllocator(
   IMemInputPin  *pPin,
   IMemAllocator **pAlloc
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппин* 
</dt> <dd>

Указатель на интерфейс [**имеминпутпин**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) входного контакта.

</dd> <dt>

*паллок* 
</dt> <dd>

Адрес переменной, которая получает указатель на интерфейс [**имемаллокатор**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) распределителя.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает \_ значение ОК в случае успешного выполнения или **HRESULT** , указывающий на причину ошибки.

## <a name="remarks"></a>Remarks

Этот метод вызывается в конце процесса подключения ПИН-кода. Он выполняет следующие действия:

1.  Вызывает метод [**имеминпутпин:: жеталлокаторрекуирементс**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocatorrequirements) , чтобы получить требования к буферу входного контакта, если таковые имеются.
2.  Вызывает метод [**имеминпутпин::-распределителя**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) для запроса распределителя от входного ПИН-кода. Если входной ПИН-код не предоставляет распределителя, то закрепление вывода создает его путем вызова метода класса [**кбасеаутпутпин:: иниталлокатор**](cbaseoutputpin-initallocator.md) .
3.  Вызывает метод класса [**кбасеаутпутпин::D еЦидебуфферсизе**](cbaseoutputpin-decidebuffersize.md) , который задает свойства распределителя. Это чистый виртуальный метод; производный класс должен реализовать его.
4.  Вызывает метод [**имеминпутпин:: нотифяллокатор**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) , который уведомляет входной ПИН-код распределителя, который используется.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>амфилтер. h (включает Потоки. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбасеаутпутпин**](cbaseoutputpin.md)
</dt> </dl>

 

 




