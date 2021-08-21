---
description: Метод CreateInstance создает новый экземпляр класса Кмемаллокатор.
ms.assetid: 87a831a4-2414-4240-8448-c5d90f130470
title: Метод Кмемаллокатор. CreateInstance (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator.CreateInstance
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a8682a667685f38cd7a73e091067a86f528f64e1ec110c473f50000c18ba4d87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118156023"
---
# <a name="cmemallocatorcreateinstance-method"></a>Кмемаллокатор. CreateInstance, метод

`CreateInstance`Метод создает новый экземпляр класса **кмемаллокатор** .

## <a name="syntax"></a>Синтаксис


```C++
static CUnknown* CreateInstance(
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pUnk* 
</dt> <dd>

Указатель на владельца этого объекта. Если объект является агрегатным, передайте указатель на интерфейс **IUnknown** объекта агрегирования. В противном случае присвойте этому параметру **значение NULL**.

</dd> <dt>

*фр* 
</dt> <dd>

Указатель на переменную, которая получает значение **HRESULT** , указывающее на успешное выполнение или ошибку метода.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает указатель на новый объект **кмемаллокатор** , типизированный как объект **кункновн** .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>амфилтер. h (включает Потоки. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кмемаллокатор**](cmemallocator.md)
</dt> </dl>

 

 




