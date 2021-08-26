---
description: в этом разделе описано, как реализовать ведение журнала ошибок в службах DirectShow editing Services.
ms.assetid: c0b3b25c-ed03-4f78-9c53-0c0bcff1c60c
title: Создание класса ведения журнала ошибок
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 194d927b2e4eae73f75a326ed03363d96f6121634e46b606ba87409e3bf07f9f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108204"
---
# <a name="creating-an-error-logging-class"></a>Создание класса ведения журнала ошибок

\[Этот API не поддерживается и может быть изменен или недоступен в будущем.\]

в этом разделе описано, как реализовать ведение журнала ошибок в [службах DirectShow editing Services](directshow-editing-services.md).

Сначала объявите класс, который будет реализовывать ведение журнала ошибок. Класс наследует интерфейс [**иамеррорлог**](iamerrorlog.md) . Он содержит объявления для трех методов **IUnknown** и для одного метода в [иамеррорлог](implementing-iamerrorlog.md). Объявление класса выглядит следующим образом:


```C++
class CErrReporter : public IAMErrorLog
{
protected:
    long    m_lRef; // Reference count.

public:
    CErrReporter() { m_lRef = 0; }

    // IUnknown
    STDMETHOD(QueryInterface(REFIID, void**));
    STDMETHOD_(ULONG, AddRef());
    STDMETHOD_(ULONG, Release());

    // IAMErrorLog
    STDMETHOD(LogError(LONG, BSTR, LONG, HRESULT, VARIANT*));
};
```



Единственной переменной-членом в классе является m \_ лреф, которая содержит счетчик ссылок объекта.

Затем определите методы в **IUnknown**. В следующем примере показана стандартная реализация для этих методов:


```C++
STDMETHODIMP CErrReporter::QueryInterface(REFIID riid, void **ppv)
{
    if (ppv == NULL) return E_POINTER;

    *ppv = NULL;
    if (riid == IID_IUnknown)
        *ppv = static_cast<IUnknown*>(this);
    else if (riid == IID_IAMErrorLog)
        *ppv = static_cast<IAMErrorLog*>(this);
        
    else 
    return E_NOINTERFACE;

    AddRef();
    return S_OK;
}

STDMETHODIMP_(ULONG) CErrReporter::AddRef()
{
    return InterlockedIncrement(&m_lRef);
}

STDMETHODIMP_(ULONG) CErrReporter::Release()
{
    // Store the decremented count in a temporary
    // variable. 
    ULONG uCount = InterlockedDecrement(&m_lRef);
    if (uCount == 0)
    {
        delete this;
    }
    // Return the temporary variable, not the member
    // variable, for thread safety.
    return uCount;
}
```



После создания COM-инфраструктуры теперь можно реализовать интерфейс **иамеррорлог** . В следующем разделе описывается, как это сделать.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Регистрация ошибок](logging-errors.md)
</dt> </dl>

 

 



