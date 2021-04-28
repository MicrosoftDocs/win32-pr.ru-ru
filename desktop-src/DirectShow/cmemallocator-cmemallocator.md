---
description: Метод конструктора Кмемаллокатор. Кмемаллокатор.
ms.assetid: 2340b39a-cab6-4524-b8cd-b22d4bdd24d0
title: Конструктор Кмемаллокатор. Кмемаллокатор (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator.CMemAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1151572c32efe69cceb89e7a5ea5a045955b5f43
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095402"
---
# <a name="cmemallocatorcmemallocator-constructor"></a>Кмемаллокатор. Кмемаллокатор, конструктор

Метод конструктора.

## <a name="syntax"></a>Синтаксис


```C++
CMemAllocator(
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pName* 
</dt> <dd>

Указатель на строку, содержащую имя распределителя.

</dd> <dt>

*pUnk* 
</dt> <dd>

Указатель на владельца этого объекта. Если объект является агрегатным, передайте указатель на интерфейс **IUnknown** объекта агрегирования. В противном случае присвойте этому параметру **значение NULL**.

</dd> <dt>

*фр* 
</dt> <dd>

Указатель на переменную, которая получает значение **HRESULT** , указывающее на успешное выполнение или ошибку метода.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Амфилтер. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кмемаллокатор**](cmemallocator.md)
</dt> </dl>

 

 




