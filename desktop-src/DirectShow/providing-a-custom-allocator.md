---
description: Предоставление пользовательского распределителя
ms.assetid: 4ce2db4b-c901-43a5-b905-7d6d923c940b
title: Предоставление пользовательского распределителя
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79b2f36f269ff30545d648c5df22e3070ec5588bcc2fa8791852fe9b6a59215c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747914"
---
# <a name="providing-a-custom-allocator"></a>Предоставление пользовательского распределителя

В этом разделе описывается, как предоставить пользовательский распределитель для фильтра. Описываются только соединения [**имеминпутпин**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) , но шаги для соединения [**иасинкреадер**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) похожи.

Сначала определите класс C++ для распределителя. Распределитель может быть производным от одного из стандартных классов распределителя, [**кбасеаллокатор**](cbaseallocator.md) или [**кмемаллокатор**](cmemallocator.md), или можно создать совершенно новый класс распределителя. При создании нового класса он должен предоставлять интерфейс [**имемаллокатор**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) .

Оставшиеся действия зависят от того, принадлежит ли распределитель к входному заводу или выходному закрепления фильтра. Входные ПИН-коды играют роль, отличную от закрепления вывода на этапе согласования распределителя, так как в конечном итоге выделяется распределитель.

**Предоставление пользовательского распределителя для входного ПИН-кода**

Чтобы предоставить распределитель для входного ПИН-кода, переопределите метод [**кбасеинпутпин::-распределителя**](cbaseinputpin-getallocator.md) входного контакта. В этом методе проверьте переменную члена **m \_ паллокатор** . Если эта переменная не имеет **значение NULL**, это означает, что распределитель уже выбран для этого соединения, поэтому метод методаического **распределителя** должен возвращать указатель на этот распределитель. Если значение **m \_ Паллокатор** равно **null**, это означает, что распределитель не выбран, **поэтому метод метода** должен возвращать указатель на предпочтительный распределитель ПИН-кода. В этом случае создайте экземпляр пользовательского распределителя и возвратите его указатель [**имемаллокатор**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) . В следующем коде показано, как реализовать метод методаического **распределителя** :


```C++
STDMETHODIMP CMyInputPin::GetAllocator(IMemAllocator **ppAllocator)
{
    CheckPointer(ppAllocator, E_POINTER);
    if (m_pAllocator)  
    {
        // We already have an allocator, so return that one.
        *ppAllocator = m_pAllocator;
        (*ppAllocator)->AddRef();
        return S_OK;
    }

    // No allocator yet, so propose our custom allocator. The exact code
    // here will depend on your custom allocator class definition.
    HRESULT hr = S_OK;
    CMyAllocator *pAlloc = new CMyAllocator(&hr);
    if (!pAlloc)
    {
        return E_OUTOFMEMORY;
    }
    if (FAILED(hr))
    {
        delete pAlloc;
        return hr;
    }

    // Return the IMemAllocator interface to the caller.
    return pAlloc->QueryInterface(IID_IMemAllocator, (void**)ppAllocator);
}
```



Когда вышестоящий фильтр выбирает распределитель, он вызывает метод [**имеминпутпин:: нотифяллокатор**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) входного контакта. Переопределите метод [**кбасеинпутпин:: нотифяллокатор**](cbaseinputpin-notifyallocator.md) , чтобы проверить свойства распределителя. В некоторых случаях входной ПИН-код может отклонить распределитель, если он не является пользовательским распределителем, хотя это может привести к сбою всего соединения с ПИН-кодом.

**Предоставление пользовательского распределителя для выходного ПИН-кода**

Чтобы предоставить распределитель для выходного ПИН-кода, переопределите метод [**кбасеаутпутпин:: иниталлокатор**](cbaseoutputpin-initallocator.md) , чтобы создать экземпляр распределителя:


```C++
HRESULT MyOutputPin::InitAllocator(IMemAllocator **ppAllocator)
{
    HRESULT hr = S_OK;
    CMyAllocator *pAlloc = new CMyAllocator(&hr);
    if (!pAlloc)
    {
        return E_OUTOFMEMORY;
    }

    if (FAILED(hr))
    {
        delete pAlloc;
        return hr;
    }

    // Return the IMemAllocator interface.
    return pAlloc->QueryInterface(IID_IMemAllocator, (void**)ppAllocator);
}
```



По умолчанию класс [**кбасеаутпутпин**](cbaseoutputpin.md) запрашивает распределитель из входного ПИН-кода. Если распределитель не подходит, закрепление вывода создает собственный распределитель. Чтобы принудительно установить соединение для использования пользовательского распределителя, переопределите метод [**кбасеаутпутпин::D еЦидеаллокатор**](cbaseoutputpin-decideallocator.md) . Однако имейте в виду, что это может препятствовать подключению выходного контакта с определенными фильтрами, так как другой фильтр может также требовать собственный пользовательский распределитель. Третий вариант — переключить порядок: сначала попробуйте выбрать пользовательский распределитель, а затем вернитесь к распределителю другого фильтра.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Согласование распределителя](negotiating-allocators.md)
</dt> </dl>

 

 



