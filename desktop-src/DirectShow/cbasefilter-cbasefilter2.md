---
description: Метод конструктора.
ms.assetid: b6433ec9-6710-4c2f-968f-00e0d9f8c7a5
title: Конструктор Кбасефилтер. Кбасефилтер (const TCHAR *, лпункновн, ккритсек*, рефклсид) (амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.CBaseFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 40ac48a1fd28b9b50a8f1fa9c698ea5db49d97b0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105656927"
---
# <a name="cbasefiltercbasefilterconst-tchar-lpunknown-ccritsec-refclsid-constructor"></a>Конструктор Кбасефилтер. Кбасефилтер (const TCHAR \* , лпункновн, ккритсек \* , рефклсид)

Метод конструктора.

## <a name="syntax"></a>Синтаксис


```C++
CBaseFilter(
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

Указатель на строку, содержащую имя фильтра, для целей отладки.

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

Идентификатор класса (CLSID) фильтра.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Для объекта критического раздела, как правило, необходимо выполнить одно из следующих действий.

-   Создайте производный класс, который наследует как **кбасефилтер** , так и **ккритсек**. Для *плокк* передайте `this` указатель.
-   Создайте производный класс, который наследует **кбасефилтер** и содержит переменную-член **ккритсек** . Для *плокк* передайте адрес этой переменной.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Амфилтер. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасефилтер**](cbasefilter.md)
</dt> </dl>

 

 




