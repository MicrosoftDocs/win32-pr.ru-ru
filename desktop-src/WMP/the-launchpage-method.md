---
title: Метод Лаунчпаже
description: Метод Лаунчпаже
ms.assetid: f0f93535-5afc-4777-9188-5bbac63ddc6b
keywords:
- Подключаемые модули проигрывателя Windows Media, метод Лаунчпаже
- подключаемые модули, метод Лаунчпаже
- подключаемые модули пользовательского интерфейса, метод Лаунчпаже
- Подключаемые модули пользовательского интерфейса, метод Лаунчпаже
- Метод Лаунчпаже
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f04974eba1ba5c86300de44acd2ba6e2920954f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068185"
---
# <a name="the-launchpage-method"></a>Метод Лаунчпаже

Метод Лаунчпаже предоставляет основные функциональные возможности подключаемого модуля, которые позволяют запустить страницу поиска, содержащую сведения об исполнителе элемента мультимедиа, переданного в метод.

Этот метод вызывается методом onSearch с использованием текущего объекта **мультимедиа** .

Для реализации этого метода используется следующий код:


```C++
void LaunchPage(IWMPMedia *pMedia)
{
    USES_CONVERSION;

    HRESULT hr;
    CComBSTR bstrType;
    CComBSTR bstrArtist;

    // Get the name of the artist.
    bstrType = _T("artist");
    hr = pMedia->getItemInfo(bstrType, &bstrArtist);
    if (SUCCEEDED(hr)) 
    {
        // Create the search URL.
        TCHAR szSearch[MAX_PATH];
        _stprintf_s(szSearch, MAX_PATH, _T("https://search.msn.com/results.asp?q=%s"), OLE2T(bstrArtist));
        CComBSTR bstrURL = szSearch;

        // Launch the search page.
        m_pPlugin->m_spCore->launchURL(bstrURL);
    }
    else
    {
        MessageBox(_T("Failed to get artist information from media."), _T("Warn"), MB_OK | MB_ICONWARNING);
    }
}

```



## <a name="related-topics"></a>См. также

<dl> <dt>

[**Реализация Кплугинвиндов**](implementing-cpluginwindow.md)
</dt> </dl>

 

 




