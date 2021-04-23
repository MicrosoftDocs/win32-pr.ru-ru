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
# <a name="working-with-localized-system-profiles"></a><span data-ttu-id="0e33b-108">Работа с локализованными системными профилями</span><span class="sxs-lookup"><span data-stu-id="0e33b-108">Working with Localized System Profiles</span></span>

<span data-ttu-id="0e33b-109">Пакет SDK для формата Windows Media включает в себя системные профили с именами и описаниями на нескольких языках.</span><span class="sxs-lookup"><span data-stu-id="0e33b-109">The Windows Media Format SDK includes system profiles with names and descriptions in several languages.</span></span> <span data-ttu-id="0e33b-110">Локализованные файлы Profile. пркс устанавливаются в \[ \] \\ папку sdkroot добавлен вмсдк \\ WMFSDK9 \\ локализедпрофилес.</span><span class="sxs-lookup"><span data-stu-id="0e33b-110">The localized system profile .prx files are installed into the \[SDKRoot\]\\WMSDK\\WMFSDK9\\LocalizedProfiles folder.</span></span> <span data-ttu-id="0e33b-111">Чтобы получить доступ к определенному файлу с помощью методов **ивмпрофилеманажерлангуаже** , необходимо переместить его в корневой каталог системы вместе с другими файлами системного профиля.</span><span class="sxs-lookup"><span data-stu-id="0e33b-111">To access a particular file with the **IWMProfileManagerLanguage** methods, you must move it into the system root directory along with the other system profile files.</span></span> <span data-ttu-id="0e33b-112">Список локализованных файлов системного профиля см. в разделе [локализованные системные профили](localized-system-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="0e33b-112">For a list of the localized system profile files, see [Localized System Profiles](localized-system-profiles.md).</span></span>

<span data-ttu-id="0e33b-113">Вы можете задать или получить язык профиля системы с помощью методов интерфейса [**ивмпрофилеманажерлангуаже**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanagerlanguage) .</span><span class="sxs-lookup"><span data-stu-id="0e33b-113">You can set or retrieve the system profile language using the methods of the [**IWMProfileManagerLanguage**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanagerlanguage) interface.</span></span> <span data-ttu-id="0e33b-114">Язык указывается как значение LANGID, состоящее из основного идентификатора языка и вторичного идентификатора языка.</span><span class="sxs-lookup"><span data-stu-id="0e33b-114">The language is specified as a LANGID value, which consists of a primary language identifier and a secondary language identifier.</span></span> <span data-ttu-id="0e33b-115">В следующем коде показано, как получить текущий язык.</span><span class="sxs-lookup"><span data-stu-id="0e33b-115">The following code demonstrates how to retrieve the current language.</span></span> <span data-ttu-id="0e33b-116">Язык по умолчанию — английский (США) (0x409).</span><span class="sxs-lookup"><span data-stu-id="0e33b-116">The default language is U.S. English (0x409).</span></span> <span data-ttu-id="0e33b-117">Дополнительные сведения об использовании этого кода см. [в разделе Использование примеров кода](using-the-code-examples.md).</span><span class="sxs-lookup"><span data-stu-id="0e33b-117">For more information about using this code, see [Using the Code Examples](using-the-code-examples.md).</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="0e33b-118">См. также</span><span class="sxs-lookup"><span data-stu-id="0e33b-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e33b-119">**Использование системных профилей**</span><span class="sxs-lookup"><span data-stu-id="0e33b-119">**Using System Profiles**</span></span>](using-system-profiles.md)
</dt> </dl>

 

 




