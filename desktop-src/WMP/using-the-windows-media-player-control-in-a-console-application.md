---
title: Использование элемента управления проигрывателя Windows Media в консольном приложении
description: Использование элемента управления проигрывателя Windows Media в консольном приложении
ms.assetid: e5162aad-69d5-4253-83d1-46735336e6da
keywords:
- Проигрыватель Windows Media, внедрение элемента управления ActiveX
- Объектная модель проигрывателя Windows Media, внедрение элемента управления ActiveX
- Объектная модель, внедрение элемента управления ActiveX
- Проигрыватель Windows Media Mobile, внедрение элемента управления ActiveX
- Элемент управления ActiveX проигрывателя Windows Media, внедрение
- Мобильный элемент управления ActiveX проигрывателя Windows Media, внедрение
- Элемент управления ActiveX, внедрение
- Проигрыватель Windows Media, консольные приложения
- Объектная модель проигрывателя Windows Media, консольные приложения
- Объектная модель, консольные приложения
- Проигрыватель Windows Media Mobile, консольные приложения
- Элемент управления ActiveX проигрывателя Windows Media, консольные приложения
- Мобильный элемент управления ActiveX проигрывателя Windows Media, консольные приложения
- Элемент управления ActiveX, консольные приложения
- внедрение консольного приложения
- внедрение, консольные приложения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53cc7701fc10848ca246d9cf100d0716e1955b5e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330704"
---
# <a name="using-the-windows-media-player-control-in-a-console-application"></a><span data-ttu-id="3b1bb-119">Использование элемента управления проигрывателя Windows Media в консольном приложении</span><span class="sxs-lookup"><span data-stu-id="3b1bb-119">Using the Windows Media Player Control in a Console Application</span></span>

<span data-ttu-id="3b1bb-120">Экземпляр COM-объекта проигрывателя Windows Media можно создать напрямую с помощью **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="3b1bb-120">You can create an instance of the Windows Media Player COM object directly by using **CoCreateInstance**.</span></span> <span data-ttu-id="3b1bb-121">При этом объект **Player** не отображает пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="3b1bb-121">When you do this, the **Player** object displays no user interface.</span></span> <span data-ttu-id="3b1bb-122">Однако объект по-прежнему полезен для задач, не требующих пользовательского интерфейса, таких как работа с библиотекой, воспроизведение цифровых звуковых файлов или доступ к свойствам проигрывателя.</span><span class="sxs-lookup"><span data-stu-id="3b1bb-122">However, the object is still useful for tasks that don't require the user interface, such as working with the library, playing digital audio files, or accessing properties of the Player.</span></span>

<span data-ttu-id="3b1bb-123">В следующем примере кода показана простая консольная программа, которая отображает версию проигрывателя Windows Media в окне сообщения.</span><span class="sxs-lookup"><span data-stu-id="3b1bb-123">The following example code shows a simple console program that displays the Windows Media Player version in a message box.</span></span> <span data-ttu-id="3b1bb-124">В примере кода используется библиотека ATL для использования смарт-указателей и класса String **CComBSTR** .</span><span class="sxs-lookup"><span data-stu-id="3b1bb-124">The example code uses ATL to take advantage of smart pointers and the **CComBSTR** string class.</span></span>


```C++
#include "atlbase.h"
#include "atlwin.h"
#include "wmp.h"

int _tmain(int argc, _TCHAR* argv[])
{
    CoInitialize(NULL);

    HRESULT hr = S_OK;
    CComBSTR bstrVersionInfo; // Contains the version string.
    CComPtr<IWMPPlayer> spPlayer;  // Smart pointer to IWMPPlayer interface.

    hr = spPlayer.CoCreateInstance( __uuidof(WindowsMediaPlayer), 0, CLSCTX_INPROC_SERVER );

    if(SUCCEEDED(hr))
    {
        hr = spPlayer->get_versionInfo(&bstrVersionInfo);
    }

    if(SUCCEEDED(hr))
    {
        // Show the version in a message box.
        COLE2T pStr(bstrVersionInfo);
        MessageBox( NULL, (LPCSTR)pStr, _T("Windows Media Player Version"), MB_OK );
    }

    // Clean up.
    spPlayer.Release();
    CoUninitialize();

    return 0;
}

```



## <a name="related-topics"></a><span data-ttu-id="3b1bb-125">См. также</span><span class="sxs-lookup"><span data-stu-id="3b1bb-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3b1bb-126">**Использование элемента управления проигрывателя Windows Media в программе на языке C++**</span><span class="sxs-lookup"><span data-stu-id="3b1bb-126">**Using the Windows Media Player Control in a C++ Program**</span></span>](using-the-windows-media-player-control-in-a-c---program.md)
</dt> </dl>

 

 




