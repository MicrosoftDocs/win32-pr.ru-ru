---
description: Метод конструктора Кбасемедиафилтер. Кбасемедиафилтер.
ms.assetid: 91290f58-a77b-447f-aa2a-bbee067f5a98
title: Конструктор Кбасемедиафилтер. Кбасемедиафилтер (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.CBaseMediaFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f123c7af29c6420de6004132180eba8dbf33fa72
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096322"
---
# <a name="cbasemediafiltercbasemediafilter-constructor"></a>Кбасемедиафилтер. Кбасемедиафилтер, конструктор

Метод конструктора.

## <a name="syntax"></a>Синтаксис


```C++
CBaseMediaFilter(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         CCritSec  *pLock,
         REFCLSID  clsid
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pName* 
</dt> <dd>

Указатель на строку, содержащую имя объекта.

</dd> <dt>

*pUnk* 
</dt> <dd>

Указатель на владельца этого объекта. Если объект является агрегатным, передайте указатель на интерфейс **IUnknown** объекта агрегирования. В противном случае присвойте этому параметру **значение NULL**.

</dd> <dt>

*плокк* 
</dt> <dd>

Указатель на [**ккритсек**](ccritsec.md) блокировку, используемый для сериализации изменений состояния.

</dd> <dt>

*этому* 
</dt> <dd>

Идентификатор класса объекта.

</dd> </dl>

## <a name="remarks"></a>Remarks

Если другой объект содержит или выполняет статистическую обработку `CBaseMediaFilter` объекта, блокировка **ккритсек** может быть внешней по отношению к `CBaseMediaFilter` объекту. В этом случае передайте указатель на блокировку в *плокк*.

В противном случае можно:

-   Создайте производный класс, который наследует `CBaseMediaFilter` и **ккритсек**. Для *плокк* передайте этот указатель.
-   Создайте производный класс, который наследует `CBaseMediaFilter` и содержит переменную-член **ккритсек** . Для *плокк* передайте адрес этой переменной.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Амфилтер. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбасемедиафилтер**](cbasemediafilter.md)
</dt> </dl>

 

 




