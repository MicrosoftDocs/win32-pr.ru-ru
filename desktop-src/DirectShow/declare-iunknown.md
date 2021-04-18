---
description: Макрос DECLARE \_ IUnknown объявляет три метода базового интерфейса для нового интерфейса.
ms.assetid: 3bf8e830-c923-4c31-8855-88fa08f80422
title: DECLARE_IUNKNOWN (Комбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DECLARE_IUNKNOWN
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4823c1b4bd4832b1047a732bc503f04b4da65483
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657711"
---
# <a name="declare_iunknown"></a>ОБЪЯВЛЕНИЕ \_ IUnknown

Макрос **Declare \_ IUnknown** объявляет три метода базового интерфейса для нового интерфейса.

**Синтаксис**

``` syntax
#define DECLARE_IUNKNOWN                                        \
    STDMETHODIMP QueryInterface(REFIID riid, void **ppv) {      \
        return GetOwner()->QueryInterface(riid,ppv);            \
    };                                                          \
    STDMETHODIMP_(ULONG) AddRef() {                             \
        return GetOwner()->AddRef();                            \
    };                                                          \
    STDMETHODIMP_(ULONG) Release() {                            \
        return GetOwner()->Release();                           \
    };
```

## <a name="remarks"></a>Комментарии

При создании нового интерфейса он должен быть производным от **IUnknown**, который имеет три метода: **QueryInterface**, **AddRef** и **Release**. Этот макрос упрощает процесс объявления, объявляя каждый из этих методов для нового интерфейса.

Этот макрос работает только с классами, которые прямо или косвенно являются производными от класса [**кункновн**](cunknown.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Комбасе. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Вспомогательные функции COM**](com-helper-functions.md)
</dt> <dt>

[**Кункновн:: owner**](cunknown-getowner.md)
</dt> <dt>

[Реализация IUnknown](how-to-implement-iunknown.md)
</dt> </dl>

 

 




