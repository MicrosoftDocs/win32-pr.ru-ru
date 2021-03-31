---
title: Изменение версий системного профиля
description: Изменение версий системного профиля
ms.assetid: 66bf4041-47b5-41b4-abb4-eb08d05e3b28
keywords:
- профили, система
- системные профили, версии
- системные профили, изменение версий
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 824e2b1cf4a43cef0e87daa461c6510a6672472d
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104336367"
---
# <a name="to-change-system-profile-versions"></a><span data-ttu-id="18cdb-106">Изменение версий системного профиля</span><span class="sxs-lookup"><span data-stu-id="18cdb-106">To Change System Profile Versions</span></span>

<span data-ttu-id="18cdb-107">При создании объекта диспетчера профилей он анализирует системные профили.</span><span class="sxs-lookup"><span data-stu-id="18cdb-107">Whenever you create a profile manager object, it parses the system profiles.</span></span> <span data-ttu-id="18cdb-108">Можно выполнить итерацию по системным профилям с помощью методов [**ивмпрофилеманажер:: жетсистемпрофилекаунт**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-getsystemprofilecount) и [**Ивмпрофилеманажер:: лоадсистемпрофиле**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadsystemprofile) , но диспетчер профилей будет подсчитывать и выводить в список только профили одной версии за раз.</span><span class="sxs-lookup"><span data-stu-id="18cdb-108">You can iterate through the system profiles using the [**IWMProfileManager::GetSystemProfileCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-getsystemprofilecount) and [**IWMProfileManager::LoadSystemProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadsystemprofile) methods, but the profile manager will count and list only the profiles of a single version at a time.</span></span> <span data-ttu-id="18cdb-109">Если вы хотите использовать этот метод для поиска системных профилей, необходимо убедиться, что диспетчер профилей работает с требуемой версией.</span><span class="sxs-lookup"><span data-stu-id="18cdb-109">If you want to use this method of finding system profiles, you need to ensure that the profile manger deals with the version you want.</span></span> <span data-ttu-id="18cdb-110">Используйте методы интерфейса [**IWMProfileManager2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager2) , чтобы задать и получить версию системного профиля, используемую диспетчером профилей.</span><span class="sxs-lookup"><span data-stu-id="18cdb-110">Use the methods of the [**IWMProfileManager2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager2) interface to set and retrieve the system profile version used by the profile manager.</span></span>

