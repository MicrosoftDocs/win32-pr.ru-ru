---
title: Обработка событий в C++
description: Обработка событий в C++
ms.assetid: 5d9eb1c7-7022-4442-b67a-6a96fe5ce97f
keywords:
- Проигрыватель Windows Media, C++
- Объектная модель проигрывателя Windows Media, C++
- Объектная модель, C++
- Проигрыватель Windows Media Mobile, C++
- Элемент управления ActiveX проигрывателя Windows Media, C++
- Элемент управления ActiveX в проигрывателе Windows Media Mobile, C++
- Элемент управления ActiveX, C++
- Внедрение программ на C++
- внедрение, программы на C++
- Элемент управления ActiveX проигрывателя Windows Media, обработка событий
- Мобильный элемент управления ActiveX проигрывателя Windows Media, обработка событий
- Элемент управления ActiveX, обработка событий
- события, C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16cbef547ab2604244c5c204707a08eb87a6b70a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104132978"
---
# <a name="handling-events-in-c"></a><span data-ttu-id="6bb2e-116">Обработка событий в C++</span><span class="sxs-lookup"><span data-stu-id="6bb2e-116">Handling Events in C++</span></span>

<span data-ttu-id="6bb2e-117">События из проигрывателя Windows Media можно получить двумя способами.</span><span class="sxs-lookup"><span data-stu-id="6bb2e-117">You can receive events from Windows Media Player in two ways.</span></span>

-   <span data-ttu-id="6bb2e-118">Через **IDispatch** с помощью интерфейса **\_ вмпокксевентс** .</span><span class="sxs-lookup"><span data-stu-id="6bb2e-118">Through **IDispatch** by using the **\_WMPOCXEvents** interface.</span></span> <span data-ttu-id="6bb2e-119">Этот интерфейс используется для большинства сценариев внедрения.</span><span class="sxs-lookup"><span data-stu-id="6bb2e-119">This is the interface to use for most embedding scenarios.</span></span>
-   <span data-ttu-id="6bb2e-120">Через интерфейс **ивмпевентс** .</span><span class="sxs-lookup"><span data-stu-id="6bb2e-120">Through the **IWMPEvents** interface.</span></span> <span data-ttu-id="6bb2e-121">Этот интерфейс доступен, если код подключен к проигрывателю в полноэкранном режиме, например при удаленном доступе к элементу управления проигрывателя Windows Media или в подключаемом модуле пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="6bb2e-121">This interface is available when your code is connected to the full mode Player, such as when remoting the Windows Media Player control or in a UI plug-in.</span></span>

<span data-ttu-id="6bb2e-122">В каждом сценарии начинается прослушивание событий с помощью точек подключения COM.</span><span class="sxs-lookup"><span data-stu-id="6bb2e-122">In each scenario, you start listening to events by using COM connection points.</span></span>

<span data-ttu-id="6bb2e-123">В следующем примере кода используются три переменные члена:</span><span class="sxs-lookup"><span data-stu-id="6bb2e-123">The following example code uses three member variables:</span></span>


```C++
CComPtr<IWMPPlayer>         m_spWMPPlayer;
CComPtr<IConnectionPoint>   m_spConnectionPoint;
DWORD                       m_dwAdviseCookie;

```



<span data-ttu-id="6bb2e-124">Чтобы получить точку подключения, сначала выведите **QueryInterface** для контейнера точки подключения.</span><span class="sxs-lookup"><span data-stu-id="6bb2e-124">To retrieve a connection point, you first **QueryInterface** for the connection point container.</span></span>


```C++
HRESULT  hr = S_OK;
// Smart pointer to IConnectionPointContainer
CComPtr<IConnectionPointContainer>  spConnectionContainer;

hr = m_spWMPPlayer->QueryInterface(&spConnectionContainer);

```



<span data-ttu-id="6bb2e-125">Затем запросите точку подключения для интерфейса событий, который вы хотите использовать.</span><span class="sxs-lookup"><span data-stu-id="6bb2e-125">Next, request the connection point for the event interface you want to use.</span></span> <span data-ttu-id="6bb2e-126">В следующем примере код сначала пытается использовать **ивмпевентс**.</span><span class="sxs-lookup"><span data-stu-id="6bb2e-126">The following example code first attempts to use **IWMPEvents**.</span></span> <span data-ttu-id="6bb2e-127">Если этот интерфейс недоступен, он использует **\_ вмпокксевентс**.</span><span class="sxs-lookup"><span data-stu-id="6bb2e-127">If that interface isn't available, it uses **\_WMPOCXEvents**.</span></span>


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



<span data-ttu-id="6bb2e-128">Наконец, вызовите метод **IConnectionPoint:: Advise** , чтобы запросить события.</span><span class="sxs-lookup"><span data-stu-id="6bb2e-128">Finally, call **IConnectionPoint::Advise** to request events.</span></span>


```C++
if(SUCCEEDED(hr))
{
    hr = m_spConnectionPoint->Advise(this, &m_dwAdviseCookie);
}

```



<span data-ttu-id="6bb2e-129">В предыдущем примере первый параметр предполагает, что вызывающий класс реализует как **ивмпевентс** , так и **\_ вмпокксевентс**.</span><span class="sxs-lookup"><span data-stu-id="6bb2e-129">In the preceding example, the first parameter assumes that the calling class implements both **IWMPEvents** and **\_WMPOCXEvents**.</span></span> <span data-ttu-id="6bb2e-130">Второй параметр — это возвращаемое значение, которое используется для прекращения прослушивания событий, например при выходе из программы, с использованием кода, аналогичного следующему:</span><span class="sxs-lookup"><span data-stu-id="6bb2e-130">The second parameter is a return value that you use to stop listening to events, such as when your program exits, using code similar to the following:</span></span>


