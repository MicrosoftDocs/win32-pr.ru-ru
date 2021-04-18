---
description: Метод конструктора.
ms.assetid: 1105c951-a51d-49ab-a69d-f3d482d61233
title: Конструктор Кбасеаутпутпин. Кбасеаутпутпин (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.CBaseOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0461c5056ee48caa19f21d1fcb8fcf1636157d9f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669182"
---
# <a name="cbaseoutputpincbaseoutputpin-constructor"></a>Кбасеаутпутпин. Кбасеаутпутпин, конструктор

Метод конструктора.

## <a name="syntax"></a>Синтаксис


```C++
CBaseOutputPin(
   TCHAR       *pObjectName,
   CBaseFilter *pFilter,
   CCritSec    *pLock,
   HRESULT     *phr,
   LPCWSTR     pName
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*побжектнаме* 
</dt> <dd>

Строка, содержащая имя отладки объекта. Дополнительные сведения см. в разделе [**кбасеобжект**](cbaseobject.md).

</dd> <dt>

*пфилтер* 
</dt> <dd>

Указатель на фильтр, создавший этот ПИН-код.

</dd> <dt>

*плокк* 
</dt> <dd>

Указатель на [**ккритсек**](ccritsec.md) блокировку, используемый для сериализации изменений состояния. Это может быть тот же критический раздел, что и для блокировки фильтра, [**кбасефилтер:: m \_ плокк**](cbasefilter-m-plock.md).

</dd> <dt>

*фр* 
</dt> <dd>

Указатель на переменную, которая получает значение **HRESULT** , указывающее на успешное выполнение или ошибку метода.

</dd> <dt>

*pName* 
</dt> <dd>

Строка расширенных символов, содержащая имя ПИН-кода (также используемое в качестве идентификатора ПИН-кода).

</dd> </dl>

## <a name="remarks"></a>Комментарии

Все параметры передаются непосредственно в конструктор [**кбасепин**](cbasepin.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Амфилтер. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасеаутпутпин**](cbaseoutputpin.md)
</dt> </dl>

 

 




