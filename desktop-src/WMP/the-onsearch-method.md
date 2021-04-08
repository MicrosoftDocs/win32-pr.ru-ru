---
title: Метод onSearch
description: Метод onSearch
ms.assetid: 709bb428-1a5e-4b8d-8622-5fcc816f0a1a
keywords:
- Подключаемые модули проигрывателя Windows Media, метод onSearch
- подключаемые модули, метод onSearch
- подключаемые модули пользовательского интерфейса, метод onSearch
- Подключаемые модули пользовательского интерфейса, метод onSearch
- Метод onSearch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de5c33af434028e6ee72c757c8d71def0d4109fd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068083"
---
# <a name="the-onsearch-method"></a><span data-ttu-id="80e8f-108">Метод onSearch</span><span class="sxs-lookup"><span data-stu-id="80e8f-108">The OnSearch Method</span></span>

<span data-ttu-id="80e8f-109">Метод onSearch вызывается проигрывателем Windows Media при нажатии кнопки **поиска** .</span><span class="sxs-lookup"><span data-stu-id="80e8f-109">The OnSearch method is called by Windows Media Player when the **Search** button is clicked.</span></span> <span data-ttu-id="80e8f-110">Этот метод извлекает текущий объект **мультимедиа** и передает его методу лаунчпаже.</span><span class="sxs-lookup"><span data-stu-id="80e8f-110">This method retrieves the current **Media** object and passes it to the LaunchPage method.</span></span>

<span data-ttu-id="80e8f-111">Для реализации этого метода используется следующий код:</span><span class="sxs-lookup"><span data-stu-id="80e8f-111">The following code is used to implement this method:</span></span>


```C++
LRESULT OnSearch(WORD wNotifyCode, WORD wID, HWND hwndCtl, BOOL& fHandled)
{
    HRESULT hr;
    CComPtr<IWMPMedia> spMedia;

    if( m_pPlugin && m_pPlugin->m_spCore )
    {
        // Get a pointer to the current media item.
        hr = m_pPlugin->m_spCore->get_currentMedia(&spMedia);
        if (SUCCEEDED(hr) && spMedia)
        {
            LaunchPage(spMedia);
        }
    else
        {
            MessageBox(_T("There is no media loaded."), _T("Warn"), MB_OK | MB_ICONWARNING);
        }
    }
    return 0;
}

```



## <a name="related-topics"></a><span data-ttu-id="80e8f-112">См. также</span><span class="sxs-lookup"><span data-stu-id="80e8f-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80e8f-113">**Реализация Кплугинвиндов**</span><span class="sxs-lookup"><span data-stu-id="80e8f-113">**Implementing CPluginWindow**</span></span>](implementing-cpluginwindow.md)
</dt> </dl>

 

 