```C++
// Stop listening to events
if (m_spConnectionPoint)
{
    if (0 != m_dwAdviseCookie)
        m_spConnectionPoint->Unadvise(m_dwAdviseCookie);
        m_spConnectionPoint.Release();
}

```



<span data-ttu-id="6bb2e-131">Реализация обработчиков событий для **ивмпевентс** и **\_ вмпокксевентс** отличается.</span><span class="sxs-lookup"><span data-stu-id="6bb2e-131">Implementing the event handlers for **IWMPEvents** and **\_WMPOCXEvents** differs.</span></span> <span data-ttu-id="6bb2e-132">Для **ивмпевентс** необходимо реализовать функцию для управления каждым событием, определенным интерфейсом, даже если вы не планируете использовать событие.</span><span class="sxs-lookup"><span data-stu-id="6bb2e-132">For **IWMPEvents**, you must implement a function to handle every event defined by the interface, even if you don't intend to use the event.</span></span>


```C++
// IWMPEvents methods
void STDMETHODCALLTYPE OpenStateChange( long NewState ){ return; }
void STDMETHODCALLTYPE PlayStateChange( long NewState ){ return; }
void STDMETHODCALLTYPE AudioLanguageChange( long LangID ){ return; }
// And so on...

```



<span data-ttu-id="6bb2e-133">Для реализации обработчиков **\_ вмпокксевентс** необходимо использовать **IDispatch:: Invoke**, который представляет собой отдельную реализацию обработчика событий для всех событий, происходящих в интерфейсе **IDispatch** .</span><span class="sxs-lookup"><span data-stu-id="6bb2e-133">To implement **\_WMPOCXEvents** handlers, you must use **IDispatch::Invoke**, which is a single event handler implementation for all the events happening on the **IDispatch** interface.</span></span> <span data-ttu-id="6bb2e-134">Это означает, что можно обрабатывать только определенные события и игнорировать другие.</span><span class="sxs-lookup"><span data-stu-id="6bb2e-134">This means that you can choose to handle only certain events and ignore others.</span></span> <span data-ttu-id="6bb2e-135">В следующем примере кода показан обработчик **\_ вмпокксевентс** с помощью **Invoke**, который обрабатывает только события **опенстатечанже** и **плайстатечанже** :</span><span class="sxs-lookup"><span data-stu-id="6bb2e-135">The following example code shows a **\_WMPOCXEvents** handler, using **Invoke**, that handles only the **OpenStateChange** and **PlayStateChange** events:</span></span>


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



<span data-ttu-id="6bb2e-136">В приведенном выше примере кода каждый случай просто вызывает обработчик **ивмпевентс** для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="6bb2e-136">In the preceding example code, each case simply calls through to the **IWMPEvents** handler for the corresponding event.</span></span> <span data-ttu-id="6bb2e-137">Если код обрабатывает только **\_ вмпокксевентс**, можно просто вызвать пользовательскую функцию или обработать событие в строке после инструкции **case** .</span><span class="sxs-lookup"><span data-stu-id="6bb2e-137">If your code only handles **\_WMPOCXEvents**, you can simply call a custom function or handle the event inline after the **case** statement.</span></span>

## <a name="receiving-events-from-windows-media-player-10-mobile"></a><span data-ttu-id="6bb2e-138">Получение событий от проигрывателя Windows Media 10 Mobile</span><span class="sxs-lookup"><span data-stu-id="6bb2e-138">Receiving Events from Windows Media Player 10 Mobile</span></span>

<span data-ttu-id="6bb2e-139">Мобильный элемент управления Windows Media Player 10 поддерживает получение определенных событий только через **\_ Вмпокксевентс** и **ивмпевентс**.</span><span class="sxs-lookup"><span data-stu-id="6bb2e-139">The Windows Media Player 10 Mobile control only supports receiving certain events through **\_WMPOCXEvents** and **IWMPEvents**.</span></span> <span data-ttu-id="6bb2e-140">Дополнительные сведения см. в документации по **ивмпевентс**.</span><span class="sxs-lookup"><span data-stu-id="6bb2e-140">For more information, please see the documentation for **IWMPEvents**.</span></span>

## <a name="samples"></a><span data-ttu-id="6bb2e-141">Примеры</span><span class="sxs-lookup"><span data-stu-id="6bb2e-141">Samples</span></span>

<span data-ttu-id="6bb2e-142">Пакет установки проигрывателя Windows Media устанавливает пример, демонстрирующий обработку событий.</span><span class="sxs-lookup"><span data-stu-id="6bb2e-142">The Windows Media Player setup package installs a sample that demonstrates event handling.</span></span> <span data-ttu-id="6bb2e-143">Дополнительные сведения см. в примере Вмфост.</span><span class="sxs-lookup"><span data-stu-id="6bb2e-143">See the WMPHost sample for more information.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6bb2e-144">См. также</span><span class="sxs-lookup"><span data-stu-id="6bb2e-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6bb2e-145">**Примеры**</span><span class="sxs-lookup"><span data-stu-id="6bb2e-145">**Samples**</span></span>](samples.md)
</dt> <dt>

[<span data-ttu-id="6bb2e-146">**Использование элемента управления проигрывателя Windows Media в программе на языке C++**</span><span class="sxs-lookup"><span data-stu-id="6bb2e-146">**Using the Windows Media Player Control in a C++ Program**</span></span>](using-the-windows-media-player-control-in-a-c---program.md)
</dt> </dl>

 

 




