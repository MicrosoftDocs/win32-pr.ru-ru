---
description: Метод конструктора Кбасеаутпутпин. Кбасеаутпутпин.
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
ms.openlocfilehash: 53f875ffc016a68b6cf714174f4aa39ab57565a73900a0d00ec4d2900722103c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119652484"
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

## <a name="remarks"></a>Remarks

Все параметры передаются непосредственно в конструктор [**кбасепин**](cbasepin.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>амфилтер. h (включает Потоки. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбасеаутпутпин**](cbaseoutputpin.md)
</dt> </dl>

 

 




