---
title: Размещение элемента управления проигрывателя Windows Media в приложении Windows
description: Размещение элемента управления проигрывателя Windows Media в приложении Windows
ms.assetid: 8da04160-b9db-4082-aeff-b0107189e33e
keywords:
- Проигрыватель Windows Media, внедрение элемента управления ActiveX
- Объектная модель проигрывателя Windows Media, внедрение элемента управления ActiveX
- Объектная модель, внедрение элемента управления ActiveX
- Проигрыватель Windows Media Mobile, внедрение элемента управления ActiveX
- Элемент управления ActiveX проигрывателя Windows Media, внедрение
- Мобильный элемент управления ActiveX проигрывателя Windows Media, внедрение
- Элемент управления ActiveX, внедрение
- Проигрыватель Windows Media, программы на основе Windows
- Объектная модель проигрывателя Windows Media, программы на основе Windows
- Объектная модель, программы на основе Windows
- Проигрыватель Windows Media Mobile, программы на основе Windows
- Элемент управления ActiveX проигрывателя Windows Media, программы на основе Windows
- Элемент управления мобильными устройствами ActiveX проигрывателя Windows Media, программы на основе Windows
- Элемент управления ActiveX, программы на основе Windows
- Внедрение программ на основе Windows
- внедрение, программы на основе Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2190f0d0076fe3253c39f583ae7d2c197f8cb11
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331451"
---
# <a name="hosting-the-windows-media-player-control-in-a-windows-application"></a><span data-ttu-id="53810-119">Размещение элемента управления проигрывателя Windows Media в приложении Windows</span><span class="sxs-lookup"><span data-stu-id="53810-119">Hosting the Windows Media Player Control in a Windows Application</span></span>

<span data-ttu-id="53810-120">Для использования элемента управления ActiveX проигрывателя Windows Media (включая пользовательский интерфейс) в программе на базе Windows необходимо предоставить контейнер элементов управления ActiveX.</span><span class="sxs-lookup"><span data-stu-id="53810-120">To use the Windows Media Player ActiveX control (including the user interface) in a Windows-based program, you must provide an ActiveX control container.</span></span> <span data-ttu-id="53810-121">ATL предоставляет класс **каксвиндов** для предоставления функциональных возможностей окна узла ActiveX.</span><span class="sxs-lookup"><span data-stu-id="53810-121">ATL provides the **CAxWindow** class to provide ActiveX host window functionality.</span></span>

<span data-ttu-id="53810-122">Чтобы разместить элемент управления проигрывателя Windows Media с помощью класса **каксвиндов** , выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="53810-122">To host the Windows Media Player control using the **CAxWindow** class, follow these steps:</span></span>

1.  <span data-ttu-id="53810-123">Включите следующие заголовки:</span><span class="sxs-lookup"><span data-stu-id="53810-123">Include the following headers:</span></span>
    ```C++
    #include "wmp.h"
    #include <atlbase.h>
    #include <atlcom.h>
    #include <atlhost.h>
    #include <atlctl.h>
    ```

    

2.  <span data-ttu-id="53810-124">Объявите переменные члена следующим образом:</span><span class="sxs-lookup"><span data-stu-id="53810-124">Declare member variables, as follows:</span></span>
    ```C++
    CAxWindow  m_wndView;  // ActiveX host window class.
    CComPtr<IWMPPlayer>  m_spWMPPlayer;  // Smart pointer to IWMPPlayer interface.
    
    ```

    

3.  <span data-ttu-id="53810-125">Когда окно приложения будет создано, вызовите **атлаксвининит**, которое требуется при использовании главного окна ATL ActiveX.</span><span class="sxs-lookup"><span data-stu-id="53810-125">When your application window is created, call **AtlAxWinInit**, which is required when using the ATL ActiveX host window.</span></span>
    ```C++
    AtlAxWinInit();
    
    ```

    

4.  <span data-ttu-id="53810-126">Объявите локальные переменные для кодов возврата и, чтобы они содержали указатель на интерфейс главного окна:</span><span class="sxs-lookup"><span data-stu-id="53810-126">Declare local variables for return codes and to contain the pointer to the host window interface:</span></span>
    ```C++
    CComPtr<IAxWinHostWindow>  spHost;
    HRESULT  hr;
    
    ```

    

