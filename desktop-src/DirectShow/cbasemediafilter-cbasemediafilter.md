---
description: Метод конструктора.
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
ms.openlocfilehash: 8498e9da88804291fc5cdb900ff1dbda212e8b0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665325"
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

## <a name="remarks"></a>Комментарии

Если другой объект содержит или выполняет статистическую обработку `CBaseMediaFilter` объекта, блокировка **ккритсек** может быть внешней по отношению к `CBaseMediaFilter` объекту. В этом случае передайте указатель на блокировку в *плокк*.

В противном случае можно:

-   Создайте производный класс, который наследует `CBaseMediaFilter` и **ккритсек**. Для *плокк* передайте этот указатель.
-   Создайте производный класс, который наследует `CBaseMediaFilter` и содержит переменную-член **ккритсек** . Для *плокк* передайте адрес этой переменной.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Амфилтер. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасемедиафилтер**](cbasemediafilter.md)
</dt> </dl>

 

 




