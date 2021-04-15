---
description: Класс Каутаусингаутпутпин получает и освобождает доступ к объекту Кдинамикаутпутпин.
ms.assetid: 4ded5d18-4b14-4574-ad1f-73b886a51fac
title: Класс Каутаусингаутпутпин (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAutoUsingOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b664267ce2ff0dbbeeba8bc74708c9c67e185ae4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669149"
---
# <a name="cautousingoutputpin-class"></a>Класс Каутаусингаутпутпин

Класс **каутаусингаутпутпин** получает и освобождает доступ к объекту [**кдинамикаутпутпин**](cdynamicoutputpin.md) .

**Каутаусингаутпутпин** имеет следующие типы членов:



| Открытые методы                                                           | Описание                                              |
|--------------------------------------------------------------------------|----------------------------------------------------------|
| [**каутаусингаутпутпин**](cautousingoutputpin-cautousingoutputpin.md)   | Метод конструктора. Получает доступ к указанному ПИН-коду. |
| [**~ Каутаусингаутпутпин**](cautousingoutputpin--cautousingoutputpin.md) | Метод деструктора. Получает доступ к указанному ПИН-коду.  |



 

## <a name="remarks"></a>Комментарии

При вызове определенных методов для [**кдинамикаутпутпин**](cdynamicoutputpin.md)вызывающий должен получить доступ к ПИН-коду, а затем освободить этот доступ. Для получения доступа вызывающий объект использует метод [**кдинамикаутпутпин:: стартусингаутпутпин**](cdynamicoutputpin-startusingoutputpin.md) . Чтобы освободить доступ, он вызывает метод [**кдинамикаутпутпин:: стопусингаутпутпин**](cdynamicoutputpin-stopusingoutputpin.md) . Класс **каутаусингаутпутпин** является вспомогательным классом, который обрабатывает эти задачи в конструкторе и методах деструктора. В следующем примере кода показано, как использовать этот класс:


```
CDynamicOutputPin *pPin;
HRESULT hr = S_OK;  // Important! Initialize to S_OK.

// TODO: Obtain a pointer to the pin (not shown).

// Scope for lock.
{
    // Hold lock on pin.
    CAutoUsingOutputPin UsingPin(pPin, &hr)

    if (SUCCEEDED(hr)) 
    {

        // Safe to use the pin.
        hr = pPin->Deliver(pSample);

    }

} // Object goes out of scope here.

// No longer safe to use the pin.
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Амфилтер. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Ссылка на базовый класс](base-class-reference.md)
</dt> </dl>

 

 