5.  <span data-ttu-id="53810-127">Создайте главное окно:</span><span class="sxs-lookup"><span data-stu-id="53810-127">Create the host window:</span></span>
    ```C++
    GetClientRect(&rcClient);
    m_wndView.Create(m_hWnd, rcClient, NULL, WS_CHILD | WS_VISIBLE | WS_CLIPCHILDREN, WS_EX_CLIENTEDGE);
    
    ```

    

6.  <span data-ttu-id="53810-128">Получение указателя интерфейса окна узла:</span><span class="sxs-lookup"><span data-stu-id="53810-128">Retrieve the host window interface pointer:</span></span>
    ```C++
    hr = m_wndView.QueryHost(&spHost);
    
    ```

    

7.  <span data-ttu-id="53810-129">Создайте элемент управления проигрывателя Windows Media в окне главного приложения с помощью идентификатора класса:</span><span class="sxs-lookup"><span data-stu-id="53810-129">Create the Windows Media Player control in the host window using the class ID:</span></span>
    ```C++
    hr = spHost->CreateControl(CComBSTR(_T("{6BF52A52-394A-11d3-B153-00C04F79FAA6}")), m_wndView, 0);
    
    ```

    

8.  <span data-ttu-id="53810-130">Получите указатель интерфейса **ивмпплайер** :</span><span class="sxs-lookup"><span data-stu-id="53810-130">Retrieve the **IWMPPlayer** interface pointer:</span></span>
    ```C++
    hr = m_wndView.QueryControl(&m_spWMPPlayer);
    
    ```

    

<span data-ttu-id="53810-131">При написании собственного кода обязательно проверьте каждый код возврата **HRESULT** на наличие ошибок.</span><span class="sxs-lookup"><span data-stu-id="53810-131">When you write your own code, be sure to check each **HRESULT** return code for errors.</span></span>

<span data-ttu-id="53810-132">Полный пример, демонстрирующий размещение элемента управления ActiveX проигрывателя Windows Media с помощью класса **каксвиндов** , см. в примере вмфост.</span><span class="sxs-lookup"><span data-stu-id="53810-132">For a complete sample that illustrates how to host the Windows Media Player ActiveX control by using the **CAxWindow** class, see the WMPHost sample.</span></span>

## <a name="hosting-the-windows-media-player-10-mobile-control-in-windows-ce"></a><span data-ttu-id="53810-133">Размещение мобильного элемента управления Windows Media Player 10 в Windows CE</span><span class="sxs-lookup"><span data-stu-id="53810-133">Hosting the Windows Media Player 10 Mobile control in Windows CE</span></span>

<span data-ttu-id="53810-134">При разработке приложений на основе Windows CE, на которых размещается мобильный элемент управления Windows Media Player 10, необходимо установить Microsoft eMbedded Visual C++ 4,0 и пакет SDK для Pocket PC 2003 или пакет SDK для Smartphone 2003.</span><span class="sxs-lookup"><span data-stu-id="53810-134">Microsoft eMbedded Visual C++ 4.0 and the Pocket PC 2003 SDK or the Smartphone 2003 SDK must be installed when developing Windows CE-based applications that host a Windows Media Player 10 Mobile control.</span></span> <span data-ttu-id="53810-135">Кроме того, в отличие от ATL для Windows, ATL для Windows CE не поддерживает модель потоков подразделений.</span><span class="sxs-lookup"><span data-stu-id="53810-135">Also, unlike ATL for Windows, ATL for Windows CE does not support the apartment threading model.</span></span> <span data-ttu-id="53810-136">Поэтому необходимо найти все экземпляры потоков подразделений в проекте ATL и изменить их для использования свободной потоковой обработки.</span><span class="sxs-lookup"><span data-stu-id="53810-136">Therefore, you must find all instances of apartment threading in your ATL project and change them to use free threading.</span></span>

## <a name="related-topics"></a><span data-ttu-id="53810-137">См. также</span><span class="sxs-lookup"><span data-stu-id="53810-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="53810-138">**Примеры**</span><span class="sxs-lookup"><span data-stu-id="53810-138">**Samples**</span></span>](samples.md)
</dt> <dt>

[<span data-ttu-id="53810-139">**Использование элемента управления проигрывателя Windows Media в программе на языке C++**</span><span class="sxs-lookup"><span data-stu-id="53810-139">**Using the Windows Media Player Control in a C++ Program**</span></span>](using-the-windows-media-player-control-in-a-c---program.md)
</dt> </dl>

 

 




