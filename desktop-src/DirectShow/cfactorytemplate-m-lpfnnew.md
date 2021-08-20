---
description: 'Кфакторитемплате:: m_lpfnNew член-указатель на функцию, которая создает экземпляр объекта.'
ms.assetid: 86859bf9-e16a-4494-bf1b-1d8ddbc1c805
title: 'Элемент Кфакторитемплате:: m_lpfnNew (Комбасе. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_lpfnNew
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5a08b0f1b3dc28b70e62866b58a952b12959f0a7f753d5e6b4c847489b52bfd6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119317724"
---
# <a name="cfactorytemplatem_lpfnnew-member"></a>Элемент Кфакторитемплате:: m \_ лпфннев

Указатель на функцию, которая создает экземпляр объекта.

## <a name="syntax"></a>Синтаксис


```C++
LPFNNewCOMObject m_lpfnNew;
```



## <a name="remarks"></a>Remarks

В библиотеке DLL Объявите статическую функцию, которая возвращает указатель на новый экземпляр объекта. В шаблоне фабрики задайте в качестве значения переменной члена **m \_ лпфннев** адрес этой статической функции.

Тип указателя функции — [**лпфнневкомобжект**](lpfnnewcomobject.md).

В следующем примере показана типичная функция для **m \_ лпфннев**:


```C++
CUnknown * WINAPI CMyComponent::CreateInstance(LPUNKNOWN pUnk, HRESULT *pHr) 
{
    CMyComponent *pNewObject = 
        new CMyComponent(NAME("My Component"), pUnk, pHr );

    if (pNewObject == NULL)  
    {
        *phr = E_OUTOFMEMORY;
    }
    return pNewObject;
}
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>комбасе. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кфакторитемплате**](cfactorytemplate.md)
</dt> </dl>

 

 