<span data-ttu-id="18cdb-111">Версии задаются с помощью членов типа [**перечисления \_ версии ВМТ**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_version) .</span><span class="sxs-lookup"><span data-stu-id="18cdb-111">Versions are specified using the members of the [**WMT\_VERSION**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_version) enumeration type.</span></span> <span data-ttu-id="18cdb-112">Если задать для версии системного профиля значение ВМТ \_ ver \_ 9 \_ 0, вызов будет выполнен, но число системных профилей будет равно нулю.</span><span class="sxs-lookup"><span data-stu-id="18cdb-112">If you set the system profile version to WMT\_VER\_9\_0, the call will succeed, but the system profile count will be zero.</span></span> <span data-ttu-id="18cdb-113">Это обусловлено тем, что ни один из стандартных системных профилей не использует кодеки Windows Media Audio и Video 9.</span><span class="sxs-lookup"><span data-stu-id="18cdb-113">This is because no predefined system profiles use the Windows Media Audio and Video 9 Series codecs.</span></span> <span data-ttu-id="18cdb-114">Дополнительные сведения об обновлении профилей для использования новых кодеков см. в разделе [повторное использование конфигураций потоков](reusing-stream-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="18cdb-114">For more information about updating profiles to use the newest codecs, see [Reusing Stream Configurations](reusing-stream-configurations.md).</span></span>

<span data-ttu-id="18cdb-115">Если вы загружаете системный профиль по идентификатору GUID, не имеет значения, какая версия системного профиля использует диспетчер профилей.</span><span class="sxs-lookup"><span data-stu-id="18cdb-115">If you load a system profile by its GUID identifier, it does not matter which system profile version the profile manager is using.</span></span> <span data-ttu-id="18cdb-116">Дополнительные сведения о загрузке системных профилей см. [в разделе Загрузка системного профиля](to-load-a-system-profile.md).</span><span class="sxs-lookup"><span data-stu-id="18cdb-116">For more information about loading system profiles, see [To Load a System Profile](to-load-a-system-profile.md).</span></span>

<span data-ttu-id="18cdb-117">В следующем примере кода показано, как задать и получить версию системного профиля.</span><span class="sxs-lookup"><span data-stu-id="18cdb-117">The following example code shows how to set and retrieve the system profile version.</span></span> <span data-ttu-id="18cdb-118">В этом примере для вывода на консоль используется функция printf, для которой требуется включение stdio. h.</span><span class="sxs-lookup"><span data-stu-id="18cdb-118">This example uses printf for console output and requires stdio.h to be included.</span></span> <span data-ttu-id="18cdb-119">Дополнительные сведения об использовании этого кода см. [в разделе Использование примеров кода](using-the-code-examples.md).</span><span class="sxs-lookup"><span data-stu-id="18cdb-119">For more information about using this code, see [Using the Code Examples](using-the-code-examples.md).</span></span>


```C++
int main(void)
{
    HRESULT hr = S_OK;

    IWMProfileManager*  pProfileMgr  = NULL;
    IWMProfileManager2* pProfileMgr2 = NULL;

    WMT_VERSION         profileVersion;

    // Initialize COM.
    hr = CoInitialize(NULL);
    if(FAILED(hr))
    {
        printf("Could not initialize COM.");
        return 0;
    }

    // Create a profile manager object.
    hr = WMCreateProfileManager(&pProfileMgr);
    if(FAILED(hr))
    {
        printf("Could not create a profile manager object.");
        return 0;
    }

    // Get the IWMProfileManager2 interface.
    hr = pProfileMgr->QueryInterface(IID_IWMProfileManager2, 
                                     (void**) &pProfileMgr2);
    if(FAILED(hr))
    {
        printf("Could not get the IWMProfileManager2 interface.");
        SAFE_RELEASE(pProfileMgr);
        return 0;
    }

    // Release the old interface.
    SAFE_RELEASE(pProfileMgr);

    // Get the current system profile version.
    hr = pProfileMgr2->GetSystemProfileVersion(&profileVersion);
    if(FAILED(hr))
    {
        printf("Could not retrieve profile version.");
        printf("\nError code: 0x%X\n", hr);
        SAFE_RELEASE(pProfileMgr2);
        return 0;
    }
    
    // Display the current version.
    printf("Current version: ");
    switch(profileVersion)
    {
    case WMT_VER_4_0:
        printf("WMT_VER_4_0\n");
        break;
    case WMT_VER_7_0:
        printf("WMT_VER_7_0\n");
        break;
    case WMT_VER_8_0:
        printf("WMT_VER_8_0\n");
        break;
    case WMT_VER_9_0:
        printf("WMT_VER_9_0\n");
        break;
    }

    // Set the system profile version to 8.
    profileVersion = WMT_VER_8_0;

    hr = pProfileMgr2->SetSystemProfileVersion(profileVersion);
    if(FAILED(hr))
    {
        printf("Could not change profile version.");
        printf("\nError code: 0x%X\n", hr);
        SAFE_RELEASE(pProfileMgr2);
        return 0;
    }

    // Print verification.
    printf("Successfully set version to ");
    switch(profileVersion)
    {
    case WMT_VER_4_0:
        printf("WMT_VER_4_0\n");
        break;
    case WMT_VER_7_0:
        printf("WMT_VER_7_0\n");
        break;
    case WMT_VER_8_0:
        printf("WMT_VER_8_0\n");
        break;
    case WMT_VER_9_0:
        printf("WMT_VER_9_0\n");
        break;
    }

    // Clean up.
    SAFE_RELEASE(pProfileMgr2);
}
```



## <a name="related-topics"></a><span data-ttu-id="18cdb-120">См. также</span><span class="sxs-lookup"><span data-stu-id="18cdb-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="18cdb-121">**Использование системных профилей**</span><span class="sxs-lookup"><span data-stu-id="18cdb-121">**Using System Profiles**</span></span>](using-system-profiles.md)
</dt> </dl>

 

 




