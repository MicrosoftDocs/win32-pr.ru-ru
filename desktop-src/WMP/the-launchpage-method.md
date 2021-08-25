---
title: Метод Лаунчпаже
description: Метод Лаунчпаже
ms.assetid: f0f93535-5afc-4777-9188-5bbac63ddc6b
keywords:
- подключаемые модули проигрыватель Windows Media, метод лаунчпаже
- подключаемые модули, метод Лаунчпаже
- подключаемые модули пользовательского интерфейса, метод Лаунчпаже
- Подключаемые модули пользовательского интерфейса, метод Лаунчпаже
- Метод Лаунчпаже
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11a22e1f4b136711a6f4336fbe54d6d90e4bb18b24a88645587311a0b4046f6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119762724"
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



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Реализация Кплугинвиндов**](implementing-cpluginwindow.md)
</dt> </dl>

 

 




