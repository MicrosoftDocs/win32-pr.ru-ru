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
# <a name="the-onsearch-method"></a>Метод onSearch

Метод onSearch вызывается проигрывателем Windows Media при нажатии кнопки **поиска** . Этот метод извлекает текущий объект **мультимедиа** и передает его методу лаунчпаже.

Для реализации этого метода используется следующий код:


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



## <a name="related-topics"></a>См. также

<dl> <dt>

[**Реализация Кплугинвиндов**](implementing-cpluginwindow.md)
</dt> </dl>

 

 




