---
title: Метод onSearch
description: Метод onSearch
ms.assetid: 709bb428-1a5e-4b8d-8622-5fcc816f0a1a
keywords:
- проигрыватель Windows Media подключаемые модули, метод onsearch
- подключаемые модули, метод onSearch
- подключаемые модули пользовательского интерфейса, метод onSearch
- Подключаемые модули пользовательского интерфейса, метод onSearch
- Метод onSearch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49ab5cb4b26d291a940ed329e2422240e6fc36e5ba980431af169d58f1398fdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118118004"
---
# <a name="the-onsearch-method"></a>Метод onSearch

метод onsearch вызывается проигрыватель Windows Media при нажатии кнопки **поиска** . Этот метод извлекает текущий объект **мультимедиа** и передает его методу лаунчпаже.

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



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Реализация Кплугинвиндов**](implementing-cpluginwindow.md)
</dt> </dl>

 

 




