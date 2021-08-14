---
title: Обработка событий в C++
description: Обработка событий в C++
ms.assetid: 5d9eb1c7-7022-4442-b67a-6a96fe5ce97f
keywords:
- проигрыватель Windows Media, C++
- объектная модель проигрыватель Windows Media, C++
- Объектная модель, C++
- проигрыватель Windows Media Мобильный, C++
- проигрыватель Windows Media ActiveX элемент управления, C++
- проигрыватель Windows Media мобильный ActiveX элемент управления, C++
- ActiveX элемент управления, C++
- Внедрение программ на C++
- внедрение, программы на C++
- проигрыватель Windows Media ActiveX элемент управления, обработка событий
- проигрыватель Windows Media управление мобильными ActiveXми, обработка событий
- управление ActiveXми, обработка событий
- события, C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf5d50be4622cee9ee455710f8b9d2e4cafc63d6560e08faf5c3deaddcdaccc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117748409"
---
# <a name="handling-events-in-c"></a>Обработка событий в C++

события от проигрыватель Windows Media можно получить двумя способами.

-   Через **IDispatch** с помощью интерфейса **\_ вмпокксевентс** . Этот интерфейс используется для большинства сценариев внедрения.
-   Через интерфейс **ивмпевентс** . этот интерфейс доступен, если код подключен к проигрывателю в полноэкранном режиме, например при удаленном взаимодействии с элементом управления проигрыватель Windows Media или в подключаемом модуле пользовательского интерфейса.

В каждом сценарии начинается прослушивание событий с помощью точек подключения COM.

В следующем примере кода используются три переменные члена:


```C++
CComPtr<IWMPPlayer>         m_spWMPPlayer;
CComPtr<IConnectionPoint>   m_spConnectionPoint;
DWORD                       m_dwAdviseCookie;

```



Чтобы получить точку подключения, сначала выведите **QueryInterface** для контейнера точки подключения.


```C++
HRESULT  hr = S_OK;
// Smart pointer to IConnectionPointContainer
CComPtr<IConnectionPointContainer>  spConnectionContainer;

hr = m_spWMPPlayer->QueryInterface(&spConnectionContainer);

```



Затем запросите точку подключения для интерфейса событий, который вы хотите использовать. В следующем примере код сначала пытается использовать **ивмпевентс**. Если этот интерфейс недоступен, он использует **\_ вмпокксевентс**.


```C++
// Test whether the control supports the IWMPEvents interface.
if(SUCCEEDED(hr))
{
    hr = spConnectionContainer->FindConnectionPoint(__uuidof(IWMPEvents), &m_spConnectionPoint);
    if (FAILED(hr))
    {
        // If not, try the _WMPOCXEvents interface, which uses IDispatch.
        hr = spConnectionContainer->FindConnectionPoint(__uuidof(_WMPOCXEvents), &m_spConnectionPoint);
    }
}

```



Наконец, вызовите метод **IConnectionPoint:: Advise** , чтобы запросить события.


```C++
if(SUCCEEDED(hr))
{
    hr = m_spConnectionPoint->Advise(this, &m_dwAdviseCookie);
}

```



В предыдущем примере первый параметр предполагает, что вызывающий класс реализует как **ивмпевентс** , так и **\_ вмпокксевентс**. Второй параметр — это возвращаемое значение, которое используется для прекращения прослушивания событий, например при выходе из программы, с использованием кода, аналогичного следующему:


```C++
// Stop listening to events
if (m_spConnectionPoint)
{
    if (0 != m_dwAdviseCookie)
        m_spConnectionPoint->Unadvise(m_dwAdviseCookie);
        m_spConnectionPoint.Release();
}

```



Реализация обработчиков событий для **ивмпевентс** и **\_ вмпокксевентс** отличается. Для **ивмпевентс** необходимо реализовать функцию для управления каждым событием, определенным интерфейсом, даже если вы не планируете использовать событие.


```C++
// IWMPEvents methods
void STDMETHODCALLTYPE OpenStateChange( long NewState ){ return; }
void STDMETHODCALLTYPE PlayStateChange( long NewState ){ return; }
void STDMETHODCALLTYPE AudioLanguageChange( long LangID ){ return; }
// And so on...

```



Для реализации обработчиков **\_ вмпокксевентс** необходимо использовать **IDispatch:: Invoke**, который представляет собой отдельную реализацию обработчика событий для всех событий, происходящих в интерфейсе **IDispatch** . Это означает, что можно обрабатывать только определенные события и игнорировать другие. В следующем примере кода показан обработчик **\_ вмпокксевентс** с помощью **Invoke**, который обрабатывает только события **опенстатечанже** и **плайстатечанже** :


```C++
HRESULT CMyClass::Invoke(
    DISPID  dispIdMember,      
    REFIID  riid,              
    LCID  lcid,                
    WORD  wFlags,              
    DISPPARAMS FAR*  pDispParams,  
    VARIANT FAR*  pVarResult,  
    EXCEPINFO FAR*  pExcepInfo,  
    unsigned int FAR*  puArgErr )
{
    if (!pDispParams)
        return E_POINTER;

    if (pDispParams->cNamedArgs != 0)
        return DISP_E_NONAMEDARGS;

    HRESULT hr = DISP_E_MEMBERNOTFOUND;

    switch (dispIdMember)
    {
        case DISPID_WMPCOREEVENT_OPENSTATECHANGE:
            OpenStateChange(pDispParams->rgvarg[0].lVal /* NewState */ );
            break;

        case DISPID_WMPCOREEVENT_PLAYSTATECHANGE:
            PlayStateChange(pDispParams->rgvarg[0].lVal /* NewState */);
            break;

        // Other cases can handle additional events by using DISPIDs.
    }

    return( hr );
}

```



В приведенном выше примере кода каждый случай просто вызывает обработчик **ивмпевентс** для соответствующего события. Если код обрабатывает только **\_ вмпокксевентс**, можно просто вызвать пользовательскую функцию или обработать событие в строке после инструкции **case** .

## <a name="receiving-events-from-windows-media-player-10-mobile"></a>получение событий от проигрыватель Windows Media 10 Mobile

мобильный элемент управления проигрыватель Windows Media 10 поддерживает получение определенных событий только через **\_ вмпокксевентс** и **ивмпевентс**. Дополнительные сведения см. в документации по **ивмпевентс**.

## <a name="samples"></a>Примеры

пакет установки проигрыватель Windows Media устанавливает пример, демонстрирующий обработку событий. Дополнительные сведения см. в примере Вмфост.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Примеры**](samples.md)
</dt> <dt>

[**использование элемента управления проигрыватель Windows Media в программе на языке C++**](using-the-windows-media-player-control-in-a-c---program.md)
</dt> </dl>

 

 




