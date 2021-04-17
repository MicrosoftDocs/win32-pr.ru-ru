---
description: Интерфейс Инонделегатингункновн — это версия IUnknown, которая переименовывается, чтобы обеспечить поддержку как для неделегирования, так и для делегирования интерфейсов IUnknown в одном COM-объекте.
ms.assetid: a2faf9d1-2130-4c6c-8fcd-3e118d592b7f
title: Инонделегатингункновн (Комбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- INonDelegatingUnknown
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 13e93d5ba083706ee361addeb4db2157471cbe25
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679750"
---
# <a name="inondelegatingunknown"></a>инонделегатингункновн

`INonDelegatingUnknown`Интерфейс — это версия **IUnknown** , которая переименовывается, чтобы обеспечить поддержку как неделегирования, так и делегирования интерфейсов **IUnknown** в одном COM-объекте.

## <a name="syntax"></a>Синтаксис


```C++
interface INonDelegatingUnknown
{
    virtual HRESULT NonDelegatingQueryInterface) (REFIID riid, LPVOID *ppv) PURE;
    virtual ULONG NonDelegatingAddRef)(void) PURE;
    virtual ULONG NonDelegatingRelease)(void) PURE;
};
```



## <a name="remarks"></a>Примечания

Чтобы использовать `INonDelegatingUnknown` для множественного наследования, выполните следующие действия.

1.  Создайте класс, производный от интерфейса, например IMyInterface.
2.  Включите [**объявление \_ IUnknown**](declare-iunknown.md) в определение класса, чтобы объявить реализации **QueryInterface**, **AddRef** и **Release** , которые вызывают внешнюю неизвестную функцию.
3.  Переопределите **нонделегатингкуеринтерфаце** , чтобы предоставить IMyInterface с помощью следующего кода:
    ```C++
         if (riid == IID_IMyInterface) {
             return GetInterface((IMyInterface *) this, ppv);
         } else {
             return CUnknown::NonDelegatingQueryInterface(riid, ppv);
         }
    ```

    

4.  Объявите и реализуйте функции элементов IMyInterface.

Чтобы использовать `INonDelegatingUnknown` для вложенных интерфейсов, выполните следующие действия.

1.  Объявите класс, производный от [**кункновн**](cunknown.md).
2.  Включите [**объявление \_ IUnknown**](declare-iunknown.md) в определение класса.
3.  Переопределите **нонделегатингкуеринтерфаце** , чтобы предоставить IMyInterface с помощью следующего кода:
    ```C++
         if (riid == IID_IMyInterface) {
             return GetInterface((IMyInterface *) this, ppv);
         } else {
             return CUnknown::NonDelegatingQueryInterface(riid, ppv);
         }
    ```

    

4.  Реализуйте функции члена IMyInterface. Используйте [**кункновн::-owner**](cunknown-getowner.md) для доступа к классу COM-объекта.
5.  В классе COM-объекта сделайте вложенный класс дружественным классом COM-объекта и объявите экземпляр вложенного класса как член класса COM-объекта.

Поскольку необходимо всегда передавать внешнее неизвестное значение и **HRESULT** в конструктор [**кункновн**](cunknown.md) , нельзя использовать конструктор по умолчанию. Необходимо сделать переменную-член указателем на класс и создать новый вызов в конструкторе, чтобы создать его.

Переопределите **нонделегатингкуеринтерфаце** с помощью следующего кода:


```C++
     if (riid == IID_IMyInterface) {
         return m_pImplFilter->
            NonDelegatingQueryInterface(IID_IMyInterface, ppv);
     } else {
         return CUnknown::NonDelegatingQueryInterface(riid, ppv);
     }
```



Можно использовать смешанные классы, поддерживающие некоторые интерфейсы посредством нескольких наследования и некоторых интерфейсов через вложенные классы.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Комбасе. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Вспомогательные функции COM**](com-helper-functions.md)
</dt> </dl>

 

 




