---
title: Работа с локализованными системными профилями
description: Работа с локализованными системными профилями
ms.assetid: d911baf6-0731-4f02-9001-d04464a03f56
keywords:
- профили, система
- системные профили, локализованные
- системные профили, интерфейс Ивмпрофилеманажерлангуаже
- локализованные системные профили, сведения
- ивмпрофилеманажерлангуаже
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd8c040d9804cd822b17e7caad8a8cfb5e5854c4
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "105672245"
---
# <a name="working-with-localized-system-profiles"></a>Работа с локализованными системными профилями

Пакет SDK для формата Windows Media включает в себя системные профили с именами и описаниями на нескольких языках. Локализованные файлы Profile. пркс устанавливаются в \[ \] \\ папку sdkroot добавлен вмсдк \\ WMFSDK9 \\ локализедпрофилес. Чтобы получить доступ к определенному файлу с помощью методов **ивмпрофилеманажерлангуаже** , необходимо переместить его в корневой каталог системы вместе с другими файлами системного профиля. Список локализованных файлов системного профиля см. в разделе [локализованные системные профили](localized-system-profiles.md).

Вы можете задать или получить язык профиля системы с помощью методов интерфейса [**ивмпрофилеманажерлангуаже**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanagerlanguage) . Язык указывается как значение LANGID, состоящее из основного идентификатора языка и вторичного идентификатора языка. В следующем коде показано, как получить текущий язык. Язык по умолчанию — английский (США) (0x409). Дополнительные сведения об использовании этого кода см. [в разделе Использование примеров кода](using-the-code-examples.md).


```C++
HRESULT GetCurrentSystemProfileLanguage(IMWProfilManager* pProfileMgr)
{
    HRESULT hr = S_OK;

    IWMProfileManagerLanguage* pProfileMgrLang = NULL;

    // Get the profile manager language interface.
    hr = pProfileMgr->QueryInterface(IID_IWMProfileManagerLanguage,
                                     (void **) &pProfileMgrLang);
    if(FAILED(hr))
    {
        printf("Couldn't get IWMProfileManagerLanguage.\n");
        SAFE_RELEASE(pProfileMgrLang);
        return hr;
    }

    // Retrieve the current language (as a LANGID value)
    WORD wLangID = 0;
    hr = pProfileMgrLang->GetUserLanguageID(&wLangID);
    if(FAILED(hr))
    {
        printf("Could not get the current language.\n");
        SAFE_RELEASE(pProfileMgrLang);
        return hr;
    }

    printf("The current language ID is 0x%X\n", wLangID);

    SAFE_RELEASE(pProfileMgrLang);
    return S_OK;
}
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[**Использование системных профилей**](using-system-profiles.md)
</dt> </dl>

 

 




